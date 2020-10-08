---
layout: post
title:      "Redux Toolkit: Redux As It Should Be"
date:       2020-10-08 10:44:01 -0400
permalink:  redux_toolkit_redux_as_it_should_be
---


State is key to any web app and as aplications scale into large scale companies it can become very complicated to manage. For React, one has to pass down state as proprs from parent to child. React hooks provides a different approach as well, but the end result is after a certain point an application can get too unwieldy to pass down all the pieces of state. Redux was designed to as a solution to this. To provide a centralized, predicatable, and flexible solution to state management. 

While it does fullfill this promise to a degree, vanilla redux is incredibly verbose and unwieldy. It requires a considerable amount of 'boilerplate' code and in small scale applications offers little benefit to devs. At least in concern to the amount of design work needed to implent it into an application. So using vanilla redux is a significant consideration and likely only one a larger scale company with a very complicated state would want to. Though by that point it would be difficult to implement it if an application was not designed with Redux in mind from the start.

Enter toolkit! As stated within it's documentation , toolkit will be the standard way to write redux. Toolkit is designed to address the primary concerns of excess boilerplate code, complicated setup, and unofficially required packages. Unoffically required packages being modules like thunk that are almost always used when setting up redux to the point it should be baseline. Toolkit adds that and quite a few more as baseline components now. It also adds powerful tools like  Immer and Autodux to allow writing 'mutative' logic in pieces like your reducers. Whenever you write what would be mutative logic, it'll be converted to not mutative logic in the backend with these additonal tools.

ConfigureStore is an incredibly useful function provided by the toolkit. For anyone that has configured a standard redux store either are holding their heads in a PTSD flashback or inwardly winced at the thought of doing it again. Looking at the snippet provided by the toolkit documantion

```
import { applyMiddleware, createStore } from 'redux'
import { composeWithDevTools } from 'redux-devtools-extension'
import thunkMiddleware from 'redux-thunk'

import monitorReducersEnhancer from './enhancers/monitorReducers'
import loggerMiddleware from './middleware/logger'
import rootReducer from './reducers'

export default function configureStore(preloadedState) {
  const middlewares = [loggerMiddleware, thunkMiddleware]
  const middlewareEnhancer = applyMiddleware(...middlewares)

  const enhancers = [middlewareEnhancer, monitorReducersEnhancer]
  const composedEnhancers = composeWithDevTools(...enhancers)

  const store = createStore(rootReducer, preloadedState, composedEnhancers)

  if (process.env.NODE_ENV !== 'production' && module.hot) {
    module.hot.accept('./reducers', () => store.replaceReducer(rootReducer))
  }

  return store
}
```

This is already quite a bit of what is essentially standard set up. One also has to factor in the rootReducer and other files that are not seen here. To do effectively the same work, this is all that was required of me. 

```import {configureStore} from '@reduxjs/toolkit'
import countriesReducer from '../features/CountryCard/countriesSlice.js';
import articlesReducer from '../features/ArticleCard/articlesSlice.js'
const store = configureStore({
reducer:{
    countries: countriesReducer,
    articles: articlesReducer
}

})

export default store
```
That's it. The configureStore provided by toolkit automatically applies middleware, composes,  and sets up dev tools. It removes so much of the needless redundancy foud in vanilla redux. Setting up the 'slices' of state as it is requires significantly less effort as well. The createReducer function also trememndously cuts down on needless code. Previously, you'd have to export components with connect, mapStatetoProps, and other tedious processes. No more overly long switch and case statements or dispatch set up. Commonly now you can dispatch an action inline relatively easily such as ```dispatch(addCounter)```.  Reducers can do 'mutative' logic as well which is a consdirable time saver.


There's considerably more features worth reading about in the documenation [here](https://redux-toolkit.js.org/) It makes setting up Redux on smaller scale applications much more easily accessible while also still providing the ability to scale. It will also be the standard way for Redux going forward so it's worth investing time to learn it now. The toolkit is an versatile and potent. So if you're sick of waking up in a cold sweat wondering if you made a mistake setting up the initial state, then give the toolkit a whirl.



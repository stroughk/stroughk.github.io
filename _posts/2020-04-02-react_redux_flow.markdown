---
layout: post
title:      "React Redux Flow"
date:       2020-04-03 02:43:41 +0000
permalink:  react_redux_flow
---


Using React with Redux can make state management easier by being able to trace which action causes a change in the state. The typical flow of React with Redux is the following:
1.	Creating a Redux store with the state – this holds all the data for our application. The state can only be changed via initiating an action.
2.	Create Action(s) – describe what we want to do.
3.	Dispatch Action(s) – where the action is executed
4.	Create Reducer(s) – pure functions where the action will be called and checked, and based on that action, the reducer will modify the state.

When a user interacts with a component in the browser, a function is executed via props that calls an action. These actions are mapped to props and by convention they are called ‘mapActionToProps’.
Actions contain a ‘type’ and a ‘payload’(optional). The type is usually written in all caps and it’s the precise description of that action. 
Once this action is dispatched, it will be passed on to the ‘reducer’. Reducer then modifies the ‘state’ based on the type of action. If there are multiple reducers in the application, they are combined into one reducer which is then passed as an argument to the Redux store.

The redux store is in the root component of the React app. In order for other components to receive the state data via the connect() function, we need to pass mapStateToProps() to the connect() function. Once we do this, the connected component is receiving the Redux state updates. 

Example: 
import {connect} from ‘react-redux’
function mapStateToProps(state) {
return {
//component gets some update
}
}
export default connect(mapStateToProps)(someComponent)


React Redux creates a much greater user experience when implemented. It helps to avoid unnecessary re-rendering of the page so it only renders when it’s needed. It also creates a well-organized component structure where state can be managed precisely and efficiently. 


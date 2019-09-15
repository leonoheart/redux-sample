#question to be solved
##why divide the action into SELECT_SUBREDDIT and INVALIDATE_SUBREDDIT?
##what does didInvalidate prop do?
##why [action.subreddit]: needs [] in action/index.js
it is a es6 computed property(omg!nearly forgot it)
 [action.subreddit]: posts(state[action.subreddit], action)
##The nice thing about thunks is that they can dispatch results of each other?


#notes
##when a new level needed to control the logic flow, divide it into body and function
##import fetch from 'cross-fetch'
Fetch supports the Cross Origin Resource Sharing (CORS)
##the function of thunk action creator
Thunk middleware knows how to handle functions.It passes the dispatch method as an argument to the function,thus making it able to dispatch actions itself.
##be careful about the createMiddleware
when import a module, its export can be a function or a instance
e.g
loggerMiddleware = createLogger()
thunkMiddleware can be used directly cause:
    const thunk = createThunkMiddleware();
    export default thunk;
##Be aware that any fetch polyfill assumes a Promise polyfill is already present. 
The easiest way to ensure you have a Promise polyfill is to enable Babel's ES6 polyfill in your entry point before any other code runs:

##dispatch(action) and subscribe(listener) ->connect 
connect is better cause it is the former always rerender and not judge whether it need to do that

##Relative imports outside of src/ are not supported.

##actions:source of information/reducer:change the state/action creator:functions that create actions.






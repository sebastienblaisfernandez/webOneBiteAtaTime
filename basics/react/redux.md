# Redux

Redux is a predictable state container for JS apps.

## Actions

Actions are payloads of information sending data from the app View to the store.
Actions are send to the store using `store.dispatch()`.

```js
const ADD_TODO = "ADD_TODO";

{
  type: ADD_TODO,
  text: 'Build my first Redux app'
}
```

### Actions Creators

Actions creators are function that craete actions.

```js
function addTodo(text) {
  // actions
  return {
    type: ADD_TODO, // type of action
    text, // payload
    todoId,
    morePayload
  };
}
```

## Reducers

Reducers specify how the application's state changes in response to actions sent to the store. The Actions discribe 'what happened', but don't describe how the applications state changes.

THe reducer is a pure function that takes the previous state and an action, and returns the next state.

```js
(previousState, action) => newState;
```

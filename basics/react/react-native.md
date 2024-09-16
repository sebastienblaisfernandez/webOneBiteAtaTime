More solid with react, react native, redux, SOLID.

## Explain React.PureComponent

`PureComponent` is similar to `Component` but it skips re-renders for same props and state.

Extending `PureComponent` is equivalent to defining a custom `shouldComponentUpdate()` method that shallowly compares props and state.

## Explain Class component

Ther eare ES6 classes that extend from `React.Component` or `REact.PureComponent`. They have a `render()` method where you define the structure of the component UI using JSX. Class component are used for components that need to manage state of have lifecycle methods.

## Explain React function component

There are simple JS functions that take props as input and return JSX elements. They are often used for presentational and stateless components.

## Name react lifecycle hook ?

- componentDidMount()
- componentWillUnmount()

- getDerivedStateFromProps() Introduce in react 16.3

- shouldComponentUpdate()

- componentWillUpdate()

## Explain the concept of virtual DOM in react ?

## Explain what is React context ?

Context provides a way to pass data through the component tree without having to pass props down manually at every level.

```tsx

// Context lets us pass a value deep into the component tree
// without explicitly threading it through every component.
// Create a context for the current theme (with "light" as the default).
const ThemeContext = React.createContext('light');

class App extends React.Component {
  render() {
    // Use a Provider to pass the current theme to the tree below.
    // Any component can read it, no matter how deep it is.
    // In this example, we're passing "dark" as the current value.
    return (
      <ThemeContext.Provider value="dark">
        <Toolbar />
      </ThemeContext.Provider>
    );
  }
}

// A component in the middle doesn't have to
// pass the theme down explicitly anymore.
function Toolbar() {
  return (
    <div>
      <ThemedButton />
    </div>
  );
}

class ThemedButton extends React.Component {
  // Assign a contextType to read the current theme context.
  // React will find the closest theme Provider above and use its value.
  // In this example, the current theme is "dark".
  static contextType = ThemeContext;
  render() {
    return <Button theme={this.context} />;
  }
}
```

## Explain hooks in react ?

[Using Hooks](https://react.dev/learn#using-hooks)

## Explain `useState()` hook ?

`useState()` allow to ge the currentState and a setState function.

```tsx
function MyButton() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
  }

  return <button onClick={handleClick}>Clicked {count} times</button>;
}
```

## Explain `useRoute()` hook ?

## Explain `useMemo()` hook ?

## Explain `useCallBack()` hook ?

## Explain `useReducer()` hook ?

## Explain `useContext()` hook ?

## Explain `Ref` hook ?

When you want a component to "remember" some information, but you don't want that information to trigger a new renders, use ref.

```tsx
import { useRef } from 'react';

const ref = useRef(0);
```

[Referencing Value with Refs](https://react.dev/learn/referencing-values-with-refs)

## Explain `useRef()` hook ?

#### References

- [React Component Lifecycle Methods](https://www.freecodecamp.org/news/react-component-lifecycle-methods/)

# Redux

## Explain CreateSelector()

### CreateSelector

[reselect](https://github.com/reduxjs/reselect)

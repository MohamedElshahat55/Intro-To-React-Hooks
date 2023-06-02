# React Hooks

---
> - Hooks will not work in React class components.
> - You can’t call it inside loops or conditions

## Things You Should Know About React Hooks

There are many features of React. 

React hooks is one of them. React hooks was first released in October 2018.

In React a lot of developers use the lifecycle method which is nothing, but just a series of components.

`render()`, `componentDidMount()`,`componentDidUpdate()` `componentWillUnmount()` all these are the lifecycle method. 
React hooks is the alternative approach of state management and lifecycle method. 
There are many hooks used for different purposes. Some of them are `useEffect()`, `useState()`, `useCallBack()`, `useReducer()`, `useRef()`, `useDispatcher()` etc.

## Why Use React Hooks?

It makes your component better, and it helps in writing clear, concise, and maintainable code. 
It just cut all the unnecessary code from your component and makes your code more readable. **But the question is when to use React hooks?**

Use Hooks when you’re writing a function component, and you want to add some state to it. Earlier this job was done by using a Class, but now you can write the hooks inside a function component.

**Hooks have shorter components and better readability**
Class components come with a lot of boilerplate code. Consider the counter component below:

```
class Counter extends Component {
    constructor(props) {
        super(props)
        this.state = {
        	count: 1,
        }
    }
    render() {
        return (
            <div>
                The Current Count: {this.state.count}
                <div>
                <button onClick={this.setState({ count: this.state.count - 1 })}>
                add
                </button>
                <button onClick={this.setState({ count: this.state.count + 1 })}>
                subtract
                </button>
                </div>
            </div>
    );
    }
}
```

Here’s equivalent code using functional component and React Hooks:

```
function Counter  ()  {
    const [count, setCount] = useState(1);
    return (
        <div>
            The Current Count: {this.state.count}
            <div>
                <button onClick={() => setCount(count + 1)}>add</button>
                <button onClick={() => setCount(count - 1)}>subtract</button>
            </div>
        </div>
    );
};
```

Notice how the class component is way more complex. You need a class to extend React, a constructor to initialize state, and you need to reference the `this` keyword everywhere.

Using functional components removes a lot of `this`, so our code becomes shorter and easier to read and maintain.

## Rules of Hook

There are a few rules that must be followed when using React Hooks:

- **Use Hooks only at the top level**: Hooks should only be called at the top level of a functional component or another custom Hook. They should not be called inside loops, conditions, or nested functions.

- **Use Hooks in functional components only**: Hooks should only be used in functional components or other custom Hooks. They cannot be used in class components.

- **Use Hooks only in React function components**: Hooks should only be used in React function components or custom Hooks. They should not be used in regular JavaScript functions.

By following these rules, you can ensure that your use of React Hooks is consistent, reliable, and efficient, and that your components are easy to understand and maintain.

## Most Common React Hooks

- `useState()`
- `useEffect()`
- `useContext()`
- `useReducer()`

## Resourses
[React Documentation](https://react.dev/reference/react)

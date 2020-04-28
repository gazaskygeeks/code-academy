# Hooks

if you want to test the examples then you can clone the repo:
* using HTTPS `git clone https://github.com/MohammedYehia/Hooks-G8.git`
* or using SSH `git clone git@github.com:MohammedYehia/Hooks-G8.git`

# Hooks Part 1 ✨

>With Hooks we seperate code not based on the lifecycle method name but based on what the code is doing
>
>-- <cite>Dan Abramov React Conf 2018</cite>

## So what are Hooks?🤔

Functions that let you “hook into” React state and lifecycle features from function components.
Simply with hooks you no longer need to define a class in order to have a state and it's lifecycle methods.

## Why React hooks?
- No need for classes.
- No need for lifecycle methods
- No this 🙌
- State with functional component
- You can share and reuse code easily
- Shorter and cleaner code
- One function one thing to do (instead of multiple funtion calls inside lifecycle method)

## So how would you define a state inside a function?🤷‍♀️

By calling our first built-in hook **useState** 🎉

```javascript
const [value, setValue] = useState(initialState);
//or
const state = useState(initialState)
const value = state[0];
const setValue = state[1];
```

Calling useState will return an array contains the state value and a function to change the state.

Let's discuss it with more details:

- `initialState`: can be any type of data and it doesn't have to be an object like unlike with classes even a function that return a value at the end would work fine.(if you are curious then you can check the [source code](https://github.com/facebook/react/blob/3278d242184a13add3f25f683b77ef9a6a2305f3/packages/react/src/ReactHooks.js#L83)).The initial state argument is only used during the first render.

- `value`: this is our current state and can be named anything you want.

- `setValue`: this is the updater function that we use to update our state, you can think of it as something similar to `setState` in class. Also can be name it anything you want that doesn't start with  `use` and should follow the camelCase as a convention (this is how the linter rules differentiate between the normal function and the hooks)
    > - This error would popup`React Hook "updater function name" cannot be called inside a callback. React Hooks must be called in a React function component or a custom React Hook function  react-hooks/rules-of-hooks` if you started the updater funtion with use.
    > - also because this is a linter rule something like this would happen (ex: `useCount` is wrong, while `usecount` would work fine👀)

----

**Let's have an example:**

> switch to branch example-1

***Simple Counter using class:***

```javascript
class Counter extends React.Component {

  constructor(props) {
    super(props);
    this.state= {
      count: 0,
    }
    this.countUp = this.countUp.bind(this);
  }

  countUp(){
    this.setState(state=> ({count: state.count + 1}) )
  }

  render(){
    return (
      <button
         onClick={this.countUp}
      >
       Count Up {this.state.count}
      </button>
    );
  }

}
```

***the same example using useState hook:***

```javascript
function Counter(){
    const [count, setCount] = useState(0);

    // no need for binding the function
    /* we directly call the value count without
      this or anything like a normal variable defined inside a function*/

    return (
    <button
       onClick={()=>setCount(count+1)}
       // or like this
      // onClick={()=>setCount(c=> c+1)}
     >
      Count Up {count}
    </button>);
}
```

I think you can see the difference between both of them  and how much code we have to write with class and we didn't even use all the lifecycle methods so you can see using hooks is cleaner and less code.

## How functional component works with hooks?

let's exaplain the execution of the functional component with hooks and how function can be aware of the state after re-renderng the component again

1. First we import useState form react;
    `import {useState} from 'react';`
2. Function Counter gets created.
3. after that we are calling useState hook with initial value of zero.
4. then we gets back the array that contains the state and a function that we can use to update the state.
5. then we are returning a jsx with containg the state value and assign the function updater to onClick funtion
6. after click on the button the `setCount` function gets called and we update the `count` state.
7. as with setState  calling `setCount` will re-render the component now with normal function we will be ending with initializing the state agin wiht zero and with that way the counter will remain zero with every render but the way that hooks work is:
    - hooks keep a pointer to the state before re-render and when the component re-render it will check the hooks if there is a state in there then it is going to use it if not then this is the first time and we can start with the initial value
8. so on the next render the component will be aware of the new state and will display the new value instead of the initial one

-------

**we can call useState multiple time with different values**

> switch to branch example-2
>
```javascript
function sayHi(){
  const [name, setName] = useState("Ahmed");
  const [greeting, setGreeting] = useState("Hello");

  function handleName(e) {
    setName(e.target.value);
  }

  function handleGreeting(e) {
    setGreeting(e.target.value);
  }

  return (
   <div>
     <input name={name} onChange={handleName} />
     <input name={greeting} onChange={handleGreeting}/>
     <p>{`${greeting} ${name}`}</p>
   </div>
  );
}
```

- we can explaing the above code and how react state hook keeps record of the current state using the table below it is like an array or a linkedList

    so when the component re-render will look at the state array and will start from the first and move untill it iterate over all the element
    1. the pointer will point to name and check the state.

        ||
        |----------------|
        |---> name="Ahmed"|
        |greeting="Hello" |

    2. then will move to the next state othe same order as declared on the component function.

        ||
        |----------------|
        |name="Ahmed"|
        |---> greeting="Hello"|

    and that is how state hook keep track of the new state.

**Final Note:** updating a state variable with hooks always replaces it instead of merging it(like what setState do)
> check the example on branch example-3

**Execise 1:**
create simple todo app
1- one Input
2- on button
3- list of todos


![](https://i.imgur.com/DqeJBSg.png)

----

## How would you perform a side effect?

#### First what is side effect?
* Fetching data.
* Changing the DOM.
* Listening for KeyEvents.
* Timers.

#### How would we do it using hooks?
* We can use **useEffect** to perform such operations
* **useEffect** lets you perform side effects in components, and is almost similar to lifecycle methods in classes (*componentDidMount, componentDidUpdate, and componentWillUnmount*)

```javascript
    useEffect(callbackFunction, [dependencyArray])
```

- By default every call to `render` will be followed by  a call to `useEffect`
- useEffect will be called at least once
- useEffect takes a function as a first argument and a "dependency array" as a second *optional* argument
- useEffect will watch the changes that happen on the second argument and will be called depending on the state of this argument
> If your effect "depends" on value, it needs to be listed in the array.

<br/>

**The second optional argument (dependencyArray)**:

* If any of the value in the array changes, the callback will be fired after the render.
* When it's not present, the callback will always be fired after every render.
* When it's an empty array [], the callback will only be fired once, similar to `componentDidMount`(somehow). basicly the useEffect won't find any changes so it won't be called after the first call.

```javascript
    useEffect(()=> {
        ...doSomeThing
    },[])
```

so we can describe it like this:
* useEffect(cb) ---> runs when `any state` changes
* useEffect(cb, []) ---> runs when `no state` changes(on mounting only)
* useEffect(cb, [prop1, state]) // runs when one of the dependency changes

<br/>

You can simulate `componentWillUnmount` by returning *a function* from the use Effect (it is called a **clean up** function)

```javascript
    useEffect(()=>{
        ...doSomeThing
        //this is the clean up function
        return ()=> console.log("clean");
    })
```

**CleanUp function:**
* would be called before calling the useEffect again.(so it can clean up the effect from the previous render before running the effect next time)
* would be called before the component removed from the UI.

>There is no special code for handling updates because useEffect handles them by default. It cleans up the previous effects before applying the next effects. This behavior ensures consistency by default and prevents bugs that are common in class components due to missing update logic.

<br/>

***Example 1:***
let's check this example from the [docs](https://reactjs.org/docs/hooks-effect.html#example-using-classes) where it explains the difference of using hooks vs classes to perform sideEffect

***Exerccise 1:***
Try to create this effect
*Hints*:
* use the dom `mousemove` eventListener, and don't forget to remove it with clean up.
* you can measure the window `innerWidth` and if mouseX is bigger than the half then apply `tomato` color and if not apply `blue` color.

![](https://i.imgur.com/AizMCZA.gif)


**Exercise 2**:
use Yandex translate API to translate the input from english to arabic
https://translate.yandex.net/api


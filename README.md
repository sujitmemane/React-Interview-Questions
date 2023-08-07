![image](https://github.com/sujitmemane/React-Interview-Questions/assets/114643903/a247181a-ce42-407b-be9d-5c9346cac14c)

# 🚀 Welcome to the React Interview Questions repository! 🤓

Prepare for success in your React interviews with this collection of comprehensive questions and answers. Contribute your own questions and join the community in mastering React! 👨‍💻👩‍💻 Let's level up together! 🚀💪

## REACT INTERVIEW QUESTIONS

1. **What is React, and how is it different from other JS frameworks or libraries?**
    
    React is a popular JavaScript library for building user interfaces. It was developed by Facebook and is widely used in web development. React focuses on the concept of components, which are reusable building blocks for UI elements. These components can be composed together to create complex user interfaces.
    
    The important features of React are:
    
    - It supports server-side rendering.
    - It will make use of the virtual DOM rather than real DOM (Data Object Model) as RealDOM manipulations are expensive.
    - It follows unidirectional data binding or data flow.
    - It uses reusable or composable UI components for developing the view.

1. **What is Virtual DOM in React?**
    
    The Virtual DOM is a concept in React that helps improve performance by reducing the amount of direct manipulation of the actual DOM (Document Object Model). It is a lightweight copy of the real DOM maintained by React. When there are changes in the application's state or props, React creates a virtual representation of the DOM and performs a "diffing" process to find the minimal set of changes needed to update the actual DOM.
    
    By using the Virtual DOM, React minimizes the number of DOM updates, making the rendering process more efficient. This results in better performance and a smoother user experience.
    
2. **What is the difference between state and props in React?**
    
    In React, both state and props are used to manage data and communicate between components, but they have distinct purposes and handling mechanisms:
    
    - State: State is used to manage and store mutable data within a component. It represents the internal data of a component and can be changed using the **`setState`** method. State is meant to be managed and controlled by the component itself and is often used to maintain data that might change over time.
    - Props: Props (short for properties) are used to pass data from a parent component to a child component. They are immutable and are set by the parent component. Props allow the parent component to communicate with its children by passing data down the component tree.
    
3. **Difference between Server-Side Rendering and Client-Side Rendering?**
    - Server-Side Rendering (SSR): In SSR, the server generates the initial HTML of a web page and sends it to the client's browser. This means that the page is rendered on the server before being delivered to the client. The client's browser receives a fully rendered page, and any subsequent interactions or updates are handled by JavaScript.
    - Client-Side Rendering (CSR): In CSR, the initial HTML is minimal, and the majority of the rendering process is done on the client's browser using JavaScript. The server sends a blank or basic HTML page, and then the necessary components and data are fetched and rendered on the client side.
4. **What are the uses of Refs in React?**
    
    Refs are a feature in React that provide a way to directly access and interact with DOM elements or React components. They are used in situations where direct DOM manipulation is necessary or when you need to interact with child components imperatively.
    
    Common use cases for refs include:
    
    1. Accessing DOM elements to read their values or apply focus.
    2. Triggering imperative animations or actions in third-party libraries that don't work well with the standard React data flow.
    3. Managing focus, text selection, or media playback.
5. **What is useState() in React?**
    
    The useState() is a built-in React Hook that allows you for having state variables in functional components. It should be used when the DOM has something that is dynamically manipulating/controlling.
    
    The **`useState()`** hook returns an array with two elements: the current state value and a function to update that state. It follows the array destructuring syntax to extract these values. For example:
    
    ```jsx
    const [count, setCount] = useState(0);
    ```
    
    In this example, **`count`** represents the current state value, and **`setCount`** is the function used to update **`count`**. When **`setCount`** is called with a new value, React will re-render the component with the updated state.
    

1. **What are keys in React?**
    
    In React, the **`key`** is a special attribute that is used when rendering arrays of elements (such as in a loop). It helps React identify which items have changed, been added, or been removed from the list. The **`key`** prop is required when rendering arrays to help React efficiently update the user interface without re-rendering the entire list.
    
    Each **`key`** should be a unique identifier for the corresponding element, typically provided by the data itself. Using proper **`key`** values allows React to perform a more efficient reconciliation process when updating the list, leading to better performance.
    
2. **What is JSX?**
    
    JSX stands for JavaScript XML. It is a syntax extension for JavaScript used in React to describe what the user interface should look like. JSX allows developers to write HTML-like code within their JavaScript code, making it easier to visualize and build UI components.
    
    As stated in the official docs of React, JSX provides syntactic sugar for React.createElement( ) function.
    
    > Note- We can create react applications without using JSX as well.
    > 
    
    Let’s understand **how JSX works**:
    
    Without using JSX, we would have to create an element by the following process:
    
    ```
    const text = React.createElement('p', {}, 'This is a text');
    const container = React.createElement('div','{}',text );
    ReactDOM.render(container,rootElement);
    ```
    
    **Using JSX**, the above code can be simplified:
    
    ```
    const container = (
    <div>
      <p>This is a text</p>
    </div>
    );
    ReactDOM.render(container,rootElement)
    ```
    
3. **What are the differences between functional and class components?**
    
    In React, there are two main types of components: functional components and class components.
    
    Functional Components:
    
    - They are defined as plain JavaScript functions.
    - They receive data through **`props`**.
    - They don't have their own state (**`useState`** hook can be used to introduce state in functional components with React Hooks).
    - They are simpler and easier to read and test.
    - With the introduction of React Hooks, functional components can now have more features previously reserved for class components.
    
    Class Components:
    
    - They are defined as ES6 classes that extend **`React.Component`**.
    - They have their own internal state, accessible through **`this.state`**.
    - They have lifecycle methods like **`componentDidMount`**, **`componentDidUpdate`**, etc.
    - They can be more verbose compared to functional components.
    - Prior to React Hooks, they were the only way to manage state and use lifecycle methods in React.

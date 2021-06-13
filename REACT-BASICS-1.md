1. React allows you to create re-usable and reactive components consisting of HTML and Javascript (and css).
2. React follows a declarative approach for building the components.
3. Declarative means you will define the target state and let react figure out the actual javascript DOM instructions for create, update or remove.
4. Javascript uses imperative style, where we give all the instructions clearly as to what is to be done.
<br>

## Create React app
`npx create-react-app react-complete-guide`<br>
``<br>
``<br>

A Component in React is just a javascript function.<br>
Always use element names ac Capital case for custom elements, react assumes lower case elemnts are default ones.<br>

## React Parent Child Communication
props is used to pass the parameter to a component, we have something called props.children prop to send the content within the tags.<br>
The later part is also called composition. We can also generate wrappers like Card.js using composition.<br><br>

<b>do not give paranthesis for functions caling from events, as they will be excuted while parsing, so we ust need to point with the name, without ().</b><br>

### Child to Parent
send the function as a prop from parent to child, then execute the parent function in child. Ex: See saveExpenseDataHandlerin NewExpenses.js

### Lifting the state up
To share data between siblings send the data up till the common parent arrives and pass down the data to the sibling.

## State
Whenever react evaluates this JSX code, it will call these component functions. And these component functions stand to return JSX code, which is all the evaluated, up until there's no more JSX code to be evaluated. <br>
So react keeps on calling any component functions it encounters in JSX, then calls any functions that those functions might have returned so any elements those components might have used in their JSX code until there are no more functions left.<br>
It will now translate the overall result into DOM instructions. But this process is done only the first time it is rendered in browser, so in order to notify react that a change has occured we use <b><i>state.</b></i>

## ReactHooks
All React hooks are to be called in the parent function, not in the nested functions except for ***. They all start with 'use'.<br>
It returns a pair of values: the current state and a function that updates it ` const [count, setCount] = useState()`.<br>

### Controlled vs Uncontrolled Components & Stateless vs Stateful Components
Controlled Coponents are those which are controlled by another componenet i.e. the values and changes to the value are not handled in the component <br>
Stateful are the ones which have state, otheres are called Stateless/ Presentational components.<br>

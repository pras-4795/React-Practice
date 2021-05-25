# React-Practice

Traditionally request was sent to a server and a new HTML page was sent back as a response.
Javascript in the browser is able to manipulate DOM.
React is a client side javascript library.
It builds a modern, reactive user interfaces for the web.
Declarative, Component Focused approach.

# Import, Exports 
Here are all types of export that we covered in this and previous articles.

You can check yourself by reading them and recalling what they mean:

Before declaration of a class/function/…:
    export [default] class/function/variable ...
Standalone export:
    export {x [as y], ...}.
Re-export:
    export {x [as y], ...} from "module"
    export * from "module" (doesn’t re-export default).
    export {default [as y]} from "module" (re-export default).
Importing named exports:
    import {x [as y], ...} from "module"
Importing the default export:
    import x from "module"
    import {default as x} from "module"
Import all:
    import * as obj from "module"
Import the module (its code runs), but do not assign any of its exports to variables:
    import "module"

# Spread, Rest
...
Spread operator is used to split up array elements or object properties
    const newArray = [...oldArray, 1, 2]
    const newObject = {...old object, newprop:2}
Rest operatoris used to merge list of function args into array
    function sortArgs(...args) {
        return args.sort();
    }

Do not copy arrays or objects directly. Ex: const secondPerson = firstPerson
Instead, use spread operator const secondPerson = {...person}, this will create a deep clone.
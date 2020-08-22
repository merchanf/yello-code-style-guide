# Javascript styling guide

This guide is based on airbnb's [javascript style guide](https://github.com/airbnb/javascript). Use it as the main reference for javascript styling. However, some other rules will be added to fit yello's necessities.

## Methods and functions

1. If a function needs more than three parameters, consider using an object instead, and destructure the content.

        //Bad
        const sumMeAllPlease = (param1, param2, param3, param4 ) => {
          return param1 + param2 + param3 + param4;
        }

        //Good
        const sumMeAllPlease = (param1, param2, param3 ) => {
          return param1 + param2 + param3;
        }

        //Good
        const sumMeAllPlease = (parametersOfThisFunction) => {
          const {param1, param2, param3, param4} = parametersOfThisFunction;
          return param1 + param2 + param3 + param4;
        }

2. functions must be short and concise as possible, having only a unique purpose. If you want to know when is a function too long, take this [stackOverflow answer](https://stackoverflow.com/a/475762/8407062) as a reference.

## Naming
Give as descriptive a name as possible, within reason. Do not worry about saving horizontal space as it is far more important to make your code immediately understandable by a new reader. Do not use abbreviations that are ambiguous or unfamiliar to readers outside your project, and do not abbreviate by deleting letters within a word.

1.  variable names should be self-descriptive. It should not be necessary to add a comment for additional documentation to the variable.

        // bad
        var value = 'Faustino';
        
        // bad
        var val = 'Faustino';
        
        // good
        var firstName = 'Faustino';

2. When using boolean variables use prefixes like `is` , `are` , `has` as It helps to distinguish a boolean from another variable by just looking at it.

        // bad
        var visible = true;
        var equal = false;
        var encryption = true;
        
        // good
        var isVisible = true;
        var areEqual = false;
        var hasEncryption = true;

3. Tell what the function is doing by giving the function name a verb as prefix.

        // bad
        function name(firstName, lastName) {
          return `${firstName} ${lastName}`;
        }
        
        // good
        function getName(firstName, lastName) {
          return `${firstName} ${lastName}`;
        }

4. use this standard variable names when common used variables are needed:

* `counter`: counting items.
* `max`: maximum of a set of numbers.
* `min`: minimum of a set of numbers.
* `first`: first element of an array.
* `last`: last element of an array.
* `i`: array index.

References and further read:

* [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html#naming)
* [JavaScript Naming Conventions](https://www.robinwieruch.de/javascript-naming-conventions)




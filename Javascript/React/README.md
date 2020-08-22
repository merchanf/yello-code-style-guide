# Javascript styling guide

This guide is based on airbnb's [javascript react/jsx style guide](https://github.com/airbnb/javascript/tree/master/react). Use it as the main reference for react styling. However, some other rules will be added to fit yello's neccessities.

## Naming

### Event handling

In case you need to add a functionality to a event handler in a component add `handler` as prefix to the function name that will be overridden.

    function Brick({onClick}) {

      const myOwnOnClick = (e) => { // Bad
      const handleOnClick = (e) => { // Good
        e.preventDefault();
        onClick();
      }

      return <button onClick={handleOnClick} ></button>
    }



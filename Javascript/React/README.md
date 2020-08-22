# React and jsx styling guide

This guide is based on airbnb's [javascript react/jsx style guide](https://github.com/airbnb/javascript/tree/master/react). Use it as the main reference for react styling. However, some other rules will be added to fit yello's neccessities.

## Naming

1. In case you need to add a functionality to a event handler in a component add `handler` as prefix to the function name that will be overridden.

        function Brick({onClick}) {

          const myOwnOnClick = (e) => { // Bad
          const handleOnClick = (e) => { // Good
            e.preventDefault();
            onClick();
          }

          return <button onClick={handleOnClick} ></button>
        }

## Props

1. Always destructure the props of a functional component. It helps to keep the names consistent trough the component and are easier to read. 

        // Bad
        const Brick = (props) => <h1>{ props.title }</h1>;

        // Good
        const Brick = ({ title }) => <h1>{ title }</h1>;
  
2. If you have three or less props you can destructure them in the function arguments section.

        // Bad
        const Brick = ({ prop1, prop2, prop3, prop4 }) => <div>...

        // Good
        const Brick = ({ prop1, prop2, prop3 }) => <div>...

3. For four or more props, or if one of the props have a long name, destructure all of them inside the component and indent appropiately. 

        // Bad
        const Brick = ({ prop1, prop2, otherProps }) => {
          const { prop3, prop4 } = otherProps;

        // Good
        const Brick = (props) => {
          const {
            prop1,
            prop2,
            prop3,
            prop4,
          } = props;

        // Good
        const Brick = (props) => {
          const {
            ThisIsAReallyLongPropName, 
            prop2, 
            prop3, 
            prop4
          } = props;

## PropTypes

1. The last value of the proptypes or default proptypes section, should have a trailing comma. [Airbnb's Javacript style guide](https://github.com/airbnb/javascript#commas--dangling) explains why is this neccessary.

        // Bad
        Brick.propTypes = {
          prop1: PropTypes.string,
          prop2: PropTypes.string
        }

        Brick.defaultProps = {
          prop1: 'prop1',
          prop2: 'prop2'
        };

        // Good
        Brick.propTypes = {
          prop1: PropTypes.string,
          prop2: PropTypes.string,
        }

        Brick.defaultProps = {
          prop1: 'prop1',
          prop2: 'prop2',
        };


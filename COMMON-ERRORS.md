
1. Unexpected use of file extension "js" for "./common.js"                (import/extensions)


```js
  //Bad code

import { isAuthenticated, getObjectValue, httpStatusCodes } from './common.js';

//Good code

import { isAuthenticated, getObjectValue, httpStatusCodes } from './common';

   ```


2.  Arrow function used ambiguously with a conditional expression(no-confusing-arrow)

```js

 // Bad Code

  {(Component) => Component === null
            ? <div className="center"> <Loader
                type="Puff"
                color="#00BFFF"
                height="100"
                width="100"
            /></div>
            : <Component {...props} />}

//Good code

{Component => (Component === null
      ? (
        <div className="center">
          <Loader
            type="Puff"
            color="#00BFFF"
            height="100"
            width="100"
          />
        </div>
      )
      : <Component {...props} />)}
```


3.  Prefer default export  (import/prefer-default-export)


```js

//Bad Code

export const INVALID_PROPERTY = 'Invalid Property Selected! ';



//Good Code

const INVALID_PROPERTY = 'Invalid Property Selected! ';

export default INVALID_PROPERTY;


   ```



4. JSX not allowed in files with extension '.js'  (react/jsx-filename-extension)
```
Fix: Rename files using jsx to jsx form js
````

5.  Variable is defined but never used                    (no-unused-vars)

````
Fix: Remove unused variables 
````


 6.  Unexpected var, use let or const instead                               	     (no-var)

 ```
 Fix: Never declare variables using var

 ```

 7.  Enforce component methods order                       (sort-comp)

```
  The default configuration ensures that the following order must be followed:

1. static methods and properties
2. lifecycle methods: displayName, propTypes, contextTypes, childContextTypes, mixins, statics, defaultProps, constructor, getDefaultProps, state, getInitialState, getChildContext, getDerivedStateFromProps, componentWillMount, UNSAFE_componentWillMount, componentDidMount, componentWillReceiveProps, UNSAFE_componentWillReceiveProps, shouldComponentUpdate, componentWillUpdate, UNSAFE_componentWillUpdate, getSnapshotBeforeUpdate, componentDidUpdate, componentDidCatch, componentWillUnmount (in this order).
3. custom methods
4. render method

```

8. This rule is aimed at flagging variables that are declared using let keyword, but never reassigned after the initial assignment. (No-const)

```
Fix: if a variable is never reassigned declare it with const
```

9. we can use template literals instead of string concatenation (prefer-template)

```js
var str = "Hello, " + name + "!";
/*eslint-env es6*/

var str = `Hello, ${name}!`;

/*eslint no-param-reassign: "error"*/
````

10.  No param reassign

```js
// Examples of incorrect code for this rule:

function foo(bar) {
    bar = 13;
}

function foo(bar) {
    bar++;
}
// Examples of correct code for this rule:
/*eslint no-param-reassign: "error"*/

function foo(bar) {
    var baz = bar;
}

```

       
11. Unnecessarily quoted property					               (quote-prop)

```js
//Examples of incorrect code for this rule

 var object = {
    foo: "bar",
    baz: 42,
    "qux-lorem": true
};

//Correct-code:

var object1 = {
    "foo": "bar",
    "baz": 42,
    "qux-lorem": true
};

```

12. Unexpected lexical declaration in case block          (no-case-declarations)


```js


// Bad Code

case BOOKING_SOURCES_SUCCESS:    const BookingSources = getObjectValueIfEmpty(action, 'payload.data', {});   changes = {     isBookingSourcesLoading: false,     isBookingSourcesLoaded: true,     BookingSources,   };   break; 

//Good Code

// The following case clauses are wrapped into blocks using brackets


case BOOKING_SOURCES_SUCCESS: {   const BookingSources = getObjectValueIfEmpty(action, 'payload.data', {});   changes = {     isBookingSourcesLoading: false,     isBookingSourcesLoaded: true,     BookingSources,   };   break; }
```

13. Unexpected block statement surrounding arrow body                 (arrow-body-style)

```js

//Incorrect Code

let foo = () => {
    return 0;
};

//Correct Code

let foo = () => 0;
let foo = () => ({ foo: 0 });

```

 14. Useless Constructor	 						(no-useless-constructor)

```js
//Bad Code


class Root extends React.Component {

    constructor(props) {
        super(props);
    }

    render() {
        return (
            <div className="table-wrapper mt-xl-5">
                <Header title="Manage Blacklist"/>
            </div>
        );
    }
}

export default Root;


//Good Code

class Root extends React.Component {
    render() {
        return (
            <div className="table-wrapper mt-xl-5">       
                <Header title="Manage Blacklist" />
            </div>
        );
    }
}
export default Root; 

```

15.  Component should be written as a pure function                          react/prefer-stateless-function 

```js
//Bad Code:


class Root extends React.Component {
    render() {
        return (
            <div className="table-wrapper mt-xl-5"> 
                <Header title="Manage Blacklist" />
            </div>
        );
    }}

//Good Code

const Root =() => (
  <div className="table-wrapper mt-xl-5">
    <Header title="Manage Blacklist" />

  </div>
);



export default Root;

```

16. Must use destructuring props assignment                                                react/destructuring-assignment

```js

// Bad Code

const Root = props => (
  <div className="table-wrapper mt-xl-5">
    <Header title="Manage Blacklist" />

    <List
      onFromSubmit={props.onFromSubmit}
      onSearchSubmit={props.onSearchSubmit}
      listData={props.listData}
      pageOfItems={props.pageOfItems}
      onChangePage={props.onChangePage}
      isCouponListLoading={props.isCouponListLoading}
      isCouponListLoaded={props.isCouponListLoaded}
      next={props.next}
      prev={props.prev}
      pageNo={props.pageNo}
      totalPages={props.totalPages}
      onRemove={props.onRemove}
    />

  </div>
);


export default Root;


//Good Code

const Root = (props) => {
  const {
    onFromSubmit, onSearchSubmit, listData, pageOfItems, onChangePage, isCouponListLoading, isCouponListLoaded, next, prev, pageNo, totalPages, onRemove,
  } = props;
  return (
    <div className="table-wrapper mt-xl-5">
      <Header title="Manage Blacklist" />

      <List
        onFromSubmit={onFromSubmit}
        onSearchSubmit={onSearchSubmit}
        listData={listData}
        pageOfItems={pageOfItems}
        onChangePage={onChangePage}
        isCouponListLoading={isCouponListLoading}
        isCouponListLoaded={isCouponListLoaded}
        next={next}
        prev={prev}
        pageNo={pageNo}
        totalPages={totalPages}
        onRemove={onRemove}
      />

    </div>
  );
};
export default Root;

```


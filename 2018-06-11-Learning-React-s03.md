# Pure React

## Page Setup

## The Virtual DOM

## React Elements
* `React.createElement`
* `data-reactroot` will always appear as an attribute of the root element of your React component.

## ReactDOM
* ReactDom contains the tools to render React elements into browser.
* `ReactDOM.render`

## Children
* ReactDOM only allow render single element to doucment. But the single element can nest children.
* `className` in React will render to HTML as css `class`

## Contructing Elements with Data
```javascript
var list = [
  "one", "two", "three", "four"
]

React.createElement("ul",
  { className: "someCssClass" },
  list.map(
    (item, i) => 
      React.createElement("li", { key: i }, item) //li need a unique key
  )
)
```
## React Components
### React.createClass
* `React.createClass` may deprecate in future
### React.Component
### Stateless Functional Components
## DOM Rendering
## Factories
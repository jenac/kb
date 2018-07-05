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
* es6
```javascript
class SomeComponent extends React.Component {
  ...
}

```
### Stateless Functional Components
* Stateless functional components are functions, not objects; therefore, they do not have a “this” scope.
* Functions for only to rendering.
* Pass data using props
## DOM Rendering
## Factories
* Using createFactory to create an h1
```javascript
React.DOM.h1(null, "Baked Salmon") //first arg is for properties, second is for the children
```

# React with JSX
## React Elements as JSX
### JSX Tips
* Nested Components
* className will generate HTML `class=""` for css style.
* Javascript expression wrappered in `{ }`, and will evaluated.
* Mapping array to JSX:
```javascript
<ul>
  {this.props.ingredients.map((ingredient, i) =>
    <li key={i}>{ingredient}</li>
  )}
</ul>
```
## Babel
## Intro to Webpack
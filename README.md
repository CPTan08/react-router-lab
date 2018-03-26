# React Router Lab

In this lab, use React Router to create a simple React application that supports URL routing. In this lab, we will focus on how to use React Router, and hence our components will simply comprise just `h1`, `div` and/or `a` tags.

### Getting started
- There's no need to fork and clone this repo. Simply follow the steps below and create a new project on GitHub.com, and add it as a remote in your app directory
- Create react app: `create-react-app my-app-name`
- Install dependencies:
  - `yarn add react-router-dom`
  - `yarn add enzyme enzyme-adapter-react-16 --dev`
- Remove boilerplate code in `App.js#render()`
- Create enzyme config file in `src/setupTests.js`

```js
import { configure } from "enzyme";
import Adapter from "enzyme-adapter-react-16";
configure({ adapter: new Adapter() });
```
- Smoke test:
  - `yarn test` - test should still pass
  - `yarn start` - localhost:3000 should not show any errors

### Tasks

##### MyRouter
- Create a `MyRouter` component, which simply displays:
```html
<div>
  pending implementation
</div>
```
- `MyRouter` is where you will place all of your Route and Links components (or any components that contain Route and Links components)
- Place `MyRouter` inside `App.js#render()`  

##### NavLinks
- Create a `NavLinks` component, which simply displays:

```html
<div>
  <Link to="/">Home Page </Link>
  <Link to="/tacos">Tacos Feed </Link>
  <Link to="/twitter">Twitter Feed </Link>
</div>
```

- Place NavLinks in `MyRouter`

##### HomePage
- Create a component for `HomePage.js`, which simply displays:
  
```html
<h1>This is your home page<h1>
```
- Add a route to `HomePage` component in `MyRouter.js`
  - hint: you will need to `import {BrowserRouter, Route} from 'react-router-dom'`

##### Repeat for TwitterFeed component 

##### Repeat for TacosFeed component

##### Route params for TacosFeed
- Create a `TacoDetail` component and add a route to it in `MyRouter.js`
- This component should simply display:
```jsx
<div>
  detailed page for taco with param {props.match.params.id}
</div>
```
- Any request for localhost:3000/tacos/:id should dipslay this component

##### Add a Redirect component
- Redirect requests for 'tacos/42' to `localhost:3000/specialTacoPage` (you have to define `SpecialTacoPage` component and a Route for this path and component, of course!)


### Bonus
- Add a `Switch` component to your application (see https://css-tricks.com/react-router-4/#article-header-id-2)
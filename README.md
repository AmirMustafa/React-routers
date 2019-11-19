# React JS Routing

For this we have uses react package 'react-router-dom'

# Prerquisites
You should have created 3 to 4 components like <home />, <about />, <contact />

## Installation
1. After basic react app installation create home, about and contact component and write in APP.js
2. npm install 'react-router-dom'
3. In App.js

```
import React from "react";
import logo from "./logo.svg";
import "./App.css";
import Menu from "./components/Menu";
import About from "./components/About";
import Home from "./components/Home";
import Contact from "./components/Contact";

import { BrowserRouter, Route, Switch } from "react-router-dom";  // Added this react router library

function App() {
  return (
    <BrowserRouter>             // must be written
      <div>
        <Menu />
        <Switch>                // Switch - AFter getting proper route break
          <Route path="/" exact component={Home} />   // For getting component from url URI
          <Route path="/about" component={About} />
          <Route path="/contact" component={Contact} />
        </Switch>
        {/* <Home />
      <About />
      <Contact /> */}
      </div>
    </BrowserRouter>
  );
}

export default App;

```

4. To access it  Link:

```
import React from "react";
import "./Menu.css";
import { Link } from "react-router-dom";    // we use link package

const Menu = () => {
  return (
    <div className="Menustyle">
      <ul>
        <li>
          <Link to="/">Home</Link>          // Link to access - works witout refresh
        </li>
        <li>
          <Link to="/about">About</Link>
        </li>
        <li>
          <Link to="/contact">Contact</Link>
        </li>
      </ul>
    </div>
  );
};

export default Menu;

```
## Screenshots

![Screenshot](https://user-images.githubusercontent.com/15896579/69008213-0a2d1280-096e-11ea-913f-961f2caf8812.png?raw=true "Screenshot of Passport jwt auth")

## Video

For understanding
https://www.loom.com/share/d0a64e0fb7a5407082be4e5a7957729f

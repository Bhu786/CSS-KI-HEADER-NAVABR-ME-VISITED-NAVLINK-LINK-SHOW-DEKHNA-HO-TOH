# CSS-KI-HEADER-NAVABR-ME-VISITED-NAVLINK-LINK-SHOW-DEKHNA-HO-TOH

<link> ==> yeh code kam nhi karega 
yeh <NavLink></NavLink> wale me kam karega

### REACT KA NAVLINK
** npm install react-router-dom **
main code yehi hai
```react.js
 style={({ isActive }) =>
          isActive ? { fontWeight: "bold", color: "red" } : undefined
        }
```


Explanation:
NavLink Component: React Router ka NavLink component active link par CSS apply karne ke liye bana hai.
style Prop: style prop ek function accept karta hai jo isActive status ko check karke styles apply karta hai.
Active Styles: Jab isActive true hota hai, tab bold aur red color apply hota hai.
Dynamic Styling: Har NavLink ka style ya className dynamically set hota hai based on the active page.


Example
```react.js
import React from "react";
import { BrowserRouter as Router, Route, Routes } from "react-router-dom";
import Home from "./Home";
import About from "./About";
import Contact from "./Contact";
import Header from "./Header";

const App = () => {
  return (
    <Router>
      <Header />
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </Router>
  );
};

export default App;

```
```react.js
import React from "react";
import { NavLink } from "react-router-dom";

const Header = () => {
  return (
    <nav style={{ display: "flex", gap: "20px", padding: "10px" }}>
      <NavLink
        to="/"
        style={({ isActive }) =>
          isActive ? { fontWeight: "bold", color: "red" } : undefined
        }
      >
        Home
      </NavLink>
      <NavLink
        to="/about"
        style={({ isActive }) =>
          isActive ? { fontWeight: "bold", color: "red" } : undefined
        }
      >
        About
      </NavLink>
      <NavLink
        to="/contact"
        style={({ isActive }) =>
          isActive ? { fontWeight: "bold", color: "red" } : undefined
        }
      >
        Contact
      </NavLink>
    </nav>
  );
};

export default Header;
```









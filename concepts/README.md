1. [**First React**](#first-react)
   1. [**Adding React Scripts**](#adding-react-scripts)
   2. [**Writing React**](#writing-react)
2. [**Why React?**](#why-react)
   1. [**Composable**](#composable)
      1. [**Creating Components**](#creating-components)

---

# **First React**

## **Adding React Scripts**

`index.html`

```html
<script
    crossorigin
    src="https://unpkg.com/react@17/umd/react.development.js"
></script>
<script
    crossorigin
    src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"
></script>
<script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
```

-   Add the above scripts to the head section of the HTML document.

## **Writing React**

`index.html`

```html
<script src="./index.js" type="text/babel"></script>
```

`index.js`

```jsx
ReactDOM.render(<h1>Hello, everyone!</h1>, document.getElementById("root"));
```

-   `<h1>Hello, everyone!</h1>` is the HTML content that is to be added to the "root" element

---

# **Why React?**

## **Composable**

-   Small components can be used to build something Big!

### **Creating Components**

```jsx
function Navbar() {
    return (
        <nav className="navbar navbar-expand-lg navbar-light bg-light">
            <a className="navbar-brand" href="#">
                Navbar
            </a>
            <button
                className="navbar-toggler"
                type="button"
                data-toggle="collapse"
                data-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent"
                aria-expanded="false"
                aria-label="Toggle navigation"
            >
                <span className="navbar-toggler-icon"></span>
            </button>
            ...
        </nav>
    );
}

// Challenge: Create your own custom React component!
// Call it "MainContent", and have it return a simple
// h1 element that says "I'm learning React!"

// Afterward, render it below the Navbar (which
// you can do inside the ReactDOM.render call below)

function MainContent() {
    return <h1>I'm learning React!</h1>;
}

ReactDOM.render(
    <div>
        <Navbar />
        <MainContent />
    </div>,
    document.getElementById("root")
);
```

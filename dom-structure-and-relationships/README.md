<h1>
  <span class="headline">Pre-Selenium: Basic HTML Structure & Elements</span>
  <span class="subhead">DOM Structure and Relationships</span>
</h1>

**Learning Objective:** Interpret how elements are nested within the DOM and understand their visual relationships.

## The DOM Structure

If you have experience building APIs with Python and FastAPI, you already know how crucial it is to understand data structures—such as dictionaries within dictionaries, or lists within objects. With HTML, the page itself is made up of _elements_ inside elements, forming a clear structure that browsers (and automation tools like Selenium) rely on to display and interact with content.

> 💡 _DOM_ stands for _Document Object Model_. It is the browser’s way of understanding the “family tree” of your HTML elements—who is nested inside whom.

### Understanding the DOM Tree

- The entire webpage is represented by the <html> element.
- It contains two main sections: the <head> (metadata, title, styles) and the <body> (visible content).
- Within the <body>, elements are organized hierarchically—containers like <div> may include other elements such as <form>, <button>, or <input>.
- Elements that share the same parent are called siblings. A single parent element can have multiple child elements, and each child can contain its own nested elements, creating a tree-like structure.

In HTML:

- _Parent_: An element that contains other elements.
- _Children_: Elements that are nested inside a parent.
- _Siblings_: Elements that share the same direct parent.

> ♻️ The DOM’s family tree model is universal—no matter where a web page is built or viewed, these relationships are always the same.

<div class="activity guided-walkthrough">
  <h2 class="title">Reading the DOM in DevTools</h2>
  <span class="minutes">5 min</span>
</div>

**Sample HTML for practice:**

```html
<body>
  <div>
    <form>
      <label for="name">Name:</label>
      <input type="text" id="name" />
      <button type="submit">Submit</button>
    </form>
  </div>
  <footer>
    <span>Contact support</span>
  </footer>
</body>
```

**What’s happening here:**

- `<body>` is the parent of both `<div>` and `<footer>`.
- `<div>` is the parent of `<form>`, which is, in turn, the parent of `<label>`, `<input>`, and `<button>`.
- `<label>`, `<input>`, and `<button>` are siblings.

When you open this file in Chrome and inspect it with DevTools, expand the arrows in the Elements panel to watch how elements are nested. Each indentation level represents a new “generation” in the family.

### How nesting affects what you see (and automate)

Nesting is more than just visual organization—it determines how pages look and function, and how automation tools like Selenium can interact with them.

#### Python analogy:

If you have ever nested functions within other functions, or kept key data in a sub-dictionary, you know how important context is. In HTML, clicking a button _inside_ a form triggers a different action than clicking a button alone.

- **Example:**  
  In HTML, a login form might be built like this:

  ```html
  <form>
    <input type="text" name="user" />
    <button type="submit">Login</button>
  </form>
  ```

  If you try to automate filling in the _user_ field and clicking "Login," knowing these elements are grouped inside a `<form>` helps you reliably target them.


### Mapping visual placement to the DOM: Practical analysis

Let’s examine this sample:

```html
<body>
  <main>
    <div class="signup-section">
      <form>
        <label for="email">Email:</label>
        <input type="email" id="email" />
        <button type="submit">Sign Up</button>
      </form>
    </div>
    <footer>
      <span>Help? <a href="#">Contact us</a></span>
    </footer>
  </main>
</body>
```

- `<main>` contains both the `.signup-section` and `<footer>` as siblings.
- The `<form>` inside `.signup-section` wraps its inputs and the submit button.
- `<span>` and `<a>` in `<footer>` flow inline, keeping the sentence together.

> 💡 When inspecting this structure in DevTools, use the arrow icons to expand and collapse sections. This helps reveal complex relationships that may otherwise go unnoticed.

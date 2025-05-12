<h1>
  <span class="headline">Pre-Selenium: Basic HTML Structure & Elements</span>
  <span class="subhead">Instructor Guide</span>
</h1>

## Setup

**How to deliver this microlesson:**

- Emphasize connections between the learner’s Python experience and the new HTML concepts.
- Demonstrate each step using your screen to model setup, file creation, and viewing in a browser.
- Invite learners to personalize their practice pages—encourage a diverse range of interests and introductions in their `<p>` elements to make the activity relatable.
- Walk through the use of browser DevTools. Show how highlighting different elements in the Elements panel maps code to visible output.

**Suggested solution for the activity:**

Expected sample content of <code class="filepath">practice.html</code> after following the steps:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Selenium Practice Page</title>
  </head>
  <body>
    <h2>Automating with Selenium Starts Here!</h2>
    <p>I'm a Python developer practicing HTML for test automation.</p>
  </body>
</html>
```

Learners should be able to see their heading and personalized paragraph in the browser. With DevTools, selecting these tags should highlight the corresponding content on the web page.

## Anatomy of an HTML document

**Delivery recommendations:**

- Encourage learners to draw direct parallels with familiar Python concepts. For example, relate `<head>` to configuration blocks and `<body>` to the main execution area.
- Use live walkthroughs—switch between VS Code and browser/DevTools to demonstrate the connection between code and visible page structure.
- When students experiment with DevTools, prompt them to make changes and observe live updates. This connection reinforces the link between code, DOM, and rendered output.
- Highlight the value of understanding the invisible structure behind what users see, emphasizing its role in efficient automation later.

**Knowledge check answers:**

1. What is the primary purpose of the `<head>` section of an HTML document?

   - Correct answer: To provide information about the page (such as title, metadata, and links to resources).

2. In the HTML structure, what section contains the elements you will target when automating user interactions?
   - Correct answer: The `<body>` section.

---

## Common HTML elements for test automation

### Delivering the microlesson

- Build on the learner’s comfort with structured data (from Python), emphasizing the parallels between Python containers and HTML elements.
- Demonstrate the inspection process visually, opening the sample page in a browser and walking through each element in DevTools.
- Encourage learners to use real-life analogies (like folders, labels, or forms) to describe what they see—helping make abstract concepts more concrete.

### Suggested solution for the activity & discussion

A completed set of answers for one element might look like:

- **Tag name:** `<input>`
- **Content or what it wraps:** None (self-closing tag, but collects user data)
- **Purpose:** To collect the user’s username for login
- **Key attributes:** `type="text"`, `name="username"`, `id="user"`

For the Discussion:

- **Identifying fields:**  
  Use `name="username"` and `name="password"` to select the respective input fields in Selenium. Example pseudocode: “Find the element whose `name` attribute equals 'username' and enter the username.”
- **Identifying the button:**  
  Find the `<button>` where `type="submit"` to automate pressing it for form submission.
- **Identifying `<div>` or `<span>`:**  
  It may be harder to select these for automation since they often lack unique identifiers. If needed, look for parent-child relationships or add temporary attributes just for testing.

## Exploring HTML with Chrome DevTools

**How to deliver this microlesson:**

- Model the opening and use of DevTools on your screen, emphasizing the DOM versus source HTML.
- Walk through each interaction—highlighting, using breadcrumbs, inspecting, and live editing—so learners see the immediate connection between code and display.
- Encourage learners to experiment freely in DevTools, reinforcing that all changes are temporary until the page is refreshed.
- Tie all demonstrations back to test automation: for each tool or inspection technique, discuss how it helps locate, target, or understand elements during scripting or troubleshooting.

## DOM Structure and Relationship

**How to deliver this microlesson:**

- Emphasize the connection between learners’ experience organizing data or code in Python, and how HTML elements form nested structures.
- Use relatable analogies—like family trees or rooms in a house—to clarify the concept of parents, children, and siblings.
- Demonstrate the inspection process in DevTools, modeling how to expand the DOM, use breadcrumbs, and connect the visual layout with the underlying element relationships.
- Encourage learners to articulate, either aloud or in written notes, each ancestor element and its display behavior.
- Remind learners how these skills directly support identifying robust, reliable selectors for browser automation.

---

🏗️ **Under Construction**

We are constantly working to improve our resources for instructors and students.

**Have something to contribute to this Instructor Guide?** [Let us know](https://pages.git.generalassemb.ly/modular-curriculum-all-courses/universal-resources-internal/module-feedback.html).

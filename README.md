# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>JavaScript Interaction</title>
  <style>
    #dynamic-box {
      padding: 20px;
      background-color: lightblue;
      margin: 20px 0;
      border-radius: 10px;
      text-align: center;
    }
  </style>
</head>
<body>
  <h1 id="heading">Welcome!</h1>
  <p id="description">This paragraph will change when you click the button below.</p>

  <div id="dynamic-box">I am a styled box!</div>

  <button onclick="changeContent()">Change Text & Style</button>
  <button onclick="toggleElement()">Add/Remove Element</button>

  <div id="container"></div>

  <script src="script.js"></script>
</body>
</html>


script.js
// Function to change text and style
function changeContent() {
  const heading = document.getElementById("heading");
  const description = document.getElementById("description");
  const box = document.getElementById("dynamic-box");

  heading.textContent = "Hello, JavaScript!";
  description.textContent = "The content and styles were changed using JavaScript.";

  box.style.backgroundColor = "lightgreen";
  box.style.color = "darkblue";
  box.style.fontWeight = "bold";
}

// Function to add or remove an element
function toggleElement() {
  const container = document.getElementById("container");
  const existing = document.getElementById("extra");

  if (existing) {
    existing.remove();
  } else {
    const newElement = document.createElement("p");
    newElement.id = "extra";
    newElement.textContent = "🎉 You added a new paragraph!";
    container.appendChild(newElement);
  }
}

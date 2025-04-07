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


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript DOM Manipulation</title>
    <link rel="stylesheet" href="styles.css"> <!-- Optional CSS link -->
</head>
<body>
    <header>
        <h1>DOM Manipulation with JavaScript</h1>
        <p id="intro">Click the button below to see JavaScript in action!</p>
    </header>

    <section>
        <button id="changeTextBtn">Change Text</button>
        <button id="toggleElementBtn">Toggle Element</button>
    </section>

    <div id="contentSection">
        <p>This content can be removed or changed dynamically.</p>
    </div>

    <footer>
        <p>&copy; 2025 Your Name. All Rights Reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>



// Get references to the elements
const changeTextBtn = document.getElementById('changeTextBtn');
const toggleElementBtn = document.getElementById('toggleElementBtn');
const introText = document.getElementById('intro');
const contentSection = document.getElementById('contentSection');

// Change text content dynamically when the button is clicked
changeTextBtn.addEventListener('click', function() {
    introText.textContent = "You've successfully changed the text! 🎉";
});

// Toggle the visibility of the content section when the button is clicked
toggleElementBtn.addEventListener('click', function() {
    if (contentSection.style.display === "none") {
        contentSection.style.display = "block";
    } else {
        contentSection.style.display = "none";
    }
});



body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
}

header, footer {
    text-align: center;
    background-color: #333;
    color: white;
    padding: 20px;
}

button {
    margin: 10px;
    padding: 10px 20px;
    background-color: #008CBA;
    color: white;
    border: none;
    cursor: pointer;
    font-size: 16px;
}

button:hover {
    background-color: #005f73;
}

section {
    display: flex;
    justify-content: center;
    margin-top: 20px;
}

#contentSection {
    margin-top: 20px;
    padding: 15px;
    background-color: #e2e2e2;
    border-radius: 5px;
}




Explanation:
HTML:

The document has a header with a title and introductory text, followed by two buttons that allow the user to interact with the page.

There's a section (#contentSection) containing some content that can be dynamically toggled on and off using JavaScript.

JavaScript:

changeTextBtn changes the text content of the <p> tag when clicked.

toggleElementBtn hides or shows the content in the #contentSection div each time it's clicked.

CSS (Optional):

Styling is applied for better user experience (button styles, background color, etc.).

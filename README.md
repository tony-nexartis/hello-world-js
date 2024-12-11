# Hello World JavaScript App

A simple web application that displays "Hello World" in different languages when you click a button.

## Files

### index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello World</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1 id="greeting">Hello World!</h1>
        <button id="changeGreeting">Change Greeting</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### styles.css
```css
body {
    margin: 0;
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: #f0f2f5;
}

.container {
    text-align: center;
    padding: 2rem;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

h1 {
    color: #1a73e8;
    margin-bottom: 1.5rem;
}

button {
    padding: 0.8rem 1.5rem;
    font-size: 1rem;
    background-color: #1a73e8;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
}

button:hover {
    background-color: #1557b0;
}
```

### script.js
```javascript
document.addEventListener('DOMContentLoaded', () => {
    const greetings = [
        'Hello World!',
        '¡Hola Mundo!',
        'Bonjour le Monde!',
        'Hallo Welt!',
        'Ciao Mondo!'
    ];

    let currentIndex = 0;
    const greetingElement = document.getElementById('greeting');
    const button = document.getElementById('changeGreeting');

    button.addEventListener('click', () => {
        currentIndex = (currentIndex + 1) % greetings.length;
        greetingElement.textContent = greetings[currentIndex];
    });
});
```

## Features

- Displays a greeting message
- Button to change the greeting to different languages
- Responsive design
- Simple and clean UI

## Usage

1. Clone this repository
2. Create the three files (index.html, styles.css, and script.js) with the code provided above
3. Open index.html in your web browser
4. Click the "Change Greeting" button to see the greeting in different languages

## Technologies Used

- HTML5
- CSS3
- JavaScript

## License

MIT
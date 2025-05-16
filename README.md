# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox and Grid</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <nav class="navbar">
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <div class="main-content">
        <section class="section-left">
            <h2>Section 1</h2>
            <p>This is some content for Section 1.</p>
        </section>
        <section class="section-right">
            <h2>Section 2</h2>
            <p>This is some content for Section 2.</p>
        </section>
    </div>

    <footer class="footer">
        <p>&copy; 2025 My Website</p>
    </footer>

</body>
</html>

body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.navbar {
    background-color: #333;
    padding: 10px 0;
    text-align: center;
}

.navbar ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.navbar ul li {
    display: inline-block;
    margin: 0 15px;
}

.navbar ul li a {
    color: white;
    text-decoration: none;
    font-size: 18px;
}

.main-content {
    display: flex;
    justify-content: space-between;
    margin: 20px;
    gap: 20px;
}

.section-left, .section-right {
    flex: 1;
    padding: 20px;
    background-color: #f4f4f4;
    border-radius: 8px;
}

.footer {
    background-color: #333;
    color: white;
    padding: 10px;
    text-align: center;
    position: relative;
    bottom: 0;
    width: 100%;
}

@media screen and (max-width: 600px) {
    .navbar ul {
        display: block;
        text-align: left;
    }

    .navbar ul li {
        display: block;
        margin-bottom: 10px;
    }

    .main-content {
        flex-direction: column;
    }

    .section-left, .section-right {
        margin-bottom: 20px;
    }
}

@media screen and (max-width: 900px) {
    .main-content {
        flex-direction: column;
    }
}

@media screen and (min-width: 901px) {
    .main-content {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 20px;
    }

    .navbar ul {
        text-align: center;
    }

    .navbar ul li {
        display: inline-block;
        margin: 0 15px;
    }
}


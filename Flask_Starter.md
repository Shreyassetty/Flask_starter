Hello World in Flask with HTML & CSS

```
Created by:
Name: Shreyas B R.
```

---

### What is Flask?

- **Flask** is a lightweight Python web framework that allows you to build web applications.
- It can handle **HTML**, **CSS**, and other web technologies to create interactive and visually appealing websites.

---

### Basic Folder Structure for Flask with HTML & CSS

Here’s the basic structure of a Flask app with both HTML and CSS:

```
/flask_hello_html_css
    /static
        /css
            style.css
    /templates
        hello.html
    app.py
```

- **app.py**: The main Python file for the Flask app.
- **templates/**: Folder for storing HTML files.
- **static/**: Folder for storing static files like CSS, JavaScript, and images.
- **style.css**: The CSS file for styling the HTML content.

---

### Steps to Create a "Hello World" App in Flask with HTML & CSS

1. **Install Flask**:
   - Install Flask using pip:
     ```bash
     pip install flask
     ```

2. **Create the Project Folder**:
   - Create a new folder called `flask_hello_html_css`.

3. **Create the `app.py` File**:
   - Inside the project folder, create a file called `app.py` with the following code:

   ```python
   from flask import Flask, render_template

   app = Flask(__name__)

   @app.route('/')
   def hello_world():
       return render_template('hello.html')

   if __name__ == "__main__":
       app.run(debug=True)
   ```

4. **Create the `templates` Folder**:
   - Inside the project folder, create a folder called `templates` and add a file `hello.html`.

5. **Create the `hello.html` File**:
   - Inside the `templates` folder, create the `hello.html` file and add the following code:

   ```html
   <!DOCTYPE html>
   <html>
   <head>
       <title>Hello Flask</title>
       <link rel="stylesheet" type="text/css" href="{{ url_for('static', filename='css/style.css') }}">
   </head>
   <body>
       <h1>Hello, World!</h1>
       <p>Welcome to Flask with HTML & CSS!</p>
   </body>
   </html>
   ```

   - The `link` tag links the CSS file from the **static/css** folder.

6. **Create the `static/css` Folder**:
   - Inside the project folder, create a folder called `static`, and inside it, create another folder called `css`. This is where you’ll store the CSS file.

7. **Create the `style.css` File**:
   - Inside the `static/css` folder, create a file called `style.css` and add the following CSS code:

   ```css
   body {
       background-color: #f0f0f0;
       font-family: Arial, sans-serif;
       text-align: center;
   }

   h1 {
       color: blue;
   }

   p {
       color: green;
       font-size: 18px;
   }
   ```

8. **Run the Flask App**:
   - Open a terminal in your project folder and run:
     ```bash
     python app.py
     ```

9. **View the App in a Browser**:
   - Open your browser and go to `http://127.0.0.1:5000/`. You should see a styled page with a blue heading and a green paragraph on a light gray background.

---

### Explanation of Folder Structure:

- **app.py**: The main Python file that defines the Flask routes and renders the HTML template.
- **templates/**: The folder where the HTML files are stored.
- **static/css/**: The folder where static files like CSS are stored.

---

### Key Points:

- Flask allows you to integrate **HTML** and **CSS** easily, enabling the creation of visually styled web pages.
- **CSS files** are stored in the **static** folder, while HTML files are kept in the **templates** folder.
- By linking CSS to HTML using Flask, you can style your web pages efficiently.

---

**End of Document** ✨

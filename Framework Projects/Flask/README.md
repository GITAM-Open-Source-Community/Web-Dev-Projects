# Flask 🐍

> Flask is a web application framework written in Python. Armin

### Main features

* Features development servers and debugger functionalities

* It comes with integrated aid for unit testing

* It uses Jinja2 template styles

# Usage

To use this template to start your own project:

### Existing virtualenv

If your project is already in an existing python3 virtualenv first install django by running

    $ pip install flask
    
creat app.py file and run 
```
from flask import Flask
app = Flask(__name__)
@app.route('/)
def home():
    return 'Hello World!'
if __name__ == '__main__':
    app.run()
```

    $ python3 app.py

Now your Good to go 👍
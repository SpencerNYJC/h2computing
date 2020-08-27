## Flask

A standard flask setup will be:

```python
from flask import Flask, render_template, request

# instantiate a Flask instance
app = Flask(__name__)

# this is the root directory for the domain
@app.route("/")
def main():
    # renders the html file in ./templates/index.html
    return render_template("index.html")

# run webserver at 0.0.0.0 (localhost) or (127.0.0.1)
# default port is 5000
app.run("0.0.0.0")
```



### Forms

The following HTML code creates a simple form which sends a GET request to /search with the parameters "x" and "y".

```html
<!DOCTYPE html>

<html>
    <head>
        <title>Title</title>
    </head>
    <body>
        <form action="/multiply" method="get">
            <label>Number 1:</label>
            <input type="text" name="x" value="">
            <label>Number 2:</label>
            <input type="text" name="y" value="">
            <input type="submit" value="Multiply">
        </form>
    </body>
</html>
```

Correspondingly, we must write a function which processes the request.

```python
@app.route("/multiply")
def multiply():
    # check if x is sent in the GET request
    if 'x' in request.args and 'y' in request.args:
        # retrieve data x and y
        x = float(request.args['x'])
        y = float(request.args['y'])
        result = x * y
        
        # return render_template(html_file, *args)
		# arguments can be passed into render_template to be displayed
        return render_template('multiply.html', result=result)
        
```



### Jinja2

There are a few kinds of delimiters. The default Jinja delimiters are configured as follows:

- `{% ... %}` for [Statements](https://jinja.palletsprojects.com/en/2.11.x/templates/#list-of-control-structures)
- `{{ ... }}` for [Expressions](https://jinja.palletsprojects.com/en/2.11.x/templates/#expressions) to print to the template output
- `{# ... #}` for [Comments](https://jinja.palletsprojects.com/en/2.11.x/templates/#comments) not included in the template output
- `# ... ##` for [Line Statements](https://jinja.palletsprojects.com/en/2.11.x/templates/#line-statements)

Using our current example, we have to display the variable `result` in multiply.html

```html
<!DOCTYPE html>
<head>
    <title>Title</title>
</head>
<body>
    <p>
        {{ result }}
    </p>
</body>
```

By using `{{ result }}`, we can display the variable `result` that was passed into the `render_template()` function.


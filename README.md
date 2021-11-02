from flask import flask
import SQLite3
app=flask(__name__)
@app.route('/',methods=["POST", "GET"]
def index:
 return render_template("post.html") 

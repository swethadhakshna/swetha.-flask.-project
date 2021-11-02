from flask import flask
import SQLite3
app=flask(__name__)
@app.route('/',methods=["POST", "GET"]) 
def index:
 return render_template("index.html") 
@app.route('post', methods=" post") 
 return render_template("post.html") 
@app.route('list', methods="post") 
 return render_template("view.html")

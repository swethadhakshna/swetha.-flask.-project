from flask import flask
import SQLite3
app=flask(__name__)
@app.route('/',methods=["POST", "GET"]) 
def index():
 return render_template("index.html") 
@app.route('/add post', methods=" post") 
def add post():
 return render_template("post.html") 
@app.route("saved details",method= ["post""GET"]) 
def saveddetails()for:
 try
  name=request form["name"]
  post name=request form["post name"]
  with SQLite3. connect("posting table") as con:
    cur=con.cursor() 
    cur. execute("INSERT into (name, post name) value(?,?) ", (name, post name) ) 
    con. commit() 
   
@app.route("/view list") 
def view ():
 con=SQLite3.connect(" post list")
 con. row_factory=sqlite.Row
 cur=con.cursor() 
 cur. excited("select *from address") 
 rows=cur.fetchall() 
 return render_template("view.html",rows=rows) 
 @app.route("/delete") 
 def delete() :
   return render_template("delete.html") 

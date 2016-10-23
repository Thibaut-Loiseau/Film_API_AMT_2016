# AMT-Projet01

Welcome to the Java EE application for AMT teaching at HEIG-VD.

In this application an user can register or login and ask for the actor list for a specified film on the database.

All the film in the database are from the well known sakila database.

You can also access to the REST API with the specified commands.

# SETUP and DEPLOY

WARNING : You will need Maven and docker to deploy this app.

Then only 2 steps to setup :

 -Clone the repo

 -Run the .sh

# API REST

GET			/api/films/{title}		Get all actors for the specified film

GET			/api/films/				Get all the films

POST		/api/films/				Add a film from the specified DTO in JSON

You need to secify the header 'Content-Type' with the value: 'application/json' and secify a json in the body like this

{

	"actors": [

	    {

	      "actor_id": id,

	      "first_name": fname,

	      "last_name": lname

	    }

	],

	"title":title

}

DELETE		/api/films/{title}		Delete the film with the specified title

PUT			/api/films/{OldTitle}			Update the title of the film

You need to secify the header 'Content-Type' with the value: 'application/json' and secify a json in the body like this

{

	"title":NewTitle

}



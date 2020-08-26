*Laudable.tech - Backend*

This is the backend API for the website: https://laudable.tech/ . The API allows the frontend to add users, authenticate/authorize users, add audio files, download audio files, search for audio files, like audio files, and have all liked audio files show up on the logged in users profile.

Frontend respository: https://github.com/Sc0tticus/Laudable-Frontend

*Built With*

Frontend: JavaScript, React v16.8.2, React-Apollo v2.4.1, React-Dom v16.8.2, React-Player v1.9.3,
React-Router-Dom v4.3.1, React-Scripts v2.1.5, Material-UI v3.0.1, Apollo-Boost v0.1.28, 
Axios: v0.18.0, GrapQL v14.1.1,

Backend: Python 2.7.16, Insomnia REST API, aniso8601 v7.0.0, asgiref v3.2.10, autopep8 v1.5.4, dj-database-url v0.5.0, Django v3.1, django-cors-headers v3.4.0, django-graphql-jwt v0.3.1, django-heroku v0.3.1, graphene v2.1.8, graphene-django v2.13.0, graphql-core v2.3.2, graphql-relay v2.0.1, gunicorn v20.0.4, promise v2.3
psycopg2 v2.8.5, psycopg2-binary v2.8.5, pycodestyle v2.6.0, PyJWT v1.7.1, pytz v2020.1, Rx v1.6.1
singledispatch v3.4.0.3, six v1.15.0, sqlparse v0.3.1, toml v0.10.1, Unidecode v1.1.1, 
whitenoise v5.2.0

https://cloudinary.com/: was used to host all of the uploaded audio files.

*App Features*

Become an Authenticated/Authorized User:
Create a user account with your name, email, and password and get authenticated via Django-GrapQL-JWT. 

Create, Read, Update, and Delete, Audio Files (Full CRUD):
This API endpoint allows users to create (upload) MP3 files of their choosing provided the file size is < 15MB.Creating an audio file requires users to give their audio file a Title, Description, as well as attach a audio file. Users can also read, update, and delete audio files that they have created. When a user creates an audio file the audio track that user created will show up on that user's profile.

Download Audio Files:
This API endpoint allows users to download MP3 files of their choosing.

Like Audio Files:
This API endpoint allows users to like audio files of their choosing. Liked audio files will show up on that users profile.

Search Audio Files:
This API endpoint allows users to search for audio files uploaded to https://laudable.tech/.

*Demonstration Video*
https://www.youtube.com/watch?v=y4oTaBYJs8w&feature=youtu.be


*Challenges*

This is my first project coding in Python and working with Graphene-Django, GraphQL, Insomnia, and Cloudinary. Using Graphene-Django simplified much of the backend code however understanding the nuances of how to succesfully do things within Python's virtual environment had me struggling at times. I also found the process of using GraphQL to create seed data and in using the Insomnia API REST Client for verifying user AUTH with JWT tokens, quite challenging.

*Future Implementation*

-Allow users to upload profile pictures.
-Allow users to upload PDF's of their published work to be included with the audio file.
-Text-to-speech option on uploaded PDF's in case the user doesn't have time to record an audio file.

*Collaboration*

Fork and/or clone this repo & the frontend repo - https://github.com/Sc0tticus/Laudable-Frontend
Create PostgreSQL database createdb laudible_db
Migrate database tables in backend: python3 manage.py migrate
Run backend server: python3 manage.py runserver
Install dependencies on frontend: npm install
Run frontend server: npm start
Checkout new branch

If you'd like to collaborate on this project, please email me at: ssinger303@gmail.com

git filter-branch --env-filter '

OLD_EMAIL= "github email address"
CORRECT_NAME= "Scott Singer"
CORRECT_EMAIL= "ssinger303@gmail.com"

if [ "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL" ]
then
export GIT_COMMITTER_NAME="$CORRECT_NAME"
export GIT_COMMITTER_EMAIL="$CORRECT_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL" ]
then
export GIT_AUTHOR_NAME="$CORRECT_NAME"
export GIT_AUTHOR_EMAIL="$CORRECT_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags



git push --force --tags origin 'refs/head'
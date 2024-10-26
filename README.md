# AGE-OF-ROBOTICS
Welcome to the Robotics Enthusiast Hub! This repository contains the source code and resources for a comprehensive website dedicated to the fascinating world of robotics. The website provides insights into robotics technology, trends, educational resources, and projects aimed at beginners and experts alike.
HERE WE HAVE USE GOOGLE GEMINI API KEY TO FETCH RESPONSES FROM THE GEMINI .
MAXIMUM TOKEN LIMIT IS 1,00,000 .
The app is made using python flask, javascript html5 , css3 and javascript .
Since the github supports only static websites , then to dynamically see the interface running and giving responses , use heroku to host the backend.
Hosting your Python Flask application on GitHub won't directly allow the Google Gemini API responses to function because GitHub Pages only supports static content (like HTML, CSS, and JavaScript), not dynamic server-side processing like Flask.

To properly host your Flask app, which relies on the Google Gemini API for dynamic responses, you should consider using a platform that supports server-side applications, such as:

Heroku: It's user-friendly and integrates well with GitHub for deployment.
PythonAnywhere: A simple platform for hosting Python applications.
Render: A cloud application platform that supports Python applications.
AWS, Azure, or Google Cloud: These are more advanced but very robust options for hosting.
If you still want to use GitHub, you can store your code there and then deploy it to one of the platforms mentioned. Let me know if you need help setting up the hosting!
Heroku is excellent for deploying Python Flask applications. Here's a brief guide to help you get your Flask app hosted on Heroku:

Setup Heroku CLI:

Install the Heroku CLI on your system if you haven't already.
Log in using heroku login in your command line.
Prepare Your Flask App:

Ensure your app has a requirements.txt file listing all the dependencies (you can create one using pip freeze > requirements.txt).
Create a Procfile in your app's root directory with the content:
web: python app.py
Replace app.py with the name of your Flask app's main file if it's different.
Initialize Git:

Make sure your app is version-controlled using Git. If not, initialize it:
csharp

git init
git add .
git commit -m "Initial commit"
Create Heroku App:

Use the command:
lua


heroku create
This will create a new app and set up a Git remote called heroku.
Deploy to Heroku:

Push your code to Heroku:


git push heroku main
If you are using a different branch, replace main with your branch name.
Check and Scale:

Make sure your app is running by scaling the web process:

heroku ps:scale web=1
Access Your App:

Open your app using:

heroku open
For your app to successfully interact with the Google Gemini API, ensure that your API key and related configurations are correctly set up as environment variables on Heroku. You can set environment variables using:


heroku config:set GEMINI_API_KEY=your_api_key_here

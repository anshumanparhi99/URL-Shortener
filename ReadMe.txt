# URL-Shortener
As this is a website runs locally on your computer, you need have some python libraries installed before you try to run the web site.
Follow the commands to install the websites.
Open Command Prompt on your computer (Search "cmd" on your computer and click enter)
type the follwing coammnds:
pip install django (wait for sometime for the library to get installed)
pip install graphene-django (wait for sometime for the library to get installed)

open the shorty folder
go to the directory bar and type "cmd" and press enter. You will see the cmd window pop up.
type "python manage.py runserver"
open http://localhost:8000/graphql on your computer.
you will get a text editor window and an output window.
in the text editor window, type the following
mutation {
  createUrl(fullUrl:"<url>") {  //(paste your url inside the double quotes)
    url {
      id
      fullUrl
      urlHash
      clicks
      createdAt
    }
  }
}

and press the play button up top. and you will see the following output.

{
  "data": {
    "createUrl": {
      "url": {
        "id": "2",
        "fullUrl": "<url>",
        "urlHash": "<lorem ipsum>",
        "clicks": 0,
        "createdAt": "2020-01-30T19:31:10.820062+00:00"
      }
    }
  }
}

copy the urlhash value
and paste it in the following text:
http://localhost:8000/<urlHash> and open the website.
this is merely a skeletono of a URL shortening system.
for more, use the tutorial at https://www.digitalocean.com/community/tutorials/how-to-create-a-url-shortener-with-django-and-graphql
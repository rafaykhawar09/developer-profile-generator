# developer-profile-generator

# Unit 09 Node.js and ES6+ Homework: Developer Profile Generator

I successfully created a command-line application that dynamically generates a PDF profile from a GitHub username. The application will be invoked with the following command:

```
node index.js
```

The user will be prompted for their github username and a color to choose from a list of colors, which then be used as the background color for cards.

The PDF will be populated with the following:

* Profile image
* User name
* Links to the following:
  * User location via Google Maps
  * User GitHub profile
  * User blog
* User bio
* Number of public repositories
* Number of followers
* Number of GitHub stars
* Number of users following

# Working of the app

To run the app do the following: 

* Inside the terminal enter the command "npm install" to install all the npms used in this program, which have already been listed in package.json

* After that run the command "node index.js"

* The program is going to prompt the user, asking for the user's github username and to choose a color they like 

* An axios call is made to github api in order to get the user's data, to later populate the html page

* Due to the limitations of the the github api itself, which returns only the first 30 "starred" repositories

* In order to resolve this issue and get the actual number of starred repositories github-scraper npm was used

* After all the data has been retrieved html is generated and populated with the user data

* It is then written onto a file using pdfcrowd npm - the issue with this npm is that it is paid and allows only a limited number of api calls

* Link to the video: https://drive.google.com/open?id=1mT6QPW89bifK0LyRwiQVD_kalA412Am0
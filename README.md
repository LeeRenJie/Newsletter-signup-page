# A Basic newsletter signup page that stores user's first name, last name and email into your Mail Chimp account. This project is based on the tutorial by Angela Yu on Udemy.
<b>Install:</b>
* [Hyper Terminal as my main terminal](https://hyper.is/)
* [Node.js (LTS recommended)](https://nodejs.org/en/)
* [git](https://git-scm.com/)
* [Heroku CLI](https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up)

<b>Documentation:</b>
1. Download all the files in this repository. Note that there are some parts that needs to be changed in the <b>app.js</b> file
1. Create an account on [Mail Chimp](https://mailchimp.com/)
   1. Click the bottom left to be directed to your profile.
   1. Click extras > API keys
   1. Click "Create a key". Your key would look like `xxxxxxxxxxxxxxxxxxxx-us7` note that the `us7` is your server ID.
   1. Copy the API key and server ID in a safe place. Treat it as a password. (Note that if your API keys are exposed in an public websites Mail Chimp will automatically disable the API key)
   1. Click on "Audience" > "Manage Audience" > "Settings" 
   1. Scroll down and copy the "unique ID for audience" and save it somewhere. 
1. Click into the app.js file using an Editor (VS Code or Atom).
   1. Replace `"YOUR_API_KEY"` with the API key copied
   1. Replace `"YOUR_SERVER_ID"` with the server name (for example: us7)
   1. Replace `"YOUR_UNIQUE_AUDIENCE_ID"` with the Unique ID for audience copied.
  
1. Create an account on [Heroku](https://heroku.com) 
1. Open the Hyper terminal
    1. Change directory to the folder you downloaded all the files. 
    1. For example: `$cd Desktop/Newsletter-signup-page`
    1. type in  `ls` which means "list". This will list all the files available in the directory. Therefore, the files you downloaded above should be the output.
    1. Other useful commands(Case sensitive. Spaces and spelling are important) :

    1. Description | Command
       ------------ | -------------
       Back to initial directory | `cd ~`
       Back to previous directory | `cd ..`
       Creating files | `touch file_name`
       Creating directory | `mkdir directory_name`
       Clear console(Will not delete commands) | `clear`

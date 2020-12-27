# A Basic newsletter signup page that stores user's first name, last name and email into your Mail Chimp account. This project is based on the tutorial by Angela Yu on Udemy.

![Image of the Newsletter Signup Page](https://github.com/LeeRenJie/Newsletter-signup-page/blob/main/newsletter-page.png)

<b>Install:</b>
* [Hyper Terminal as the main terminal](https://hyper.is/)
* [Node.js (LTS recommended)](https://nodejs.org/en/)
* [git](https://git-scm.com/)
* [Heroku CLI](https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up)

<b>Documentation:</b>
1. Download all the files in this repository(except "newsletter-page.png") into a folder and remember the folder's name and path. 
    * Folder Name Example: Newsletter-Signup-Page. 
    * Folder Path Example: yourName/Desktop/Newsletter-Signup-Page.
    * Note that some parts need to be changed in the <b>app.js</b> file

1. Create an account on [Mail Chimp](https://mailchimp.com/)
   1. Click the bottom left from the dashboard to be directed to your profile.
   1. Click extras > API keys
   1. Click "Create a key". 
      * Your <b>API key</b> would look like `xxxxxxxxxxxxxxxxxxxx-us7` 
      * Note that the `us7` is your <b>Server Name/ID</b>.
   1. Copy the <b>API Key</b> and <b>Server Name</b> in a safe place. Treat it like a password. (Note that if your API keys are exposed in public websites, Mail Chimp will automatically disable the API key)
   1. Click on "Audience" > "Manage Audience" > "Settings" 
   1. Scroll down and copy the <b>"Unique ID for audience"</b> and save it somewhere. 
   
1. In the app.js file:
   * Replace `"YOUR_API_KEY"` with the API key copied
   * Replace `"YOUR_SERVER_NAME"` with the server name (for example: us7)
   * Replace `"YOUR_UNIQUE_LIST_ID"` with the "Unique ID for audience" copied.
  
1. Create an account on [Heroku](https://heroku.com) 

1. Open the Hyper terminal
    1. Change the directory to the folder you downloaded all the files using `cd`.
    1. For example: `$cd Desktop/Newsletter-Signup-Page`
    1. type in  `ls` which means "list". This will list all the files available in the directory. Therefore, the files you downloaded should be the output.
        * For example: signup.html failure.html success.html public/ app.js procfile   
    1. Other useful commands(Case sensitive. Spaces and spellings are important) :

       Description | Command
       ------------ | -------------
       Back to initial directory | `cd ~`
       Back to previous directory | `cd ..`
       Creating files | `touch file_name`
       Creating directory | `mkdir directory_name`
       Clear console (Will not delete commands, just keeping it tidy!) | `clear`
       Removing files |`rm myfile`
 
1. Make sure node.js and git are installed. Type `node --version` and `git --version`. If a version is shown, then you have node and git installed.
1. Make sure you are inside the directory. Then we will start by creating a package.json file by initializing [npm](https://www.npmjs.com/).<br> `npm init`
1. Press Enter for all the default fields.
1. Next we will be installing modules from npm. (express, mail chimp, and body-parser)
    * `npm install express` or `npm i express` (Both the same)
    * `npm install @mailchimp/mailchimp_marketing`
    * `npm install body-parser`
    * `npm install -g nodemon` (You can send your files on the local host with [nodemon](https://nodemon.io). The server restarts itself each time you make a change to your files)
         * In the hyper terminal type `nodemon app.js`
         * It should log "server running at port 3000"
         * Go to your browser and type localhost:3000 to see the page.
         * You can change the image of the signup page. (redirect the path to your image. Make sure it is in the images file in the public folder)
         * You can change the design. (I used bootstrap 4 for the design. Read the [documentation](https://getbootstrap.com/docs/4.5/getting-started/introduction/) and edit)
    
    * You should see this in your package.json file:
    ```javascript
      "dependencies": {
         "@mailchimp/mailchimp_marketing": "^3.0.27",
         "body-parser": "^1.19.0",
         "express": "^4.17.1",
         }
    ```
    
1. Run the files on a local server to check if it works:
    * run `nodemon app.js` in Hyper terminal
    * In browser type localhost:3000
    * Fill in the fields.
    * Make sure you are directed to the success.html page after pressing sign up
        * if it is directed towards the failure.html page, check your API key, server name, and the unique list ID inserted earlier.
    * Go to your chimp mail account > audience > all contacts and see if your inputs are recorded there.
 
 1. If successful, we will now use Heroku to host the signup page and it will be on the world wide web to be shared.
 1. Run `heroku --version` if a version is not shown: run `npm install -g heroku`
 1. Run `heroku login` and you will be directed to a page or required to enter your email and password.
 1. Make sure you are still in the directory. `ls` to see all the files in the folder. You should have package.json files, HTML files, procfile, public folder, etc...
 1. Run `git init` to initialise git
 1. Run `git add .` add the files
 1. Run `git commit -m "Type anything here as a description"` and all the files will be committed 
 1. Run `heroku create`
     * You should see a link `https://Random-website-name.herokuapp.com/` in blue. Click it and you will see "Heroku | Welcome to your new app". This shows that you have succeeded.
     
1. Run `git push heroku master` to push your files to the heroku.
1. Refresh the page from the link just now or head to your heroku dashboard and click on "open app" 
1. You should see the signup form.
1. Test the form by inputting and checking mail chimp again.
1. If the record appears on Mail Chimp, <b>CONGRATULATIONS!</b> You have successfully created the page and hosted it on the worldwide web.

<hr> 

### Additionals<br>
* To change the URL name, refer [here](https://devcenter.heroku.com/articles/renaming-apps)
* You can now share it with others for them to signup for your newsletter and view their emails via Mail Chimp.
* An alternative for email marketing!
* There are explanations in the app.js file to have a brief explanation of how each line of codes work.
* You can change the texts in the HTML file in between the opening and closing tags.

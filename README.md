# PAPA React JS Resume Starter Pack and Digital Portfolio

![PAPA React JS Portfolio Starter Pack](resume-screenshot.jpg?raw=true "PAPA React JS Portfolio Stater Pack ")

### <a href="https://resume-portfolio-starter-pack.herokuapp.com">LIVE DEMO</a>
Updated on 19-12-24

render it with RENDER, no free Heroku
Delete the node_modules folder and package-lock.json file
and reinstall them with
$npm install
$ npm audit fix


then go to step 7


## Resume Starter Pack Description

This portfolio starter pack is made using React. The data on the portfolio is directly linked to a JSON file. Any changes to the portfolio can be made in the JSON file. The changes will then be reflected on to the portfolio. This allows you to customize your own personal portfolio that can be used for applying to jobs or other personal uses. If you need to use this portfolio for your own personal website then follow the steps below:

## 1. Initial Setup Procedures

Firstly, you will need to download the latest version of Node by <a href="https://nodejs.org/en/download/">CLICKING HERE</a>

## 2. Building a Create-React-App

Next, you will build the application using Create-React-App. Go <a href="https://reactjs.org/docs/installation.html">HERE</a> to get started. (A video demonstration of this step can be found in our Zero to Full Stack Hero module)
Once the build procedure is finished run the command `cd yourappname` and then `npm start` to confirm the app works

## 3. Download the template

Once the steps above have been followed successfully, download the code above using the green button.
IMPORTANT: You will have to replace the "public" and "src" folders of your newly built app with the downloaded code. Run the command `npm start` after and you should see a similar render like the LIVE DEMO link above. If it is not the same then go back to Step 1 and try again.

## 4. Fill in your personal info

To populate the website with all of your own data, open the public/resumeData.json file and simply replace the data in there with your own. Images for the porfolio section are to be put in the public/images/portfolio folder.

## 5. (OPTIONAL) Replacing images and/or fonts

If you want to display your own pictures then you have to replace the files at these locations: public/images/header-background.jpg, public/images/testimonials-bg.jpg and public/favicon.ico. FILE NAMES MUST NOT BE CHANGED UNDER ANY CIRCUMSTANCES.

## 7. Finalising Resume

Once all the formatting and data input is finalised, run the command `npm start` and you'll see your resume on local host.
if you get error, you need to update the package.json file with 

"start": "react-scripts --openssl-legacy-provider start",



Then finally run `npm run build`. This will create a dedicated build folder.

To deploy on firebase

$ npm install -g firebase-tools

$ firebase login > will take you to log into yoru firebase account

$ firebase init

select hosting option and follow the screen options to login to firebase with pre created or new created location 
in the hosting setting set the answers y-y-n
Do not connect the github update

$ firebase deploy


## 8. Host Resume Online

1) Upload all the Resume related files to your Github Profile
2) Go to <a href="https://render.com">Render</a> and set up your profile
3) Create a New Web Service
4) Connect your GitHub repository
5) Select the correct resume repository that you uploaded in Step 1 and deploy

## Credits

##### Original Idea

<a href="https://github.com/tbakerx/react-resume-template/blob/master/README.md">Inspiration from Tim Baker (tbakerx)</a>


## Manual deploy

npm run build

then move the build folder to hosting site

update the .htaccess file with
<IfModule mod_rewrite.c>
  RewriteEngine On
  RewriteBase /
  RewriteRule ^index\.html$ - [L]
  RewriteCond %{REQUEST_FILENAME} !-f
  RewriteCond %{REQUEST_FILENAME} !-d
  RewriteRule . /index.html [L]
</IfModule>
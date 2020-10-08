# My Portfolio

This repository contains the code used during the **"Build your Portfolio Website for FREE" Firebase Virtual Hands-on-Workshop** organized by Developer Student Clubs, Alex Ekwueme Federal University Ndufu Alike Ikwo (DSC AE-FUNAI), on Friday, 9th October 2020, from 8pm to 10:30pm GMT+1, on the [DSC AE-FUNAI WhatsApp Group](https://bit.ly/dscaefunaiwhatsapp). Know more about the event at https://dsc.community.dev/e/mjgxev/ 

## Workshop Instructions
The instructions to follow are divided under two categories. The first category (Github) involves getting the website and customizing it for your portfolio, while the second category (Firebase) involves setting up a Firebase project and deploying your website with Firebase for FREE.

### A. GitHub 
1. [Fork](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo) this [repository](https://github.com/DSC-AEFUNAI/myportfolio). The fork button is at the top right corner of this page (Be sure you are viewing this README from GitHub and on a desktop site).

2. Setup Git on your computer.
  * Download and install Git for your computer type from https://git-scm.com/download
  * Setup your name and email on your computer's Git using the following commands
    ```
    git config --global user.name "YOUR NAME"
    git config --global user.email "email@example.com"
    ```

3. [Clone your fork](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo#step-2-create-a-local-clone-of-your-fork)  of this repo, locally on your computer. Use the following command a terminal/command line. 
    ```
    git clone https://github.com/YOUR-GITHUB-USERNAME/myportfolio
    ```
4. Edit the contents of the website to contain your name and bio instead. 
  * Open the `myportfolio` folder you just cloned in a text editor of choice. 
  * Open `index.html` found in the `public` folder. 
  * Locate the following code in the upper `head` part. 
      ```
      <title>DSC AE-FUNAI | Developer Student Clubs | Alex Ekwueme Federal University Ndufu Alike</title>
      <meta name="keywords" content="Developer Student Clubs, DSC, Google Developers, AE-FUNAI, DSC AE-FUNAI">
      <meta name="description" content="DSC AE-FUNAI is a university based community group for AE-FUNAI students, to bridge the gap between theory and practice, to grow their knowledge in a peer-to-peer environment, and to build solutions for local, business and community problems.">
      ``` 
  * Edit the contents of the `<title> ... </title>` tag to contain your full name instead.
  * Edit the contents of the quotation marks (" ") of the `content="..."` attributes found in the next two  `<meta>` tags to contain your full name and your bio respectively.
  * Next, locate the following code in about a next few lines.
    ```
        <h1 id="name">DSC AE-FUNAI</h1>
        <p id="bio">Developer Student Clubs || Alex Ekwueme Federal University Ndufu Alike Ikwo.</p>
    ``` 
  * Edit the contents of the `<h1 id="name"> ... </h1>` and the `<p id="bio"> ... </p>` tags to contain your full name and bio respectively. 

5. Edit the contents of the website to contain your own social media links. 
  * Still in the `index.html` file, locate the 5 social links all starting with `<a href="https://...`. 
  * Replace the usernames on the URLs of various social media profiles (at the end of the contents of `href="..."`) with your own usernames. 
  * When editing for [LinkedIn](https://linkedin.com), change the "company" in the URL to "in". That is instead of `href="https://linkedin.com/company/...`, use `href="https://linkedin.com/in/...`
  * If there are any social media there you don't use, delete the entire `<a> ... </a>` tag for that social media link OR create an account on the respective social media platform and update with your username accordingly.

6. Change the website pictures to contain your pictures instead. 
  * Navigate into the `images` folder, contained in the `assets` folder, in the `public` folder. There are 6 images there in: profile-picture.jpg and gallery-N.jpg where N are numbers 1 to 5. 
  * Get your 6 square pictures of yourself (preferably, one of them should be one head/face shot for your profile picture). 
  * Delete the 6 pictures of DSC AE-FUNAI's logo and flyers. 
  * Copy your 6 pictures into this images folder. 
  * Rename your head/face shot to `profile-picture.jpg`. Rename the other 5 to `gallery-1.jpg`, `gallery-2.jpg`, `gallery-3.jpg`, `gallery-4.jpg` and `gallery-5.jpg`. 
  * **Note:** Your pictures should all be squares for best results. In other words, their widths and heights should be equal. Some DSC AE-FUNAI flyers in the images folder are not squares and were intentionally left that way to show how poor non-square pictures would look on this simple portfolio website.
   
7. Save your changes to your GitHub fork. 
  * **(Optional)** If you are familiar with HTML and CSS, you can also edit and test the website files to change/add any other customizations you want.
  * In your terminal/command line, be sure you are in the `myportfolio` folder. (Run `cd myportfolio` to enter the folder, if you are not in it, in your terminal/command line). 
  * Run the following commands, in that exact order, to save your personal changes to GitHub.
    ```
    git add .
    git commit -m "Update website to use my personal details"
    git push -u origin main
    ```
    
#### Congratulations!!! You now have your personal portfolio website. Now is time to deploy it for FREE with Firebase.

### B. Firebase
[Firebase](https://firebase.google.com) is a platform developed by Google for creating mobile and web applications. Firebase is easy to use and has many services you can employ in building your apps. One of such Firebase Services is Firebase Hosting with which you can deploy a website in a few minutes by just running the `firebase deploy` command. In addition, Firebase gives you free .web.app domain names for all sites deployed with Firebase.

#### On Firebase Projects and Project IDs
Everything done in Firebase is done in a project. Essentially, a Firebase project serves as a reference container where you can access all Firebase services. When creating a project, you give the Firebase project a name. However, in addition to the project's name, Firebase auto-generates a *permanent globally unique* project ID alongside your project's name. This project ID can be found below the project's name in a smaller size font, together with a pencil icon. You can customize this project ID before creating the project, and once the project is created, you cannot edit the project ID again. 

The first site you deploy through a Firebase project is deployed to YOUR-PROJECT-ID.web.app. What this means is, your portfolio website will be at a YOUR-PROJECT-ID.web.app and you have to customize with the way you want at the time of creating the project else, you can't change it again. 

Feel free to remove the appended random letters and numbers and use a project ID coined from your name or nickname; totally unrelated to the project's name itself. Continue the following instructions to deploy your just-created-portfolio website with Firebase, so that anyone out there can access it. Remember to set a desirable project ID so you can share your portfolio website with a FREE and nice.web.app domain name.

8. Create a Firebase project.
  * Go to https://console.firebase.google.com
  * Create a new project, name it `MyPortfolio`
  * Customize the project ID as you wish (you can use a tweaked version of your name). Remember that it will be your .web.app domain name.
  * Enable [Google Analytics](https://analytics.google.com/analytics/web/) so you can track website visitors. 

9. Setup Firebase on your computer.
  * Download and install NodeJS from https://nodejs.org/
  * In your terminal/command line, install Firebase by running the following command
    ```
    npm install -g firebase-tools
    ```
  * Login into your Firebase in your terminal/command line with your Google account by running the following command
    ```
    firebase login
    ```

10. Deploy your portfolio website with Firebase.
  * Still in your terminal/command line, while in your `myportfolio` folder, run the following command to link your Firebase project with your website data. Press Enter to choose your project and when prompted for project alias, use `default`
    ```
    firebase use --add
    ```
  * Finally, deploy your website
    ```
    firebase deploy
    ```

#### Hooray!!! 
If you got to this point, look into a mirror, tap yourself on the back, and be proud that you just got for yourself a personal portfolio website. Share it with your friends and enter it in your online profiles. Your portfolio website is at YOUR-PROJECT-ID.web.app






[![Codemagic build status](https://api.codemagic.io/apps/61408ce7db3816c8e2627b45/61408ce7db3816c8e2627b44/status_badge.svg)](https://codemagic.io/apps/61408ce7db3816c8e2627b45/61408ce7db3816c8e2627b44/latest_build)



# PWA Tutorial

Link:  
[Website-Preview](https://flutter-flashcard-portrait-pwa.firebaseapp.com/#/)  

<img src="https://github.com/iwilfried/Flutter-Flashcards-Portrait-PWA/blob/main/assets/images/Flash.png" width="150">  

# PWA Tutorial
- Clone your project and open this project in your IDE.
- Open your IDE terminal and type
```sh
$ dart pub get
```  
```
$ flutter config --enable-web
```
- You may need to restart your IDE to read new settings.
- Run your app on chrome first (optional) to make sure your app runs as expected.
```
$ flutter run -d chrome
```
Now get build for web with 
```
$ flutter build web
```
&nbsp;

## PWA With Firebase
- Erstellen Sie zuerst ein Firebase-Konto und ein neues Project: &nbsp;&nbsp; <https://firebase.google.com>  

<img src="https://github.com/iwilfried/Flutter-Flashcards-Portrait-PWA/blob/main/assets/images/firebaseProjekt.gif" width="650" height="450" />

Open your IDE Terminal and login with
```
$ firebase login
```
```
$ firebase init
```
Before we get started, keep in mind:

  * You are initializing within an existing Firebase project directory

? Are you ready to proceed? Yes  

? Which Firebase features do you want to set up for this directory? Press Space to select features, then Enter to confirm your choices. Press space to select, a to toggle all, i to invert selection, and enter to proceed)  
```
 ( ) Firestore: Configure security rules and indexes files for Firestore  

 ( ) Functions: Configure a Cloud Functions directory and its files  

>(*) Hosting: Configure files for Firebase Hosting and (optionally) set up GitHub Action deploys    

( ) Hosting: Set up GitHub Action deploys  

 ( ) Storage: Configure a security rules file for Cloud Storage  

 ( ) Emulators: Set up local emulators for Firebase products  

 ( ) Remote Config: Configure a template file for Remote Config  
```
(Move up and down to reveal more choices)

Woohoo!
Firebase CLI GitHub Login Successful

You are logged into GitHub via the Firebase CLI. You can immediately close this window and continue using the Firebase CLI.

Node.js installation is required for the next step.

You open your terminal and type  
```
npm install -g firebase-tools  
````

Next you have to login into your Firebase Account
```
firebase login
```


After that, a site in your browser will open and you have to sign in into your google account and allow permission for firebase


Then go to you project terminal and type  
```
firebase init  
```  
 and if you get message run press "y" and press enter.


After you have some options, go on hosting and press space and after that press enter



Here you have to have project on your firebase console. if you don't have project go to the https://console.firebase.google.com and login with your google account and create project.  

if you have project, your project id shows in terminal and choose project and press enter.


7.after you choosed your project, you get this message.  

What do you want to use as your public directory?  
type ```build/web" and press enter```  

Configure a single-page app (rewrite all urls to /index.html)? (y/N)  

type  

```
y
```  

Set up automatic builds and deploys with GitHub? (y/N)  

```
n  
```  
we create it manually laterm  


if you any more messages type "n" and press enter


10.after process done. Type  

```firebase deploy --only hosting\  
```


![11](https://user-images.githubusercontent.com/95560640/150305612-ef3c08a2-049b-46f7-9fbb-7b5bbb73a6cf.png)


11.copy this link.


![12](https://user-images.githubusercontent.com/95560640/150305793-93997143-30ae-4fbd-bf9b-53907f1b31aa.png)

till here it's like manuel development and let's make it automatic.


12.downlaod zip file of this project : https://github.com/JohannesMilke/flutter_firebase_hosting


13.copy github file from project and paste it into your project


![15](https://user-images.githubusercontent.com/95560640/150306509-8ebfa3d2-3084-4db6-b4d2-dd75eeb6ecf8.png)


14.open main.yml file in github/workflows folder.


![16](https://user-images.githubusercontent.com/95560640/150306631-1f22a876-08da-4ded-977c-c49c844d413f.png)


15.paste your link that you copied from deploy.


![17](https://user-images.githubusercontent.com/95560640/150306855-ebccf938-481c-4fd5-b300-dff12afd000f.png)


16.remove https:// and .web.app and your link shoud like this


![18](https://user-images.githubusercontent.com/95560640/150307095-705b822f-e9e3-44be-bff2-09428d62fc17.png)


17.after that open your cmd and type "firebase login:ci"


![19](https://user-images.githubusercontent.com/95560640/150307431-8d189f83-058e-46f7-9ef1-a3f6c6c559ec.png)


18.again that open you page and you shoud login to your google account.


19.when you logged in, go to your cmd and it's give to token. copy that token


![21](https://user-images.githubusercontent.com/95560640/150307729-3a1412de-89ba-465b-823c-4174636adda0.png)


20.you to your github repo and go to the setting tab


![22](https://user-images.githubusercontent.com/95560640/150307860-f1a17552-88f4-4582-baac-840e9fa01dcd.png)


21.choose secrets and press new repo secret


![23](https://user-images.githubusercontent.com/95560640/150308021-b5977574-521a-4346-ab99-6617b0e3b052.png)


22.in name type FIREBASE_TOKEN and paste your token in value and press add secret


![24](https://user-images.githubusercontent.com/95560640/150308235-f3e50783-eeb2-4d4c-8f73-5e0173c8133b.png)


done! now after every push github automaticly build web and update link.

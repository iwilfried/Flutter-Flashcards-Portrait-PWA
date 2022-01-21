



[![Codemagic build status](https://api.codemagic.io/apps/61408ce7db3816c8e2627b45/61408ce7db3816c8e2627b44/status_badge.svg)](https://codemagic.io/apps/61408ce7db3816c8e2627b45/61408ce7db3816c8e2627b44/latest_build)



# PWA Tutorial

Link:  
[Website-Preview](https://flutter-flashcard-portrait-pwa.firebaseapp.com/#/)  

[](https://qr.page/g/2iL4anjbVB4)


<img src="https://github.com/iwilfried/Flutter-Flashcards-Portrait-PWA/blob/main/assets/images/qr-code.png" width="150">


  




1. First clone project and open in your IDE.

2. When you open project in your IDE you have so many errors and you should run "dart pub get" in your IDE terminal.

```
$ dart pub get

```  


Your PWA created.


# PWA With Firebase
<div align="center">
<img src="https://github.com/iwilfried/Flutter-Flashcards-Portrait-PWA/blob/main/assets/images/firebaseProjekt.gif" width="450" height="250" />
</div>





1.first you have to installed node.js and after that open your cmd and run npm install -g firebase-tools"" to install firebase tools


![1](https://user-images.githubusercontent.com/95560640/150303073-ad679579-27a8-49bc-99aa-39c458da26e0.png)


2.after that you have to login to your google account for firebase, so run "firebase login"


|![2](https://user-images.githubusercontent.com/95560640/150303225-f56fc773-e0c8-4470-926c-a384b76a550a.png)


3.if you get this message type "y" and press enter


![3](https://user-images.githubusercontent.com/95560640/150303433-8211e614-328d-4e94-b4c7-1ce70d881472.png)

after that, a site in your browser will open and you have to sign in into your google account and allow permission for firebase


4.then go to you project terminal and type "firebase init" and if you get message run press "y" and press enter.


![5](https://user-images.githubusercontent.com/95560640/150303903-26fe259b-978a-4c68-866d-87139c860aee.png)


5.after you have some options, go on hosting and press space and after that press enter


![6](https://user-images.githubusercontent.com/95560640/150304088-ad91747e-db79-412d-827e-ea02e0d9a3dd.png)


6.here you have to have project on your firebase console. if you dont have project go to the https://console.firebase.google.com and login with your google account and create project. if you have project, your project id shows in terminal and choose project and press enter.


7.after you choosed your project, you get this message. type "build/web" and press enter


![8](https://user-images.githubusercontent.com/95560640/150304853-59cc1af1-42ed-4450-9c32-0eacf9950a7d.png)


8.if you get this message type "y" and press enter


![9](https://user-images.githubusercontent.com/95560640/150304984-6467323e-8178-4fcb-8ec8-c894cca07912.png)


9.here show you message for craete automatic firebase. type "n" and press enter. (we create it manuely later)


![10](https://user-images.githubusercontent.com/95560640/150305248-d496cec8-0952-4588-9715-7c171218ff00.png)

if you any more messages type "n" and press enter


10.after process done. run "firebase deploy --only hosting"\


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

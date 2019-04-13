MSP Moscow Upskill. Xamarin
=

Xamarin is a tool for creating an apps for **Android and iOS**. Moreover, it provides ability to create a **cross-platform** mobile application with shared logic. Today we'll try to get deeper into this technology and gain some experience in cross-platform development. 

Objectives
==
In this lab, you will learn, how to:

* Understand the differences between Xamarin Classic and Xamarin.Forms 
* Create simple mobile app throug XAML or code
* Add a mobile backend with SQL database
* Use Visual Studio App Center for crash reports

Prerequisites 
==
The folowing is required to finish this lab:

* [Visual Studio Community] (https://visualstudio.microsoft.com/downloads/?rr=https%3A%2F%2Fwww.google.com%2F) or higher with [Xamarin installed] (https://docs.microsoft.com/en-us/xamarin/get-started/installation/windows)
* At least [Android Emulator](https://docs.microsoft.com/en-us/xamarin/android/get-started/installation/android-emulator/) should be installed
* Active Azure subscription. If you don't have it [see all options here (Rus)] (https://habr.com/ru/company/microsoft/blog/352786/)

Overview
==
* Exercise 1: Create Android app
* Exercise 2: Create Xamarin.Forms app
* Exercise 3: XAML vs Code
* Exercise 4: Making a mobile backend
* Exercise 5: Using Visual Studio App Center

Estimated time to finish this lab: 60 minutes

Disclaimer: All screenshots below are made in Visual Studio 2019 for Mac. However, there're similar in different IDE versions or operating systems. If you have any questions, please **do not** hesitate to shoot me an email: *ilia.ryabukhin@studentpartner.com*

Exercise 1: Create Android app
==
* Open new instance of Visual Studio
![](https://github.com/ilia2108/XamarinLab/blob/master/ex1/1.png)
* Create new Adroid app (follow screenshots below)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex1/2.png)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex1/3.png)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex1/4.png)
* Explore solution

![](https://github.com/ilia2108/XamarinLab/blob/master/5.png)

  Solution consists of several directories: References, Packages, Assets, Properties, Resources and MainActivity.cs

  * **References**: System libraries, usually shouldn't be modified
  * **Packages**: NuGet packages or different SDK's that are used in the app
  * **Assets**: Fast way to upload global assets into application. It could be fonts or general styles
  * **Properties**: General properties of application. Stands for general info (application name, description, version) and special app permissions (camera, GPS, calls etc.)
  * **Resources**: All visible assets of app. Such that design files (axml), resouces (e.g. images)
  * **MainActivity.cs**: Starting point of application. Handles all basic methods of application (like OnCreate)
* Deploy application
![](https://github.com/ilia2108/XamarinLab/blob/master/ex1/6.png)
* Explore the result
![](https://github.com/ilia2108/XamarinLab/blob/master/ex1/7.png)

Exercise 2: Create Xamarin.Forms app
==
* Create a Xamarin.Forms project (follow screenshots below)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex2/1.png)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex2/2.png)
* Explore solution
![](https://github.com/ilia2108/XamarinLab/blob/master/ex2/3.png)
This solution contains several differences from Classic approach:
  1. It has more than one project in solution. It contains project for each OS (there's also UWP project on Windows)
  2. It has extra project that is called from platform-specified projects.
* Set Android app as a Startup project and deploy app. The result sould be the following
![](https://github.com/ilia2108/XamarinLab/blob/master/ex2/4.png)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex2/5.png)
* Optional: set iOS/Win10 app as a Startup project and deploy it. Compare design with Android


Exercise 3: XAML vs Code
==
* Let's get more into XAML. Here's info about [basic XAML controls](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/xaml/xaml-controls). Your goal is to create a page for collecting a survey about this Upskill Seminar. You're free to place controls wherever you want.
* Now let's change some things in the code. All controls can be implemented from code as well. 
  Let's assume you have this code:
  ```<Label Text="Welcome to Xamarin.Forms!" HorizontalOptions="Center" VerticalOptions="CenterAndExpand" />```
  This could be represented in C#:
  ```var label = Label(){ Text="Welcome to Xamarin.Forms!", HorizontalOptions=LayoutOptions.Center, VerticalOptions=LayoutOptions.CenterAndExpand };```
  Try to rewrite your page in C# code. Here's info about [Xamarin controls in C#](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/)

Exercise 4: Making a mobile backend
==
* Open [Azure portal](http://portal.azure.com/)
* Create Azure Mobile App
![](https://github.com/ilia2108/XamarinLab/blob/master/ex4/1.png)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex4/2.png)
* Configure SQL Connection String
![](https://github.com/ilia2108/XamarinLab/blob/master/ex4/3.png)
* Create backend based on either C# or Node.js (I'll proceed with Node.js)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex4/4.png)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex4/5.png)
* Change DB schema to the corresponding to the task (e.g. change several fields)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex4/6.png)
![](https://github.com/ilia2108/XamarinLab/blob/master/ex4/7.png)
* Make an insertion request from the client

Exercise 5: Using Visual Studio App Center
==
* Open [Visual Studio App Center](https://appcenter.ms/) and create new app
![](https://github.com/ilia2108/XamarinLab/blob/master/ex5/1.png)
* Follow the instructions similar to the screenshot:
![](https://github.com/ilia2108/XamarinLab/blob/master/ex5/2.png)

Summary 
==
This lab is about basic conpepts of Xamarin and life cycle near it. I would like tp hear your feedback and error reports via email: *ilia.ryabukhin@studenpartner.com*


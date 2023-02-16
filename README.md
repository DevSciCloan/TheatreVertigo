# TheatreVertigo
---

**Introduction**
----------------

>For this project I was tasked with constructing the Cast Member pages for Theatre Vertigo's website. We used ASP.NET Framework with a MVC structure.  
I used Razor with C#, HTML, and minimal JS on the Views. The Controllers were written in C# and so were the Models.  
Below I will share some specific details with you.

***

**Restricted Pages**
--------------------  
>Some pages are restricted to the Cast Director role using Identity.

[![Restricted Pages](https://raw.githubusercontent.com/DevSciCloan/TheatreVertigo/main/images/restrictedToRole.PNG "Code Snippet")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/restrictedToRole.PNG)
[![Restricted Pages](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/AccessDenied.gif?raw=true "GIF")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/AccessDenied.gif)  

**Easy Login Button**
---------------------
>I made a button that will log the user in as the Cast Director for testing purposes. The button will only display on relevant pages and if  
the user isn't currently logged in.  

[![Login Button](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/displayButtonSpecificPages.PNG?raw=true "Code Snippet")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/displayButtonSpecificPages.PNG)
[![Login Button](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/LoginCastDirectorButton.gif?raw=true "GIF")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/LoginCastDirectorButton.gif)  
>When the button is clicked the SignInManager will sign the user in by passing the Cast Directors credentials and return to the current page if successful. 

[![Login Button Controller](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/controllerCastDirectorLoginButton.PNG?raw=true "Code Snippet")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/controllerCastDirectorLoginButton.PNG)  

**Edit and Create Photo Preview**
---------------------------------
>While creating a new user, or editing an existing one, the user is able to upload a photo. The photo is previewed inline with the file input. Each photo is stored in the database as a byte array.  

>This is the method in a Controller that will convert the uploaded file to a byte array before saving it to the database.
[![Convert image to byte array](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/convertImageToByteArray.PNG?raw=true "Code Snippet")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/convertImageToByteArray.PNG)  

>This is some JavaScript to handle displaying a preview of the image  
[![Convert image to byte array](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/fileUploadPreview.PNG?raw=true "Code Snippet")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/fileUploadPreview.PNG)  

[![Preview Image](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/Edit.gif?raw=true "GIF")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/Edit.gif)  

**Details Modal**
-----------------

>When the user clicks on a Cast Members name a modal is displayed with all of the Cast Member's details.  

[![Details Modal](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/DetailsModal.gif?raw=true "GIF")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/DetailsModal.gif)  
>Here are some code snippets to show you a bit more how it works.  
>>*The key point here is that each Cast Member uses the same modal instead of creating a new modal for each of them.*  

[![Details Modal](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/convertToJSON.PNG?raw=true "Code Snippet")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/convertToJSON.PNG)  
>Here is how I used jQuery on the JSON object that was passed to the data-whatever attribute when the Cast Member's name is clicked.
[![Details Modal Update](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/jQueryModalUpdate.PNG?raw=true "Code Snippet")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/jQueryModalUpdate.PNG)  

**Filter Cast Members**
-----------------------
>I added a search feature that allows the user to find Cast Members by name or by searching text that matches a Cast Members bio section.  

[![Search](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/SearchFilter.gif?raw=true "GIF")](https://github.com/DevSciCloan/TheatreVertigo/blob/main/images/SearchFilter.gif)  
 
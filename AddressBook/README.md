 Address Book web app powered by Spring MVC and H2 database
[An example Spring Web MVC app that can store/retreive/edit address book entries (CRUD functionality)]
 
## Functionalities -
Add Entries , Search for Entries , Edit Entries ,Delete Entries 

 
## Uses -
* Spring MVC
* Spring Annotations, Java Configuration
* JSP, Bootstrap
* Maven (version 3.5) Build Tool
* Tomcat (version 8.5)
* H2 (version 1.4.195) database to store Address Book Entries

I guess, newer versions of tools can be used as well, but just for stable experience I would stick with versions I used.

## Pre requisites
* Download and install latest [Java SE](http://www.oracle.com/technetwork/java/javase/downloads/index.html) (if you haven't done so already)
* Download and install [Maven](https://maven.apache.org/download.cgi) build Tool
* Download and unzip [Tomcat](https://tomcat.apache.org/) application Server
* Download and install/unzip [STS](https://spring.io/tools/sts/all)(it's a flavour of Eclipse IDE)
* Download and unzip [H2](http://www.h2database.com/html/main.html) database.

### Import the project to STS
 
### Add Tomcat Server to STS

### Create database
Let's create **address_book** database and **ENTRIES** table in it. Without this application won't work.
* Navigate to downloaded and unzipped h2 folder **/h2/bin/** and run **h2-1.4.195.jar** or it may have different numbers in name due to a different version
* A database console login page should open up in the browser. Fill it with details as follows:
![021 database console](https://user-images.githubusercontent.com/11411618/27842266-50d63572-6100-11e7-96be-8f844be84bc2.JPG)
* Press **Connect**
* A H2 Console should open up:
![022 console open](https://user-images.githubusercontent.com/11411618/27842689-1f52b134-6104-11e7-83ce-5a9bf6f434c4.jpg)
* Enter following query and press **Run**:
```
CREATE TABLE ENTRIES (
ID INT PRIMARY KEY AUTO_INCREMENT,
NAME VARCHAR(255),
SURNAME VARCHAR(255),
ADDRESS VARCHAR(255),
PHONE_NUMBER VARCHAR(255),
EMAIL VARCHAR(255),
ZIP VARCHAR(255)
);
```
* It should table named "ENTRIES" (look at top left):
![024 console with table](https://user-images.githubusercontent.com/11411618/27842691-1f552072-6104-11e7-8380-0e7bba543f32.jpg)
* Now press red button in very top-left of H2 Console to disconnect from database. **IT IS IMPORTANT TO DO THIS!** Otherwise Application won't work, I guess because it uses same connection(login details) as we used to enter H2 Console.
### Running Application
* click on Tomcat server in Servers tab
* click button with play icon in Servers tab
* server will start (takes about 15 seconds)
* cross the fingers, hope everythings works fine
* once Server startup finished the console will display something like *INFO: Server startup in 12508 ms*
* go to application URL: **http://localhost:8080/AddressBook_SpringMVC_H2DB/home.html**
* use the app
 
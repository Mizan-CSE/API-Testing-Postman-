
# Postman

Postman is **an interactive and automatic tool for verifying the APIs of your project**. 

Postman is a Google Chrome app for interacting with HTTP APIs. It presents you with a friendly GUI for constructing requests and reading responses. It works on the backend and makes sure that each API is working as intended.

###
In this repository, I have tried to keep all the related documents of API testing with Postman that I have practiced. Now I will try to explain all one by one.

First I want to answer two common questions which may arise in your mind.


#### 1. What is API?
#### 3. Why do we need to test API?

## API
API is the acronym for **Application Programming Interface**, which is a software intermediary that allows two applications to talk to each other. Each time you use an app like Facebook, send an instant message or check the weather on your phone, you're using an API.

There are four principal types of API commonly used in web-based applications: **public, partner, private and composite**.


##  The purpose of API Test
The purpose of API Testing is **to check the functionality, reliability, performance, and security of the programming interfaces**. 

In API Testing, instead of using standard user inputs(keyboard) and outputs, you use software to send calls to the API, get output, and note down the system's response.

# Working Procedures
To test API, you need to install Postman on your machine. Simply browse the website and [download](https://www.postman.com/downloads/) it. Then you have to create an account to use Postman. It is a cloud-based platform, so you can work on it without installing it on your machine.

#### Now the environment is ready.
First You have to create a **workspace**. It's like a project name. And then you have to create a **collection** in it. It's like a container. It contains **requests**.

There are so many requests. Generally, we work with **four** requests.


| Request | Description                       |
| :-------- | :-------------------------------- |
| `GET`       | A way for you to grab data from a data source with the help of the internet. |
| `POST`       | Used to send data to the API server to create or update a resource.|
| `PUT`       | Used to create a resource, or overwrite it.|
| `DELETE`       | Used to delete a resource from the server.|

You can learn more details from their [Learning Center](https://learning.postman.com/docs/getting-started/introduction/).

## Collections
 For my learning purposes, I played with so many things-
### 1. DemoAPI
Initially, I made the collection and tried to learn how to use **GET** and **POST** requests.

### 2. EmployeeAPI
In this collection, I used **GET**, **POST**, **PUT** and **DELETE** requests to learn-

- How to get a response from API
- How to insert a record to API
- How to update a record of API
- How to delete record from API


### 3. Authorizations
You know, sometimes we need to permit to browse a site. In this collection I used
- How to authorize with ```Basic Auth```
- How to authorize with ```API Key Auth```
- How to authorize with ```Bearer Token Auth```

### 4. API_Chaining
Sometimes we need to pass data from another ```response body```. By this collection, I learned-
- How to capture data from another response

### 5. Data_Driven
Sometimes you need to work with a lot of records. If I give you a **CSV** or **JSON** file with hundreds of records and tell you to insert the records to an API. You won't insert the records one by one right. Because It's a lengthy and iterative process. With one script you can insert multiple requests easily.

Record file:
``` data.json```, 
``` data.csv```

Click on **Runner** option of **Postman** to run the whole collection, where you can set the file.

### 5. Own_API
Actually, there are a few API, where you can work. Sometimes the APIs are too busy. We can not work properly. That's why we need to know how to create an API, how to work in it.

Own API file: ```info.json```

I created a file in **JSON** format and put it in the user section path like ```C:\Users\HP```. To access the API, you need to connect with **JSON Server**. So, open the command prompt then write ``` json-server info.json```. After a few seconds you will get a local API. Use the ```url``` in postman. Make sure the server is running. Without running the server, you can not work with the local API.

### 6. Order_of_Execution
After a while, you may ask- **"What is the execution order of collection, folder, and request?"** Let me clear it. To test it, you need to create a **collection** then create a **folder** under the collection and then create a **request** on it.
After all, write ```Pre-request Script``` and ```Test``` of collection, folder, request like-

```console.log("This is Folder level Pre-request Script.");```

```console.log("This is Request level Pre-request Script.");```

```console.log("This is Request level Test Script.");```

Then run the collection and open the console panel to see the order of execution.

### 7. Postman_Scripting
You are testing API right. You need to test everything like ```Status code```, ```Header```, ```Content-Type``` and so many things. From this file, you would be able to learn how to test each thing. 


## Newman

Suppose a developer gives you a few API to test. After testing you have to give feedback with proper documents right. **Newman** helps us to generate documents of API testing.
For this, we need to install **Node.js** software.

Then open the command prompt and check ```Node.js``` install or not.

For checking, write command ```node -v``` and then ```npm -v``` which refer to **Node Package Manager**.

Then install **Newman** using ```npm install -g newman``` command.
You can generate a report of a collection in command by using ```json file```, ```json link``` from the postman shareable file.

To generate report in **command prompt**. Simply write the command in command prompt.
```newman run <exported file name.json>``` or
```newman run <shareable link>```

Another way, to generate **HTML** report you need to write an extra command like-

```newman  run <exported file name.json -r html>``` or
```newman run <shareable link -r html>```

For **colorful html report** you need to ```globally``` install the ```htmlextra``` package:

```npm install -g newman-reporter-htmlextra```
then write the bellow command

```newman run <exported file name.json -r htmlextra>```or

```newman run <shareable link -r htmlextra>```

## My Workspace
You can import the **"My Workspace"** file as your workspace. All collections are in here.
Or you can import collections one by one under your workspace from **Collections**.


# Thank you

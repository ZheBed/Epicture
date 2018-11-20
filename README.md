# Epicture 

## Install

```sh
$ npm install
$ npm start
```
 Then you have to launch expo your Smartphone

## Project

Epicture is a mobile application that allows you to perform some task similar to Imgur.
The two main part of the projet are :
- Core of the application in React-Native
- Imgur api in Javascript

### Application

The React-native part is composed of componnent in the Componnent directory.
These componnent are used in the Route. This facilitate the integration of routes

```
Project
│   
└───Route
│   └───App
│       │   Mains.js
│       │   Flux.js
│       │   ...
│   └───Auth
│       │   Auth.js
│       │   ...
└───Componnent
    │   ImageUploader.js
    │   ...
```

### Api

The Api is constructed as a JS Class.
It contains all the POST/DELETE/PUT/GET request for all the Imgur that we require
Each method of the class begin by the type of the request.
Each request return a Promise as an asyncronous callback, which contains the data of the response and if the request was successful.
There is a description of the params, return value and the task of each method in the Api file located at `src/Api.js`

A Jasmine Test Framework is implemented to the test all the Api Callback.
There are located at `src/spec/Apispec.js`
To run them do :

```sh
$ cd src
$ npm install
$ npm jasmine
```

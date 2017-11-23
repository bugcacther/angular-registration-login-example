angular-registration-login-example
==============================

AngularJS User Registration and Login Example

To see a demo and further details go to http://jasonwatmore.com/post/2015/03/10/AngularJS-User-Registration-and-Login-Example.aspx

Running the Protractor test:
Pre-requites:
  1. The Java Development Kit (JDK) should be installed
  2. NodeJS should be installed
  3. A local web server like http-server of NodeJS should be available, up and running
  4. Protractor should be installed, if not you can get it by running "npm install -g protractor" in the command line. This will install two command line tools, protractor and webdriver-manager. Try running protractor --version to make sure it's working. The webdriver-manager is a helper tool to easily get an instance of a Selenium Server running. Use it to download the necessary binaries with:

webdriver-manager update

Now start up a server with:

webdriver-manager start

This will start up a Selenium Server and will output a bunch of info logs. The Protractor test will send requests to this server to control a local browser. You can see information about the status of the server at http://localhost:4444/wd/hub.

To run the project on your local machine first download the code from GitHub at https://github.com/bugcacther/angular-registration-login-example.

Once you've downloaded the code you need to use a local web server to serve the files to your browser, opening the index.html directly from the file system will not work. One of the easiest ways to setup a local web server is to use NodeJS.
Open a command prompt in windows and change directory to the extracted folder of the application, where index.html is located. Run http-server. The screen should look something like below:
Starting up http-server, serving ./
Available on:
  http://192.168.1.100:8080
  http://127.0.0.1:8080
Hit CTRL-C to stop the server

Open browser and enter localhost:8080 to open the login page of the application. Open a command line and goto the application installation/tests folder. Execute below command to run the protractor test.

protractor conf.js

Upon running the test you would see the chrome browser opening and running the test for user registration, login & logout automatically. The browser would also close automatically. Upon completion of test you may see something like below in the terminal:

(node:10804) [DEP0022] DeprecationWarning: os.tmpDir() is deprecated. Use os.tmp
dir() instead.
[00:41:16] I/launcher - Running 1 instances of WebDriver
[00:41:16] I/hosted - Using the selenium server at http://localhost:4444/wd/hub
Started
..


2 specs, 0 failures
Finished in 8.883 seconds

[00:41:28] I/launcher - 0 instance(s) of WebDriver still running
[00:41:28] I/launcher - chrome #01 passed

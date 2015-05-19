# protractorsetup

To set up protractor you need the following software installed on your PC.

    1) Node.js(need this for NPM)
    2) Python(Please select version 2.7 as higher version give error)
    3) JDK 
    
  Ensure Set up of the following environment variables -

    JAVA_HOME
    NODE_PATH (Set to npm/node_modules folder, eg. C:\FAST\nodejs\0.12.0\node_modules\npm)
    PYTHON (eg. C:\FAST\Python\2.7)
    
    Install Protractor and webdriver-manager

Run the following command: npm install -g protractor

This will install two command line tools, protractor and webdriver-manager. 
Try running protractor --version to make sure it's working.

The webdriver-manager is a helper tool to easily get an instance of a Selenium Server running. 
Use it to download the necessary binaries with: webdriver-manager update

webdriver-manager takes a proxy as an argument, so the command will be:

webdriver-manager update 
    
    
    Add and run Tests

Now create a maven the project

Main files to be present areare -

    Configuration File - conf.js
    Test File - Anything under specs folder. Need to be added to conf.js to run it.

Start up selenium server - webdriver-manager start

Install jasmine reporters with this command

npm install jasmine-reporters@^1.0.0

Run it via maven using mvn.

Test output goes to folder test-output under src/test.

Alternate ways to run tests -

Configure your test runner to use phantomjs

Use directConnect - In the conf.js make the property true. directConnect works only in Firefox/Chrome.

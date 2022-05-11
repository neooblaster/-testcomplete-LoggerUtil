# TestComplete - LoggerUtil

> A log output interface to let scripts working with TestComplete & NodeJS at the same time.

* **Version** : ``v0.1.1``
* **Dependencies** :
    * none
  
  
## Summary

[](BeginSummary)
* [Summary](#summary)
* [FileSystemUtil Setup for TestComplete](#filesystemutil%20setup%20for%20testcomplete)
* [Get Started](#get%20started)
* [Log a message `message()`](#log%20a%20message%20%60message()%60)
* [Log a warning `warning()`](#log%20a%20warning%20%60warning()%60)
* [Log an error `error()`](#log%20an%20error%20%60error()%60)
[](EndSummary)



## FileSystemUtil Setup for TestComplete

As this library is published on **npmjs**,
you can easily get library with the following command
if you have **nodejs** installed on your computer.

````bash
npm install @testcomplete/loggerutil
````

Please confer to this documentation to add script in TestComplete :

Script List for the setup :

* ``./node_modules/@testcomplete/loggerutil/LoggerUtil.js``

[TestComplete Library Setup](https://gitlab.viseo.com/testcomplete/documentations/testcompletelibrarysetup)



## Get Started

First of all, you have to add the script ``LoggerUtil.js`` to your
script library in **TestComplete**.

In any script (TestComplete of NodeJs), require library like this

````javascript
// Check for NodeJS. If NodeJS, require need relative path
let sPrePath = typeof process !== 'undefined' ? './' : '';

let logger = require(`${sPrePath}LoggerUtil`);
````
    
    
    
## Log a message `message()`

The method ``message( ...[] )`` log an info message text.

````javascript
// Log a message in registry (or stdout)
logger().message('My message text');
````



## Log a warning `warning()`

The method ``warning( ...[] )`` log the provided message with the warning state.

````javascript
// Log a warning in registry (or stdout)
logger().warning('My message text');
````



## Log an error `error()`

The method ``error( ...[] )`` log the provided message with the error state.

````javascript
// Log an error in registry (or stdout)
logger().error('My message text');
````

# TestComplete - LoggerUtil

> A log output interface to let scripts working with TestComplete & NodeJS at the same time.

* **Version** : ``v0.1.0``
* **Dependencies** :
    * none
  
  
## Summary

[](BeginSummary)
[](EndSummary)



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

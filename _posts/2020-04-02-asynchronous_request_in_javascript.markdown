---
layout: post
title:      "Asynchronous Request in JavaScript"
date:       2020-04-03 01:05:23 +0000
permalink:  asynchronous_request_in_javascript
---


JavaScript language is a single-threaded language, which means it can only complete one task at a time. All codes are executed step by step, one after another. However, this does not stop JavaScript from completing an asynchronous request. While the browser is waiting for a response from a different source, another operation can be performed.
So, how do we create an asynchronous request and send an HTTP request? 
There is a very useful function built in modern JavaScript called ‘fetch()’. We can pass a ‘url’ in this fetch method and that will send a GET request. Fetch method uses a promise. We can chain ‘.then’ to it and get a response back in a json method. When we call on the ‘response’ object, JSON will parse the body of the response and converts it into a JavaScript object.

return fetch(url).then(response => {
return response.json();
});

In case we need to create a POST, PUT, PATCH or DELETE requests, we need to add a second argument which should be an object. For the key of the object we use ‘method’ and we set it to ‘POST’ or other HTTP request, and for the body we set it for data converted to JSON.

return fetch(url, {
method: ‘POST’,
body: JSON.stringify(data)
}).then (response => {
return response.json();
});


If we have technical or network connectivity issues, we might not get the response back from the promise. We can add a ‘catch’ promise chain to catch any errors.  For example:

return fetch(url, {
method: ‘POST’,
body: JSON.stringify(data)
}).then (response => {
return response.json();
}).catch(error => {
Console.log(error);
});

The fascinating thing about asynchronous request is that even though JavaScript is single threaded, it will still execute other functions and eventually processes the API request once it’s available. It does not stop the flow of code execution. This gives the user a much better experience with the browser since other things can display and function while the asynchronous request is pending completion. 


Welcome to the FETCH-API wiki!

fetch api

sandox fetxh api sandbox

ashchronous 

https://jsonplaceholder.typicode.com



all kinds of request:

get text

get json all the user

get api data


post request using fetch

ES6:
arrow function
template string

xthml + http -> XHR:

fetch api

app.js:

->fetch(url,options);

->fetch(url).then(function(response){
 console.log('status',response.status);
 });

->what  kind of data 
->json 
->respone.json()->promises()

app.js:

fetch(url).then(function(response){
 console.log('status',response.status);

 response.json().then(function(data){
 console.log('FETCH Result:',data);
}).catch(function(err){
 console.log('FETCH Parsing Error',err);
    });
  });

 

status code:
 
->inline function()

function checkStatus(response){
if(response.status == 200){
return Promise.resolve(response);
}else{
return Promise.reject(
 new Error(response.statusText));
 }
}

function getJSON(response){
return response.json();
}

app.js:

fetch(url)
 .then(checkStatus)
 .then(getJSON)
 .then(function(data){
 console.log('DATA',data);
})
 .catch(function(err){
 console.log('ERROR',err);
});


Fetch options:
->method
->HTTP header
->body
->credentials
->cors->cross domain

OAUTH token:
->post then results of some user input along with OAUTH

var options = {
"method" : "post",
"headers": {
  "Authorization " : "Bearer XXXX"},
"body" : "Hello body!"
};

->cross domain.

fetch mode options:
->same origins
->cors
->cors-with-forced-preflight
->no-cors






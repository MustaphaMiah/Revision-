


# Introduction to the JSON APIs and AJAX Challenges
Similar to how User Interfaces help people use programs, Application Programming Interfaces (APIs) help programs interact with other programs. APIs are tools that computers use to communicate with one another, in part to send and receive data. You can use API functionality in your page once you understand how to make requests and process data from it. Programmers often use AJAX technologies when working with APIs.

The term AJAX originated as an acronym for Asynchronous JavaScript And XML. It refers to a group of technologies that make asynchronous requests to a server to transfer data, then load any returned data into the page. An asynchronous process has a couple key properties. The browser does not stop loading a page to wait for the server's response. Also, the browser inserts updated data into part of the page without having to refresh the entire page.

User experience benefits from asynchronous processes in several ways. Pages load faster since the browser isn't waiting for the server to respond in the middle of a page render. Requests and transfers happen in the background, without interrupting what the user is doing. When the browser receives new data, only the necessary area of the page refreshes. These qualities especially enhance the user experience for single page applications.

The data transferred between the browser and server is often in a format called JavaScript Object Notation (JSON). JSON resembles JavaScript object literal syntax, except that it's transferred as a string. Once received, it can be converted into an object and used in a script.

### Handle Click Events with JavaScript using the onclick property
You want your code to execute only once your page has finished loading. For that purpose, you can attach a JavaScript event to the document called DOMContentLoaded. Here's the code that does this:
```
document.addEventListener('DOMContentLoaded', function() {

});
```
You can implement event handlers that go inside of the DOMContentLoaded function. You can implement an onclick event handler which triggers when the user clicks on the element with id getMessage, by adding the following code:
```
document.getElementById('getMessage').onclick = function(){};
```
### Change Text with click Events
When the click event happens, you can use JavaScript to update an HTML element.

For example, when a user clicks the "Get Message" button, it changes the text of the element with the class message to say "Here is the message".

This works by adding the following code within the click event:

document.getElementsByClassName('message')[0].textContent="Here is the message";

### Get JSON with the JavaScript XMLHttpRequest Method
You can also request data from an external source. This is where APIs come into play.

Remember that APIs - or Application Programming Interfaces - are tools that computers use to communicate with one another. You'll learn how to update HTML with the data we get from APIs using a technology called AJAX.

Most web APIs transfer data in a format called JSON. JSON stands for JavaScript Object Notation.

JSON syntax looks very similar to JavaScript object literal notation. JSON has object properties and their current values, sandwiched between a { and a }.

These properties and their values are often referred to as "key-value pairs".

However, JSON transmitted by APIs are sent as bytes, and your application receives it as a string. These can be converted into JavaScript objects, but they are not JavaScript objects by default. The JSON.parse method parses the string and constructs the JavaScript object described by it.

You can request the JSON from freeCodeCamp's Cat Photo API. Here's the code you can put in your click event to do this:
```
const req = new XMLHttpRequest();
req.open("GET",'/json/cats.json',true);
req.send();
req.onload = function(){
  const json = JSON.parse(req.responseText);
  document.getElementsByClassName('message')[0].innerHTML = JSON.stringify(json);
};
```
Here's a review of what each piece is doing. The JavaScript XMLHttpRequest object has a number of properties and methods that are used to transfer data. First, an instance of the XMLHttpRequest object is created and saved in the req variable. Next, the open method initializes a request - this example is requesting data from an API, therefore is a "GET" request. The second argument for open is the URL of the API you are requesting data from. The third argument is a Boolean value where true makes it an asynchronous request. The send method sends the request. Finally, the onload event handler parses the returned data and applies the JSON.stringify method to convert the JavaScript object into a string. This string is then inserted as the message text.

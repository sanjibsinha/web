We can see an example of JavaScript and HTML interaction. A JavaScript code makes a web page interactive. Let’s see how it works.

Without interactivity a web page looks stale.

However, before digging deep into this serious matter we must lighten the atmosphere so Let’s Smile with Code.

They say that during sex you burn off as many calories as running eight miles. Who the hell runs eight miles in 30 seconds?

One example of how JavaScript can make a web page interactive is by adding event listeners to elements on the page. 

An event listener is a function that listens for a specific event. 

It might be a button click, and based on that click it performs an action when that event occurs.

For example, consider a simple HTML button:

<button id="myButton">Click me!</button>
We can use JavaScript to add an event listener to the button that will execute a function when the button is clicked:

let button = document.getElementById("myButton");
button.addEventListener("click", function() {
    alert("Button was clicked!");
});
What happens after that?

Now, when the user clicks on the button, the browser will execute the function specified by the event listener.

As a result there appears an alert box that says “Button was clicked!”.

If you are a programming beginner you may take an interest in the following posts.
Steps in program development
Learn Programming Techniques
The levels of programming languages
What is high level language?
What is language portability?
Programming languages translators
Learn structured programming
Machine language to Assembly language
We can see another example.

Let’s suppose we want to change the content of a web page when a button is clicked.

It is possible to change the content of a specific HTML element by manipulating its inner HTML property:

<div id="content">This is some initial content</div>
<button id="changeContentButton">Change Content</button>

let button = document.getElementById("changeContentButton");
let content = document.getElementById("content");
button.addEventListener("click", function() {
    content.innerHTML = "Content has been changed!";
});
Now, when the user clicks on the “changeContentButton”, the text inside the “content” div will change to “Content has been changed!”.

These are just a couple of examples of how we can use JavaScript to make web pages interactive.

As it allows users to interact with the page and update it dynamically.

How can we place a JavaScript code inside HTMl?
There are a few ways to place JavaScript code inside an HTML document:

We can use the script tag.

It’s the most common way to include JavaScript in an HTML document.

We can use the <script> tag. 

As an outcome this tag embeds JavaScript code directly into an HTML document. 

Now we can place the JavaScript code either in the <head> section of the HTML document or in the <body> section.

For example we can see the following specimen.

<script>
    function sayHello() {
        alert("Hello, World!");
    }
</script>
On the other hand, we have another alternative. We can use the “src” attribute which actually means the source code. 

It indicates that we have kept the source code somewhere else and used it instead keeping it directly on the web page.

We can also use an external JavaScript file using the src attribute. 

This is useful when you have a lot of JavaScript code or if you want to reuse the same code across multiple pages.

<script src="script.js"></script>
Another example we can consider. It is the “onclick” attribute.

We can include JavaScript code in an HTML document by using the “onclick” attribute of an HTML element. 

This attribute also specifies a JavaScript function and when we click the button, it executes.

<button onclick="sayHello()">Click me</button>
Where to place the JavaScript code?
If we place the JavaScript code in the head section of the HTML file, it executes even before the web page loads.

Because the browser reads it first and loads it before it renders the HTML file.

Therefore, to avoid that it’s common to include the JavaScript code at the end of the body section.

As a result it’s executed after the page has fully loaded.

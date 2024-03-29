### How servers connect to the Internet?
Clients use a URL to connect to a server across the Internet. The URL has four main components:

A connection scheme, usually HTTPS (“Hypertext Transfer Protocol Secure”), browsers and web servers use to talk with one another.
A subdomain that specifies the particular server (usually organized by resource type) to be delivered to the client.
A domain name that specifies the name of the organization(s) associated with the URL.
A top-level domain that specifies the type of organization associated with the URL.
For the URL https://www.codecademy.com, “https” is the scheme, “www” is the subdomain, “codecademy” is the domain name, and “com” is the top-level domain. In further detail, the following happens:


## INTRODUCTION TO NODE.JS
### Introduction
For a long time, the browser was the only place JavaScript code could be executed. Web developers had to use a different programming language on the front-end than the back-end. It also meant that, even as JavaScript evolved into a more robust and powerful language, it remained a front-end only language.

Though multiple attempts to create off-browser JavaScript environments have been attempted, Node.js, invented by Ryan Dahl in 2009, found unprecedented popularity and is currently being used by numerous top-tier companies including Netflix, Uber, Paypal, and eBay. Node.js is a JavaScript runtime, or an environment that allows us to execute JavaScript code outside of the browser. A “runtime” converts code written in a high-level, human-readable, programming language and compiles it down to code the computer can execute.

Though Node was created with the goal of building web servers and web applications in JavaScript, it can also be used for creating command-line applications or desktop applications. In this lesson, we’ll explore some features of Node so you start to feel comfortable with running JavaScript in the Node environment and gain some familiarity with features unique to Node. For more advanced development, Node can be combined with any number of robust frameworks like the Express.js framework for creating effective web application back-ends.

There’s more to learn about Node than we could ever fit in one lesson. We’ll try to point to great resources like MDN and the Node.js documentation. Take your time exploring and use the documentation.

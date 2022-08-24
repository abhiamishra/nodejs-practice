# What is Node
- Node is Javascript runtime
    - Javascript was designed to run in browser
    - Allows developers to use JS to accomplish more
    - Allows you to run JS code on a machine w/o going through a web browser

# Event Driven
- Node is an *asynchronous event driven* JS runtime
    - asynchronous = when you write code, you do not try to predict the exact sequence in which every line will run.
        - You write code as a collection of smaller functions that get called in response to specific events such as network request (event driven).
    - allow you to run multiple functions/actions @ same time 
    - while both processes are running, Node sits and waits on an event
        - When event is complete, Node fires off an event that will run the next process we've defined.
    - as programmer, we don't care about the order

# Callbacks
- Callbacks are functions that are passed into another function as an argument
- Anatomy of a function
    - Normal functions:
        - ``` function funkyFunction(music, isWhiteBoy) {
                if (isWhiteBoy) {
                    console.log('Play: ' +  music);
                }
            } ```
        - called like this: ``` funkyFunction('that funky music', true); ```
    - Anonymous Functions
        - not named
        - can be assigned to a variable
        - however, it can be called the exact same away.
        - ``` const funkyFunction = function(music, isWhiteBoy) {
                if (isWhiteBoy) {
                    console.log('Play: ' +  music);
                }
            }

            // This is called an arrow function, we'll get into these soon.
            const funkyFunction = (music, isWhiteBoy) => {
                if (isWhiteBoy) {
                    console.log('Play: ' +  music);
                }
            }```
        - called like this: ``` funkyFunction('that funky music', true); ```
    - Arrow Functions
        - Shorter way to write a function
        - If only one argumen, parenthesis can be omitted
        - if arrow functions are one line, bracks can be omitted
            - returns evaluted expression without requiring the "return" keyword
    - Callback Functions
        - Functions passed into other functions as arguments
        - callback() -> allows you to call the callback function

# Event Listeners (DOM)
- ``` const element = document.querySelector("#myId");
element.addEventListener('click', (event) => {
  console.log(event.target.value);
  event is passed into the callback from the addEventListener function when it receives a 'click' event.
}); ```
- callbacks are just functions calling another functions as arugments

# Introduction to the Server Side
- Websites use server-side code to display different data 
- allows you to tailor website content for individual users
- web browswers communicate with web servers using HTTP
    - when you do anything on a web page, an HTTP request is sent from your browser to the target server
- Web servers wait for client request messages, process as they arrive, and reply to the web browswer with an HTTP response message
    - response message contains resource that was 
- Static sites have simple client-and-server architecture where HTTP requests and responses are exchanged.
- Dynamic sites is where the response content is generated dynamically only when it is needed
    - on a dynamic website, pages are created by inserting data from a database into placeholders in HTML TEMPLATES
    - sites can return different data for a URL based on information provided by the user or stored preferences 
- devs write code usigng web frameworks - collections of funcitons, objects, rules, and other constructs to solve problems
- server-side allows us to efficiently deliver info tailored for individual users and thereby creating a much better use exp
- Benefits of server-side programming
    - effcient storage and delivery of info
    - customized user exp
    - controlled access to content
    - store session/state info
    - notifications and communication
    - data analysis

# Client - Server Overview
- Web servers and HTTP 
    - request has: URL, method that defines required action, additional info 
    - wait for client request messages, process them when they arrive, and reply to the web browser with an HTTP response message
- dynamic sites generate and turn content based on specific request URL and data
- data is stored in database and when a GET response is received, server fetches data from database and then constructs a html page for response by inserting data into the template
- idea of returning data to a web browser so that it cna dynamically update its own content is very popular


    
***Q1: Difference Between getElementById, getElementsByClassName, and querySelector / querySelectorAll,

1.getElementById("id")

  i. Selects one element,
  ii. Uses an id,
  iii. Returns a single element,
  iv. Very fast,
  
example:
      document.getElementById("myId");

2.getElementsByClassName("class")

  i. Selects elements by class name,
  ii. Returns multiple elements,
  iii. Returns a live HTMLCollection,

example:
      document.getElementsByClassName("myClass");
      
3.querySelector("selector")

  i. Selects the first matching element,
  ii. Uses CSS selectors,
  iii. Very flexible,

example:
      document.querySelector(".myClass");
      document.querySelector("#myId");
      
4.querySelectorAll("selector")

  i. Selects all matching elements
  ii. Returns a NodeList
  iii. Static list (not live)

example:
      document.querySelectorAll("p");


<br>
<hr>
<br>


***Q2:How to Create and Insert a New Element into the DOM
The 3 Simple Steps are:
  i. Create,
  ii. Add content,
  iii. Attach to page,

  1. Create element: 
  let newDiv = document.createElement("div");

  2. Add content: 
  newDiv.textContent = "Hello World";

  3. Insert into page: 
  document.body.appendChild(newDiv);


<br>
<hr>
<br>

***Q3:What is Event Bubbling?

Event bubbling means:

When an event happens on a child element, it moves up to its parent elements.

Example:
If you click a button inside a div:
  i. Button runs,
  ii. Div runs,
  iii. Body runs,
<br>
<hr>
<br>

***Q4:What is Event Delegation?

Event delegation means:
Instead of adding event listeners to many child elements, you add one event listener to the parent.

Example:
    document.querySelector("ul").addEventListener("click", function(event) {
      console.log(event.target);
    });


<br>
<hr>
<br>


***Q5:Difference Between preventDefault() and stopPropagation()
<br>
1.preventDefault()
  i. Stops the browser’s default behavior,
  ii. Example: Stop form submission,
          event.preventDefault();
          
  <br>
  
2.stopPropagation()
  i. Stops event bubbling
  ii. Parent elements will not receive the event
  iii. example:  
          event.stopPropagation();

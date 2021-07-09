# Foo-Fighters-Web-Page

Mock website for the band Foo Fighters with a functioning shopping cart; HTML, CSS, JavaScript

[Video Demo (click here)](https://www.youtube.com/watch?v=0HfuE604wps&t=1s)

Learnt web development by designing a mock website for the band Foo Fighters with 3 pages, and includes a working cart where items can be added and removed. 

There is a header where the user can navigate the website. 

There is a home page with tour dates and buttons (which do not do anything right now), an about page which contains an image and text, and a shop page which contains items (with titles, prices, and images) which can be added to a cart. The cart has a field for the quantity and a button to remove. There is a purchase button which creates a pop-up message thanking the user for their purchase and deleting all the items in the cart. There is also a total price displayed at the bottom of the cart. 

In the footer there are links to Foo Fighter's Facebook, Spotify, and Youtube pages. 

The website also adjusts neatly according to the window size. 

## Installation

For now, you must pull the code onto your computer and click on any html file to give it a go yourself. 

## Implementation

### HTML, CSS, JavaScript

The HTML is used to construct the elements of the page and how they are put together. The CSS seperates the styling from this basic structure, by specifying the styling under different class names. The HTML elements are given these class names, which allows the correct matching for styling via the CSS file. Class names also allow for referencing in JavaScript, so that the correct element can be easily fetched. The JavaScript is used for the shopping cart on the store page. 

### Cart

When an item is added to the cart a new div is created for the cart row. Its HTML contents are set to include the title, image, and price (all retrieved from the item clicked) as well as the quantity and remove button. This cart row div is appended to the cart items div, which already exists in the original HTML for the store page. Event listeners are added for the remove button and quantity input (for changing the quantity to 1 if the input is invalid and updating the cart total). The cart total is then updated. 

Removing an item involves using the in-built remove() function for HTML elements, and then also updating the cart total. Updating the cart total is done by calling a function which takes the sum of the price multiplied by the quantity of each item in the cart. This function is called whenever the quantity of an item is changed or an item is added/removed. 

When the purchase button is clicked, the cart is cleared by removing the first child element of the cart div until the cart div has no more child nodes. 

An alert is created when the purchase button is clicked to thank the user for their purchase. An alert also appears when a user tries to add an item to the cart that is already in there (to say that they have already added this item), and then the function returns to avoid adding the same item twice. 

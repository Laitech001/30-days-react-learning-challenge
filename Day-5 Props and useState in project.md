## Challenge
use react to display a list data and update the UI when a data is remove or deleted.

## Solution 
1. To display a list of the data, I created a reusable component that receives props from a parent component
2. This parent component has a list a data and this list of data was created with useState so it can update on the page automatically.
3. I call the child component and gave the props a value that as already created in with useState and this display a list that's in my state.
4. Each list's template has it own delete button.
5. for this button to work, each list in my object already have a unique id and the template for the list already have the key-value that have the id.
6. I gave the button an onClick atribute that call the a jabascript function.
7. This function receive a parameter which is "id", the function is below.
   const deleteItem = (id) => {
     const newBlogs = blogs.filter(blog => blog.id !== id);
     setBlogs(blogs);
   }
   the function above receive a parameter of id, create a variable and filter a list of that has a different id with the click item, and use useState to display the remaining list on the page.

## what I learn
This approach is more powerful and flexible than vanilla JavaScript. I’ve used the same logic in my e-commerce project for product lists and cart items.

In vanilla JavaScript, I manually update the DOM. In React, I just update the state, and React updates the UI automatically. This makes the code cleaner, more predictable, and easier to manage.

ON TO THE NEXT LEVEL.....

   

## What I Learned Today
1. What React Router really is
2. What “exact match” means and why it is used
3. What Link does in React Router

## What React Router really is:
React Router is a way to change what shows on the screen based on the URL, without reloading the page.

## In a normal website that does not use React Router, whenever you navigate to another page, the browser reloads the entire page. During this process:
1. The browser sends the URL to the server
2. The server responds with a new page
3. This makes the website feel slower
## With React Router, the page is loaded once. When you click an element to navigate:
1. The URL changes
2. React Router listens to that URL change
3. React switches the component that should be displayed
No full page reload happens. Only the component changes.

## WhaT "Exact match" means and why it is used:
<Route path="/" component={Home} />
<Route path="/about" component={About} />
This can cause a problem because:
1. React thinks / and /about are related
2. Since both paths start with /, React may render the wrong component or multiple components

# This is where exact match comes in.
exact tells React Router:
“Only render this component if the URL matches this path exactly.”

Example: <Route exact path="/" component={Home} />

# Now:
1. / shows the Home component
2. /about does NOT show the Home component
Exact match prevents unwanted route matching.

## What links does in react
In React apps, we avoid using the normal HTML <a> tag for internal navigation.
Using <a>:
1. Reloads the whole page
2. React state is lost
3. The app feels slow
# React Router provides Link as a replacement:
<Link to="/about">About</Link>

with link: 
1. there's no page reload
2. react only switch component
3. application state stay intact
4. the app feels smooth and like a real application.

## How These Three Concepts Connect

1. React Router listens to the URL
2. Routes decide which component matches the URL
3. Exact match prevents unwanted route matching
4. Links change the URL without reloading the page

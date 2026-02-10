## The topics I focused on were:

1. Route parameters
2. useEffect cleanup
3. Reusing logic with custom hooks

## Route Parameters
Route parameters allow one component to handle different data based on the URL.

## Example idea:

* /products/1
* /products/2
Even though the page changes, the same component is reused. The difference comes from the id in the URL.

## What I understood:
1. Route params help avoid duplicating pages
2. The URL acts like an input to the component
3. This is very useful for product details pages in an e-commerce app

## useEffect Cleanup
useEffect is used for side effects like:
1. Fetching data
2. Timers
3. Event listeners
The cleanup function exists to remove or stop anything that was started by the effect.

## What I understood:
1. Cleanup runs when a component unmounts
2. Cleanup also runs before the effect runs again
3. This prevents memory leaks and outdated requests

## Why this matters:
When route parameters change, old fetch requests should be cancelled
Without cleanup, old data can override new data

## Reusing Logic with Custom Hooks
Custom hooks are used to extract reusable logic from components.
Instead of repeating the same useEffect and fetch logic in multiple components, the logic can live inside a custom hook.

## What I understood:
1. Components should focus on UI, not data logic
2. Custom hooks make code cleaner and easier to maintain
3. Hooks make scaling a project easier

## How These Concepts Connect
These three concepts work best together:
1. Route parameters decide what data is needed
2. useEffect fetches the data when the parameter changes
3. Cleanup prevents old requests from causing bugs
4. Custom hooks wrap everything into reusable logic

# This pattern is very important for real-world React apps, especially e-commerce platforms.

## Reflection
Today was about foundation, not speed.

I am intentionally learning how things work and where they should be used before applying them to my project. I believe that once I start using these concepts inside my own e-commerce app, the understanding will become deeper and more natural.
The plan is:
Learn the concept
Understand the purpose
Apply it in the project
Then document the actual implementation logic
This approach helps me stay focused and avoid blindly copying tutorials.

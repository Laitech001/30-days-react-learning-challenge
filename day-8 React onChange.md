## onChange in React
## What it is

The onChange event in React is used to listen for user input and respond to it, such as updating state with useState. Without onChange, an input field with a fixed value would be read-only, preventing users from typing or modifying its content.

## Where to use it
## You can use onChange anywhere you need to respond to user input, such as:

1. Form fields
2. Input validation
3. Dynamic calculations based on user input

## Practical example
<input 
  type="text" 
  placeholder="Course Name" 
  value={course.name} 
  onChange={(e) => onChange('name', e.target.value)}
/>


Here, when the user types in the input, the onChange handler updates the corresponding course state, keeping the UI and state in sync.

## Topic: React State & useState Hook

## What I learned
•	What state is in React
•	Why state is used for dynamic data
•	How to use the useState hook
•	How React re-renders UI when state changes.

## Concepts covered
•	useState syntax
•	State update with setter function
•	Event handling (onClick)
•	Conditional UI updates.

## What I built
I built a counter app with:
•	Add button
•	Minus button
•	Reset button
The counter updates automatically when buttons are clicked.

## the code of the counter app.
const [count, setCount] = useState(0);
function App() {
  return (
    <h1>{ count }</h1>
    <button onClick = { () => setCount(count + 1)}>Add to count</button>
    <button onClick = { () => setCount(count - 1)}>Minus</button>
    <button onClick = { () => setCount(0)}>Reset</button>
  )
}

## What I understand now
•	State is used to store changing data
•	Updating state automatically updates the UI
•	React components can have their own memory (state).

## Challenges
•	Understanding why normal variables don’t update the UI
•	Learning when to use setState instead of changing variables directly.

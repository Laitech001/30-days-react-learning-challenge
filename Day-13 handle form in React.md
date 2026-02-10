## Topics:
1. Controlled Input
2. Form Submit Event
3. POST Request

# Control Input:
  A control Input is a form input whose value is controlled by react state instead of DOM
  In React: **The Input value comes from React State**. **Every change Update the State using onChange**
  This gives React full control over the input.

## Why Controlled Inputs Are Important:
  1. eact always knows the current value
  2. Easy validation
  3. Easy form submission
  4. redictable behavior
Controlled inputs are the standard and recommended way to handle forms in React.

## Basic Example of Controlled Input:
  const [name, useName] = ueState('')

  <input
    type="text"
    value={name}
    onChange = { (e) => setName(e.target.value) }
  />

  the example below show how controlled input works in real life scenerous.
  1. value={name}: React control the input
  2. onChange: this update the state whenever the user type

## Handling mutiple Input
  When a State have multiple input, each input maps to state
# Example using one state object
  const [formData, setFormData] = usestate(
    email: "",
    password: ""
  );

  const handleChange = (e) => {
    const {name, value} = e.target;
    setFormData((prev) => ({
      ...prev, 
      [name]: value,
    }));
  }

  <input 
    type="text"
    value={formData.email}
    onChange= {handleChange}
  />
this above solution Reduces repetition and scale better for large form.

## Form submit event: 
  By default, submitting a form:
  * Refreshes the page
  * Sends data to the server automatically
  In React, we prevent this default behavior.
# prevent default submit behaviour
  const handleSubmit = (e) => {
    e.preventDefault();
    // custom logic here
  };
  <form onSubmit={handleSubmit}>
    <button type="submit">Submit</button>
  </form>
# Why e.preventDefault()?
  * Stops page refresh
  * Allows full control of submission logic
## Submitting Form Data
  1. Once the form is submitted, we usually:
  2. Validate data
  3. Send data to a backend
  4. Show success or error message

## POST Request in React:
  A POST Reaquest send a new data to a server to:
  * Create a New Data
  * save form Data
  * Register User
  common tools that's always use is: fetch, axious.
## POST Request using fetch method.
  const handleSubmit = async (e) => {
    e.preventDefault();
    const response = await fetch("https://example.com/api/users", {
    method: "POST",
    headers: { "Content-Type": "application/json", },
    body: JSON.stringify(formData),
    });
    
  const data = await response.json();
  console.log(data);
  };
# Explanation
  method: "POST" sending data
  headers: tell server data format
  body: Data being sent

## Handling Loading and Errors
  const [isLoading, setIsLoading] = useState(false);
  const [error, setError] = useState(null);

  const handleSubmit = (e) => {
    e.preventDefault();
    setIsLoading(true);
    setError(null);
    try {
      const res = await fetch("https://example.com/api/users", {
      method: "POST",
      headers: { "Content-Type": "application/json", },
      body: JSON.stringify(formData),
      });
      if (!res.ok) throw new Error("Request failed")
    } catch (err) {
      setError(err.message);
    } finally {
      setIsLoading(false);
    }
  }

## Real-Life Use Cases
  1. Login forms
  2. Registration forms
  3. Contact forms
  4. Checkout pages.
  

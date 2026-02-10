# React Hooks – Complete Documentation
---

## 1. What are React Hooks?

Hooks are special functions introduced in **React 16.8** that let you:

* Use state in function components
* Handle side effects (API calls, subscriptions)
* Reuse logic across components

👉 Hooks **only work in function components**.

---

## 2. Rules of Hooks (Very Important)

1. Only call hooks at the **top level** (not inside loops or conditions)
2. Only call hooks inside **React function components** or **custom hooks**

---

## 3. Built‑in React Hooks

### 3.1 useState

**Purpose:** Manage component state

* Stores a value
* Triggers re‑render when updated

**Common use cases:**

* Form inputs
* Toggles (modal open/close)
* Counters

---

### 3.2 useEffect

**Purpose:** Handle side effects

Side effects include:

* Fetching data
* Updating the DOM
* Subscriptions
* Timers

Runs:

* After render
* On dependency change
* On unmount (cleanup)

---

### 3.3 useContext

**Purpose:** Share global data without prop drilling

Used with `React.createContext`

**Common use cases:**

* Auth user
* Theme (dark/light)
* Language settings

---

### 3.4 useRef

**Purpose:** Reference DOM elements or persist values

* Does NOT cause re‑render
* Value persists across renders

**Use cases:**

* Focus input
* Store previous values
* Timers / intervals

---

### 3.5 useReducer

**Purpose:** Manage complex state logic

Similar to Redux pattern:

* state
* action
* reducer

**Use cases:**

* Forms with many fields
* Complex state updates

---

### 3.6 useMemo

**Purpose:** Optimize expensive calculations

* Memorizes computed values
* Improves performance

**Use cases:**

* Heavy calculations
* Filtering large lists

---

### 3.7 useCallback

**Purpose:** Memoize functions

* Prevents unnecessary re‑renders
* Useful with `React.memo`

**Use cases:**

* Passing callbacks to child components

---

### 3.8 useLayoutEffect

**Purpose:** Like useEffect but runs synchronously

* Runs **before browser paints UI**

**Use carefully** (can block UI)

---

### 3.9 useImperativeHandle

**Purpose:** Customize values exposed via ref

Used with `forwardRef`

**Advanced use case:**

* Exposing methods from child component

---

### 3.10 useDebugValue

**Purpose:** Debug custom hooks

* Shows values in React DevTools

---

### 3.11 useId

**Purpose:** Generate unique IDs

* Prevents hydration mismatch
* Useful for accessibility

---

### 3.12 useTransition

**Purpose:** Handle non‑urgent updates

* Improves UI responsiveness

Used in concurrent rendering

---

### 3.13 useDeferredValue

**Purpose:** Defer updating a value

* Helps with performance
* Useful in search inputs

---

### 3.14 useSyncExternalStore

**Purpose:** Subscribe to external stores

* Used by libraries
* Ensures consistent state

---

### 3.15 useInsertionEffect

**Purpose:** Inject styles before layout

* Mostly for CSS‑in‑JS libraries

---

## 4. React Router Hooks (Important)

### useNavigate (Modern replacement for useHistory)

**Purpose:** Programmatic navigation

* Redirect users
* Navigate after form submit

> ⚠️ `useHistory` is **deprecated** (React Router v5)
> Use `useNavigate` in React Router v6+

---

### useParams

**Purpose:** Read URL parameters

**Use cases:**

* Product ID
* User profile

---

### useLocation

**Purpose:** Access current URL info

* pathname
* query string

---

### useSearchParams

**Purpose:** Read & update query params

Useful for:

* Filters
* Pagination

---

## 5. Custom Hooks

**Purpose:** Reuse logic across components

Rules:

* Must start with `use`
* Can use other hooks inside

**Examples:**

* useFetch
* useLocalStorage
* useAuth

---

## 6. When to Use Which Hook (Summary)

* UI state → useState
* Side effects → useEffect
* Global state → useContext
* DOM access → useRef
* Complex logic → useReducer
* Performance → useMemo / useCallback
* Routing → useNavigate / useParams

---

## 7. Final Notes

* Hooks are the **core of modern React**
* Mastering them = frontend confidence
* Build projects using each hook

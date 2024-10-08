# Student Application

# Login Page

```js
const initialState = {
  collegeId: "",
  password: "",
  loading: false,
  error: "",
};
```

- Local storage is used to store the token and user details.
- UseContext is used to pass the user details to the other components.

# Sign up

```js
const initialState = {
  collegeId: "",
  password: "",
  name: "",
  loading: false,
  error: "",
};
```

- Local storage is used to store the token and user details.
- UseContext is used to pass the user details to the other components.

# Home Page

## Register Manual

this is the basic state of the register manual page and this might change for each category and their relative sections of feedback maybe added or removed.

```js
const initialState = {
  blockname: "",
  floorno: "",
  classroom: "",
  type: "",
  Domain: "",
  Content: "",
  anonymous: false,
  loading: false,
  error: "",
};
```

- Api call to the relevent endpoint is made to post the feedback.

## My reports

- api call with userid to retrieve the feedbacks given by the user.

```js
const state = {
  issueID: "",
  issueDomain: "",
  issueType: "",
  issueStatus: "",
};
```

- navigation to next page with the issue id and retrieve the issue data there

## User Profile

- display the user details and the feedbacks given by the user.
- usage of useContext to remove the user details from the local storage and navigate to the login page.

# Admin Application

# Login Page

```js
const initialState = {
  collegeId: "",
  password: "",
  loading: false,
  error: "",
};
```

- Local storage is used to store the token and user details.
- UseContext is used to pass the user details to the other components.

# Sign up

```js
const initialState = {
  collegeId: "",
  password: "",
  name: "",
  loading: false,
  error: "",
};
```

- Local storage is used to store the token and user details.
- UseContext is used to pass the user details to the other components.

# Home Page

## Admin Dashboard

### View all Users

- api call to retrieve all the users and display them in cards

```js
const state = {
  collegeId: "",
  name: "",
  role: "",
};
```

- user deletion
- Storing the recent search data in local storage and displaying them in the search bar.

### create new user

- api call to create a new admin with the employee id and password

```js
const state = {
  employeeId: "",
  name: "",
  role: "",
};
```

- a notification service to send all the other admins a notification about the new user created.

### statistics

TBD

### Resolved issues

- api call to retrieve all the resolved issues and display them in cards

```js
const state = {
  issueID: "",
  issueDomain: "",
  issueType: "",
  issueStatus: "",
};
```

- navigation to next page with the issue id and retrieve the issue data there

### Todo Page

- displaying all the unresolved issues in card with infinite scroll and lazy loading.

### view Issue

- add comments to the issue raised

- api call to update the issue status and comments

```js
const state = {
  issueID: "",
  issueDomain: "",
  issueType: "",
  issueStatus: "",
};
```

## User Profile

- display the user details and the feedbacks given by the user.

- usage of useContext to remove the user details from the local storage and navigate to the login page.

```js
const state = {
  collegeId: "",
  name: "",
  role: "",
};
```

- General Hooks

  - all the pages in the application uses the `useReducer` hooks and the pages with specific data will be fetched using the `useEffect` hooks.

  - the `useContext` hook is used to pass the user details to the other components.

  - the `useNavigate` hook is used to navigate to the other pages.

  - the `expo router` is used inorder to navigate between pages

  - `Expo async Storage` is used to store the local data and use when ever necessary

  - the Backend url will be retrieved from the app.json using `expo constant` inorder to abstract and protect the url from the user.

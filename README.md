# React Router Dom: Missing Catch-all Route
This repo demonstrates a common error in React Router DOM v6 and above:  failing to include a catch-all route to handle non-existent paths.  Without a catch-all, the application will not gracefully handle attempts to navigate to undefined routes.

## Problem
The initial `App.js` lacks a route to handle any path that doesn't explicitly match `/` or `/about`.  This leads to a blank screen or, depending on your error handling, an error message when a user navigates to a nonexistent URL.

## Solution
The `AppSolution.js` file demonstrates the fix by adding a `Route` with the path `*`, which acts as a catch-all.  This ensures that any invalid path will trigger the component specified (here, `NotFound`), providing a more user-friendly 404 experience.  Consider implementing custom error handling or a proper 404 page for production applications.
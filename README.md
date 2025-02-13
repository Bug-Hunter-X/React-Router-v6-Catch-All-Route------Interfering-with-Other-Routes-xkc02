# React Router v6 Catch-All Route Issue

This repository demonstrates a subtle issue with the catch-all route (`/*`) in React Router v6.  The catch-all route, intended to handle 404 errors, unexpectedly overrides other defined routes.

## Problem

The `App.js` file contains a simple React Router setup. Despite having explicit routes for `/` and `/about`, the catch-all route (`/*`) is triggered, even if the URL matches one of the defined routes. This masks any errors that might occur in those other routes, making debugging difficult.

## Solution

The `AppSolution.js` file shows how to resolve this.  The catch-all route should be placed *after* all other routes to ensure it only matches URLs that don't match any other defined route.

## Reproduction

1. Clone this repository.
2. Run `npm install`
3. Run `npm start`
4. Observe the behavior by navigating to `/`, `/about`, and other arbitrary URLs.
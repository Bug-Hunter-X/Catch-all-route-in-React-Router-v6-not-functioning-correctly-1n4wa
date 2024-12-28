# React Router v6 Catch-all Route Issue

This repository demonstrates a bug in React Router v6 where the catch-all route (`/*`) behaves unexpectedly.  The issue arises when the catch-all route is triggered even when a valid route exists, leading to incorrect 404 errors.

## Problem Description

In React Router v6, the catch-all route (`/*`) is intended to match any path that doesn't match any other defined routes. However, in some scenarios, even with valid routes, the catch-all route is triggered. This is especially true when the order of routes in the `Routes` component matters.  This inconsistent behavior breaks expected application functionality.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to `/` or `/about` which should render the Home and About components.
5. Notice that even though routes for `/` and `/about` are explicitly defined, the catch-all route (`/*`) is also activated, resulting in an unexpected rendering of the 404 component. 

## Solution

The solution involves reviewing the order of routes in the Routes component. The catch-all route (`/*`) should always be placed last.  See the solution branch or file for a corrected version of the code.

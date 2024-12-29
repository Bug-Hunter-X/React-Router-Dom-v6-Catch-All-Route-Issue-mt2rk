# React Router Dom v6 Catch All Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in React Router v6.  The catch-all route unexpectedly matches all routes, even if more specific routes are defined earlier.

## Problem

The `/*` route in `react-router-dom` should ideally only match routes not matched by other, more specific routes. However, when placed after other routes, it intercepts all requests.

## Solution

The solution involves reordering the routes.  Place the catch-all route (`/*`) at the very end of your `Routes` component.  This ensures that more specific routes are checked before the catch-all route is considered.
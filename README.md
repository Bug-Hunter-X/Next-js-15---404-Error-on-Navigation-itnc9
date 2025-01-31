# Next.js 15 - 404 Error on Navigation

This repository demonstrates a common issue in Next.js 15 applications where a 404 error is thrown when navigating to a page, even when that page is correctly defined. The bug is primarily related to the dynamic import behavior of Next.js and its interaction with client-side routing.

## Bug Description
The issue arises when using client-side navigation to a page that is not directly under the `pages` directory, potentially resulting from using dynamic imports or other routing techniques. Next.js may incorrectly fail to resolve the route leading to a 404.

## Solution
Ensure that the page being navigated to is properly declared within Next.js routing structure. Consider using the `Link` component for internal navigation to guarantee proper route resolution. For dynamic routing, carefully review your routing configurations to ensure they correctly resolve the dynamic segments.
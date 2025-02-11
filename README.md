# Next.js 15 getServerSideProps with fetch - ReferenceError: fetch is not defined

This repository demonstrates a common error encountered when using `getServerSideProps` in Next.js 15 applications and provides a solution.

## Problem

When attempting to use `fetch` within `getServerSideProps` to fetch data, a `ReferenceError: fetch is not defined` is thrown. This occurs because the `fetch` API is not globally available in the Node.js environment used by `getServerSideProps`.

## Solution

The solution involves explicitly importing the `node-fetch` library, which provides a fetch implementation compatible with Node.js.  This ensures that the `fetch` API is available within your `getServerSideProps` function.

## Steps to Reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server.
4. Navigate to the `/about` page.  You'll observe the error in the console.
5.  After applying the fix, the About page will display the list of characters.

## Additional Notes

Remember to adjust the API endpoint and data handling to match your specific requirements.  Always handle potential errors during the API call to prevent unexpected behavior.  Consider using error boundaries in your components for more robust error handling.
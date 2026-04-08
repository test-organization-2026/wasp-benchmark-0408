A third-party service needs to programmatically insert tasks into the Wasp application via HTTP requests, bypassing the standard React client.

You need to configure a custom HTTP POST endpoint at `/api/tasks` in `main.wasp` and implement an Express route handler in Node.js to parse a JSON payload and create a new `Task` in the Wasp server environment. 

**Constraints:**
- The endpoint MUST be declared using the `api` block in `main.wasp`.
- The Node.js handler must validate that the `title` field is present in the request body, returning a `400` status code if it is missing.
- You MUST utilize Wasp's context to access the database (`context.entities.Task`) instead of importing Prisma manually.
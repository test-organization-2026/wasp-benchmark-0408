The app is transitioning to a multi-tenant model where tasks belong to teams rather than being globally visible to all authenticated users.

You need to create a `Team` entity, associate both `Task` and `User` entities with a `Team` in the schema, and update the `getTasks` Wasp query to return only the tasks associated with the current user's team in the Wasp full-stack environment. 

**Constraints:**
- The `getTasks` Node.js operation MUST throw a `HttpError(401)` if `context.user` is undefined.
- Ensure the database schema accurately reflects a one-to-many relationship between `Team` and `User`, and `Team` and `Task`.
- Do NOT modify the existing frontend query hooks; only modify the server-side operation logic and Prisma schema.
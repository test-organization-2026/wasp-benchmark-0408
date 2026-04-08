The analytics team wants to track the total volume of tasks created in the system over time without impacting the performance of user-facing requests.

You need to declare a background job in `main.wasp` and implement the corresponding Node.js function to query the total number of tasks in the database, logging the integer result to the server console in the Wasp backend environment. 

**Constraints:**
- The job MUST be scheduled using cron syntax within the `job` declaration in `main.wasp` to run exactly once every hour.
- Use the automatically provided Prisma client instance (`context.entities.Task.count()`) to perform the database operation.
- Do NOT expose this job's logic as a public API or client-callable Operation.
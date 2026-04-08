The current application has a basic `Task` entity defined using Prisma Schema Language in `schema.prisma` but lacks categorization.

You need to add a required `category` (String) field to the `Task` entity and update the `TaskList.jsx` React component to visually display this new field next to each task in the Wasp development environment. 

**Constraints:**
- You MUST run `wasp db migrate-dev` after modifying the schema to apply the changes.
- Do NOT modify or remove the existing `description` or `isDone` fields on the `Task` entity.
- The Wasp development server (`wasp start`) must be running during schema updates to ensure type generation completes successfully.
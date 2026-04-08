The starter Wasp project defaults to SQLite, but the project has outgrown this and requires a production-ready PostgreSQL database setup.

You need to update `schema.prisma` to use the `postgresql` provider, provide the connection string, and properly reset the development database state to apply the new schema in the Wasp project environment. 

**Constraints:**
- You MUST delete the existing `migrations/` directory and run `wasp clean` before generating new migrations.
- Do NOT hardcode the database credentials; provide the PostgreSQL connection string via the `DATABASE_URL` environment variable.
- Create an initial migration using `wasp db migrate-dev` after the cleanup process.
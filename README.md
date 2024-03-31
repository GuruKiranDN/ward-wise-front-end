# Ward Wise Frontend

This is a refactored, reimagined, and expanded implementation of the current [Ward Wise frontend](https://github.com/ward-wise/alderman-spending-data-viz), built in Next.js.

## Low-fidelity Prototype
Here is a lo-fi paper mockup of the site; it's not complete, but it's somewhere to start from.
![PXL_20240110_014235957~2](https://github.com/GuruKiranDN/ward-wise-front-end/assets/28895925/50880115-d9a2-4c49-91c0-98a682dd76ac)

We are planning to make it a single-page scroll website.
![PXL_20240110_014252656~2](https://github.com/GuruKiranDN/ward-wise-front-end/assets/28895925/0ab645f7-7aca-4b0c-bb43-359e2f4cd42e)

## Setup

1. Clone/Fork the repo and install dependencies (`npm install`)

2. Install [PostgreSQL](https://www.postgresql.org/docs/current/tutorial-install.html), if you do not already have an instance installed.

3. Run `createdb wardwise` in your terminal. 
> **Note:** If PostgreSQL was not added to your system PATH during installation, you'll need to be in the PostgreSQL `bin` directory for this command to work.

4. Create a `.env.local` file in your project directory and add the below, where USERNAME and PASSWORD are the credential for:
    * your system user
    * the user authorized to run Postgres on your machine, or
    * the **postgres** admin account setup during installation
```
DATABASE_URL="postgresql://USERNAME:PASSWORD@localhost:5432/wardwise?schema=public"
```

5. Run `npm run migrate:dev` to create tables and seed your database. If the seeding does not happen automatically, run `npm run db:seed`.

6. Run `npm run dev` to start a development server (located at [http://localhost:3000](http://localhost:3000) by default)

For additional database management scripts, see `package.json`

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

# Tasks

Create a simple full-stack app.

## Frontend
1. Setup new page and components for CRUD operations
   1. Simple list (table) with data from the API. Click on row should open a modal with item details and CRUD buttons.
      a. Nice to have a pagination or infinity scroll
   2. As an option you can use `swr` to call backend api (`axiosApi` const is ready for use as fetcher function)
   3. `react-hook-form` example for update
2. Generate new redux slice for persisting some data into the store during above operations


## Backend
1. Setup `api` module with standard REST endpoints for `CRUD` operations (accepting both query strings and body data)
   1. Setup DB model (example in `api/src/user`) and DTO classes (with `class-validator` decorators)
   2. Any DB you like (MongoDB, sqllite etc)
   3. Link column in generated model with `user.model.ts` using sequelize foreign keys
   4. Create service using sequelize model methods for CRUD functions
2. Setup secondary `api` module with random `service`
   1. It could be some service that takes an item ID, mutates it in a simple way and return new entity
3. Inject service in first generated module
4. Add correct `@nestjs/swagger` decorators on controller
5. 

## Tests
1. Add unit tests to `api` module (one endpoint)
2. Add E2E test to `api` module, using `supertest` and `expect` schemas (eg: `toMatchObject(schema)`) (example in `app.e2e-spec.ts`) (one endpoint)
3. Add frontend component test for one React component ensuring it renders correctly (example in `Dashboard.spec.tsx`)


#### Setup

```shell
nvm use
pnpm install
pnpm dev
pnpm test
```

#### Local Development

- [Back Office](http://localhost:3000/) (`backoffice/app`)
- [Back Office API](http://localhost:4000/) (`backoffice/api`)

## DELIVER
- Push to your GitHub repo and share a link;
- Share a link to the deployed application;

## IMPORTANT NOTE
Please be reasonable about your time. This task shouldn't take more than 4-6 hours.

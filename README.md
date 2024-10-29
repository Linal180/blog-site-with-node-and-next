
# Blog Site Project

This monorepo hosts a blog site’s frontend and backend. The frontend, built with Next.js, uses SSR and SSG for performance and SEO, displaying dynamic content from the backend API. The backend, built with Node.js and TypeScript, uses PostgreSQL with TypeORM, supporting migrations, seeding, and environment-specific configs.

## Table of Contents
- [Project Overview](#project-overview)
- [Frontend Setup (Next.js)](#frontend-setup-nextjs)
- [Backend Setup (Node.js with TypeScript and PostgreSQL)](#backend-setup-nodejs-with-typescript-and-postgresql)
- [Environment Variables](#environment-variables)
- [Running the Project](#running-the-project)
- [Building for Production](#building-for-production)
- [Database Migrations and Seeding](#database-migrations-and-seeding)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
This project consists of a frontend built with Next.js for dynamic blog content display and a backend built with Node.js, TypeScript, and PostgreSQL for content management. The backend API integrates with the frontend to provide blog content dynamically.

---

## Frontend Setup (Next.js)

### Prerequisites
- Node.js (v14+)
- npm or yarn

### Setup
1. Clone the repository:
   ```bash
   git clone git@github.com:AdeelKamalMalik/nextjs-template.git
   cd nextjs-template
   ```

2. Install dependencies:
   ```bash
   npm install
   ```
   or with yarn:
   ```bash
   yarn install
   ```

3. Set up environment variables by creating a `.env.local` file:
   ```env
   NEXT_PUBLIC_API_URL=<your_backend_api_url>
   ```

### Running the Frontend
To start the development server:
```bash
npm run dev
```
or with yarn:
```bash
yarn dev
```

### Building for Production (Frontend)
To create an optimized production build:
```bash
npm run build
```
To start the production server:
```bash
npm start
```
or with yarn:
```bash
yarn start
```

---

## Backend Setup (Node.js with TypeScript and PostgreSQL)

### Prerequisites
- Node.js (v14+)
- PostgreSQL
- TypeORM

### Setup
1. Clone the repository:
   ```bash
   git clone git@github.com:AdeelKamalMalik/nodejs-template.git
   cd nodejs-template
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure environment variables by creating `.env.local` and `.env.prod` files for local development and production, respectively:
   ```env
   DB_HOST=localhost
   DB_PORT=5432
   DB_USERNAME=your_username
   DB_PASSWORD=your_password
   DB_DATABASE=your_database
   ```

4. Create the database:
   ```bash
   npm run create-database
   ```

### Running the Backend
To start the development server:
```bash
npm run dev
```
To start the production server:
```bash
npm run start
```

### Database Migrations and Seeding
To generate a new migration:
```bash
npm run typeorm:generate -- NameOfMigration
```
To run migrations:
```bash
npm run typeorm:migrate
```
To revert the last migration:
```bash
npm run typeorm:revert
```
To drop the database schema:
```bash
npm run typeorm:drop
```
To seed the database with initial data:
```bash
npm run seed
```

---

## Environment Variables
Environment variables should be set up in both frontend and backend for seamless integration. Refer to the respective `.env` files for each setup.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License.
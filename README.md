# Gemovia — Jewelry E-Commerce Platform

Gemovia is a modern jewelry e-commerce web application designed to provide customers with an elegant and convenient online shopping experience. The platform will allow customers to discover jewelry collections, explore product details, manage their shopping carts, and place orders.

The project is being developed incrementally, beginning with a Minimum Viable Product (MVP) and expanding towards a more personalized shopping experience.

## Project Objectives

- Build a responsive and user-friendly jewelry storefront.
- Provide structured product catalogs, detailed product pages, and product variants.
- Implement a reliable shopping cart and checkout experience.
- Support product, inventory, and order management.
- Apply secure development practices and maintainable software architecture.
- Prepare the platform for future integration with an AI-powered shopping assistant.

## Technology Stack

| Technology | Purpose |
|---|---|
| Next.js | Full-stack React framework |
| React | Component-based user interface |
| TypeScript | Static type checking |
| Tailwind CSS | Responsive styling |
| PostgreSQL | Relational database |
| Prisma ORM | Database access and schema migrations |
| Git and GitHub | Version control and collaboration |
| GitHub Actions | Automated quality checks |

## Planned MVP Features

- Responsive homepage and jewelry collections
- Product catalog and product detail pages
- Product categories and basic filtering
- Product variants, such as ring sizes and materials
- Shopping cart and checkout
- Customer accounts and guest checkout
- Payment integration
- Order confirmation and order management
- Administrative product and inventory management

Features will be implemented progressively. Items listed here are planned functionality and may not yet be available.

## Future Enhancements

- AI-powered shopping assistant
- Personalized product recommendations
- Wishlists and recently viewed products
- Product reviews and ratings
- Enhanced product search and filtering
- Delivery tracking and automated notifications
- Advanced inventory management and business analytics

## Getting Started

### Prerequisites

Install the following tools before setting up the project:

- Node.js — a supported LTS release compatible with the installed Next.js version
- npm
- Git
- Visual Studio Code or another code editor

PostgreSQL and Prisma will be configured in a later development stage.

### Installation

Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd gemovia-jewelry-e-commerce
```

Install the dependencies:

```bash
npm ci
```

If the project does not yet have a committed `package-lock.json`, run `npm install` instead and commit the generated lockfile.

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Available Scripts

```bash
npm run dev
npm run build
npm run start
npm run lint
```

- `dev` starts the local development server.
- `build` creates a production build.
- `start` serves the production build.
- `lint` checks code quality using the configured linting tool.

Additional scripts for type checking and testing will be added as the project develops.

## Project Structure

The application uses the Next.js App Router. The structure will grow as new features are introduced.

```text
gemovia-jewelry-e-commerce/
├── public/              # Static assets
├── src/
│   ├── app/             # Routes, layouts, and global styles
│   ├── components/      # Reusable UI components
│   ├── lib/             # Shared utilities and infrastructure
│   ├── services/        # Application service logic
│   └── types/           # Shared TypeScript types
├── .github/
│   └── workflows/       # GitHub Actions workflows
├── .gitignore
├── package.json
├── package-lock.json
├── tsconfig.json
└── README.md
```

Some directories may be introduced only when they are needed.

## Git Workflow

The project follows a feature-branch workflow:

- `main` contains stable, release-ready code.
- `develop` integrates completed and tested features.
- `feature/*` branches contain individual features or development tasks.
- `fix/*` branches contain targeted bug fixes.

### Development Process

1. Create a feature branch from `develop`.
2. Implement the feature in small, focused commits.
3. Run linting, type checking, tests, and the production build as applicable.
4. Push the feature branch to GitHub.
5. Open a pull request targeting `develop`.
6. Review the changes and wait for required automated checks.
7. Merge the pull request after the checks pass.
8. Merge tested releases from `develop` into `main`.

### Commit Message Convention

Use descriptive commit messages with a consistent prefix:

- `feat:` new functionality
- `fix:` bug fixes
- `chore:` setup and maintenance
- `refactor:` code restructuring
- `test:` tests
- `docs:` documentation
- `style:` formatting and styling changes

Example:

```text
feat: add responsive jewelry product grid
```

## Environment Variables

Keep credentials and private configuration in local environment files or the deployment platform's secret manager.

Never commit real database URLs, payment secrets, authentication secrets, or private API keys.

An `.env.example` file may document required variable names using safe placeholder values.

## Development Principles

- Keep components reusable and focused.
- Validate input on the server.
- Enforce authorization for protected operations.
- Treat server-side data as the source of truth for prices, stock, orders, and payments.
- Write tests for important business rules.
- Keep dependencies and documentation up to date.
- Use pull requests and automated checks to maintain code quality.

## Project Status

**Current phase:** Stage 1 — Project setup and development workflow.

The storefront, database integration, checkout, and advanced features will be developed in subsequent stages.

## License

A license will be selected before public distribution. Until then, no open-source license is implied by this README.

# Multi-Tenant Marketplace Platform

A modern multi-tenant eCommerce marketplace built with Next.js 15, Payload CMS, and Stripe Connect.

This platform allows multiple merchants to run storefronts under vendor subdomains while the platform owner manages operations from a centralized admin dashboard.

Core capabilities include product listings, reviews, role-based access control, payments, vendor payouts, and automatic platform fees.

## Table of Contents

- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [Stripe Setup](#stripe-setup)
- [Available Scripts](#available-scripts)
- [Screenshots](#screenshots)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## Overview

The Multi-Tenant Marketplace Platform enables:

- Multiple vendors in one platform
- Vendor-specific storefront experiences
- Secure checkout and payout workflows
- Platform-level fee collection
- Clear permission boundaries for admins, merchants, and customers

## Tech Stack

### Frontend

- Next.js 15 (App Router)
- Tailwind CSS v4
- shadcn/ui
- TypeScript

### Backend

- Payload CMS
- Node.js

### Payments

- Stripe Connect

### Tooling

- ESLint
- PostCSS
- Bun (optional package manager)

## Features

### Multi-tenant marketplace

- Supports multiple merchants
- Each merchant manages products and storefront settings

### Vendor subdomains

Merchants can have unique storefront URLs such as:

```
vendor1.platform.com
vendor2.platform.com
```

### Custom storefronts

- Merchant-level customization for product display and branding

### Stripe Connect integration

- Secure customer payments
- Merchant payouts
- Centralized platform commission support

### Automatic platform fees

- Platform owner collects fees on each eligible transaction

### Ratings and reviews

- Customers can rate products
- Customers can leave written reviews

### User purchase library

- Customers can view purchased products from their account

### Role-based access control

- Admin
- Merchant
- Customer

### Admin dashboard

- Manage users
- Manage vendors
- Monitor transactions
- Configure platform settings

### Merchant dashboard

- Add and manage products
- Track orders
- Manage inventory
- View revenue insights

### Catalog and discovery

- Category filtering
- Attribute-based filtering
- Sorting options
- Product search

### Media support

- Product image upload and display

## Project Structure

```
.
```
📦 
├─ .gitignore
├─ README.md
├─ bun.lock
├─ components.json
├─ eslint.config.mjs
├─ next.config.ts
├─ package.json
├─ postcss.config.mjs
├─ public
│  ├─ file.svg
│  ├─ globe.svg
│  ├─ next.svg
│  ├─ vercel.svg
│  └─ window.svg
├─ src
│  ├─ app
│  │  ├─ favicon.ico
│  │  ├─ globals.css
│  │  ├─ layout.tsx
│  │  └─ page.tsx
│  ├─ components
│  │  └─ ui
│  │     ├─ accordion.tsx
│  │     ├─ alert-dialog.tsx
│  │     ├─ alert.tsx
│  │     ├─ aspect-ratio.tsx
│  │     ├─ avatar.tsx
│  │     ├─ badge.tsx
│  │     ├─ breadcrumb.tsx
│  │     ├─ button-group.tsx
│  │     ├─ button.tsx
│  │     ├─ calendar.tsx
│  │     ├─ card.tsx
│  │     ├─ carousel.tsx
│  │     ├─ chart.tsx
│  │     ├─ checkbox.tsx
│  │     ├─ collapsible.tsx
│  │     ├─ combobox.tsx
│  │     ├─ command.tsx
│  │     ├─ context-menu.tsx
│  │     ├─ dialog.tsx
│  │     ├─ direction.tsx
│  │     ├─ drawer.tsx
│  │     ├─ dropdown-menu.tsx
│  │     ├─ empty.tsx
│  │     ├─ field.tsx
│  │     ├─ form.tsx
│  │     ├─ hover-card.tsx
│  │     ├─ input-group.tsx
│  │     ├─ input-otp.tsx
│  │     ├─ input.tsx
│  │     ├─ item.tsx
│  │     ├─ kbd.tsx
│  │     ├─ label.tsx
│  │     ├─ menubar.tsx
│  │     ├─ native-select.tsx
│  │     ├─ navigation-menu.tsx
│  │     ├─ pagination.tsx
│  │     ├─ popover.tsx
│  │     ├─ progress.tsx
│  │     ├─ radio-group.tsx
│  │     ├─ resizable.tsx
│  │     ├─ scroll-area.tsx
│  │     ├─ select.tsx
│  │     ├─ separator.tsx
│  │     ├─ sheet.tsx
│  │     ├─ sidebar.tsx
│  │     ├─ skeleton.tsx
│  │     ├─ slider.tsx
│  │     ├─ sonner.tsx
│  │     ├─ spinner.tsx
│  │     ├─ switch.tsx
│  │     ├─ table.tsx
│  │     ├─ tabs.tsx
│  │     ├─ textarea.tsx
│  │     ├─ toggle-group.tsx
│  │     ├─ toggle.tsx
│  │     └─ tooltip.tsx
│  ├─ hooks
│  │  └─ use-mobile.ts
│  └─ lib
│     └─ utils.ts
└─ tsconfig.json

```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/marketplace-platform.git
cd marketplace-platform
```

### 2. Install dependencies

Using Bun:

```bash
bun install
```

Or using npm:

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the project root and add the required variables from the section below.

### 4. Run the development server

Using Bun:

```bash
bun dev
```

Or using npm:

```bash
npm run dev
```

Open http://localhost:3000.

## Environment Variables

Create a `.env` file in the root directory:

```env
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=
DATABASE_URI=
PAYLOAD_SECRET=
NEXT_PUBLIC_APP_URL=
```

Optional examples (if used in your app):

```env
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=
PLATFORM_FEE_PERCENT=
```

## Stripe Setup

1. Create a Stripe account.
2. Enable Stripe Connect in your Stripe dashboard.
3. Copy API keys into your `.env` file.
4. Configure webhook endpoints for payment and account events.
5. Verify Connect onboarding flow for merchants.

## Available Scripts

Run the development server:

```bash
npm run dev
```

Build for production:

```bash
npm run build
```

Start production server:

```bash
npm start
```

Run lint checks:

```bash
npm run lint
```


## License

This project is licensed under the MIT License.

## Author

Sofia Asif  
Cybersecurity Student and Developer

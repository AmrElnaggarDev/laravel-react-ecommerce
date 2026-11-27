# Laravel React E-Commerce

An e-commerce web application built with Laravel, React, TypeScript, and Inertia.js as a solo developer portfolio project.

## Current Progress

- Base Laravel, React (TypeScript), and Inertia.js application initialized.
- UI components organized into Core and App directories.
- DaisyUI (v4) and Tailwind CSS configured.
- Storefront Navbar component implemented and integrated into application layouts and pages.

## Tech Stack

- **Backend:** Laravel
- **Frontend:** React, TypeScript, Inertia.js
- **Styling:** Tailwind CSS, DaisyUI v4
- **Database:** SQLite

## Local Setup

1. Install PHP dependencies:
   ```bash
   composer install
   ```
2. Install Node dependencies:
   ```bash
   npm install
   ```
3. Configure environment and database:
   ```bash
   cp .env.example .env
   php artisan key:generate
   php artisan migrate
   ```
4. Run development servers:
   ```bash
   npm run dev
   php artisan serve
   ```

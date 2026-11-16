# Toko Danish – Computer Spare-Part E-Commerce

A multi-seller online store for computer spare parts, built with **Laravel 11** and **Tailwind CSS** as a team project (4 people) for the Software Engineering Project course (PPL), Universitas Sebelas Maret, 2025.

## Features

- Product catalog with categories and product detail pages
- User accounts (Laravel Breeze), profile and shipping addresses
- Cart, checkout, order summary and order history
- **Midtrans** payment gateway
- Shipping cost lookup by province/city and courier via the **RajaOngkir** API
- Product ratings
- Seller onboarding and seller dashboard to add, edit and delete products
- Product images stored on **Google Cloud Storage** (Cloudinary also configured)
- Deployable to **Vercel** (serverless PHP, see `vercel.json`)

## My contribution (Muhammad Aspa Zikra)

- Cart and payment flow: cart CRUD, quantity updates, checkout, Midtrans integration
- Seller product management
- Google Cloud Storage configuration for product image uploads

## Tech stack

Laravel 11, PHP, Blade, Tailwind CSS, MySQL, Vite, Midtrans, RajaOngkir API, Google Cloud Storage, Vercel

## Running locally

```bash
git clone https://github.com/aspazikra/Toko-Danish-PPL-Kel-4.git
cd Toko-Danish-PPL-Kel-4
composer install
npm install
cp .env.example .env
php artisan key:generate
```

Fill in `.env`:

- Database: `DB_CONNECTION`, `DB_HOST`, `DB_PORT`, `DB_DATABASE`, `DB_USERNAME`, `DB_PASSWORD`
- Midtrans: `MIDTRANS_SERVER_KEY`
- RajaOngkir: `API_ONGKIR_KEY`
- Google Cloud Storage: `GOOGLE_CLOUD_PROJECT_ID`, `GOOGLE_CLOUD_KEY_FILE`, `GOOGLE_CLOUD_STORAGE_BUCKET`

Then:

```bash
php artisan migrate --seed
npm run dev
php artisan serve
```

## Team

[Abqli484](https://github.com/Abqli484) · Muhammad Danish Dhiyaulhaq · qmafaza · [Muhammad Aspa Zikra](https://github.com/aspazikra)

Forked from [Abqli484/Toko-Danish-PPL-Kel-4](https://github.com/Abqli484/Toko-Danish-PPL-Kel-4).

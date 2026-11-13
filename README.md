# Phone Catalog

## Introduction

Phone Catalog is a multi-page web application for browsing and choosing Apple products: phones, tablets and accessories. Users can explore the catalog, open a product page with its characteristics and available variants, add items to the cart and save favourites. The project was built to practice React, TypeScript, routing, state management with Context and SCSS modules.

## Live Preview

[View the deployed version](https://uuunemployed.github.io/react_phone-catalog-own/)

## Design Reference

[Figma mockup](https://www.figma.com/design/T5ttF21UnT6RRmCQQaZc6L/Phone-catalog--V2--Original?node-id=0-1&p=f&t=7FSNMq2esMHt85pD-0)

## Key Features

- **Home page:** hero banner, models slider and product categories.
- **Catalog pages:** separate pages for Phones, Tablets and Accessories, built from a product grid.
- **Product page:** detailed characteristics, photos, color and capacity variants, and suggested products.
- **Cart:** add and remove items and see the list of selected products.
- **Favourites:** save products you like and view them on a separate page.
- **Persistent state:** the cart and favourites are shared through React Context and saved between visits.
- **Sorting and pagination controls:** dropdown components for managing how products are displayed.
- **Navigation:** client-side routing with a header, a burger menu and a footer.
- **Loading and error states:** loader, error message and a "Page not found" page.
- **Responsive design:** the layout adapts to mobile, tablet and desktop screens.

## Technical Requirements

To run this project, you will need:

- NPM (version 8.x or newer)

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/uuunemployed/react_phone-catalog-own.git
   ```

2. Navigate to the project directory:

   ```bash
   cd react_phone-catalog-own
   ```

3. Install dependencies:

   ```bash
   npm install
   # or
   yarn install
   ```

4. Run the project locally:

   ```bash
   npm start
   # or
   yarn start
   ```

After starting, the project is available at `http://localhost:5173` (the default Vite port).

## Project Structure

```
public/
├── api/            # JSON data: phones, tablets, accessories, products
├── fonts/          # Mont font files
├── icons/
└── img/            # product photos and banners
src/
├── components/     # reusable UI components (Header, Footer, ProductCard, Dropdown, ...)
├── modules/
│   ├── HomePage/
│   ├── PhonesPage/
│   ├── TabletsPage/
│   ├── AccessoriesPage/
│   ├── ProductPage/
│   ├── FavouritesPage/
│   ├── SelectedItemsPage/   # cart
│   ├── PageNotFound/
│   └── shared/     # contexts, hooks, types, utils, icons
├── style/          # SCSS mixins and font styles
├── App.tsx
├── Root.tsx        # router setup
└── index.tsx
```

## Technologies Used

- **React:** building the user interface from reusable components.
- **TypeScript:** static typing for components, data models and utilities.
- **Vite:** fast dev server and bundler.
- **React Router (HashRouter):** client-side routing between pages.
- **Context API:** global state for the cart and favourites.
- **SCSS (CSS Modules):** component-scoped styling.
- **vite-plugin-svgr:** importing SVG icons as React components.
- **ESLint and Prettier:** code style checks.
- **Git and GitHub:** version control, repository hosting and deployment (GitHub Pages).

## Challenges

- **Shared state:** keeping the cart and favourites in sync across all pages with Context API and saving them between visits.
- **Product variants:** switching between colors and capacities on the product page and updating the URL and data accordingly.
- **Routing on GitHub Pages:** using `HashRouter` so that page reloads do not lead to a 404 error.
- **SVG as components:** configuring `vite-plugin-svgr` and TypeScript types to import icons with the `?react` suffix.

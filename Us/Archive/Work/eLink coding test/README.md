---
tags:
  - incidental
---
# eLink Coding Challenge
##
Thank you for your interest in working at eLink and welcome to the shopping cart coding challenge!

For this challenge, you will build out some important features for a new ecommerce project of ours, Artisan's Alley Store. Specifically, you will be implementing an add to cart button for products on the home page of the website.

This website is being built out in Laravel, and uses ==Laravel Inertia, Vue 3, Tailwindcss, and Pinia==. This challenge will gauge your adaptability and problem solving skills.
## Requirements

==To complete this feature, the website has to meet the following requirements:==
* An add to cart button must be placed within the image portion of the product card's on the home page
* When clicked, this button will create a line item in the database per the product that was clicked, and update the cart icon in the right of the navbar in the following ways:
    * Update the pinia  `cart` store to include the clicked product, and update the cart count indicator with the count of line items in the cart
    * Show a list of created line items in the popover that appears when you click the icon, or "No items are in your cart." if no line items have been created
    * The count and line items should persist in the icon and popover even if the page is refreshed

Feel free to style this as you please!

## Installation

If you don't already have a local development environment, please refer to https://laravel.com/docs/10.x/installation#main-content.

After you have the project cloned, make sure you have Composer (https://getcomposer.org/), and npm installed on your computer. Then run `composer install` and `npm install` in the cloned project's directory. Next, rename the .env.example file to .env, and update it to have correct `APP_URL` and database name / credentials. Once this is done, generate the app key by running `php artisan key:generate`. Run `php artisan migrate` to run the migration files, and `php artisan app:seed-products` to create the products. Lastly, run `npm run dev` to start the frontend server.

> It's highly recommended to download Vue Devtools to help debug the application from Chrome devtools. This extention can be installed at https://devtools.vuejs.org/.

## Setup

As mentioned above, this challenge uses Laravel, and has two key models. `Product` and `LineItem`. The controllers for these models have already been created, so please use those for the above tasks. On the frontend, there is a Pinia store setup for managing the cart state on the frontend, and axios should be used to handle the requests asynchronously. Frontend components are located in the `resources/js` folder, the main components are the Home, ProductCard, and CartPopup components. The pinia cart store is located in the store directory, `./stores/cart.ts`

> Note: Usually, there would be a Cart entity the LineItem entity is related to, but for this challenge the Cart entity has been omitted.

If you have any questions about the challenge, please email tstacy@elinkdesign.com or jreid@elinkdesign.com. Good luck!

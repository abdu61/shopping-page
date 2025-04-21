# ShopEase: React Shopping Cart Application

A modern, responsive shopping cart application built with React. This project demonstrates routing, component structure, state management, API fetching, and clean, reusable styling.

## Features

*   **Responsive Design:** Fully responsive layout with a focus on modern UI elements and rounded corners (12px radius)
*   **Routing:** Uses `react-router-dom` for navigation between pages
*   **Shopping Cart:** Add items to cart with quantity selection, view in dropdown
*   **Checkout Process:** Complete order flow with form validation and success confirmation
*   **Product Browsing:** View products fetched from FakeStoreAPI
*   **Search & Filter:** Filter products by category and search by keywords
*   **Component Structure:** Organized into reusable, well-documented components
*   **Loading States:** Visual feedback during API requests
*   **Error Handling:** User-friendly error messages and form validation
*   **Clean UI:** Modern design with consistent spacing, typography, and color scheme
*   **Accessibility:** Semantic HTML and appropriate ARIA attributes

## Tech Stack

*   **React:** UI library for building component-based interfaces
*   **React Router DOM:** Navigation and routing
*   **PropTypes:** Runtime type checking for React props
*   **CSS:** Custom styling with variables and responsive design
*   **FakeStoreAPI:** External API for product data
*   **Vitest & React Testing Library:** Testing framework and utilities

## Project Structure

```
shopping-cart/
├── public/
│   └── vite.svg
├── src/
│   ├── assets/
│   │   └── react.svg
│   ├── components/
│   │   ├── NavBar.css
│   │   ├── NavBar.jsx
│   │   ├── NavBar.test.jsx
│   │   ├── ProductCard.css
│   │   ├── ProductCard.jsx
│   │   └── ProductCard.test.jsx
│   ├── pages/
│   │   ├── HomePage.css
│   │   ├── HomePage.jsx
│   │   ├── HomePage.test.jsx
│   │   ├── ShopPage.css
│   │   ├── ShopPage.jsx
│   │   ├── CheckoutPage.css
│   │   ├── CheckoutPage.jsx
│   │   ├── CheckoutSuccessPage.css
│   │   └── CheckoutSuccessPage.jsx
│   ├── App.css           # Global styles and design system
│   ├── App.jsx           # Main application component with state and routing
│   ├── index.css         # Base styles
│   ├── main.jsx          # Entry point with router setup
│   └── setupTests.js     # Test configuration
├── vite.config.js        # Vite + Vitest configuration
├── package.json          # Dependencies and scripts
└── README.md             # This file
```

## Design System

The application uses a consistent design system with:

*   **Color Palette:**
    *   Primary: #4361ee (blue)
    *   Secondary: #4cc9f0 (light blue)
    *   Accent: #f72585 (pink)
    *   Success: #4ade80 (green)
    *   Background, text and border colors for contrast

*   **Typography:**
    *   System font stack for optimal performance and familiarity
    *   Clear hierarchy with weights and colors

*   **Spacing:**
    *   Consistent spacing with CSS variables (xs, sm, md, lg, xl)
    *   Responsive adjustments for different screen sizes

*   **Borders & Shadows:**
    *   Consistent border-radius (12px for most elements)
    *   All transitions use CSS variables for consistency

*   **Responsive Breakpoints:**
    *   Mobile: < 480px
    *   Desktop: > 768px

## Key Components & Logic

*   **`App.jsx`**:
    *   Manages cart state and provides cart functionality (add, remove, update)
    *   Sets up routing with React Router including checkout flow
    *   Calculates cart totals and passes data to child components

*   **`NavBar.jsx`**:
    *   Cart dropdown with item preview and management
    *   Responsive navigation with mobile adaptations
    *   Active link highlighting

*   **`HomePage.jsx`**:
    *   Welcoming landing page with clear call-to-action
    *   Modern, clean design with clear hierarchy

*   **`ShopPage.jsx`**:
    *   Fetches products from FakeStoreAPI
    *   Responsive product grid layout

*   **`CheckoutPage.jsx`**:
    *   Checkout form with validation
    *   Order summary with calculations
    *   Responsive layout for all devices

*   **`CheckoutSuccessPage.jsx`**:
    *   Order confirmation with details
    *   Simulates a successful purchase

*   **`ProductCard.jsx`**:
    *   Displays product details with consistent layout
    *   Hover effects for improved user experience

## Checkout Flow

The application includes a complete checkout flow:

1. **Cart Management:**
   * Add products to cart from the shop page
   * View and manage cart from the dropdown
   * Update quantities or remove items

2. **Checkout Process:**
   * Fill shipping and payment information
   * Form validation ensures correct data entry
   * View order summary with pricing breakdown  

3. **Order Confirmation:**
   * Success page with order details
   * Simulated order number and estimated delivery
   * Options to return home or continue shopping

## Testing

This project uses Vitest and React Testing Library for component and functionality testing.

Test files are co-located with their respective components with a `.test.jsx` extension.

### Testing Strategy

*   **Component Unit Tests:** Verify components render correctly with different props
*   **User Interaction Tests:** Simulate user actions like clicks and input changes
*   **Integration Tests:** Test components working together (like adding to cart)
*   **Mocking:** Mock external resources like API calls
*   **Accessibility:** Basic checks for accessible elements

### Running Tests

```bash
npm test
```

## Getting Started

### Prerequisites

*   Node.js 14.0 or later
*   npm or yarn package manager

### Installation

1. Clone the repository
   ```bash
   git clone <repository-url>
   cd shopping-cart
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Start development server
   ```bash
   npm run dev
   ```

4. Open [http://localhost:5173](http://localhost:5173) in your browser

### Available Scripts

*   `npm run dev` - Start the development server
*   `npm run build` - Build for production
*   `npm run preview` - Preview the production build locally
*   `npm run lint` - Lint the codebase
*   `npm test` - Run tests with Vitest

## Future Improvements

*   Add user authentication and profiles
*   Implement persistence with localStorage or backend
*   Add product details page
*   Add sorting options for products
*   Improve test coverage
*   Add animations for smoother transitions
*   Add payment processing integration (e.g., Stripe)
*   Implement order history and tracking

## Design Decisions

*   **State Management:** Local React state was chosen for simplicity, though Context or Redux could be used for scaling
*   **CSS Approach:** Component-level CSS files for maintainability
*   **API Handling:** Direct fetch calls in components for simplicity
*   **Error Handling:** User-friendly error displays with developer console logs
*   **Responsive Design:** Mobile-first approach with flexible layouts
*   **Checkout Flow:** Simple form with validation for demonstration purposes

## Credits

*   Product data from [FakeStoreAPI](https://fakestoreapi.com/)
*   Icon designs from emoji set
*   Design inspiration from modern e-commerce sites

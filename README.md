# ShareBite
Description

ShareBite is a collaborative meal-sharing platform that connects food lovers, home cooks, and community members. Our app allows users to share homemade meals, discover local culinary talents, reduce food waste, and build meaningful connections through shared dining experiences.

## Key Features
- Create and list homemade meals
- Browse nearby meal offerings
- Book and order meals from local cooks
- Rate and review meal experiences
- Secure payment integration
- Dietary preference and allergen filtering

## Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v18.0.0 or later)
- npm (v9.0.0 or later)
- MongoDB (v5.0 or later)
- Git

### Required Accounts
- Stripe Account (for payment processing)
- Google Maps API Key (for location services)
- Firebase Authentication

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/share-bite.git
cd share-bite
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure Environment Variables
Create a `.env` file in the root directory with the following variables:
```
MONGODB_URI=your_mongodb_connection_string
STRIPE_SECRET_KEY=your_stripe_secret_key
GOOGLE_MAPS_API_KEY=your_google_maps_api_key
JWT_SECRET=your_jwt_secret
```

### 4. Database Setup
```bash
npm run db:migrate
npm run db:seed
```

### 5. Run the Application
```bash
# Development mode
npm run dev

# Production build
npm run build
npm start
```

## Usage Examples

### Creating a Meal Listing
```javascript
const newMeal = {
  title: 'Homemade Lasagna',
  description: 'Authentic Italian lasagna with beef and bechamel sauce',
  price: 12.99,
  servings: 4,
  dietaryRestrictions: ['vegetarian', 'halal'],
  availableDate:

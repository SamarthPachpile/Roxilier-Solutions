# MERN Stack Coding Challenge

This project implements a MERN stack-based application for handling product transactions, including a set of APIs and a frontend interface. The application fetches data from a third-party API and provides features for transaction listing, statistics, bar chart, and pie chart visualization based on product categories.

## Features

### Backend
The backend exposes several APIs:

1. **Initialize Database**: Fetches data from a third-party API and seeds the database.
   - API: `GET /api/init-db`
   
2. **Transaction Listing API**:
   - Fetches and lists all product transactions.
   - Supports search and pagination on product title, description, and price.
   - API: `GET /api/transactions?month=<month>&search=<query>&page=<page>&perPage=<limit>`

3. **Statistics API**:
   - Provides the total sale amount, total sold items, and total unsold items for a selected month.
   - API: `GET /api/statistics?month=<month>`

4. **Bar Chart API**:
   - Returns the number of items sold in specific price ranges for a selected month.
   - API: `GET /api/bar-chart?month=<month>`

5. **Pie Chart API**:
   - Provides unique categories and the number of items in each category for a selected month.
   - API: `GET /api/pie-chart?month=<month>`

6. **Combined Data API**:
   - Combines and fetches the data from all the above APIs and returns a unified JSON response.
   - API: `GET /api/combined-data?month=<month>`

### Frontend
The frontend consumes these APIs and presents the following features:

1. **Transaction Table**:
   - Displays a list of transactions with search and pagination functionalities.
   - Allows filtering by month (January - December) and searching by product details.
   
2. **Transaction Statistics**:
   - Displays the total sale amount, number of sold items, and unsold items for the selected month.

3. **Bar Chart**:
   - Shows the distribution of items across price ranges.

4. **Pie Chart**:
   - Displays the count of items in different product categories.

## How to Run the Project

### Prerequisites
- Node.js
- MongoDB

### Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/mern-coding-challenge.git
   ```

2. Navigate to the project directory:
   ```bash
   cd mern-coding-challenge
   ```

3. Install backend dependencies:
   ```bash
   npm install
   ```

4. Set up environment variables:
   - Create a `.env` file and add the required configurations, such as MongoDB URI and API keys.

5. Start the backend server:
   ```bash
   npm start
   ```

6. In a separate terminal, navigate to the `client` folder and install frontend dependencies:
   ```bash
   cd client
   npm install
   ```

7. Start the frontend server:
   ```bash
   npm start
   ```

### API Documentation
- API documentation is available [here](link_to_documentation) or by running the server and navigating to `/api-docs`.

## Mockup and Design
The project follows the mockups provided in the challenge with custom design improvements.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

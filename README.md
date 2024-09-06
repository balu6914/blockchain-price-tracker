# Blockchain Price Tracker

   This project is a **Blockchain Price Tracker** built using Nest.js, which tracks the prices of Ethereum and Polygon. The     project provides features such as automatic price fetching, email alerts, and APIs for price tracking.

Features:
   - Automatically save the price of **Ethereum and Polygon** every 5 minutes.
   - Send an email alert if the price of a chain increases by more than 3% compared to its price an hour ago.
   - API for retrieving hourly prices for the last 24 hours.
   - API for setting price alerts for specific prices (e.g., alert when Ethereum hits $1000).
   - No user authentication required.
   - Full Swagger API documentation.
   - Dockerized for easy setup and deployment.

Tech Stack :
   - **Nest.js** (Node.js framework)
   - **PostgreSQL** (RDB)
   - **Moralis or Solscan API** (for fetching prices)
   - **Nodemailer** (for sending email alerts)
   - **Swagger** (for API documentation)
   - **Docker** (for containerization)

Setup Instructions:

   Prerequisites
     - Docker
     - Node.js and npm

Clone the Repository:
   
     git clone <repository-url>
     cd blockchain-price-tracker

Install Dependencies
   
   npm install
   
 Docker Setup
   Make sure you have Docker installed on your system. Then, run the following command to build and run the project:

   docker compose up --build

   This will:
     - Set up a PostgreSQL database
     - Run the Nest.js service

  API Endpoints:
       - **GET /prices**: Retrieve prices for the last 24 hours.
       - **POST /set-alert**: Set a price alert. Parameters:
         - `chain`: Ethereum or Polygon
         - `dollar`: Price to set the alert
         - `email`: Email to receive the alert

   Environment Variables
   - `MORALIS_API_KEY` or `SOLSCAN_API_KEY`: Your API key for fetching prices.
   - `SMTP_USER`, `SMTP_PASS`: SMTP credentials for sending emails.

   ## License
   This project is licensed under the MIT License.
   ```

# Block Stone Company Management Web App

A web application for managing inventory, production, and sales for a block stone manufacturing company.

## Features

- Worker management
- Daily production tracking (cement packets used)
- Automatic stock calculation based on stone production rates
- Sales recording with stock updates
- Summary dashboard showing total packets used, payments, and sales

## Stone Types

- **Type 1**: 13x3.75x6.5 inch stones - 176 stones per cement packet
- **Type 2**: 7x14x4 inch stones - 144 stones per cement packet

## Payment

- 1100/= per cement packet used

## Quick Start

1. Run the backend: Double-click `run_backend.bat`
2. Run the frontend: Double-click `run_frontend.bat` (in a new terminal)
3. Open http://localhost:5173 in your browser

## Manual Setup

### Backend

1. Navigate to the backend directory:
   ```
   cd block_stone_app/backend
   ```

2. Install dependencies:
   ```
   pip install fastapi uvicorn sqlalchemy pydantic
   ```

3. Run the backend server:
   ```
   python -m uvicorn main:app --reload
   ```

### Frontend

1. Navigate to the frontend directory:
   ```
   cd block_stone_app/frontend
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Run the development server:
   ```
   npm run dev
   ```

## Usage

1. Add workers to the system
2. Record daily production by selecting worker, stone type, and packets used
3. Stock is automatically updated based on production
4. Record sales to deduct from stock
5. View current stock levels and summary statistics

## API Endpoints

- `POST /workers/` - Add a new worker
- `GET /workers/` - Get all workers
- `POST /production/` - Add production record
- `POST /sales/` - Record a sale
- `GET /stocks/` - Get current stock levels
- `GET /summary/` - Get summary statistics
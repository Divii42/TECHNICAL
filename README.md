# FoodExpress – Full Stack Food Delivery (Experiments 1 to 6)

| Folder | What it is | Experiments |
|---|---|---|
| `food-frontend/` | Bootstrap + JavaScript website | 1 and 5 |
| `react-app/` | React login, register, dashboard | 2 and 6 |
| `backend/` | Node.js + Express + MySQL REST API with JWT | 3 and 4 |

## Run order (PowerShell)
1. Backend: `cd backend`, `npm install`, copy `.env.example` to `.env` and fill it, `npm run setup`, `npm start`
2. Website: open http://localhost:5000/food/
3. React app: `cd react-app`, `npm install`, `npm run dev`, open http://localhost:5173
4. Test API: with the backend running, `cd backend` then `npm test`

## Main API routes
- `GET/POST /api/restaurants`, `GET/PUT/DELETE /api/restaurants/:id`
- `GET/POST /api/menu`, `GET/PUT/DELETE /api/menu/:id`  (filters: category, cuisine, minPrice, maxPrice, search, restaurantId)
- `GET /api/cart/:sessionId`, `POST /api/cart/:sessionId`, `PUT/DELETE /api/cart/:sessionId/:menuItemId`, `DELETE /api/cart/:sessionId`
- `POST /api/auth/register`, `POST /api/auth/login`, `GET/PUT /api/auth/me` (JWT)
- `POST /api/orders`, `GET /api/orders` (JWT)

Experiment 1 mode (no server): set `USE_BACKEND = false` in `food-frontend/js/store.js` and open `food-frontend/index.html`.

# Meal Match Backend (Flask + MySQL)

Quick start (Windows PowerShell):

1. Create DB and tables
   - Create database `mealmatch` in MySQL
   - Run `schema.sql` in that database

2. Create and activate venv
```
python -m venv .venv
.venv\Scripts\Activate.ps1
```

3. Install deps
```
pip install -r requirements.txt
```

4. Configure env (optional)
   - Copy `.env.example` to `.env` and fill values (or rely on defaults)

5. Run server
```
python app.py
```

API summary
- POST /api/auth/register (multipart form: name, email, password, role, photo)
- POST /api/auth/login (json: email, password)
- POST /api/auth/logout
- GET  /api/auth/me
- GET  /api/profile
- PUT  /api/profile (multipart form: name?, password?, photo?)
- POST /api/owner/restaurants (json: name, area, cuisine, price_level, image_url)
- GET  /api/restaurants (q, area, cuisine, price)
- GET  /api/menu/<restaurant_id>
- GET  /api/orders
- POST /api/orders (json: restaurant_id, items: [{menu_item_id, quantity}])







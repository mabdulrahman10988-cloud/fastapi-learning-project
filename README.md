# FastAPI Learning Project

This is a small project I built while learning **FastAPI**. It covers the basics of building an API, working with **Pydantic** for data validation, and doing full **CRUD** operations.

## What's inside

- **`main.py`** — Patient Management API. Stores patient records in a JSON file and supports:
  - `GET /view` — see all patients
  - `GET /patient/{id}` — get one patient
  - `GET /sort` — sort patients by height, weight, or BMI
  - `POST /create` — add a new patient
  - `PUT /edit/{id}` — update a patient
  - `DELETE /delete/{id}` — remove a patient

  BMI and health verdict (Underweight / Normal / Obese) are calculated automatically using Pydantic's `computed_field`.

- **`app.py`** — Insurance Premium Category Predictor API. Takes in basic user details (age, height, weight, income, smoker status, city, occupation) and returns a predicted premium category using a trained ML model (`model.pkl`).

- **`frontend.py`** — A simple Streamlit form that calls the `/predict` endpoint from `app.py`, so you can test the model through a UI instead of Swagger docs.

## What I learned

- Building REST APIs with FastAPI (GET, POST, PUT, DELETE)
- Data validation with Pydantic (`Field`, `Literal`, `Annotated`)
- Auto-generating computed fields (BMI, age group, lifestyle risk, city tier)
- Reading/writing a JSON file as a mini database
- Serving a pre-trained ML model through an API endpoint
- Testing endpoints with FastAPI's built-in `/docs` (Swagger UI)



# Real-Time Analytics Dashboard Simulator

Full-stack dashboard simulator with:

- React + Vite frontend
- FastAPI gateway
- Spring Boot core service
- MongoDB persistence

## Project Structure

- `frontend/` - React dashboard UI
- `backend/gateway/` - FastAPI gateway service
- `backend/coreservice/coreservices/` - Spring Boot service

## Frontend

```bash
cd frontend
npm install
npm run dev
```

Default frontend URL: `http://127.0.0.1:5174`

## Spring Boot Core Service

```bash
cd backend/coreservice/coreservices
mvn spring-boot:run
```

Important environment variables:

- `SERVER_PORT` - defaults to `8000`
- `MONGODB_URI` - defaults to `mongodb://localhost:27017/Dashboard`
- `MONGODB_DATABASE` - defaults to `Dashboard`
- `JWT_SECRET` - defaults to a local development value

For MongoDB Atlas, set `MONGODB_URI` in your environment instead of committing credentials.

## FastAPI Gateway

```bash
cd backend/gateway
pip install -r requirements.txt
uvicorn main:app --host 127.0.0.1 --port 9000
```

Set `SPRING_URL` if Spring Boot is not running on `http://127.0.0.1:8000`.

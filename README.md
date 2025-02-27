# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh


# Product Management Application

A full-stack web application for product management built with Laravel, React, and Docker.

## Features

- 🔐 Secure Authentication with Laravel Sanctum
- 📦 Product CRUD Operations
- 🚀 Real-time Form Validation
- 🎨 Modern UI with Tailwind CSS
- 🔄 State Management with React Context
- 🐳 Docker Containerization
- 🔒 Role-based Authorization
- ⚡ Fast API Response Times

## Tech Stack

### Backend
- Laravel 10.x
- PHP 8.2
- MySQL/PostgreSQL
- Laravel Sanctum for Authentication
- PHPUnit for Testing

### Frontend
- React 18
- Vite
- Tailwind CSS
- React Router v6
- React Hook Form
- React Hot Toast

### DevOps
- Docker & Docker Compose
- Nginx
- GitHub Actions (CI/CD)
- Heroku Deployment

## Local Development Setup

### Prerequisites
- Docker and Docker Compose
- Git
- Node.js 18+ (for local frontend development)
- PHP 8.2+ (for local backend development)

### Installation Steps

1. Clone the repository with submodules:

### Installation Steps

1. Clone the repository with submodules:

```bash
git clone --recursive https://github.com/yourusername/product-app-meta.git
cd product-app-meta
```

2. Copy environment files:

```bash
cp backend/.env.example backend/.env
cp frontend/.env.example frontend/.env
```

3. Build and start Docker containers:

```bash
docker-compose up -d
```


4. Install backend dependencies:

```bash
docker-compose exec backend composer install
docker-compose exec backend php artisan key:generate
docker-compose exec backend php artisan migrate --seed
```


5. Install frontend dependencies:

```bash
docker-compose exec frontend npm install
```


6. Access the application:
- Frontend: http://localhost:5173
- Backend API: http://localhost:8000
- API Documentation: http://localhost:8000/api/documentation

### Default Users
- Admin: admin@example.com / password
- User: user@example.com / password

### API Documentation
- Swagger UI: http://localhost:8000/api/documentation

## Code Structure

### Backend Structure

backend/
├── app/
│ ├── Http/Controllers/ # Request handlers
│ ├── Models/ # Eloquent models
│ └── Services/ # Business logic
├── database/
│ ├── migrations/ # Database structure
│ └── seeders/ # Sample data
└── routes/
└── api.php # API endpoints

### Frontend Structure

frontend/
├── src/
│ ├── components/ # Reusable UI components
│ ├── context/ # React Context providers
│ ├── pages/ # Route components
│ └── services/ # API integration

## Security Features

- CSRF Protection
- XSS Prevention
- SQL Injection Protection
- Input Validation
- Secure Authentication with Sanctum
- Rate Limiting
- CORS Configuration

## Best Practices

- RESTful API Design
- Repository Pattern
- Form Validation
- Error Handling
- Responsive Design
- Code Documentation
- Type Safety
- Testing

## Performance Optimizations

- Database Query Optimization
- API Response Caching
- Lazy Loading
- Code Splitting
- Asset Optimization

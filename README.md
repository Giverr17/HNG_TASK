# Gender Classify API

A Laravel API that classifies names by gender using the Genderize.io API.

## Live Endpoint
https://your-url.up.railway.app/api/classify

## Usage

### Request
GET /api/classify?name={name}

### Success Response example (200)
{
  "status": "success",
  "data": {
    "name": "Little",
    "gender": "Female",
    "probability": 0.99,
    "sample_size": 1234,
    "is_confident": true,
    "processed_at": "2026-04-01T12:00:00Z"
  }
}

### Error Responses
- 400: Missing name parameter
- 422: Invalid name or no prediction available
- 502: External API failure

## Tech Stack
- PHP 8.5
- Laravel 13
- Genderize.io API

## Run Locally
composer install
cp .env.example .env
php artisan key:generate
php artisan serve
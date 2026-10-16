# API-контракты — ShelfShare (черновик)

Базовый URL: `https://localhost:5001/api` (или другой после деплоя)

## 1. Bookcases (Шкафчики)

### GET /api/bookcases
Получить список всех шкафчиков

**Ответ:**
```json
[
  {
    "id": 1,
    "title": "Шкафчик на Ленина",
    "address": "ул. Ленина, 15",
    "latitude": 55.75,
    "longitude": 37.61,
    "isActive": true
  }
]

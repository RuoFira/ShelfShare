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
2. Books & BookCopies
GET /api/bookcases/{id}/books
Получить все книги в конкретном шкафчике
POST /api/bookcopies
Добавить книгу в шкафчик
Тело запроса:
{
  "bookId": 5,
  "bookcaseId": 2,
  "condition": "Good"
}
POST /api/bookcopies/{id}/take
Забрать книгу из шкафчика

3. Reviews
GET /api/books/{id}/reviews
Получить отзывы на книгу
POST /api/reviews
Оставить отзыв

4. Wishlist
GET /api/wishlist
Получить свой список желаний
POST /api/wishlist
Добавить книгу в wishlist
DELETE /api/wishlist/{id}
Удалить из wishlist

5. Reports (Жалобы)
POST /api/reports
Создать жалобу
GET /api/reports
Получить список жалоб (только модератор)

6. Auth
POST /api/auth/register
Регистрация
POST /api/auth/login
Вход (возвращает JWT-токен)

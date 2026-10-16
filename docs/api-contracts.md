# API-контракты — ShelfShare (черновик)

Базовый URL: `https://localhost:5001/api`

## 1. Bookcases (Шкафчики)

- `GET /api/bookcases` — получить список всех шкафчиков
- `GET /api/bookcases/{id}` — получить один шкафчик + книги в нём
- `POST /api/bookcases` — создать новый шкафчик
- `PUT /api/bookcases/{id}` — обновить шкафчик
- `DELETE /api/bookcases/{id}` — деактивировать шкафчик

## 2. Books & BookCopies

- `GET /api/bookcases/{id}/books` — получить все книги в шкафчике
- `POST /api/bookcopies` — добавить книгу в шкафчик
- `POST /api/bookcopies/{id}/take` — забрать книгу из шкафчика

## 3. Reviews

- `GET /api/books/{id}/reviews` — получить отзывы на книгу
- `POST /api/reviews` — оставить отзыв

## 4. Wishlist

- `GET /api/wishlist` — получить свой список желаний
- `POST /api/wishlist` — добавить книгу в wishlist
- `DELETE /api/wishlist/{id}` — удалить из wishlist

## 5. Reports (Жалобы)

- `POST /api/reports` — создать жалобу
- `GET /api/reports` — получить список жалоб (только модератор)

## 6. Auth

- `POST /api/auth/register` — регистрация
- `POST /api/auth/login` — вход (возвращает JWT-токен)

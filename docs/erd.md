# ERD — Принципиальная диаграмма сущностей ShelfShare

## Список сущностей и связи

### Основные сущности

**User**  
- Имеет много Bookcase (создаёт шкафчики)
- Имеет много BookCopy (добавляет книги)
- Имеет много Review
- Имеет много WishlistItem
- Имеет много Report
- Имеет много Notification
- Имеет много ModerationLog (если модератор)

**Bookcase**  
- Принадлежит User (CreatedBy)
- Содержит много BookCopy
- Имеет много Photo
- Привязан к District

**Book**  
- Имеет много BookCopy
- Имеет много Review
- Имеет много WishlistItem

**BookCopy**  
- Принадлежит Book
- Находится в Bookcase
- Имеет много BookMovement
- Может иметь Photo
- Может иметь Report

**BookMovement**  
- Связан с BookCopy
- Связан с User (кто переместил)
- Связан с Bookcase (откуда и куда)

**Review**  
- Связан с User и Book

**WishlistItem**  
- Связан с User и Book

**Report**  
- Связан с User
- Может быть привязан к BookCopy или Bookcase

**Photo**  
- Связан с Bookcase или BookCopy
- Связан с User

**Notification**  
- Принадлежит User

**District**  
- Содержит много Bookcase

**ModerationLog**  
- Связан с User (модератор)

## Примечание

Полную графическую ERD-диаграмму можно нарисовать в:
- draw.io
- dbdiagram.io
- Figma
- Lucidchart

Пока достаточно этого текстового описания связей.

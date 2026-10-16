# Сущности проекта ShelfShare

## Список сущностей (12 штук)

### 1. User (Пользователь)
- Id
- Username
- Email
- PasswordHash
- Role (User / Moderator / Admin)
- CreatedAt

### 2. Bookcase (Книжный шкафчик)
- Id
- Title (название)
- Description
- Address
- Latitude
- Longitude
- IsActive
- CreatedAt
- CreatedByUserId

### 3. Book (Книга — справочник)
- Id
- Title
- Author
- ISBN (необязательно)
- Description
- CoverImageUrl
- PublicationYear

### 4. BookCopy (Экземпляр книги)
- Id
- BookId
- BookcaseId (где сейчас находится)
- Condition (состояние: Good / Average / Bad)
- AddedAt
- AddedByUserId

### 5. BookMovement (История перемещений)
- Id
- BookCopyId
- FromBookcaseId
- ToBookcaseId
- UserId (кто переместил)
- MovedAt
- Type (Added / Taken / Moved)

### 6. Review (Отзыв)
- Id
- BookId
- UserId
- Rating (1-5)
- Comment
- CreatedAt

### 7. WishlistItem (Список желаний)
- Id
- UserId
- BookId
- CreatedAt

### 8. Report (Жалоба)
- Id
- UserId (кто пожаловался)
- BookCopyId (или BookcaseId)
- Reason
- Description
- Status (New / InProgress / Resolved)
- CreatedAt

### 9. Photo
- Id
- BookcaseId (или BookCopyId)
- Url
- UploadedByUserId
- UploadedAt

### 10. Notification
- Id
- UserId
- Title
- Message
- IsRead
- CreatedAt

### 11. District (Район)
- Id
- Name
- City

### 12. ModerationLog
- Id
- ModeratorId
- Action
- TargetType
- TargetId
- CreatedAt

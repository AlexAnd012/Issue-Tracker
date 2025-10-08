# Issue Tracker 

**Цель:** показать умение проектировать, реализовывать и документировать backend-сервис на Go  (аутентификация, CRUD, REST API, БД, JWT, CI/CD, тесты, Docker).

--- 

## Стек технологий

| Категория | Технология |
|------------|-------------|
| Язык | Go 1.22+ |
| HTTP | Gin |
| База данных | PostgreSQL |
| ORM / SQL | GORM (или sqlc) |
| Миграции | golang-migrate |
| Аутентификация | JWT (github.com/golang-jwt/jwt/v5) |
| Конфигурация | ENV + godotenv |
| Логирование | zap/logrus |
| Метрики | Prometheus `/metrics` |
| Документация | Swagger (swaggo/gin-swagger) |
| Контейнеризация | Docker, docker-compose |
| CI/CD | GitHub Actions |
| Тесты | testify + Testcontainers |

---

##  Архитектура проекта
/cmd/api # main.go
/internal/config # загрузка env и конфигов
/internal/models # модели ORM
/internal/http/
handlers # REST-хэндлеры
middleware # JWT, recover, request-id
/internal/domain # бизнес-логика (usecases)
/internal/repo # работа с БД (gorm/sqlc)
internal/db # подключение PostgreSQL
/migrations # SQL миграции
/api/openapi.yaml # Swagger/OpenAPI



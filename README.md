# Crypto Exchange

## Описание
Crypto Exchange - это приложение для торговли криптовалютами в реальном времени с использованием многопоточности для обработки данных.

## Структура проекта
Проект разделен на несколько слоев для улучшения читаемости и поддерживаемости кода:

- **Domain**: Основная бизнес-логика и правила.
- **Application**: Интерфейсы, юзкейсы и реализации для работы с данными.
- **Infrastructure**: Реализация деталей инфраструктуры, таких как модели данных, контроллеры и утилиты.
- **Presentation**: Визуализация данных и взаимодействие с пользователем.

## Установка
1. Клонируйте репозиторий:
    ```bash
    git clone <URL репозитария>
    ```
2. Перейдите в каталог проекта:
    ```bash
    cd crypto_exchange
    ```
3. Скомпилируйте проект:
    ```bash
    g++ -std=c++11 main.cpp -o crypto_exchange
    ```

## Запуск
Для запуска проекта выполните команду:
```bash
./crypto_exchange
```

## Структура каталогов
```plaintext
crypto_exchange/
├── domain/
│   ├── entities/
│   │   └── Order.h
│   │   └── User.h
│   ├── services/
│   │   └── OrderService.h
│   │   └── UserService.h
│   └── repositories/
│       └── OrderRepository.h
│       └── UserRepository.h
├── application/
│   └── usecases/
│       └── CreateOrder.h
│       └── CreateUser.h
├── infrastructure/
│   ├── models/
│   │   └── OrderModel.h
│   │   └── UserModel.h
│   ├── controllers/
│   │   └── OrderController.h
│   │   └── UserController.h
│   ├── views/
│       └── OrderView.h
│   └── utils/
│       └── ThreadPool.h
└── main.cpp
```

## Описание компонентов
### Domain
- **Order.h**: Класс сущности ордера.
- **User.h**: Класс сущности пользователя.

### Application
- **CreateOrder.h**: Юзкейс для создания ордера.
- **CreateUser.h**: Юзкейс для создания пользователя.

### Infrastructure
- **OrderModel.h**: Модель данных ордера.
- **UserModel.h**: Модель данных пользователя.
- **OrderController.h**: Контроллер для ордеров.
- **UserController.h**: Контроллер для пользователей.
- **ThreadPool.h**: Утилита для управления потоками.

### Presentation
- **OrderView.h**: Представление для ордеров.

## Лицензия
Этот проект лицензирован под лицензией MIT. Для получения дополнительной информации см. файл LICENSE.

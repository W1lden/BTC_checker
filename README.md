# 📊 Крипто-трекер на Docker Compose

Этот проект отслеживает цену пары BTC/USDT с Binance и отображает её график в реальном времени. Состоит из двух микросервисов на Python (checker и plot), MongoDB для хранения и mongo-express для визуального доступа к данным.

---

## 🧱 Стек технологий

- Python 3.10
- Flask
- MongoDB + mongo-express
- Docker + Docker Compose
- Chart.js

---

## 🗂 Структура проекта

```
train_compose/
├── checker/              # Сервис, получающий цену BTC/USDT и записывающий в MongoDB
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
├── plot/                 # Веб-интерфейс на Flask для отображения графика
│   ├── app.py
│   ├── requirements.txt
│   ├── Dockerfile
│   └── templates/
│       └── index.html
├── docker-compose.yml
├── .env
└── README.md
```

---

## 🚀 Запуск проекта

1. Клонируйте репозиторий:
```bash
git clone https://github.com/W1lden/BTC_checker.git
cd BTC_checker/train_compose
```

2. Создайте файл `.env`. Вот пример:
```env 
MONGO_INITDB_ROOT_USERNAME=root
MONGO_INITDB_ROOT_PASSWORD=example
MONGO_PORT=27017
MONGO_CONTAINER_NAME=mymongo
MONGO_EXPRESS_PORT=8081
PLOT_EXTERNAL_PORT=5050
```

3. Соберите и запустите контейнеры:
```bash
docker-compose up --build
```

---

## 🌐 Интерфейсы

- Mongo Express: [http://localhost:8081](http://localhost:8081)
- Веб-интерфейс (Plot): [http://localhost:5050](http://localhost:5050)

---

## 👤 Автор

[W1lden (GitHub)](https://github.com/W1lden)
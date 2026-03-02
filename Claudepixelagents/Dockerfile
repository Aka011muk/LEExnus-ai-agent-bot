# Используем официальный образ Python
FROM python:3.11-slim

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем файлы зависимостей
COPY requirements.txt .

# Устанавливаем зависимости
RUN pip install --no-cache-dir -r requirements.txt

# Копируем весь проект (код, генераторы, шаблоны)
COPY . .

# Создаем папку для генерации ботов и даем права доступа
RUN mkdir -p generated_bots && chmod 777 generated_bots

# Запускаем твоего мастер-бота
CMD ["python", "simple_hybrid_bot.py"]

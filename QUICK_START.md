# Быстрый старт

## 🚀 Запуск проекта

### 1. Локальный запуск
```bash
python server.py
```
Откройте: `http://localhost:8000/Index_standalone.html`

### 2. Загрузка на GitHub

1. **Создайте репозиторий на GitHub**
2. **Загрузите файлы:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: CDEK Analytics Dashboard"
   git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
   git push -u origin main
   ```
3. **Включите GitHub Pages:**
   - Settings → Pages → Source: Deploy from branch → main → Save

### 3. Доступ к сайту
Ваш сайт будет доступен по адресу:
`https://YOUR_USERNAME.github.io/REPO_NAME/Index_standalone.html`

## 📁 Структура проекта
```
├── Index_standalone.html  # Основное приложение
├── data.json             # Данные для анализа
├── server.py            # Локальный сервер
├── README.md            # Документация
├── DEPLOYMENT.md        # Инструкции по развертыванию
└── package.json         # Метаданные проекта
```

## ⚡ Что дальше?
- Прочитайте [README.md](README.md) для подробной информации
- Следуйте [DEPLOYMENT.md](DEPLOYMENT.md) для развертывания
- Настройте данные в `data.json` под ваши нужды

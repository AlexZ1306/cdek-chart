# Инструкции по развертыванию

## Развертывание на GitHub Pages

### 1. Создание репозитория на GitHub

1. Перейдите на [GitHub](https://github.com) и войдите в свой аккаунт
2. Нажмите кнопку "New repository" или "+" → "New repository"
3. Заполните поля:
   - **Repository name**: `cdek-analytics-dashboard` (или любое другое название)
   - **Description**: `Интерактивная аналитическая панель для анализа данных CDEK`
   - Выберите **Public** (для бесплатного GitHub Pages)
   - НЕ добавляйте README, .gitignore или лицензию (они уже созданы)
4. Нажмите "Create repository"

### 2. Загрузка файлов в репозиторий

#### Вариант A: Через командную строку (рекомендуется)

```bash
# Инициализация Git репозитория
git init

# Добавление всех файлов
git add .

# Первый коммит
git commit -m "Initial commit: CDEK Analytics Dashboard"

# Добавление удаленного репозитория (замените YOUR_USERNAME на ваш GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/cdek-analytics-dashboard.git

# Отправка файлов на GitHub
git push -u origin main
```

#### Вариант B: Через веб-интерфейс GitHub

1. На странице созданного репозитория нажмите "uploading an existing file"
2. Перетащите все файлы из папки проекта:
   - `Index_standalone.html`
   - `data.json`
   - `server.py`
   - `package.json`
   - `README.md`
   - `.gitignore`
3. Добавьте commit message: "Initial commit: CDEK Analytics Dashboard"
4. Нажмите "Commit changes"

### 3. Настройка GitHub Pages

1. В репозитории перейдите в **Settings** (вкладка в верхнем меню)
2. Прокрутите вниз до раздела **Pages** в левом меню
3. В разделе **Source** выберите:
   - **Deploy from a branch**: `main`
   - **Folder**: `/ (root)`
4. Нажмите **Save**
5. GitHub автоматически начнет развертывание

### 4. Доступ к сайту

- Ваш сайт будет доступен по адресу: `https://YOUR_USERNAME.github.io/cdek-analytics-dashboard/Index_standalone.html`
- Процесс развертывания может занять несколько минут
- Статус развертывания можно отслеживать во вкладке **Actions**

## Локальное тестирование

Перед загрузкой на GitHub рекомендуется протестировать проект локально:

```bash
# Запуск локального сервера
python server.py

# Или альтернативный способ
python -m http.server 8000
```

Затем откройте `http://localhost:8000/Index_standalone.html` в браузере.

## Обновление сайта

Для обновления сайта после внесения изменений:

```bash
# Добавление изменений
git add .

# Коммит изменений
git commit -m "Описание изменений"

# Отправка на GitHub
git push origin main
```

GitHub Pages автоматически обновит сайт в течение нескольких минут.

## Возможные проблемы

### Проблема с CORS
Если возникают проблемы с загрузкой данных, убедитесь, что:
- Файл `data.json` находится в корне репозитория
- Используется HTTPS (GitHub Pages автоматически предоставляет HTTPS)

### Проблема с путями
Убедитесь, что все ссылки на файлы используют относительные пути, а не абсолютные.

## Дополнительные настройки

### Кастомный домен
Если у вас есть собственный домен, вы можете настроить его в разделе **Pages** → **Custom domain**.

### HTTPS
GitHub Pages автоматически предоставляет HTTPS сертификат. Убедитесь, что опция "Enforce HTTPS" включена в настройках Pages.

# 🚀 Руководство по настройке GitLab для проекта

## 📋 Что уже сделано

✅ Git репозиторий инициализирован  
✅ Создан .gitignore файл  
✅ Настроена конфигурация Git  
✅ Ветка переименована в `main`  
✅ Первый коммит создан  

## 🔗 Подключение к GitLab

### 1. **Создание репозитория на GitLab**

1. Зайдите на [gitlab.com](https://gitlab.com) (или ваш корпоративный GitLab)
2. Нажмите **"New Project"** или **"Создать проект"**
3. Выберите **"Create blank project"** (Создать пустой проект)
4. Заполните форму:
   - **Project name**: `flask-dating-app`
   - **Description**: `Flask dating application with chat functionality`
   - **Visibility Level**: Выберите Private или Public
5. Нажмите **"Create project"**

### 2. **Подключение локального репозитория к GitLab**

После создания проекта GitLab покажет команды. Выполните их:

```bash
# Добавить удаленный репозиторий
git remote add origin https://gitlab.com/YOUR_USERNAME/flask-dating-app.git

# Отправить код на GitLab
git push -u origin main
```

### 3. **Настройка SSH ключей (рекомендуется)**

Для удобной работы без ввода пароля:

```bash
# Генерация SSH ключа
ssh-keygen -t ed25519 -C "your_email@example.com"

# Показать публичный ключ
cat ~/.ssh/id_ed25519.pub
```

Затем добавьте этот ключ в GitLab:
1. Перейдите в **Settings** → **SSH Keys**
2. Вставьте публичный ключ
3. Нажмите **"Add key"**

После этого используйте SSH URL:
```bash
git remote set-url origin git@gitlab.com:YOUR_USERNAME/flask-dating-app.git
```

## 🔄 Работа с Git в PyCharm

### **Настройка PyCharm**

1. Откройте проект в PyCharm
2. Перейдите в **VCS** → **Enable Version Control Integration**
3. Выберите **Git**
4. Нажмите **OK**

### **Коммит и пуш изменений**

1. **Просмотр изменений**: 
   - Откройте **Git** панель (Alt+9)
   - Просмотрите измененные файлы

2. **Добавление файлов**:
   - Правый клик на файл → **Git** → **Add**
   - Или в панели Git нажмите **+** рядом с файлом

3. **Создание коммита**:
   - Нажмите **Ctrl+K** (или **Cmd+K** на Mac)
   - Напишите сообщение коммита
   - Нажмите **Commit**

4. **Отправка на GitLab**:
   - Нажмите **Ctrl+Shift+K** (или **Cmd+Shift+K** на Mac)
   - Выберите **Push**
   - Нажмите **OK**

### **Получение изменений**

1. **Pull изменений**:
   - Нажмите **Ctrl+T** (или **Cmd+T** на Mac)
   - Выберите **Pull**
   - Нажмите **OK**

## 📝 Примеры коммитов

```bash
# Новые функции
git commit -m "feat: add chat message sending functionality"

# Исправления багов
git commit -m "fix: resolve Socket.IO connection issues"

# Улучшения
git commit -m "improve: enhance user interface alignment"

# Документация
git commit -m "docs: update deployment guide"

# Рефакторинг
git commit -m "refactor: clean up database queries"
```

## 🔧 Полезные команды Git

```bash
# Проверить статус
git status

# Посмотреть историю коммитов
git log --oneline

# Создать новую ветку
git checkout -b feature/new-feature

# Переключиться на ветку
git checkout main

# Объединить ветки
git merge feature/new-feature

# Удалить ветку
git branch -d feature/new-feature
```

## 🚨 Важные моменты

### **Что НЕ коммитится** (уже в .gitignore):
- База данных (`*.db`, `*.sqlite`)
- Виртуальное окружение (`venv/`)
- Загруженные файлы (`static/uploads/*`)
- Логи (`*.log`)
- Конфиденциальные данные (`.env`)

### **Что коммитится**:
- Исходный код (`*.py`)
- HTML шаблоны
- CSS/JS файлы
- Конфигурационные файлы
- Документация
- Requirements.txt

## 🎯 Следующие шаги

1. **Создайте репозиторий на GitLab**
2. **Подключите локальный репозиторий**
3. **Отправьте первый коммит**
4. **Настройте PyCharm для работы с Git**
5. **Начните регулярно коммитить изменения**

## 📞 Поддержка

Если возникнут проблемы:
1. Проверьте настройки Git: `git config --list`
2. Убедитесь, что SSH ключи настроены правильно
3. Проверьте права доступа к репозиторию на GitLab
4. Обратитесь к документации GitLab или Git

---

**Удачи с вашим проектом! 🎉** 
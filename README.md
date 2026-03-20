# Aether Browser

<div align="center">

![Aether](https://img.shields.io/badge/Aether-Browser-6366f1?style=for-the-badge&logo=firefox&logoColor=white)
![Electron](https://img.shields.io/badge/Electron-33.0.0-47848F?style=flat-square&logo=electron&logoColor=white)
![Svelte](https://img.shields.io/badge/Svelte-5.14-FF3E00?style=flat-square&logo=svelte&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

**Aether** — приватный браузер нового поколения с встроенным AI-ассистентом на базе Mistral AI.

[Скачать для Windows](https://github.com/s0nettap/Aether-Browser/releases) · [Возможности](#возможности) · [Установка](#установка)

</div>

---

## Почему Aether?

> **Приватность по умолчанию.** Aether не отслеживает вашу активность, не собирает телеметрию и не показывает рекламу. Это ваш браузер — без сюрпризов.

- 🔒 **Полная приватность** — никакой телеметрии и сбора данных
- 🤖 **AI-ассистент** — встроенный чат с Mistral AI знает контекст страницы
- ⚡ **Высокая производительность** — оптимизированный рендеринг, webview pooling, умное управление памятью
- 🎨 **Современный UI** — минималистичный дизайн на Svelte 5 с тёмной темой
- 💾 **Локальное хранение** — вся история и данные хранятся локально

---

## Возможности

### 🤖 AI-ассистент (Mistral AI)

Интегрированный чат с искусственным интеллектом, который:
- Знает содержимое текущей страницы
- Понимает ваши поисковые запросы
- Может кратко пересказать информацию с сайта
- Отвечает на вопросы о любой странице

### 🔍 Смена поисковой системы

Выбор из популярных поисковых систем:
- DuckDuckGo (по умолчанию)
- Google
- Yandex
- Bing
- Brave Search
- Startpage

### 📥 Менеджер загрузок

- Отслеживание прогресса в реальном времени
- История загрузок
- Открытие файлов прямо из браузера

### 📜 Тонкая настройка вкладок

- Контекстное меню вкладок (правый клик)
- Закрыть вкладки слева/справа
- Закрыть все вкладки кроме текущей

### ⌨️ Горячие клавиши

| Клавиша | Действие |
|---------|----------|
| `Ctrl+T` | Новая вкладка |
| `Ctrl+W` | Закрыть вкладку |
| `Ctrl+L` | Фокус на адресную строку |
| `Ctrl+K` | Командная палетка |
| `Ctrl+H` | История |

### 💾 Персистентность

- Сохранение истории посещений
- Сохранение закладок
- Восстановление вкладок после перезапуска
- История AI-чатов

### ⚡ Оптимизация производительности

- **Webview pooling** — переиспользование webview-объектов
- **Tab suspension** — фоновые вкладки замедляются автоматически
- **Visibility API** — часы и таймеры останавливаются когда браузер скрыт
- **Debouncing** — оптимизация IPC-вызовов
- **Memory optimization** — флаги GPU и Canvas для снижения потребления RAM

---

## Установка

### Windows

1. Скачайте последний релиз с [страницы Releases](https://github.com/YOUR_USERNAME/Aether-Browser/releases)
2. Распакуйте `Aether-1.0.0-portable.exe` в любую папку
3. Запустите `Aether.exe`

### Сборка из исходников

```bash
# Клонирование репозитория
git clone https://github.com/YOUR_USERNAME/Aether-Browser.git
cd Aether-Browser

# Установка зависимостей
npm install

# Режим разработки
npm run electron:dev

# Сборка для Windows
npm run dist
```

---

## Технологии

| Технология | Версия | Назначение |
|------------|--------|------------|
| Electron | 33.0.0 | Кроссплатформенный браузерный движок |
| Svelte | 5.14 | Реактивный UI-фреймворк |
| Vite | 6.0 | Сборщик и dev-сервер |
| TypeScript | 5.6 | Типизация |
| electron-store | 11.0 | Локальное хранение данных |
| electron-builder | 25.1 | Упаковка в исполняемые файлы |

---

## Структура проекта

```
Aether-Browser/
├── electron/
│   ├── main.js          # Главный процесс (IPC, окна, загрузки)
│   └── preload.cjs      # Контекстный мост (безопасный API)
├── src/
│   ├── App.svelte       # Главный компонент
│   ├── stores/
│   │   └── browser.svelte.ts  # Состояние (вкладки, настройки)
│   └── components/
│       ├── ContentArea.svelte   # Webview и New Tab страница
│       ├── ChatPopup.svelte     # AI чат
│       ├── DownloadsPopup.svelte
│       ├── CommandPalette.svelte
│       ├── HistoryPopup.svelte
│       └── ExtensionsPopup.svelte
├── package.json
└── README.md
```

---

## Конфиденциальность

Aether создан с фокусом на приватность:

- 🚫 **Нет телеметрии** — браузер не отправляет никаких данных
- 🚫 **Нет рекламы** — никаких рекламных вставок
- ✅ **Локальное хранение** — все данные остаются на вашем устройстве
- ✅ **Open Source** — код открыт для аудита

---

## Contributing

1. Fork репозиторий
2. Создайте ветку (`git checkout -b feature/amazing-feature`)
3. Commit изменения (`git commit -m 'Add amazing feature'`)
4. Push в ветку (`git push origin feature/amazing-feature`)
5. Откройте Pull Request

---

## Лицензия

MIT License — используйте свободно!

---

<div align="center">

**Сделано с ❤️ для приватного веб-серфинга**

[⬆ Вернуться наверх](#aether-browser)

</div>

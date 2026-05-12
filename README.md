# Profitlab — Landing

Одностраничный лендинг 12-недельной программы Profitlab. Собран на токенах Profitlab Design System v1.0.

## Стек

- HTML5 (semantic, A11y)
- CSS custom properties (CSS variables — токены DS)
- Vanilla JS (mobile menu + IntersectionObserver для fade-in)
- Inter (Google Fonts) + JetBrains Mono для технических меток
- Никаких сборщиков, фреймворков, зависимостей — открывается напрямую в браузере

## Структура

```
landing/
├── index.html      # одностраничный лендинг
└── README.md       # этот файл
```

## Что улучшено относительно Tilda-версии

1. **Хедлайн с конкретикой** — «Поток клиентов с AI — за 12 недель» + sub с цифрами (300К–2М ₽/мес, 4 заявки/неделя)
2. **Гарантия в hero** — pill «Возврат за 3 недели» в eyebrow, отдельный блок под тарифами
3. **Один блок «4 элемента»** вместо дубля
4. **Квиз 9 архетипов** как lead magnet перед программой
5. **AI-бот показан через chat-frame** — два реальных диалога вместо описаний
6. **6 кейсов с лицами и метриками** — testi-карточки с аватарами и result-блоками
7. **Авторы с конкретными цифрами** — 200+ INTEGRITY, 1500+ Profitlab, 47М ₽ продаж, 10 лет практики
8. **Уникальные результаты модулей** — без копипасты между Module 3 и Module 6
9. **Разнообразные CTA** — Записаться / Пройти квиз / Скачать PDF / Условия гарантии

## Frontend best practices

- Mobile-first responsive (1024 / 880 / 640 / 480 breakpoints)
- `prefers-reduced-motion` respected
- WCAG AA контраст
- Семантика: `<header>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `aria-*`
- Smooth scroll + focus-visible outlines
- Native `<details>` для FAQ (без JS)
- IntersectionObserver вместо scroll-event для fade-in
- Шрифт через `preconnect` + `display=swap`
- Бургер-меню работает с клавиатуры (Escape, focus management)

## Локальный запуск

```bash
# просто открой index.html в браузере
open landing/index.html

# или подними локальный сервер
cd landing && python3 -m http.server 8000
```

## Деплой

- **GitHub Pages**: включи Pages в Settings → Pages → Source: `main` branch, `/landing` folder
- **Cloudflare Pages / Vercel / Netlify**: подключи репо, build command пустой, output directory `landing`
- **Любой статический хостинг**: загрузи `landing/index.html`

## TODO для дальнейшей итерации

- Заменить аватары-инициалы на фото учеников (после согласования)
- Подключить квиз 9 архетипов (форма + Make.com роутинг в Telegram-бот)
- Добавить OpenGraph-картинку (`/landing/og.png` 1200×630)
- Подключить Yandex.Metrika / Google Analytics
- Lighthouse-аудит: целевой LCP < 2.5s, CLS < 0.1, A11y 100
- Подложить реальные ссылки на профили учеников (Instagram/Telegram)

## Лицензия

Внутренняя разработка. Все права у ООО «Вуман Проджектс».

# vikup-metropol.by — лендинг выкупа авто

Одностраничный лендинг ООО «Метрополь Авто» (Минск).
Чистый HTML/CSS/JS, без сборки и зависимостей.

## Структура
- `index.html` — весь сайт
- `assets/` — изображения (WebP ≤ 150 КБ)
- `Dockerfile` + `nginx.conf` — для деплоя на Railway

## Деплой на Railway
1. Запушить репозиторий в GitHub
2. railway.app → New Project → Deploy from GitHub repo → выбрать репозиторий
3. Railway сам соберёт Dockerfile и выдаст адрес вида `*.up.railway.app`
4. Settings → Networking → Custom Domain → добавить `vikup-metropol.by` и `www.vikup-metropol.by`
5. В DNS-панели регистратора домена создать CNAME-записи на адрес из п.4
   (для корневого домена без www удобнее всего подключить бесплатный Cloudflare — он умеет CNAME на корне)

Каждый push в ветку `main` автоматически обновляет сайт.

## Live

Сайт: https://web-production-5758c.up.railway.app (скоро: https://vikup-metropol.by)

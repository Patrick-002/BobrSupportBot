# Telegram Support Bot

Бот для технической поддержки в Telegram. Автоматически создает отдельный топик для каждого пользователя в группе поддержки.

## Что умеет бот

- Создает топик в группе для каждого нового пользователя
- Пересылает сообщения между пользователями и поддержкой
- Работает с текстом, фото, видео и документами

## Установка

```bash
apt-get install git
```
```bash
git clone https://github.com/Patrick-002/BobrSupportBot.git
```
```bash
cd BobrSupportBot
```
```bash
sudo apt update
```
```bash
sudo apt install python3 python3-pip python3-venv
```
```bash
python3 -m venv venv
```
```bash
source venv/bin/activate
```
```bash
pip install -r requirements.txt
```
```bash
cp example.env .env
```
Откройте файл `.env` в текстовом редакторе и заполните его своими данными:

```env
BOT_TOKEN=YOUR_TOKEN
SUPPORT_GROUP_ID=-100xxxxxxxxxx
```
```bash
apt-get install screen
```
```bash
screen -dmS SupportBt python3 main.py
```

Готово! Бот запущен.

## Как пользоваться

**Для клиентов:**
1. Найдите бота в Telegram
2. Нажмите `/start`
3. Напишите свой вопрос
4. Ждите ответа от поддержки

**Для операторов поддержки:**
1. Новые обращения появляются как топики в группе
2. Отвечайте в топике — пользователь получит ваше сообщение

## Структура файлов

```
TelegramSupportBot/
├── main.py              # Запуск бота
├── requirements.txt     # Список библиотек
├── .env                 # Настройки (токен и ID группы)
├── LICENSE.md           # Лицензия MIT
├── README.md            # Инструкция
└── modules/             # Код бота
    ├── bot_runner.py
    ├── config.py
    ├── database.py
    └── handlers.py
```

## Требования

- Python 3.10+
- Git (для клонирования репозитория)
- Супергруппа Telegram с включенными топиками
- Бот должен быть администратором группы

## Проблемы?

Проверьте:
- Правильность токена в файле `.env`
- ID группы начинается с `-100`
- Бот является администратором группы
- В группе включены топики
- Виртуальное окружение активировано

## Лицензия

Этот проект распространяется под лицензией MIT. Подробности в файле [LICENSE](LICENSE.md).

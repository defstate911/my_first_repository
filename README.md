# my_first_repository
 
# Чат-бот напоминания о питье воды

Этот бот создан с использованием библиотеки `Telebot` для отправки напоминаний пить воду в течение дня. Также он может делиться интересными фактами о воде. Бот работает в Telegram и запускается локально.

## Функциональность

1. **Напоминания о питье воды**  
   Бот отправляет регулярные напоминания в заданные часы, чтобы напомнить пользователю о необходимости выпить стакан воды.

2. **Интересные факты о воде**  
   По команде бот отправляет случайный факт о воде, чтобы мотивировать и заинтересовать пользователя.

## Как использовать?

### Команды:
- `/start` — Запускает бота и включает напоминания.
- `/fact` — Отправляет случайный факт о воде.

## Установка

Создайте файл config.py
Добавьте в него ваш токен Telegram-бота:
TOKEN = "ВАШ_ТОКЕН_ОТ_TELEGRAM_BOT"

Как работает бот?

После запуска команда /start начинает работу бота. Бот приветствует пользователя и запускает поток напоминаний.
Напоминания отправляются в определенные часы (с 10:00 до 19:00, с интервалом в 1 час).
При вызове команды /fact бот выбирает случайный факт из списка и отправляет его пользователю.

Используемые библиотеки
- Telebot — для взаимодействия с Telegram API.
- datetime — для определения текущего времени.
- threading — для запуска напоминаний в отдельном потоке.
- random — для выбора случайного факта.
- time — для управления задержками.

Примечания

Бот запущен в режиме постоянного опроса (polling), поэтому его работа требует стабильного интернет-соединения.
Напоминания работают на основе фиксированных временных интервалов, которые можно изменить в коде, редактируя массив time_rem.
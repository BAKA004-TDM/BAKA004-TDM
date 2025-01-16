# Установка ngrok в Termux

pkg update && pkg upgrade -y  # Обновление пакетов

pkg install wget -y           # Установка wget для загрузки файлов

# Скачивание ngrok

wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-arm.zip

# Установка unzip для распаковки архива

pkg install unzip -y

# Распаковка ngrok

unzip ngrok-stable-linux-arm.zip

# Добавление ngrok в PATH для удобства использования

mv ngrok /data/data/com.termux/files/usr/bin/

# Активация ngrok (замени YOUR_AUTH_TOKEN на ваш токен)

./ngrok authtoken YOUR_AUTH_TOKEN

# Запуск ngrok (например, для HTTP на порту 8080)

./ngrok http 8080

Этот код устанавливает и активирует ngrok в Termux. После запуска ngrok создаст туннель и предоставит публичный URL.
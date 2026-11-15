# Настройка SSH-доступа к GitHub

Автор: SprayQuezza (sunny.zhopkina@mail.ru)

## 1. SSH-клиент и генерация ключа
- Проверка клиента: ssh -V
- Генерация ключа: ssh-keygen -t ed25519 -C "sunny.zhopkina@mail.ru"
- Приватный ключ защищён passphrase
- Файлы: ~/.ssh/id_ed25519 (права 600), ~/.ssh/id_ed25519.pub (права 644)

## 2. Добавление ключа в GitHub
- Settings -> SSH and GPG keys -> New SSH key
- Title: WSL
- Email в ключе: sunny.zhopkina@mail.ru

## 3. Проверка подключения
$ ssh -T git@github.com
Hi <SprayQuezza>! You've successfully authenticated, but GitHub does not provide shell access.

## 4. Работа с репозиторием по SSH
$ git clone git@github.com:<username>/ssh-test.git
$ git remote -v
origin  git@github.com:<SprayQuezza>/ssh-test.git (fetch)
origin  git@github.com:<SprayQuezza>/ssh-test.git (push)
$ git push

## Ссылка на репозиторий
https://github.com/<SprayQuezza>/ssh-test

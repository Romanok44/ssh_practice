# Работа по теме «Работа с серверами и протокол удалённого управления SSH»

Работу выполнил Квасной Роман Борисович

## 1. Установка SSH-клиента и генерация ключевой пары
- Проверка клиента SSH: “ssh -V” → OpenSSH_10.2p1.

  <img width="245" height="64" alt="1" src="https://github.com/user-attachments/assets/1e9c2573-824d-41e1-a0db-534496768161" />

- Проверка наличия и версии git: “git --version” → git version 2.53.0.

  <img width="160" height="32" alt="2" src="https://github.com/user-attachments/assets/8f704f7e-9884-417a-a409-bd1a18a208d9" />

- Сгенерирована пара ключей ed25519 с паролем:
  ‘ssh-keygen -t ed25519 -C “romankvasnoy@gmail.com”’

  <img width="315" height="204" alt="3" src="https://github.com/user-attachments/assets/6c85d172-694b-4150-b12a-25eb7d17820f" />

- Проверка ключей: “ls -la ~/.ssh”

  <img width="243" height="79" alt="4" src="https://github.com/user-attachments/assets/4a2e7897-3673-42e7-b123-2b1f445171a9" />

- Отпечаток публичного ключа: “ssh-keygen -l -f ~/.ssh/id_ed25519.pub”

  <img width="398" height="35" alt="Отпечаток" src="https://github.com/user-attachments/assets/f6b835f1-35d1-4dce-9511-707b9676bff1" />

- Настройка ssh-agent для ввода без пароля:

  <img width="398" height="95" alt="6" src="https://github.com/user-attachments/assets/c48799f0-2072-4e67-87ef-c80ca45830eb" />


## 2. Добавление публичного ключа в аккаунт GitHub
- Получение ключа: “cat ~/.ssh/id_ed25519.pub”

  <img width="473" height="39" alt="7" src="https://github.com/user-attachments/assets/5b637c7d-cff5-478c-a2f8-c8fadac93561" />

- Добавление ключа в GitHub (Settings → SSH and GPG keys → New SSH key (тип: Authentication Key)):

  <img width="718" height="369" alt="8" src="https://github.com/user-attachments/assets/7d46a823-f545-45a8-ab9a-557ac0cbc563" />

  <img width="711" height="305" alt="9" src="https://github.com/user-attachments/assets/6c103f34-25a8-431e-9077-327accaff3ec" />


## 3. Проверка SSH-подключения к GitHub
- Установка соединения с GitHub: “ssh -T git@github.com”

  <img width="424" height="103" alt="10" src="https://github.com/user-attachments/assets/26a77a5e-387c-4d0d-a3d5-ac4998614ab2" />


## 4. Работа с репозиторием по SSH
- Создание репозитория для клонирования:

  <img width="579" height="571" alt="11" src="https://github.com/user-attachments/assets/f7158290-2352-4467-ba9f-db6c6fedb8c5" />

- Клонирование репозитория: “git clone git@github.com:Romanok44/ssh_practice.git”

  <img width="324" height="80" alt="12" src="https://github.com/user-attachments/assets/f9913fe1-0061-4f2f-8159-a905c6943fe7" />

- Коммит и пуш репозитория:

  <img width="353" height="152" alt="13" src="https://github.com/user-attachments/assets/d9b8b92f-dfea-49cf-93d9-b1130aec7517" />

Пароль не запрашивался — аутентификация по ключу через ssh-agent.

## Вывод
Были освоены генерация ключей ed25519, аутентификация по ключам вместо паролей, работа с Git-репозиторием по SSH.

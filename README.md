<img width="1920" height="1080" alt="изображение" src="https://github.com/user-attachments/assets/a4a21166-33e5-44d4-9c9b-bcd343fc34a0" />



<img width="1920" height="1080" alt="изображение" src="https://github.com/user-attachments/assets/75465617-8f92-4f87-a69f-313b28e9966f" />
Ответы на вопросы

    **Что такое SQL инъекция? SQL инъекция**
SQL-инъекция – одна из наиболее распространенных атак, используемых хакерами для атаки на веб-приложения, управляемых базой данных SQL. Это метод, при котором SQL-код/инструкции вставляются в поле выполнения с целью изменения содержимого базы данных, передачи полезного содержимого базы данных атакующему, возникновения проблем с отказом от использования, подделки идентификационных данных и многого другого
    
    
    **Почему ввод строки ' or 1=1;-- позволил войти в аккаунт администратора?**
Эта атака работает благодаря изменению логики SQL-запроса. В уязвимом приложении запрос для проверки логина и пароля выглядит примерно так: `SELECT * FROM users WHERE username = '$username' AND password = '$password'`. При подстановке зловредной строки запрос превращается в: `SELECT * FROM users WHERE username = 'admin' or 1=1;-- ' AND password = '...'`. Здесь конструкция `or 1=1` делает условие всегда истинным, а двойной дефис `--` комментирует оставшуюся часть запроса, включая проверку пароля. В результате система возвращает первую запись из таблицы пользователей (обычно администратора), и приложение ошибочно предоставляет доступ.
    
    **Как защитить web-ресурс от подобного рода атак?**
Основные меры защиты:
1. **Подготовленные выражения (Prepared Statements)** — главный метод, при котором параметры запроса передаются отдельно от его структуры
2. **Экранирование пользовательского ввода** — преобразование специальных символов в безопасные последовательности
3. **Строгая валидация данных** — проверка формата и типа всех входных параметров
4. **Принцип минимальных привилегий** — ограничение прав учетной записи БД до необходимого минимума
5. **Регулярное обновление и патчинг** — своевременное исправление уязвимостей в используемых框架 и библиотеках
6. **Веб-файрвол (WAF)** — фильтрация и блокировка подозрительных запросов на уровне приложения



Задание 2. Узнайте пароль администратора
<img width="1920" height="1080" alt="изображение" src="https://github.com/user-attachments/assets/3780a869-f251-4634-84de-ddcf34a104b0" />
<img width="1920" height="1080" alt="изображение" src="https://github.com/user-attachments/assets/5078354a-140e-4cb4-af2d-9b361b29effb" />
<img width="1920" height="1080" alt="изображение" src="https://github.com/user-attachments/assets/be33b036-888f-485d-9e4d-4e04bc3e475f" />

eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJzdGF0dXMiOiJzdWNjZXNzIiwiZGF0YSI6eyJpZCI6MSwidXNlcm5hbWUiOiIiLCJlbWFpbCI6ImFkbWluQGp1aWNlLXNoLm9wIiwicGFzc3dvcmQiOiIwMTkyMDIzYTdiYmQ3MzI1MDUxNmYwNjlkZjE4YjUwMCIsInJvbGUiOiJhZG1pbiIsImRlbHV4ZVRva2VuIjoiIiwibGFzdExvZ2luSXAiOiIiLCJwcm9maWxlSW1hZ2UiOiJhc3NldHMvcHVibGljL2ltYWdlcy91cGxvYWRzL2RlZmF1bHRBZG1pbi5wbmciLCJ0b3RwU2VjcmV0IjoiIiwiaXNBY3RpdmUiOnRydWUsImNyZWF0ZWRBdCI6IjIwMjUtMTEtMjEgMDU6MzQ6MzYuMzMzICswMDowMCIsInVwZGF0ZWRBdCI6IjIwMjUtMTEtMjEgMDU6MzQ6MzYuMzMzICswMDowMCIsImRlbGV0ZWRBdCI6bnVsbH0sImlhdCI6MTc2MzcwNTk4OX0.khcp5ic31iKbpemqUiI-UZ_WZmy21_J_A0ANmxdkGm5E24fNAfzwHvlclII1tSJ_eSbdTKr49tvwHKMrXl-qoVdYEyUjjXZbzgGBkwNOSwjqR-Mr3yZTILLLiHJeMSwEa3Et0Wl4kUihPOGeZHNL3zAT7hEOhRWyTw5sCdeFAZ0


<img width="1920" height="1080" alt="изображение" src="https://github.com/user-attachments/assets/28774b5f-3a36-4399-83c2-9d48cfdf7209" />
{
  "status": "success",
  "data": {
    "id": 1,
    "username": "",
    "email": "admin@juice-sh.op",
    "password": "0192023a7bbd73250516f069df18b500",
    "role": "admin",
    "deviceToken": "",
    "lastLoginIp": "",
    "profileImage": "assets/public/images/uploads/defaultAdmin.png",
    "topSecret": "",
    "isActive": true,
    "createdAt": "2025-11-21 05:34:36.333 +00:00",
    "updatedAt": "2025-11-21 05:34:36.333 +00:00",
    "deletedAt": null
  },
  "iat": 1763705989
}
<img width="1920" height="1080" alt="изображение" src="https://github.com/user-attachments/assets/36162ef8-10b9-4833-8e01-bfb03c601e0a" />










Использанные frameworks:

1. antd
2. react-router-dom.
3. react-google-login

Бизнес логика:

1. Пользователь вводит логин и пароль.
2. При вводе логина и пароля проверяется наличие пользователя в базе данных.
3. Если пользователь найден, то происходит переход на страницу профиля.
4. Если пользователь не найден, то происходит переход на страницу входа.
5. При выходе пользователя из системы происходит переход на страницу входа.

Technical task.

**В данном задании необходимо реализовать приложение для поиска youtube-видео по ключевым словам, а также сохранение запросов поиска.**

**Интерфейс**

1.  Реализовать страницу авторизации пользователя с формой входа: логин, пароль. Для аутентификации можно использовать json-файл со списком пользователей. После входа, необходимо сгенерировать и сохранить токен. Полученный токен использовать для авторизации - проверка наличия токена в localStorage, если токена нет, значит пользователь не авторизован (видит только страницу авторизации).

2.  После авторизации пользователь должен попадать на главную страницу сервиса, на которой расположена строка поиска. Необходимо реализовать поиск youtube-видео, при помощи Youtube API.

Результаты поиска вывести на той же странице в виде карточек видео (подобно тому, как оно реализовано в youtube).
Список видео может принимать два вида: список (рис. 4) и карточки (рис 3).
По умолчанию необходимо вывести 12 видео в виде списка.

3.  Также, в приложении должна быть реализована страница “Сохраненные запросы”, на которой выводится список сохраненных запросов. Запросы этого списка можно редактировать или выполнить.

Чтобы выполнить запрос, необходимо нажать кнопку “Выполнить”, после чего происходит переход на главную страницу, на которой отображаются результаты запроса, при этом, количество выводимых видео равно количеству, указанному при сохранении запроса (см. ниже, Максимальное количество)

Для сохранения запроса необходимо добавить в строке поиска на главной странице иконку “Сохранить поиск”, при нажатии на которую открывается форма.

В форме заранее заполнено значение из строки поиска в неизменяемом поле “Запрос” и отображается пустое поле “Название”, а также дополнительные пустые поля: Сортировать по (выпадающий список, доступные значения взять из API YouTube), Максимальное количество (числовое значение от 0 до 50).

Пользователь должен ввести название запроса, и, после этого, может сохранить запрос, остальные поля - опциональные, т.е. могут быть не заполнены.

Редактирование запроса происходит по нажатию на кнопку “Редактировать”. После этого открывается форма редактирования. Для редактирования использовать тот же компонент, что и для сохранения запроса. Обратите внимание, что при редактировании запроса можно изменять все поля формы, включая сам запрос.

4.  Реализовать выход пользователя из сервиса.

5.  После повторного входа пользователя сохраненные запросы должны отображаться. Если пользователь - другой, то отображать запросы соответствующие для него (другого). Для хранения можно использовать localStorage браузера. Либо другие методы на усмотрение исполнителя.

**Рекомендуется**

Использование библиотеки axios для запросов.
Использование библиотеки Ant Design при реализации интерфейса.

1.  YouTube API: [https://developers.google.com/youtube/v3/docs/](https://developers.google.com/youtube/v3/docs/) (Внимательно почитать search)

2.  Axios: https://github.com/axios/axios

3.  Ant Design: https://ant.design/

4.  Redux: https://redux.js.org/

5.  React Router: https://reacttraining.com/react-router/

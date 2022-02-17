# Блоговый движок (дипломная работа Skillbox)
### Краткое описание
Блоговый движок позволяет публиковать, просматривать, редактировать и модерировать посты. Предусмотрен поиск по блогу, вывод списка постов по тегу и по дате, сортировка постов по дате, количеству комментариев и рейтингу. Реализована регистрация, аутентификация и восстановление доступа к аккаунту пользователя, предусмотрена возможность изменения данных аккаунта. Есть возможность просмотра статистики постов статистики постов авторизованного пользователя и по всему блогу. Также реализована возможность изменения глобальных настроек блога.
### Подробное описание
#### 1. Главная страница
На главной странице приведена информация об авторских правах, контактные данные и название блога. Также представлен список превью утвержденных активных постов. Есть возможность сортировки постов по рейтингу (количество лайков и дизлайков), по дате публикации и по количеству комментариев (сортировка по-умолчанию - от новых к старым). Отображен список тэгов по частоте встречаемости в постах (чем чаще встречается тэг, тем крупнее название). При выборе тэга происходит отображение всех утвержденных акитвных постов, в которых этот тэг встречается. Для поиска постов по слову или фразе можно воспользоваться строкой поиска.
#### 2. Страница поста
При выборе поста открывается страница поста с полным текстом поста, включая форматирование и вставленные изображения. Здесь можно оставить комментарий к посту или ответить на  оставленный комментарий. Комментарии могут оставлять только авторизованные пользователи. Можно поставить лайк/дизлайк посту (это доступно и с главной страницы). При каждом просмотре поста увеличивается количество его просмотров, в случае, если просматривающий пользователь не является автором поста или модератором.
#### 3. Календарь
На этой странице представлен календарь на 1 год. Есть возможность переключения между годами, в течение которых зафиксированы утвержденные активные публикации. В ячейке даты, за которую есть публикации отображается их количество. При выборе такой ячейки, будут отображены все утвержденные активные публикации за эту дату.
#### 4. Статистика
Здесь отображаются статистические данные по всему блогу и по авторизованному пользователю.  
В зависимости от значения глобальных настроек статистика по всему блогу может быть показана всем (в т.ч. неавторизованным пользователям) или только модераторам.
#### 5. Регистрация и авторизация
Переход к странице аторизации возможен с любой страницы. Для перехода нужно выбрать **_"Войти"_**, после чего будет предложено ввести e-mail и пароль.  
Для регистрации необходимо на странице авторизации выбрать **_"Регистрация"_**. Далее необходимо ввести в соответствующие поля e-mail, пароль, имя пользователя и код каптчи. Если все поля заполнены верно, то пользователь может авторизоваться и продолжить работу с блогом.  
В зависимости от значения глобальных настроек блога, регистрация новых пользователей может быть запрещена. В этом случае на странице авторизации вместо  **_"Регистрация"_** будет отображена надпись **_"Регистрация закрыта"_**.  
Если зарегистрированный пользователь забыл пароль, на странице авторизации нужно выбрать **_"Забыли пароль?"_**. После этого будет предложено ввести зарегистрированный e-mail, на который будет направлена ссылка для изменения пароля к аккаунту.
#### 6. Редактирование профиля
Авторизованный пользователь может в любое время изменить данные своего профиля: имя, e-mail, пароль, добавить/изменить/удалить фото. При добавлении, фото обрезается до квадрата от левого верхнего угла и сжимается до размеров 36x36 пикселей.
#### 7. Добавление и редактирование публикаций
Авторизованный пользователь может добавлять новые публикации, а также редактировать их, если он является их автором. При добавлении публикации допускается указывать время публикации позднее текущего момента (отсрочка публикации). При указании времени публикации раньше текущего, будет автоматически установлено текущее время публикации. После добавления новой публикации, если она не скрыта она попадает на модерацию (в случае включенного режима премодерации в глобальных настройках блога).  
Редактирование публикации доступно автору публикации со страницы **_"Мои публикации"_** и модератору со страницы **_"Модерация"_**. При переходе на страницу **_"Мои публикации"_**, публикации автора будут разделены на 4 группы:
- **Скрытые** - публикации с отметкой **_"Публикация скрыта"_** (черновик)
- **Активные** - ожидающие утверждения модератором
- **Отклонённые** - отклоненные модератором
- **Опубликованные** - утвержденные модератором (отображаются на главной странице)
При редактировании публикации ее автором, она переходит в список ожидающих модерации, количество просмотров, лайков и дизлайков обнуляется. При редактировании публикации модератором ее статус не изменяется. Время публикации устанавливается текущим в любом случае, если не указано время позднее текущего момента.
#### 8. Модерация постов
При переходе на страницу модерирования публикаций, доступные модератору публикации разделены на 3 группы:
- **Новые** - ожидающие утверждения, модератор не является их автором (могут быть утверждены или отклонены)
- **Отклоненные** - отклоненные авторизованным модератором (могут быть утверждены)
- **Утвержденные** - утвержденные авторизованным модератором (могут быть отклонены)
#### 9. Глобальные настройки блога
Как и предыдущий пункт, доступны только модераторам и включают в себя:
- **Многопользовательский режим** - регистрация новых пользователей разрешена. При отключении - запрещена
- **Премодерация постов** - все новые или отредактированные автором публикации попадают на модерацию. При отключении - минуя модерацию приобретают статус утвержденных
- **Показывать статистику блога всем** - статистика публикаций по всему блогу доступна всем. При отключении - только модераторам

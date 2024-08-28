# Подсистема работы с чат ботом Телеграм

<ol>
<li><h4>Нужно заполнить реквизит БазовыйURL в регистре НастройкиТелеграм (на даный момент это https://api.telegram.org)</h4></li>

<li><h4>Все примеры использования методов можно посмотреть в справочники СправочникЧатБоты, на форме объекта есть соответствующие команды</h4></li>
</ol>    
<h5>Методы:</h5>
<ul>    
<li><h6>метод ИнформацияОБоте(Токен: Строка): Соответствие<Строка, Объект?></h6></li>

        Выполняет запрос /getMe, возвращающий базовую информацию о боте: имя, id, возможность добавлять бота в группы и т.д.
        Возвращаемое значение: Соответствие Из КлючИЗначение - сериализованный JSON ответ от Telegram
        Результат:
            {
                "ok": true,
                "result": {
                "id": ИдентификаторБота,
                "is_bot": true,
                "first_name": "Имя Бота",
                "username": "sicheebot",
                "can_join_groups": true,
                "can_read_all_group_messages": false,
                "supports_inline_queries": false,
                "can_connect_to_business": false
            }
            Пример использования: 
                Команда "Информация о Боте" в справочнике

<li><h6>метод Обновить(Токен: Строка): Соответствие<Строка, Объект?></h6></li>

            Выполняет запрос /getUpdates, возвращающий информацию о событиях бота
            Результат:
            {
                "ok": true,
                "result": [
                {
                "update_id": 291366000,
                "channel_post": {
                    "message_id": 4685,
                    "sender_chat": {
                    "id": -1001893407333,
                    "title": "Тестовый канал",
                    "username": "testsichee",
                    "type": "channel"
                    },
                    "chat": {
                    "id": -1001893407333,
                    "title": "Тестовый канал",
                    "username": "testsichee",
                    "type": "channel"
                    },
                    "date": 1717054881,
                    "pinned_message": {
                    "message_id": 4670,
                    "sender_chat": {
                    "id": -1001893407333,
                    "title": "Тестовый канал",
                    "username": "testsichee",
                    "type": "channel"
                    },
                    "chat": {
                    "id": -1001893407333,
                    "title": "Тестовый канал",
                    "username": "testsichee",
                    "type": "channel"
                    },
                    "date": 1717054721,
                    "text": "Строковое значение"
                    }
                }
                },
                {
                "update_id": 291366001,
                "message": {
                    "message_id": 2446,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054906,
                    "message_thread_id": 2446,
                    "forum_topic_created": {
                    "name": "Тестовая тема fb0492fb-3a2d-4496-8309-b119226ef9f9",
                    "icon_color": 7322096,
                    "icon_custom_emoji_id": "5357419403325481346"
                    },
                    "is_topic_message": true
                }
                },
                {
                "update_id": 291366002,
                "message": {
                    "message_id": 2448,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054907,
                    "message_thread_id": 2446,
                    "reply_to_message": {
                    "message_id": 2446,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054906,
                    "message_thread_id": 2446,
                    "forum_topic_created": {
                    "name": "Тестовая тема fb0492fb-3a2d-4496-8309-b119226ef9f9",
                    "icon_color": 7322096,
                    "icon_custom_emoji_id": "5357419403325481346"
                    },
                    "is_topic_message": true
                    },
                    "forum_topic_edited": {
                    "name": "Новый тестовый заголовок",
                    "icon_custom_emoji_id": "5310132165583840589"
                    },
                    "is_topic_message": true
                }
                },
                {
                "update_id": 291366003,
                "message": {
                    "message_id": 2449,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054912,
                    "forum_topic_reopened": {}
                }
                },
                {
                "update_id": 291366004,
                "message": {
                    "message_id": 2450,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054912,
                    "forum_topic_closed": {}
                }
                },
                {
                "update_id": 291366005,
                "message": {
                    "message_id": 2451,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054912,
                    "message_thread_id": 2446,
                    "reply_to_message": {
                    "message_id": 2446,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054906,
                    "message_thread_id": 2446,
                    "forum_topic_created": {
                    "name": "Тестовая тема fb0492fb-3a2d-4496-8309-b119226ef9f9",
                    "icon_color": 7322096,
                    "icon_custom_emoji_id": "5357419403325481346"
                    },
                    "is_topic_message": true
                    },
                    "forum_topic_closed": {},
                    "is_topic_message": true
                }
                },
                {
                "update_id": 291366006,
                "message": {
                    "message_id": 2452,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054937,
                    "forum_topic_reopened": {}
                }
                },
                {
                "update_id": 291366007,
                "message": {
                    "message_id": 2453,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054937,
                    "message_thread_id": 2446,
                    "reply_to_message": {
                    "message_id": 2446,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054906,
                    "message_thread_id": 2446,
                    "forum_topic_created": {
                    "name": "Тестовая тема fb0492fb-3a2d-4496-8309-b119226ef9f9",
                    "icon_color": 7322096,
                    "icon_custom_emoji_id": "5357419403325481346"
                    },
                    "is_topic_message": true
                    },
                    "forum_topic_reopened": {},
                    "is_topic_message": true
                }
                },
                {
                "update_id": 291366008,
                "message": {
                    "message_id": 2454,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717054995,
                    "forum_topic_edited": {
                    "name": "Новое имя главной темы b7ff8b12-563b-417f-8218-a460d59d7f7f"
                    }
                }
                },
                {
                "update_id": 291366009,
                "message": {
                    "message_id": 2455,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717055002,
                    "general_forum_topic_hidden": {}
                }
                },
                {
                "update_id": 291366010,
                "message": {
                    "message_id": 2456,
                    "from": {
                    "id": 6129457865,
                    "is_bot": true,
                    "first_name": "Имя бота",
                    "username": "sicheebot"
                    },
                    "chat": {
                    "id": -1001971186208,
                    "title": "Тест",
                    "is_forum": true,
                    "type": "supergroup"
                    },
                    "date": 1717055007,
                    "general_forum_topic_unhidden": {}
                }
                }
                ]
            }
            Пример использования: 
                Команда "Обновить учатников" в справочнике
        
<li><h6>метод ОтправитьСообщение(СообщениеДляОтправки: ОбщийМодульРаботаСТелеграмКонструкторы.СообщениеДляОтправки): Соответствие<Строка, Объект?></h6></li>

            Отправляет текстовое сообщение в чат или канал
            Результат:
            {
                "ok": true,
                "result": {
                "message_id": 4638,
                "from": {
                "id": 6129457865,
                "is_bot": true,
                "first_name": "Имя бота",
                "username": "sicheebot"
                },
                "chat": {
                "id": 461699897,
                "first_name": "Имя",
                "last_name": "Фамилия",
                "username": "Имя пользователя",
                "type": "private"
                },
                "date": 1717072354,
                "text": "Строковое значение"
                }
            }
            Пример использования: 
                Команда "Отправить сообщение" в справочнике
        
<li><h6>метод ОтправитьСообщениеСКонтентом(СообщениеДляОтправки: ОбщийМодульРаботаСТелеграмКонструкторы.СообщениеДляОтправки): Соответствие<Строка, Объект?></h6></li>

            Отправляет сообщение с указанным конентом
            Результат:
            {
                "ok": true,
                "result": {
                "message_id": 4638,
                "from": {
                "id": 6129457865,
                "is_bot": true,
                "first_name": "Имя бота",
                "username": "sicheebot"
                },
                "chat": {
                "id": 461699897,
                "first_name": "Имя",
                "last_name": "Фамилия",
                "username": "Имя пользователя",
                "type": "private"
                },
                "date": 1717072354,
                "text": "Строковое значение"
                }
            }
            Пример использования: 
                Команда "Отправить видео", "Отправить картинку", ""Отправить документ" в справочнике
</ul>
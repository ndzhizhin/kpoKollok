# **Документация API**


### Получение всех тренировок:

**GET /api/workouts**

Ответ:

 
    {
        "id": 3,
        "name": "legs and shoulders day",
        "description": "legs + shoulders",
        "duration": 2,
        "trainer": "Kirill"
    },
    {
        "id": 2,
        "name": "biceps and back day\n",
        "description": "biceps + back",
        "duration": 2,
        "trainer": "Nikita\n"
    },
    {
        "id": 1,
        "name": "chest and triceps day",
        "description": "chest + triceps",
        "duration": 3,
        "trainer": "S4vel"
    }

### Создание тренировки:

**POST /api/workouts**


    {
        "id": 4,
        "name": "whole body",
        "description": "whole body day",
        "duration": 3,
        "trainer": "Igor"
    }


Ответ:

   
    {
        "id": 4,
        "name": "whole body",
        "description": "whole body day",
        "duration": 3,
        "trainer": "Igor"
    }

### Получение тренировки по ID:
**GET /api/workouts/3**

Ответ при успешном запросе:

   
    {
      "id": 3,
      "name": "legs and shoulders day",
      "description": "legs + shoulders",
      "duration": 2,
      "trainer": "Kirill"
    }
 


Ответ при неудачном запросе:

HTTP/1.1 404 Not Found

### Обновление тренировки по ID:


**PUT /api/workouts/3**

    {
            "id": 4,
            "name": "whole body",
            "description": "whole body day",
            "duration": 3,
            "trainer": "Vova"
    }
    
Ответ при успешном запросе:



     {
             "id": 4,
             "name": "whole body",
             "description": "whole body day",
             "duration": 3,
             "trainer": "Vova"
     }
    


Ответ при неудачном запросе:

HTTP/1.1 404 Not Found

### Удаление тренировки по ID:


**DELETE /api/workouts/3**

Ответ при успешном запросе:

HTTP/1.1 200 OK

Ответ при неудачном запросе:

HTTP/1.1 404 Not Found

# **Валидация**

Поле name не может быть пустым. Поле description не может быть пустым. Поле duration не может быть пустым и должно быть целым числом. Поле trainer не может быть пустым.

# **База данных**

По умолчанию приложение использует базу данных PostgreSQL. Для изменения параметров подключения к базе данных необходимо изменить параметры в файле application.properties.

# **Автор**

Жижин Никита Дмитриевич

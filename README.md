# API 

Простой веб сервис для работы со списком задач

Data types:

* *TO DO LIST* :
    
```
    
{
        

    id: уникальный идентификатор задачи. Тип Numeric.
    title: Краткое описание задачи. Тип String.
    description: подробное описание задачи. Тип Text.
    done: отметка о выполнении. Тип Boolean.

    
}
```

    

## Urls
### Get list of tasks
* **Request**
	* **URL:** `/tasks`
	* **Method:** `GET`
	* **Body:** *empty*
* **Response**
	* **Code:** `200 HTTP_OK`
	* **Body:** `TO DO LIST`
	
### Get list
* **Request**
	* **URL:** `/tasks/task_id`
	* **Method:** `GET`
	* **Body:** *empty*
* **Response**
        * **Content-Type:** `application/json`
	* **Code:** `200 HTTP_OK`
	* **Body:** `TO DO LIST`
	
### Create new task
* **Request**
	* **URL:** `/tasks`
	* **Method:** `POST`
	* **Body:** `TO DO LIST`
* **Response**
        * **Content-Type:** `application/json`
	* **Code:** `201 HTTP_CREATED`, `404 HTTP_NOT_FOUND`, `403 HTTP_FORBIDDEN`
	* **Body:** `empty`
	
### Update task
* **REQUEST**
    * **URL:** `/tasks/task_id`
    * **Method:** `PUT`
    * **Body:** `TO DO LIST`
* **RESPONSE**
    * **Content-Type:** `application/json`
    * **Code:** `200 HTTP_OK`, `404 HTTP_NOT_FOUND`, `403 HTTP_FORBIDDEN`
    * **Body:** `empty`
    
### Delete task
* **REQUEST**
    * **URL:** `/tasks/task_id`
    * **Method:** `DELETE`
* **RESPONSE**
    * **Content-Type:** `application/json`
    * **Code:** `200 HTTP_OK`, `404 HTTP_NOT_FOUND`, `403 HTTP_FORBIDDEN`

    
	
  

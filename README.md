# api fastcgi

Cервис для сбора жалоб и предложений о работе  жилищно-коммунального хозяйства. 

Data types:

* *COMMENT_ABOUT_WORK*:
    
```
    
{
        
	  "Id": "GUID",

    "CommentDate": "YYYY-MM-DD HH:MM:SS",
    
    "City": "string",
    
    "Comment": "string"
    
}
```
* *CITY_COMMENT_REPORT*:

```
    
{
        
	"City": "string",

   "Comment1": "string",
   
   "Comment2": "string",
   
   "Comment3": "string",
   ...
    
}
    
```
## Urls
### Create Comment
* **Request**
	* **URL:** `/comments/(user_id)`
	* **Method:** `POST`
	* **Body:** *COMMENT_ABOUT_WORK*
* **Response**
	* **Code:** `201 HTTP_CREATED`
	* **Body:** user_id , comment_id
	
### Edit Comment
* **Request**
	* **URL:** `/comments/(user_id)/(Comment_id)`
	* **Method:** `PUT`
	* **Body:** *COMMENT_ABOUT_WORK*
* **Response**
  * **Content-Type:** `application/json`
	* **Code:** `201 HTTP_CREATED`, `404 HTTP_NOT_FOUND`, `403 HTTP_FORBIDDEN`
	* **Body:** empty
	
### Delete Comment
* **Request**
	* **URL:** `/comments/(user_id)/(Comment_id)`
	* **Method:** `delete`
* **Response**
  * **Content-Type:** `application/json`
	* **Code:** `201 HTTP_CREATED`, `404 HTTP_NOT_FOUND`, `403 HTTP_FORBIDDEN`
	* **Body:** empty
	
### Get comment reports sorted by city
* **REQUEST**
    * **URL:** `/comments/reports/city/(city)`
    * **Method:** `GET`
* **RESPONSE**
    * **Content-Type:** `application/json`
    * **Code:** `200 HTTP_OK`, `404 HTTP_NOT_FOUND`, `403 HTTP_FORBIDDEN`
    * **Body:** *CITY_COMMENT_REPORT*
	
  

# CRUDAPI
API for simple CRUD operations in Docker Containerization.

You can get all the files in master branch!!!

This API is built in Django framework with postgresql database and in docker containerization.

Steps to use this API:
1. Install docker if not installed earlier using Docker documentation(https://docs.docker.com/get-docker/)
2. Install docker-compose also using the Docker Documentation(https://docs.docker.com/compose/install/)
3. Then clone this project.
4. In the terminal(since I have used the Linux OS), use these steps:
    - Go to the projects directory which has the manage.py file(newapp), in terminal.
    - ``` docker-compose build ``` 
    
    (This will install all the required libraries in loading this API.)
    - ```docker-compose up -d```
    
    (This will make the status up for the app and the db)
    - ```docker-compose run web python3 manage.py makemigrations```
    - ```docker-compose run web python3 manage.py migrate```
    - ```docker-compose run web python3 manage.py runserver```
    
5. While testing the API, I used Postman.
  - for GET method: ![alt text](https://github.com/chaudharynidhi/CRUDAPI/blob/main/Get_Response.png?raw=true)
  
  - for POST method: ![alt text](https://github.com/chaudharynidhi/CRUDAPI/blob/main/post_request.png?raw=true), the status is marked as 201 created! and the file is: https://github.com/chaudharynidhi/CRUDAPI/blob/main/get_response2.json
  
  - for UPDATE method used PUT method: ![alt text](https://github.com/chaudharynidhi/CRUDAPI/blob/main/before_update.png?raw=true), here I have changed the 'regular_price_value' to 45.0, the changes are clearly described in the next GET request: https://github.com/chaudharynidhi/CRUDAPI/blob/main/after_update.json
  
  - for deleting I have deleted the id=4: before DELETE: https://github.com/chaudharynidhi/CRUDAPI/blob/main/before_delete.json, after deleting: ![alt_text](https://github.com/chaudharynidhi/CRUDAPI/blob/main/after_delete.png?raw=true) and here is the JSON file after updations: https://github.com/chaudharynidhi/CRUDAPI/blob/main/after_delete_response.json.
  
  
I have used the Linus OS and postgresql for db storage and Django restframework for the building of API.

Few SS for the built API in localhost: 
- Opening Screen: ![alt_text](https://github.com/chaudharynidhi/CRUDAPI/blob/main/opening%20screen.png?raw=true)

- Second Screen begore any set input: ![alt_text](https://github.com/chaudharynidhi/CRUDAPI/blob/main/2nd.png?raaw=true)

- After testing all the operations done in the Postman: ![alt_text](https://github.com/chaudharynidhi/CRUDAPI/blob/main/after%20all%20the%20operations%20done.png?raw=true)

If any error occurs in docker file kindly use: 
``` docker-compose down```
or check on 
``` docker-compose logs``` 
and act accordingly.

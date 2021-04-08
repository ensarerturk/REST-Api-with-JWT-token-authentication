# REST-Api-with-JWT-token-authentication

authentication için:
   curl --location --request POST 'http://127.0.0.1:5000/auth' \
   --header 'Content-Type: application/json' \
   --data-raw '{
       "username" : "abc",
       "password" : "abc"
   }'

GET:
   curl --location --request GET 'http://127.0.0.1:5000/users' \
   --header 'Authorization: JWT {{token}}' \
   --data-raw ''   

GET:
   curl --location --request GET 'http://127.0.0.1:5000/users/<id>' \
   --header 'Authorization: JWT {{token}}' \
   --data-raw ''   

POST:
   curl --location --request GET 'http://127.0.0.1:5000/users' \
   --header 'Authorization: JWT {{token}}' \
   --header 'Content-Type: application/json' \
   --data-raw '{
       "username" : "{{name}}",
       "password" : "{{password}}",
       "email" : "{{email}}"
   }'

PUT:
   curl --location --request PUT 'http://127.0.0.1:5000/users/<id>' \
   --header 'Authorization: JWT {{token}}' \
   --header 'Content-Type: application/json' \
   --data-raw '{
       "username" : "{{name}}",
       "password" : "{{password}}",
       "email" : "{{email}}"  
   }'

DELETE:
   curl --location --request DELETE 'http://127.0.0.1:5000/users/<id>' \
    --header 'Authorization: JWT {{token}}' \
   --data-raw ''

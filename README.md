# Strapi application

A quick description of your strapi application


Récupérer token jwt au préalable en passant par : POST http://localhost:1337/auth/local avec pour body en JSON : 
{
  "identifier": "diego@gmail.com",
  "password": "azerty"
}
 

Auth : 

Création de sujet de discussion : POST http://localhost:1337/sujets-de-discussions
header:  eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiaWF0IjoxNjExMjY5NTE5LCJleHAiOjE2MTM4NjE1MTl9.yBbY5I8raYZQwR6H2Rb3zn0SqkglK_lM2_x5C9riMX8 type (bearer token)
body :  
 {
      "titre": "Sport",
      "created_at": "Fri Sep 28 201",
      "users": [1]
 }

Création de message : POST http://localhost:1337/messages
header:  eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiaWF0IjoxNjExMjY5NTE5LCJleHAiOjE2MTM4NjE1MTl9.yBbY5I8raYZQwR6H2Rb3zn0SqkglK_lM2_x5C9riMX8 type (bearer token)
body :
{
  "body": "Je débute le sport",
  "createdAt": "2021-01-21T22:36:51.178Z",
  "discussion_subject": 2,
  "user_id": 1,
  "user": 1
}



Consulter un sujet de discussion : GET http://localhost:1337/sujets-de-discussions/2
header:  eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiaWF0IjoxNjExMjY5NTE5LCJleHAiOjE2MTM4NjE1MTl9.yBbY5I8raYZQwR6H2Rb3zn0SqkglK_lM2_x5C9riMX8 type (bearer token)

Consulter les messages associer à ce sujet de discussion: GET http://localhost:1337/messages?discussion_subject.id=2
header: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiaWF0IjoxNjExMjY5NTE5LCJleHAiOjE2MTM4NjE1MTl9.yBbY5I8raYZQwR6H2Rb3zn0SqkglK_lM2_x5C9riMX8 type (bearer token)

Consulter un message et l'auteur associé : GET http://localhost:1337/messages/7
header: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiaWF0IjoxNjExMjY5NTE5LCJleHAiOjE2MTM4NjE1MTl9.yBbY5I8raYZQwR6H2Rb3zn0SqkglK_lM2_x5C9riMX8 type (bearer token)



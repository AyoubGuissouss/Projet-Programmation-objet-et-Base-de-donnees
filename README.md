# Projet-Programmation-objet-et-Base-de-donnees
Projet de fin de session du cours programmation objet et base de données.
Utilisation de Hibernat et Spring boot, MySql et Java.


Notre projet permet l’affichage de la liste de voitures qui appartiennent au service de location de voiture ainsi que la liste de voitures louées, il permet la recherche d’une voiture en particulier, d’une liste de voiture par filtre de prix, d’année ou de kilométrage.
On peut créer un nouveau client, afficher la liste des clients, modifier les informations d’un client existant ou supprimer un client.
On peut également ajouter une nouvelle réservation (louer une voiture), afficher la liste des réservations ou supprimer une réservation (retourner la voiture).


Les étapes à suivre pour le fonctionnement du projet :
1-	Modifier les informations dans le fichier application.properties pour permettre l’accès au SGBD (username et password) puis effectuer une première exécution du projet.
2-	Dans la class VoitureConfig, enlevez le commentaire à coté du @Bean à la ligne 14, puis effectuer une deuxième exécution du projet, cela permettra de remplir la base de données avec une liste de 10 voitures. Puis le remettre en commentaire par la suite.




Les fonctionnalités (Path et captures d’écran(Browser et PostMan)) :
Important : Vue que les id sont générés automatiquement et que plusieurs tests ont été fait, les exemples ci-dessous ne marcherons surement pas pour vous, essayez de toujours vérifier les id existant dans votre base de données avant d’effectuer chaque test, Merci.
1-	Afficher la liste des voitures :
Path: http://localhost:8090/cars

2-	Affiche une voiture par Id :
Path: http://localhost:8090/car/{Id}  (dans l’exemple Id=143)

3-	Afficher voitures par prix (Plus petit ou égal au prix entré comme paramètre) :
Path: http://localhost:8090/carsByPrice/{price}  (dans l’exemple price=20000)

4-	Afficher voitures par année (Plus petit ou égal à l’année entrée comme paramètre) :
Path: http://localhost:8090/carsByYear/{year}  (dans l’exemple year = 2017)

5-	Afficher voitures par kilométrage (Plus petit ou égal au kilométrage entré comme paramètre) :
Path : http://localhost:8090/carsByMileage/{mileage} (dans l’exemple mileage = 100000)

6-	Afficher voitures louées (dans l’exemple uniquement une voiture est louée)
Path : http://localhost:8090/rentedCars

7-	Ajouter un nouveau client :
L’ajout d’un nouveau client se fait sur PostMan vue qu’il nécessite d’entrer plusieurs paramètres
Path: http://localhost:8090/addClient

8-	Afficher la liste des clients :
Path: http://localhost:8090/clients

9-	Modifier les informations d’un client :
La modification des informations d’un client se fait sur PostMan vue qu’elle nécessite d’entrer plusieurs paramètres
Path : http://localhost:8090/updateClient/{clientId} (dans l’exemple clientId = 3)

10-	Supprimer un client :
La suppression d’un client se fait sur PostMan
Path: http://localhost:8090/deleteClient/{clientId} (dans l’exemple clientId = 7)

11-	 Ajouter une réservation (Louer une voiture) :
Pour ajouter une réservation, il faut premièrement que le client existe dans la base de données, si ce n’est pas le cas l’inscription du client (L’ajout du client) se fait en premier lieu. L’ajout de la réservation se fait sur PostMan vue qu’il nécessite d’entrer plusieurs paramètres
Path : http://localhost:8090/reserveCar/{carId} (dans l’exemple carId = 143)

12-	Afficher la liste des réservations
Path : http://localhost:8090/reservations

13-	Supprimer une réservation (Retourner une voiture) :
La suppression d’une réservation se fait sur PostMan
Path : http://localhost:8090/deleteReservation/{reservationId} (dans l’exemple réservation = 6)

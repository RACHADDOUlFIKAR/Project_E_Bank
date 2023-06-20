<h3>Introduction :</h3>
L'objectif de ce projet est de créer une application de gestion de comptes bancaires en utilisant le framework Spring Boot. L'application permettra aux utilisateurs de gérer leurs comptes bancaires, d'effectuer des opérations de débit et de crédit, et de visualiser les informations liées à leurs comptes. Le projet est divisé en deux parties principales : la couche DAO (Data Access Object) et la couche service, DTOs et RestController.

<h2>Partie 1 : Couche DAO</h2>
La couche DAO est responsable de l'interaction avec la base de données et de la manipulation des entités. Voici les étapes suivies pour mettre en place cette couche :

Création du projet Spring Boot :

Un nouveau projet Spring Boot a été créé en utilisant les outils appropriés.<br><br>
<img src="images/Capture0.png"><br><br>
<h4>Création des entités JPA :</h4>
Les entités suivantes ont été créées :

Customer <br><br>
<img src="images/Capture.png">
BankAccount <br><br>
<img src="images/Capture1.png">
SavingAccount <br><br>
<img src="images/Capture3.png"><br>
CurrentAccount <br><br>
<img src="images/Capture4.png">
AccountOperation <br><br>
<img src="images/Capture5.png">
Création des interfaces JPA Repository :
Les interfaces JPA Repository suivantes ont été créées pour chaque entité :

CustomerRepository : Interface pour la manipulation des entités Customer.<br><br>
<img src="images/Capture6.png">
BankAccountRepository : Interface pour la manipulation des entités BankAccount.<br><br>
<img src="images/Capture7.png">
AccountOperationRepository : Interface pour la manipulation des entités AccountOperation.<br><br>
<img src="images/Capture8.png">
Test de la couche DAO :

Des tests ont été effectués pour vérifier le bon fonctionnement des méthodes définies dans les interfaces JPA Repository.
Les opérations de création, récupération, mise à jour et suppression des entités ont été testées pour chaque repository.<br><br>
<h2>Partie 2 : Couche service, DTOs et RestController</h2>
La couche service est responsable de la logique métier de l'application. Les DTOs (Data Transfer Objects) sont utilisés pour transférer les données entre les différentes couches de l'application. Le RestController permet d'exposer les services via des API REST. Voici les étapes suivies pour mettre en place cette couche :

<h4>Création des services :</h4>
<img src="images/Capture12.png">
<img src="images/Capture9.png">
<img src="images/Capture10.png">
<img src="images/Capture11.png">

Des services ont été créés pour gérer les opérations liées aux entités Customer, BankAccount, SavingAccount, CurrentAccount et AccountOperation.<br>
Les méthodes appropriées ont été implémentées pour effectuer les opérations de création, récupération, mise à jour et suppression des entités.<br>
<h4>Création des DTOs :</h4>

<img src="images/Capture16.png"><br>
<h5>Example de DTO</h5>
<img src="images/Capture13.png">
<img src="images/Capture14.png">
<img src="images/Capture15.png"><br>
Des DTOs ont été créés pour chaque entité afin de transférer les données entre les couches.<br>
Les DTOs contiennent uniquement les informations nécessaires et évitent les dépendances directes sur les entités JPA.<br><br>
<h4>Création du RestController :</h4>

Un RestController a été créé pour exposer les services via des API REST.<br><br>
<img src="images/Capture17.png">
<img src="images/Capture18.png">
Les méthodes appropriées ont été définies pour effectuer les opérations CRUD (Create, Read, Update, Delete) sur les entités.<br><br>
<img src="images/Capture19.png">
<img src="images/Capture20.png">
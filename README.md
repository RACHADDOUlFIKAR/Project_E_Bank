# Project_E_Bank

<h2>Application de gestion de comptes bancaires</h2>

<h4>Introduction :</h4>
L'objectif de ce projet est de créer une application de gestion de comptes bancaires en utilisant le framework Spring Boot. L'application permettra aux utilisateurs de gérer leurs comptes bancaires, d'effectuer des opérations de débit et de crédit, et de visualiser les informations liées à leurs comptes. Le projet est divisé en deux parties principales : la couche DAO (Data Access Object) et la couche service, DTOs et RestController.
<h2>I. Dans le Back-End</h2>
<h3>Partie 1 : Couche DAO</h3>
La couche DAO est responsable de l'interaction avec la base de données et de la manipulation des entités. Voici les étapes suivies pour mettre en place cette couche :

<h4>Création du projet Spring Boot :</h4>

Un nouveau projet Spring Boot a été créé en utilisant les outils appropriés.<br><br>
![Capture0](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/1fdd49d4-b9f2-41e8-aa73-d731e303c634)
<h4>Création des entités JPA :</h4>

Les entités suivantes ont été créées :

Customer : Représente un client avec des informations telles que nom, prénom, etc.<br><br>
![Capture3](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/4677e01c-0a49-4cd1-a0c0-001a1f88df21)<br>
BankAccount : Représente un compte bancaire avec des informations telles que le solde, le numéro de compte, etc.<br><br>
![Capture7](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/660a6101-3420-40c7-8b8c-2f6abbd3019e)<br>
SavingAccount : Représente un compte d'épargne et étend la classe BankAccount.<br><br>
![Capture4](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/98037977-f9df-41ee-a5fe-d7ea8c115ba5)<br>
CurrentAccount : Représente un compte courant et étend la classe BankAccount.<br><br>
![Capture5](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/39eb11fc-0b4d-4112-b65a-cf75e9105ce6)<br>

AccountOperation : Représente une opération effectuée sur un compte avec des détails tels que le montant, la date, etc.<br><br>
![Capture6](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/1ebf2513-5c21-4858-aaf2-d8201d6db2c4)

Création des interfaces JPA Repository :
<h4>Les interfaces JPA Repository suivantes ont été créées pour chaque entité :</h4>

CustomerRepository : Interface pour la manipulation des entités Customer.<br><br>
![Capture](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/7418d4a4-b05d-4443-b96d-d6accc4ba5b1)<br>
BankAccountRepository : Interface pour la manipulation des entités BankAccount.<br><br>
![Capture1](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/8100198f-7ce7-47ee-9679-696f1409a3b3)

AccountOperationRepository : Interface pour la manipulation des entités AccountOperation.<br><br>
![Capture2](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/d579479c-ee37-4c58-8428-02d93ef57305)


Test de la couche DAO :

Des tests ont été effectués pour vérifier le bon fonctionnement des méthodes définies dans les interfaces JPA Repository.
Les opérations de création, récupération, mise à jour et suppression des entités ont été testées pour chaque repository.<br><br>
![Capture8](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/a7bf43cc-e542-42b8-a405-3ae6f548357a)

![Capture21](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/e26b008b-2858-457a-a62d-33cef53fa5b7)

![Capture22](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/c978a851-e342-4f7b-9474-78bb7461c802)

![Capture23](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/9cd95cfb-338f-43bb-810e-6aa8c59bae74)

<br>
<h3>Partie 2 : Couche service, DTOs et RestController</h3>
La couche service est responsable de la logique métier de l'application. Les DTOs (Data Transfer Objects) sont utilisés pour transférer les données entre les différentes couches de l'application. Le RestController permet d'exposer les services via des API REST. Voici les étapes suivies pour mettre en place cette couche :<br>
<h4>Création des services :</h4>
Des services ont été créés pour gérer les opérations liées aux entités Customer, BankAccount, SavingAccount, CurrentAccount et AccountOperation.
Les méthodes appropriées ont été implémentées pour effectuer les opérations de création, récupération, mise à jour et suppression des entités.<br><br>

![Capture9](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/4fd4ccb4-c0cb-4f3d-8c88-e26467eead77)<br>
![Capture10](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/65b8d4eb-1f7b-406e-8177-53009430ceeb)
![Capture11](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/53ef90a4-6843-4792-813f-29647425b641)
![Capture12](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/54c7211c-b90c-4d46-bd66-671395c3e3b0)

<h4>Création des DTOs :</h4>

Des DTOs ont été créés pour chaque entité afin de transférer les données entre les couches.
Les DTOs contiennent uniquement les informations nécessaires et évitent les dépendances directes sur les entités JPA.<br><br>
![Capture13](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/2e4a6524-af61-4d88-af02-6639e1ffdca0)
![Capture14](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/0ba8bff9-8d90-44b0-b105-24f0d6caaa0d)

<h4>Création du RestController :</h4>

Un RestController a été créé pour exposer les services via des API REST.
Les méthodes appropriées ont été définies pour effectuer les opérations CRUD (Create, Read, Update, Delete) sur les entités.<br>
<br>
![Capture15](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/366fdd12-1d4b-4ecf-9c50-022ecabbc585)
<h3>TEST</h3>
<h4>Affichage</h4>

![Capture16](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/9fa4eefc-f2bd-4abf-837e-72da30234367)

<h4>Rechercher</h4>

![Capture17](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/ae44055f-ebbc-4ae3-b798-dfc67a56a100)

<h4>Inserssion</h4>

![Capture19](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/44ab4255-f223-4817-891d-2dedc14dba7c)

<h4>Suppression</h4>

![Capture20](https://github.com/RACHADDOUlFIKAR/Project_E_Bank/assets/97551741/a1cd77a3-3996-4360-b65f-a4aad7952002)

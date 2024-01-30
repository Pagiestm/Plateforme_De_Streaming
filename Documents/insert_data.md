# Ajout des valeurs dans les tables

```sql
INSERT INTO Films (id, Titre, Duree_du_film, Date_de_sortie)
VALUES (1, 'Zombieland', '01:28:00', '2009-11-25'),
	(2, 'Pulp Fiction', '02:34:00', '1994-10-26'),
       (3, 'L Empire contre-attaque', '02:04:00', '1980-08-20'),
       (4, 'Oppenheimer', '03:01:00', '2023-07-19'),
       (5, 'Inception', '02:28:00', '2010-07-21');


INSERT INTO realisateurs (id, Nom, Prenom)
VALUES (1, 'Ruben', 'Fleischer'),
	(2, 'Tarantino', 'Quentin'),
       (3, 'Kershner', 'Irvin'),
       (4, 'Nolan', 'Christopher');


INSERT INTO realiser (id, id_Films, id_Réalisateurs)
VALUES (1, 1, 1),
	(2, 2, 2),
       (3, 3, 3),
       (4, 4, 4),
       (5, 5, 4);


INSERT INTO Acteurs (id, Nom, Prenom, Date_de_naissance, Sexe, Role)
VALUES (1, 'Harrelson', 'Woody', '1961-07-23', 'M', 'Principal'),
       (2, 'Eisenberg', 'Jesse', '1983-10-05', 'M', 'Principal'),
       (3, 'Stone', 'Emma', '1988-11-06', 'F', 'Secondaire'),
       (4, 'Breslin', 'Abigail', '1996-04-14', 'F', 'Secondaire'),
       (5, 'Travolta', 'John', '1954-02-18', 'M', 'Principal'),
       (6, 'Jackson', 'Samuel L.', '1948-12-21', 'M', 'Principal'),
       (7, 'Stoltz', 'Eric', '1961-09-30', 'M', 'Secondaire'),
       (8, 'Ford', 'Harrison', '1942-07-13', 'M', 'Principal'),
       (9, 'Hamill', 'Mark', '1951-09-25', 'M', 'Principal'),
       (10, 'Jeremy', 'Bulloch', '1945-02-16', 'M', 'Secondaire'),
       (11, 'Murphy', 'Cillian', '1976-05-25', 'M', 'Principal'),
       (12, 'DiCaprio', 'Leonardo', '1974-11-11', 'M', 'Principal');


INSERT INTO jouer (id, id_Films, id_Acteurs)
VALUES (1, 1, 1),
	(2, 1, 2),
       (3, 1, 3),
       (4, 1, 4),
       (5, 2, 5),
       (6, 2, 6),
       (7, 2, 7),
       (8, 3, 8),
       (9, 3, 9),
       (10, 3, 10),
       (11, 4, 11),
       (12, 5, 12);


INSERT INTO utilisateurs (id, Nom, Prenom, Email, Mot_de_passe, Role)
VALUES (1, 'Pagies', 'Theotime', 'theotime@gmail.com', SHA2('motdepasse123', 256), 'ADMIN'),
       (2, 'Pinkman', 'Jesse', 'jesse@gmail.com', SHA2('motdepasse456', 256), 'USER');


INSERT INTO favoris (id, id_Films, id_Utilisateurs)
VALUES (1, 1, 1),
	(2, 2, 1),
       (3, 5, 1),
       (4, 3, 2),
       (5, 2, 2);
```

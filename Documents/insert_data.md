# Ajout des valeurs dans les tables

```sql
INSERT INTO films (Titre, Duree_du_film, Date_de_sortie)
VALUES ('Zombieland', '01:28:00', '2009-11-25'),
	('Pulp Fiction', '02:34:00', '1994-10-26'),
       ('L Empire contre-attaque', '02:04:00', '1980-08-20'),
       ('Oppenheimer', '03:01:00', '2023-07-19'),
       ('Inception', '02:28:00', '2010-07-21');


INSERT INTO realisateurs (Nom, Prenom)
VALUES ('Ruben', 'Fleischer'),
	('Tarantino', 'Quentin'),
       ('Kershner', 'Irvin'),
       ('Nolan', 'Christopher');


INSERT INTO realiser (id_Films, id_Réalisateurs)
VALUES (1, 1),
	(2, 2),
       (3, 3),
       (4, 4),
       (5, 4);


INSERT INTO acteurs (Nom, Prenom, Date_de_naissance, Sexe, Role)
VALUES ('Harrelson', 'Woody', '1961-07-23', 'M', 'Principal'),
       ('Eisenberg', 'Jesse', '1983-10-05', 'M', 'Principal'),
       ('Stone', 'Emma', '1988-11-06', 'F', 'Secondaire'),
       ('Breslin', 'Abigail', '1996-04-14', 'F', 'Secondaire'),
       ('Travolta', 'John', '1954-02-18', 'M', 'Principal'),
       ('Jackson', 'Samuel L.', '1948-12-21', 'M', 'Principal'),
       ('Stoltz', 'Eric', '1961-09-30', 'M', 'Secondaire'),
       ('Ford', 'Harrison', '1942-07-13', 'M', 'Principal'),
       ('Hamill', 'Mark', '1951-09-25', 'M', 'Principal'),
       ('Jeremy', 'Bulloch', '1945-02-16', 'M', 'Secondaire'),
       ('Murphy', 'Cillian', '1976-05-25', 'M', 'Principal'),
       ('DiCaprio', 'Leonardo', '1974-11-11', 'M', 'Principal');


INSERT INTO jouer (id_Films, id_Acteurs)
VALUES (1, 1),
	(1, 2),
       (1, 3),
       (1, 4),
       (2, 5),
       (2, 6),
       (2, 7),
       (3, 8),
       (3, 9),
       (3, 10),
       (4, 11),
       (5, 12);


INSERT INTO utilisateurs (Nom, Prenom, Email, Mot_de_passe, Role)
VALUES ('Pagies', 'Theotime', 'theotime@gmail.com', SHA2('motdepasse123', 256), 'ADMIN'),
       ('Pinkman', 'Jesse', 'jesse@gmail.com', SHA2('motdepasse456', 256), 'USER');


INSERT INTO favoris (id_Films, id_Utilisateurs)
VALUES (1, 1),
	(2, 1),
       (5, 1),
       (3, 2),
       (2, 2);
```

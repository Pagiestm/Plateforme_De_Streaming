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


INSERT INTO realiser (id_Films, id_Realisateurs)
VALUES (1, 1),
	(2, 2),
       (3, 3),
       (4, 4),
       (5, 4);


INSERT INTO acteurs (Nom, Prenom, Date_de_naissance, Sexe)
VALUES ('Harrelson', 'Woody', '1961-07-23', 'M'),
       ('Eisenberg', 'Jesse', '1983-10-05', 'M'),
       ('Stone', 'Emma', '1988-11-06', 'F'),
       ('Breslin', 'Abigail', '1996-04-14', 'F'),
       ('Travolta', 'John', '1954-02-18', 'M'),
       ('Jackson', 'Samuel L.', '1948-12-21', 'M'),
       ('Stoltz', 'Eric', '1961-09-30', 'M'),
       ('Ford', 'Harrison', '1942-07-13', 'M'),
       ('Hamill', 'Mark', '1951-09-25', 'M'),
       ('Jeremy', 'Bulloch', '1945-02-16', 'M'),
       ('Murphy', 'Cillian', '1976-05-25', 'M'),
       ('DiCaprio', 'Leonardo', '1974-11-11', 'M');


INSERT INTO jouer (id_Films, id_Acteurs, Role)
VALUES 
    (1, 1, 'Principal'),
    (1, 2, 'Principal'),
    (1, 3, 'Secondaire'),
    (1, 4, 'Secondaire'),
    (2, 5, 'Principal'),
    (2, 6, 'Principal'),
    (2, 7, 'Secondaire'),
    (3, 8, 'Principal'),
    (3, 9, 'Principal'),
    (3, 10, 'Secondaire'),
    (4, 11, 'Principal'),
    (5, 12, 'Principal');



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

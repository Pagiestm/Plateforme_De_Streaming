# Requête SQL


### requête 1 :

```sql
SELECT Titre, Date_de_sortie
FROM films
ORDER BY Date_de_sortie DESC;
```

### requête 2 :

```sql
SELECT Nom, Prenom, TIMESTAMPDIFF(YEAR, Date_De_naissance, NOW()) AS Age
FROM acteurs
HAVING Age > 30
ORDER BY Nom, Prenom;
```

### requête 3 :

```sql
SELECT Nom, Prenom
FROM jouer
INNER JOIN Acteurs ON Jouer.id_Acteurs = Acteurs.id
WHERE jouer.id_Films = 1
      AND acteurs.Role = 'Principal';
```

### requête 4 :

```sql
SELECT Nom AS Nom_Acteur, Prenom AS Prenom_Acteur, Titre
FROM Jouer
<<<<<<< HEAD
INNER JOIN acteurs ON Jouer.id_Acteurs = acteurs.id
INNER JOIN films ON Jouer.id_Films = films.id
WHERE acteurs.id = 4;
```

### requête 5 :

```sql
INSERT INTO Films (Titre, Duree_du_film, Date_de_sortie)
VALUES ('Forrest Gump', '02:20:00', '1994-10-05');
```

### requête 6 :

```sql
INSERT INTO acteurs (Nom, Prenom, Date_de_naissance, Sexe, Role)
VALUES ('Hanks', 'Tom', '1956-07-09', 'M', 'Principal');
```

### requête 7 : 

```sql

```
=======
INNER JOIN Acteurs ON Jouer.id_Acteurs = Acteurs.id
INNER JOIN Films ON Jouer.id_Films = Films.id
WHERE Acteurs.id = 4;
```
>>>>>>> daaba2555ea6a17d541254b308d35d1993d99296

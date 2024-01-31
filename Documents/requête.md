# Requêtes SQL


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
GROUP BY Nom, Prenom, Date_De_naissance
HAVING Age > 30
ORDER BY Nom, Prenom;
```

### requête 3 :

```sql
SELECT acteurs.Nom, acteurs.Prenom, Role
FROM jouer
INNER JOIN acteurs ON jouer.id_Acteurs = acteurs.id
WHERE jouer.id_Films = 1
      AND jouer.Role = 'Principal';
```

### requête 4 :

```sql
SELECT Nom AS Nom_Acteur, Prenom AS Prenom_Acteur, Titre
FROM jouer
INNER JOIN acteurs ON jouer.id_Acteurs = acteurs.id
INNER JOIN films ON jouer.id_Films = films.id
WHERE acteurs.id = 4;
```

### requête 5 :

```sql
INSERT INTO films (Titre, Duree_du_film, Date_de_sortie)
VALUES ('Forrest Gump', '02:20:00', '1994-10-05');
```

### requête 6 :

```sql
INSERT INTO acteurs (Nom, Prenom, Date_de_naissance, Sexe)
VALUES ('Hanks', 'Tom', '1956-07-09', 'M');
```

### requête 7 : 

```sql
UPDATE films
SET 
    Titre = "test"
WHERE id = 6;
```

### Requête 8 :

```sql
DELETE FROM acteurs WHERE id = 13;
```

### Requête 9 :

```sql
SELECT *
FROM acteurs
ORDER BY id DESC
LIMIT 3;
```

### Requête 10 :

```sql
SELECT *
FROM films
ORDER BY Date_de_sortie ASC
LIMIT 1;
```

### Requête 11 :

```sql
SELECT *
FROM acteurs
ORDER BY Date_de_naissance DESC
LIMIT 1;
```

### Requête 12 :

```sql
SELECT COUNT(Date_de_sortie) AS Nombre_de_films, Titre
FROM films
WHERE YEAR(Date_de_sortie) = 1990
ORDER BY Titre DESC;
```

### Requête 13 :

```sql
SELECT Titre, SUM(id_Acteurs IS NOT NULL) AS Somme_des_acteurs
FROM films 
LEFT JOIN Jouer ON films.id = jouer.id_Films
GROUP BY Titre;
```
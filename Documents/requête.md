# Requête SQL

```sql
SELECT Titre, Date_de_sortie
FROM Films
ORDER BY Date_de_sortie DESC;
```

```sql
SELECT Nom, Prenom, TIMESTAMPDIFF(YEAR, Date_De_naissance, NOW()) AS Age
FROM acteurs
HAVING Age > 30
ORDER BY Nom, Prenom;
```

```sql
SELECT Nom, Prenom
FROM Jouer
INNER JOIN Acteurs ON Jouer.id_Acteurs = Acteurs.id
WHERE Jouer.id_Films = 1
      AND Acteurs.Role = 'Principal';
```

```sql
SELECT Nom AS Nom_Acteur, Prenom AS Prenom_Acteur, Titre
FROM Jouer
INNER JOIN Acteurs ON Jouer.id_Acteurs = Acteurs.id
INNER JOIN Films ON Jouer.id_Films = Films.id
WHERE Acteurs.id = 4;
```

# Commandes MySQL pour la création de la base de données et des tables

## Création de la base de données

```sql
CREATE DATABASE PlateformeStreaming;
```

## Création des tables

```sql
CREATE TABLE Films(
   id INT PRIMARY KEY,
   Titre VARCHAR(50) NOT NULL,
   Durée_du_film TIME NOT NULL,
   Date_de_sortie DATE NOT NULL
);

CREATE TABLE Acteurs(
   id INT PRIMARY KEY,
   Nom VARCHAR(25) NOT NULL,
   Prénom VARCHAR(25) NOT NULL,
   Rôle VARCHAR(25) NOT NULL,
   Date_de_naissance DATE NOT NULL,
   Sexe VARCHAR(5) NOT NULL
);

CREATE TABLE Réalisateurs(
   id INT PRIMARY KEY,
   Nom VARCHAR(25) NOT NULL,
   Prénom VARCHAR(25) NOT NULL
);

CREATE TABLE Utilisateurs(
   id INT PRIMARY KEY,
   Nom VARCHAR(25) NOT NULL,
   Prénom VARCHAR(25) NOT NULL,
   Email VARCHAR(50) NOT NULL,
   Mot_de_passe VARCHAR(255) NOT NULL,
   Rôle VARCHAR(10) NOT NULL
);

CREATE TABLE Jouer(
   id INT PRIMARY KEY AUTO_INCREMENT,
   id_Films INT REFERENCES Films(id),
   id_Acteurs INT REFERENCES Acteurs(id)
);

CREATE TABLE Réaliser(
   id INT PRIMARY KEY AUTO_INCREMENT,
   id_Films INT REFERENCES Films(id),
   id_Réalisateurs INT REFERENCES Réalisateurs(id)
);

CREATE TABLE Favoris(
   id INT PRIMARY KEY AUTO_INCREMENT,
   id_Films INT REFERENCES Films(id),
   id_Utilisateurs INT REFERENCES Utilisateurs(id)
);

```
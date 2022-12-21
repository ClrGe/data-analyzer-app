# Data Analyzer App
#### *Service permettant d'afficher la fréquentation par gare en France pour la période 2015-2021*

---

Ce service s'appuit sur deux autres services : l'un, Data Analyzer DB (Python-Flask puisant dans une base SQLite3) renvoit les données du référentiel des gare (nom, département, région, identifiant...), et l'autre Data Analyzer File (Golang puisant dans des fichiers CSV) renvoit les données de fréquentation par année selon l'identifiant (Code UIC) fourni par le service Data Analyzer DB.

Les requêtes HTTP prennent comme paramètres de recherche le code postal ou la région. 

---
#### Pile logicielle

- Routage        : NGINX
- Runtime       : NodeJS
- Framework : NodeRED

---
#### Exemples de requête : 
- GET https://lab.jmg-conseil.eu/data/search?region=auvergne
- GET https://lab.jmg-conseil.eu/data/search?zipcode=75007

---
Documentation API : https://lab.jmg-conseil.eu/data/docs
Source des données :  https://ressources.data.sncf.com/

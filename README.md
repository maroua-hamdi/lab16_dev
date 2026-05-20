# LAB 16 : Maîtriser les Services dans une Application Android

## Cours
Programmation Mobile : Android avec Java

---

## 1. Objectif du lab

Ce lab a pour objectif de réaliser une application Android de type chronomètre en utilisant les Services Android.

L’application permet de démarrer et d’arrêter un chronomètre à partir d’une interface simple.  
Le temps est affiché directement dans l’application, et la logique de fonctionnement est liée à un service Android.

Dans ce lab, nous avons appris à utiliser :

- Un Foreground Service
- Une notification persistante
- Un Bound Service pour communiquer avec l’Activity
- Les boutons de démarrage et d’arrêt
- Le cycle de vie d’un Service Android
- Une interface Android simple en Java

---

## 2. Technologies utilisées

- Android Studio
- Java
- XML
- Android SDK
- Emulator Pixel 5
- Foreground Service
- Notification Android

---

## 3. Présentation du lab

Le but principal est de créer une application appelée Mon Temps.

Cette application affiche un chronomètre au centre de l’écran avec deux boutons :

- Démarrer : pour lancer le chronomètre
- Arrêter : pour arrêter le chronomètre

Le chronomètre commence à 00:00 puis continue à compter le temps.

---

## 4. Structure du projet


La structure générale du projet est la suivante :
---

app/
 └── src/
     └── main/
         ├── java/
         │   └── package_name/
         │       ├── MainActivity.java
         │       └── ChronometerService.java
         ├── res/
         │   └── layout/
         │       └── activity_main.xml
         └── AndroidManifest.xml

---

## 5. Étapes de réalisation

### Étape 1 : Création du projet

Nous avons commencé par créer un nouveau projet Android dans Android Studio.

Le langage utilisé est Java.

L’activité principale du projet est MainActivity.java.

---

### Étape 2 : Création de la classe Service

Nous avons créé une classe de service qui permet de gérer le fonctionnement du chronomètre.

Le service est responsable de calculer le temps et de garder la logique du chronomètre séparée de l’interface graphique.

---

### Étape 3 : Déclaration du service dans AndroidManifest.xml

Pour que le service soit reconnu par Android, il doit être déclaré dans le fichier AndroidManifest.xml.

Cette étape est obligatoire, sinon le service ne peut pas être lancé correctement.

---

### Étape 4 : Ajout des permissions nécessaires

Comme l’application utilise un Foreground Service, il faut gérer les permissions liées aux notifications.

Les notifications permettent d’indiquer que le service est actif.

---

### Étape 5 : Création de l’interface utilisateur

L’interface contient :

- Un titre : Mon Temps
- Un cercle contenant le temps du chronomètre
- Un bouton vert Démarrer
- Un bouton rouge Arrêter

L’interface est simple, lisible et adaptée à l’utilisation sur un émulateur Android.

---

### Étape 6 : Test de l’application

Après la programmation, l’application a été lancée sur un émulateur Pixel 5.

Les tests réalisés montrent que le chronomètre fonctionne correctement.

---



## 7. Emplacement des images dans le README

### Image 1 : Chronomètre au début


Cette image correspond à l’écran où l’horloge du téléphone affiche 10:05 et le chronomètre affiche 00:00.


<img width="330" height="606" alt="image" src="https://github.com/user-attachments/assets/bc450c48-e18a-4e67-bd3e-fcf753ef9195" />


---

### Image 2 : Chronomètre après démarrage



Cette image correspond à l’écran où l’horloge du téléphone affiche 10:06 et le chronomètre affiche 00:07.



<img width="325" height="599" alt="image" src="https://github.com/user-attachments/assets/8111c85d-e5da-476b-a101-123488674773" />


---

## 8. Résultat obtenu

Le résultat final est une application Android fonctionnelle permettant de lancer et d’arrêter un chronomètre.

Au lancement, le chronomètre affiche :

00:00

Après le démarrage, le temps commence à augmenter.

Dans notre test, le chronomètre affiche :

00:07

Cela montre que le service fonctionne correctement et que l’interface reçoit bien la mise à jour du temps.

---

## 9. Fonctionnement du service

Le service Android permet d’exécuter une tâche en arrière-plan.

Dans ce lab, le service est utilisé pour gérer le chronomètre.

Lorsqu’on clique sur le bouton Démarrer, le service commence le comptage du temps.

Lorsqu’on clique sur le bouton Arrêter, le service arrête le chronomètre.

---

## 10. Rôle du Foreground Service

Le Foreground Service est utilisé lorsque l’application doit continuer une tâche importante.

Dans ce cas, le chronomètre est une tâche active.

Android demande une notification persistante pour ce type de service afin d’informer l’utilisateur qu’une tâche est en cours.

---

## 11. Rôle du Bound Service

Le Bound Service permet à l’activité principale de communiquer avec le service.

Grâce à ce mécanisme, MainActivity peut recevoir les informations du service et afficher le temps dans l’interface.

---

## 12. Points importants appris dans ce lab

Dans ce lab, nous avons appris :

- Comment créer un service Android
- Comment déclarer un service dans AndroidManifest.xml
- Comment utiliser un Foreground Service
- Comment créer une notification persistante
- Comment démarrer et arrêter un service
- Comment afficher le temps dans une Activity
- Comment tester une application sur un émulateur Android

---

## 13. Conclusion

Ce lab nous a permis de comprendre l’utilisation des Services dans une application Android.

Nous avons réalisé une application simple de chronomètre, mais le principe utilisé peut être appliqué à plusieurs applications réelles comme :

- Les applications de sport
- Les lecteurs audio
- Les applications GPS
- Les applications de suivi du temps
- Les applications de suivi en arrière-plan

Les Services Android sont donc très importants pour créer des applications mobiles plus avancées.

---

## Auteur

Réalisé par : HAMDI Maroua

Lab : LAB 16 - Maîtriser les Services dans une Application Android

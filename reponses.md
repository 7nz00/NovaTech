1. l’identifiant court du premier commit :49e319a
2. le commit correspondant à l’ajout de la page Contact : e7a884a
3. le nombre actuel de commits : 6
4. la commande utilisée pour afficher l’historique sous forme graphique : git log --oneline --graph --all
5. Analyse un commit : git show e7a884a


Mission 9:

Reset réécrit l’historique en supprimant le commit et il 
ajoute un commit d’annulation : l’historique partagé reste intact,
et tout le monde peut simplement faire un pull.

Mission 11:

La commande git cherry-pick <id>, l’identifiant, et pourquoi pas de merge.
Un merge aurait importé les 3 commits, y compris les couleurs expérimentales et le texte de test alors
que cherry-pick copie uniquement qle commit voulu sur main

Mission 12:

1 = version majeure : changements incompatibles
0 = version mineure : nouvelles fonctionnalités compatibles
0 = correctif : corrections de bug

Les versions suivantes seraient :

bug mineur -> 1.0.1
nouvelle fonctionnalité compatible -> 1.1.0
refonte incompatible -> 2.0.0


Reponses finales :  

1. Quelle différence existe-t-il entre la zone de travail, la zone de staging et l’historique ?

La zone de travail contient les fichiers que j'ai modifié. 
Le staging (git add) contient ce qui partira dans le prochain commit. 
L’historique contient les commits enregistrés.

2. Pourquoi est-il préférable de réaliser une fonctionnalité sur une branche dédiée ?

Elle isole le développement. Je peux travailler en parallèle et abandonner 
facilement une fonctionnalité.

3. Quelle différence fondamentale existe-t-il entre les deux méthodes d’annulation utilisées dans
   les missions 8 et 9 ?

Reset réécrit l’historique en supprimant le commit : à utiliser en local seulement. 
Revert ajoute un commit inverse : sûr pour un commit déjà partagé.

4. Dans quelle situation est-il utile de mettre temporairement ses modifications de côté ?

C'est utile quand on doit changer de tâche ou de branche en urgence alors que le travail en cours 
n’est pas prêt à être commité.

5. Pourquoi la récupération d’un commit précis peut-elle être préférable à la fusion complète
   d’une branche ?

Il récupère seulement la correction utile, sans les commits expérimentaux ou non terminés de la branche.

6. À quoi sert HEAD ?

C’est le pointeur vers le commit et la branche sur lequel je me trouve actuellement.

7. Que représente HEAD~2 ?

C’est le commit situé deux commits avant HEAD.

8. À quoi sert un tag Git ?

Il marque un commit précis de façon permanente, en général une version publiée (v1.0.0).

9. Pourquoi des commits petits et précis facilitent-ils la maintenance d’un projet ?

Ils rendent l’historique lisible et facilitent la recherche de l’origine d’un bug.
On peut annuler ou cherry-pick une seule modif.

10. Pourquoi certains fichiers ne doivent-ils pas être versionnés ?

Ce sont des fichiers générés (logs, cache), ou des secrets (.env avec des mots de passe) 
qui ne doivent pas se retrouver publics.
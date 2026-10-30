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
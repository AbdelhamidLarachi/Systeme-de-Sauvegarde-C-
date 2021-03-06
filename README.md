Le cahier des charges de cette première version est le suivant :

- Le logiciel sera déployé dans les pays anglophones.
- Le logiciel sera en mode Console.
- Le logiciel devra utiliser un Framework 4.X
- L’interface doit permettre à l’utilisateur d’enregistrer jusqu’à 5 Travaux de sauvegarde. Les informations minimales à enregistrer pour un travail sont :

* Nom du travail
* Type de Sauvegarde
* Miroir
* Différentiel
* Répertoire Source
* Répertoire Cible

- L’utilisateur peut demander l’exécution d’un travail de sauvegarde spécifique ou l’exécution séquentielle des travaux.
Les répertoires pourront être sur des disques
* Locaux
* Externes
* Lecteurs réseaux

- Le logiciel doit journaliser, dans un fichier journalier, l’historique des travaux de sauvegarde. Les informations minimales attendues sont :

* Horodatage
* Nom de la tache
* Adresse du fichier Source
* Adresse du fichier de destination
* Taille du fichier
* Temps de transfert en ms (négatif si erreur)

- Le logiciel doit écrire en temps réel dans un fichier unique au format JSON (ou XML) l’état d’avancement des travaux de sauvegarde. Les informations à enregistrer pour chaque travail sont :

* Horodatage de l’écriture de l’information
* Le nombre total de fichiers éligibles 
* La taille des fichiers à transférer
* La progression        
* Nombre de fichiers restants 
* Taille des fichiers restants 
* Fichier en cours de sauvegarde 

- Tous les fichiers (configuration, historique, …) devront être au format JSON (ou XML) avec retour à la ligne entre chaque élément.

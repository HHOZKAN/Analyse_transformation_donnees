# Trafic routier à Paris : Av. de l'Opéra, St-Jacques, Bd Vincent Auriol

## La question
Comment la congestion varie-t-elle selon l'heure, le jour et l'axe, et à partir de quelle occupation chaque route bascule-t-elle en saturation ?

## Les données
Source : opendata.paris.fr
Axes étudiés : Av. de l'Opéra, St-Jacques, Bd Vincent Auriol (33 capteurs au total).
Période : mars à septembre 2026 (144 012 lignes avant nettoyage).

## Résultats
- Bd Vincent Auriol est l'axe le plus chargé, avec un débit moyen de 342 véhicules par heures contre 267 sur Av. de l'Opéra et 228 sur St-Jacques.
- La congestion est maximale en semaine, avec deux pics nets vers 8h-9h et 15h-18h (occupation médiane > 6%), contre une seule montée progressive en milieu de journée le week-end.
- Le seuil de bascule vers la congestion (capacité maximale) n'est pas le même partout : Av. de l'Opéra sature dès 22.5% d'occupation, contre 57.5% pour St-Jacques et Bd Vincent Auriol signe d'une capacité structurelle plus faible sur cet axe.
- Le diagramme fondamental (débit en fonction de l'occupation) confirme la théorie du trafic : le débit augmente avec l'occupation jusqu'au seuil de capacité, puis s'effondre brutalement au-delà (jusqu'à moins de 50 véh/h à 77% d'occupation).
- 12 054 lignes (8.4%) ne contenaient aucune information exploitable (débit et occupation manquants simultanément, capteur en état "Invalide") et ont été supprimées.


## Limites
Les capteurs en panne ("Invalide") ont été exclus, ce qui réduit la couverture temporelle réelle de certains axes. 26 des 33 capteurs du jeu de données partagent des séries de débit strictement identiques à un autre capteur, sans explication claire (doublons de capteurs ou artefact d'export) 
à vérifier avant toute conclusion par capteur individuel. Le nombre de voies par axe n'est pas connu, donc la comparaison des seuils de capacité entre axes reste indicative plutôt que normalisée.

## Lancer le projet
## Lancer le projet

Installation et exécution manuelle :

**pip install -r requirements.txt**
python download_data.py

une seule commande, avec le script fourni qui installe les dépendances, télécharge les données et exécute les 4 notebooks dans l'ordre :

**python run_all.py**

sinon éxécuter manuellement un par un les notebook dans l'ordre jour 1 à 4. 

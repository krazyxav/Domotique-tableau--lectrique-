# Domotique-tableau-lectricit-
Domotique pour lecture consommations, température eau chaude et commande chauffe-eau

Composition de cette partie:
- carte Arduino Uno
- sonde de température DS18B20 (avec résistance 4,7 kOhms entre 3,3v et Data),
- 3 cartes pzems (alimentation maison en tri-phasé
- 1 relais 5V pour commande relais chauffe-eau
- 1 ethernet W5500
- 1 alimentation 5V 2A

Fonctionnement:
Les données de la carte Arduino sont collectées et envoyées au serveur homeAssistant par protocole MQTT.
Le tableau de bord homeAssistant intègre un bouton pour commande du relais permettant l'alimentation du
chauffe-eau, ou par traitement automatique suivnat les possbilités de l'installation solaire.

Chronologie:
t0: mise à jour de l'état du bouton "chauffe-eau" 
t0 + 2 secondes: mise à jour homeAssistant de la température d'eau, et infos des Pzems
t0 + 4 secondes: lecture et mémorisation des infos des capteurs.

Pourquoi avoir scindé?
Pour une meilleue gestion de l'affichage du bouton de commande du chauffe-eau.

En cours de mise à jour

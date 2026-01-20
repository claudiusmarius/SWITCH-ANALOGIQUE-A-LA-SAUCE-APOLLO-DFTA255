# SWITCH-ANALOGIQUE-A-LA-SAUCE-APOLLO-DFTA255

📜 Contexte historique

Ce projet est né après le visionnage de la vidéo de CuriousMarc :
“Apollo Comms Part 37: Apollo's weirdest (but genius) analog circuit”.

Cette vidéo met en lumière un circuit analogique particulièrement atypique utilisé dans les systèmes de communication Apollo, reposant sur un composant aujourd’hui quasiment introuvable : le 3N68, un transistor bipolaire NPN à deux émetteurs.

Ce transistor était utilisé comme un multiplexeur analogique, bien avant l’apparition des circuits intégrés dédiés à cette fonction.

🔬 Le transistor 3N68

Le 3N68 est un BJT NPN possédant :

un collecteur

une base

deux émetteurs indépendants

Principe simplifié :

Les émetteurs E1 reçoivent des tensions analogiques

Les émetteurs E2 sont reliés ensemble vers une entrée de conversion (ADC)

La conduction n’est pas commandée par la jonction base-émetteur, mais par la polarisation de la jonction base-collecteur

👉 C’est ce mode de commande inhabituel qui rend le circuit à la fois génial… et déroutant.

🧠 Problème clé : une commande flottante

La polarisation de la jonction base-collecteur impose que les signaux de commande soient :

galvaniquement isolés

flottants

incapables de renvoyer des tensions parasites vers les signaux analogiques

À l’époque, les ingénieurs de la NASA ont résolu ce problème à l’aide de tores magnétiques à plusieurs enroulements, permettant :

l’excitation du transistor

l’injection de la commande BC

la suppression de la rémanence magnétique

Une solution élégante, robuste et parfaitement adaptée aux contraintes spatiales.

🧪 Objectif du projet

N’ayant pas réussi à me procurer un véritable transistor 3N68 malgré des recherches approfondies (États-Unis, Royaume-Uni, réseaux de collectionneurs), j’ai choisi de :

recréer le comportement fonctionnel du 3N68

comprendre ses limites

l’étudier via simulation LTspice

expliquer pourquoi une démonstration sur breadboard est délicate sans circuits auxiliaires supplémentaires

Ce dépôt n’a pas vocation à être une reproduction exacte, mais une exploration pédagogique d’un design analogique hors normes.

🧰 Contenu du dépôt

Schémas LTspice

Scripts de simulation

Notes techniques et commentaires

Explications sur les choix d’architecture

Références historiques

⚠️ Limitations

Le comportement réel du 3N68 dépend fortement de paramètres technologiques aujourd’hui disparus

Les simulations restent des approximations

Sans commande réellement flottante (transformateur, optique, etc.), les essais pratiques sont limités

📚 Sources et crédits

Vidéos et archives : NASA Image and Video Library
https://images.nasa.gov

Vidéo originale : CuriousMarc – Apollo Comms

Documentation technique Apollo (NTRS, archives NASA)

Les images et vidéos NASA sont dans le domaine public.

✨ Pourquoi ce projet

Ce projet est avant tout :

un hommage à l’ingénierie analogique des années 60

une démonstration de solutions élégantes sans circuits intégrés

une invitation à regarder autrement les composants « mal foutus »

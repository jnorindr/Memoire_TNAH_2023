# Mémoire TNAH 2023 :waning_crescent_moon:
Ce dépôt contient l'ensemble des documents liés au mémoire de stage rédigé dans le cadre du master Technologies numériques appliquées à l'histoire de l'École nationale des chartes. Intitulé _Le traitement des sources historiques par la vision artificielle. L'exemple des manuscrits d'astronomie de tradition ptoléméenne_, ce mémoire fait suite à un stage réalisé d'avril à juillet 2023 à l'Observatoire de Paris, au sein de l'équipe d'ingénierie du projet EIDA.

* `main.pdf` : mémoire de stage au format PDF.
* `main.tex` : fichier LaTeX complet du mémoire.
* `bibliographie` : contient le fichier BibTex de bibliographie.
* `images` : contient les images du mémoire.
* `templates` : contient les fichiers `.tex` de chaque chapitre du mémoire.
* `livrables` : livrables techniques réalisés lors du stage.

## Table des matières
### I. Construire une plateforme pour la détection : outils, interfaces et modèles de données
#### I.1. Le projet EiDA
* I.1.1. Contexte et objectifs du projet
* I.1.2. Sources primaires
#### I.2. Images et interopérabilité
* I.2.1. L’image comme source
* I.2.2. Le standard IIIF
#### I.3. Corpus historiques et jeux de données pour l’apprentissage machine
* I.3.1. Dimensions et cadre
* I.3.2. Objectifs scientifiques et possibilités numériques
  
### II. Intégrer la vision artificielle aux pratiques des chercheurs
#### II.1. Principes et utilisation de l’apprentissage profond
* II.1.1. Réseaux de neurones et _computer vision_
* II.1.2. Modèles de détection _off-the-shelf_ : outils libres pour l'extraction d’objets
#### II.2. Construire une plateforme pour la détection : outils, interfaces et modèles de données
* II.2.1. Penser une application pour la détection d'objet
* II.2.2. Annoter sur un GPU : extractorAPI
#### II.3. Intégrer la vision artificielle aux pratiques des chercheurs
* II.3.1. De la numérisation à l’annotation : l'automatisation du traitement des sources
* II.3.2. Médiation et documentation

### III. Perspectives pour le traitement des sources : vers un outil pour l’édition et la recherche
#### III.1. Éditer des diagrammes : vectorisation et édition critique
* III.1.1. Édition numérique des diagrammes astronomiques
* III.1.2. De l’image aux vecteurs : la vision artificielle pour l’édition numérique
#### III.2. Recherche de similarité et partitionnement de données
* III.2.1. La recherche de similarité pour l'étude de la circulation des images
* III.2.2. Le partitionnement de données : découvrir des motifs dans un corpus

## Livrables techniques
### extractorAPI
Dans le cadre du stage, une API pour le lancement sur un GPU de l'inférence d'un modèle de détection d'objet a été développée. Le code est disponible dans le dépôt suivant : [extractorAPI](https://github.com/jnorindr/extractorAPI).

En parallèle du développement de cette API, des modifications ont été apportés à l'application EIDA, dont le code n'est, à ce jour, pas public.

### Documentation de l'API
#### Wiki
Un [wiki pour extractorAPI](https://github.com/jnorindr/extractorAPI/wiki) a été rédigé et contient de la documentation à destination des développeurs. Il est composé de trois pages : 
* **Page d'accueil** : décrivant les fonctionnalités de l'API, son contexte de développement et la structure du dépôt.
* **Annotate images from EiDA with extractorAPI** : décrivant le _workflow_ d'annotation des numérisations et explicitant la connection avec l'application EIDA/VHS.
* **Deployment to production** : décrivant les étapes pour le déploiement en production de l'API et la gestion en contexte de production.

#### Autres documents
* `dh_seminar_june.pdf` : support de la présentation d'extractorAPI donnée à l'occasion du _DH Seminar_ du 13 juin 2023.
* `exapi_cahier_charges.pdf` : cahier des charges pour la réalisation d'extractorAPI.
* `exapi-eida_recettes_fonctionnelles.xslx` : document de recettes fonctionnelles pour tester la connexion entre l'application EIDA et extractorAPI.

### Documentation annexe
* `annotation_workflow_april.pdf` : document de description du _workflow_ d'annotation des numérisations avant la création de l'API.
* `yolov5_training_model.pdf` : document de description des étapes d'entraînement d'un modèle de détection à partir du _workflow_ d'entraînement de YOLOv5.

Ce projet, réalisé dans le cadre du cours de Deep Learning de master 2 (Executive Master Statistique & Intelligence artificielle) à l’Université Paris Dauphine, a pour objectif de différencier automatiquement les visages de trois catégories d’actrices sur des photos téléchargées sur internet :

Nathalie Portman
Keira Knightley
Autres actrices

Objectif :   
Construire un pipeline de classification d’images pour reconnaître à partir d’une photo à quelle catégorie d’actrice elle appartient.

Données :  
Les jeux de données sont constitués de photos réparties en trois classes principales :

  Jeu d'entraînement : 143 photos/catégorie
  Validation : 56 photos/catégorie
  Test : 56 photos/catégorie
  
Approche :
CNN fait maison : Prototype de réseau de neurones convolutif simple pour une première approche.
ConvNeXt : Architecture de pointe essayée sur l’ensemble des images originales puis sur les visages préalablement découpés.
Optimisation
Détection et Sélection de Visages

Utilisation de YOLOv8-Face pour détecter tous les visages présents sur les images.
Automatisation du choix du « meilleur » visage pour chaque photo selon trois critères : score de détection, surface occupée, et proximité du centre.

Régularisation L2 (weight decay) et dropout pour limiter l’overfitting et améliorer la généralisation.
Résultats :  
La meilleure performance est obtenue avec ConvNeXt, entraîné sur les visages détectés.

Conclusion : 
Ce projet démontre la capacité à développer une chaîne complète de traitement d’images basée sur la détection et la classification, à optimiser les hyperparamètres pour obtenir un modèle robuste et performant, véritablement utile pour des cas concrets de reconnaissance faciale.

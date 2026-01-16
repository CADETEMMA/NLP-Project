# NLP-Project

1) Choix du nettoyage du texte
Le nettoyage du texte permet de réduire le bruit (ponctuation, chiffres, mots fréquents peu informatifs) afin d’améliorer la qualité des représentations textuelles et les performances des modèles.

Les stopwords sont supprimés car ils apparaissent très fréquemment dans les textes mais apportent peu d’information discriminante pour identifier une pathologie.

La lemmatisation est préférée au stemming car elle conserve une forme linguistique correcte des mots, ce qui est particulièrement important dans un contexte médical où la précision du vocabulaire est essentielle.

2) Choix de TF-IDF pour les mots-clés
TF-IDF permet de pondérer les mots en fonction de leur importance dans un document tout en réduisant le poids des termes trop fréquents dans l’ensemble du corpus, ce qui facilite l’identification de mots-clés discriminants.

Contrairement à un simple comptage des mots, TF-IDF met en valeur les termes spécifiques à un document, ce qui est plus pertinent pour l’analyse et la classification de textes médicaux.

3) Choix du modèle de classification
La régression logistique a été choisie car elle est bien adaptée aux problèmes de classification de texte avec des représentations TF-IDF de grande dimension, tout en restant simple à interpréter.

Étant donné la taille limitée du corpus, un modèle simple est privilégié afin de limiter le risque de surapprentissage.

4) Choix de l’évaluation
L’accuracy est utilisée comme première métrique d’évaluation car les classes sont relativement équilibrées et l’objectif est de mesurer la capacité globale du modèle à prédire correctement la pathologie.

D’autres métriques comme la précision et le rappel pourraient être utilisées pour une analyse plus fine.

5) Choix du WordCloud 
Le nuage de mots permet une exploration visuelle rapide des termes les plus fréquents dans le corpus et facilite l’interprétation des données textuelles.

6) Choix du clustering 
Le clustering est utilisé pour explorer la structure du corpus sans information préalable sur les pathologies, afin d’identifier des regroupements naturels de documents basés sur leur similarité textuelle.

KMeans est choisi pour sa simplicité et son efficacité sur des données vectorisées comme TF-IDF.

Le nombre de clusters a été fixé en cohérence avec le nombre de pathologies présentes dans le corpus.

7) Limites du projet 
Ce projet repose sur un petit corpus de textes médicaux simulés ou anonymisés, ce qui limite la généralisation des résultats à des données médicales réelles.

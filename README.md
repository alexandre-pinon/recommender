# Recommender

A company granted access to KaDo: a database containing millions of bought items, divided in 3 categories. For instance, a bottle of red wine belongs to Famille: alcohol, Univers: wine, Maille: red wine.

In order to increase customers’ loyalty, the company expects to:
- segment the customers to get a clearer insight
- add charts and figures to help this company visualize their customers’ profiles
- build a recommender system to offer a gift to each client, based on their preferences
- use different type of recommender system: user based, item based. . .
- write a kickoff to describe precisely what to do with the dataset

***


># Outlier Detection and treatment method
>
>Pas de valeur manquante dans le dataset donc pas besoin de gérer cela.
>
>## Localisation des valeurs aberrantes:
>- Les valeurs aberrantes sont cherchées en mettant en relation prix et mois.
>- On recherche les valeurs aberrantes uniquement dans les prix.
>- Choix d'une méthode de détection selon la distance inter-quartile, appliqué séparément par mois, puis couplé par la prise en compte des quartiles min et max des mois.
>
>Utilisation de la méthode IQR (Inter-Quartile Range) avec 1.7
>
>## Traitement des valeurs aberrantes identifiées:
>- Démarche Active
>>- Remplacement par valeurs de substitution
>>- Suppression
>- Démarche Passive
>> Acceptation : minimisation de leur influence dans notre algorithme 
>
>Dans notre cas remplacement le plus approprié -> pas de perte de data, et moins de complexité par la suite.

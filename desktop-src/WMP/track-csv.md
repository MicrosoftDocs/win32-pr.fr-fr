---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Lecteur Windows Media des magasins en ligne, track.csv
- magasins en ligne, track.csv
- tapez 1 magasins en ligne, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9561897fb68f53aaa4ba33e433cf6d6120ec315
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403821"
---
# <a name="trackcsv"></a>track.csv

Ce fichier contient une entrée pour chaque piste dans le catalogue. Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme. Elle ne fait pas référence au type de données du contenu. Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.




| Champ | Obligatoire | Format | Description | 
|-------|----------|--------|-------------|
| TrackID tel | Oui | Entier non négatif. Exemple : 32789<br /> | Identificateur unique fourni par le fournisseur de contenu. Doit être inférieur à 2 ^ 32. Conseil en matière de performances : si les ID affectés aux pistes du même album sont numérotés consécutivement, la compression du catalogue est plus efficace. Toutefois, la numérotation consécutive des suivis d’albums n’est pas obligatoire.<br /> | 
| TrackTitle | Oui | Chaîne Unicode. Exemple : Raygun Robbers’Blues | Nom de la piste. | 
| Duration | Oui | Entier non négatif. Exemple : 543<br /> | Durée de la piste en secondes. | 
| TrackNumber | Oui | Entier non négatif. Exemple : 7<br /> | Numéro de piste sur l’album de la piste. Le suivi des nombres commence à 1 et augmente sur les jeux de disques. Le numéro de piste doit être inférieur à 256. un numéro de piste supérieur ou égal à 256 entraîne un comportement inattendu dans Lecteur Windows Media. | 
| TrackPrice | Oui | Chaîne Unicode. Exemple : $0,99. | Suivre le prix. Le symbole monétaire doit être inclus. La chaîne vide, 0 et-ont une signification particulière. Une chaîne vide indique que le prix est inconnu. Un zéro dans ce champ signifie que la piste est libre et un trait d’Union (-) indique que la piste ne peut pas être achetée. | 
| CanStream | Oui | Propriété booléenne. Peut être 0 ou 1. exemple : 0<br /> | Indique si la piste peut être diffusée en continu. | 
| CanDownload | Oui | Propriété booléenne. Peut être 0 ou 1. exemple : 0<br /> | Indique si la piste peut être téléchargée. | 
| HasPreviewClip | Oui | Propriété booléenne. Peut être 0 ou 1. exemple : 0<br /> | Indique si la piste a un clip d’aperçu. | 
| HasVideoClip | Oui | Propriété booléenne. Peut être 0 ou 1. exemple : 0<br /> | Indique si la piste a un clip vidéo. | 
| ParentalRating | Oui | Énumération. Peut être N, E ou C. exemple : N<br /> | Indique l’évaluation de l’avis parental. Les valeurs N, E et C sont pour normal, Explicit et Clean. | 
| LinkedAlbumID | Oui | Entier non négatif. Doit être l’ID d’un album. Exemple : 32423 | ID de l’album qui contient cette piste.<blockquote>[!Note]<br />Chaque suivi doit appartenir à un album. Autrement dit, pour chaque piste, le champ LinkedAlbumID doit être égal à l’un des ID d’album figurant dans le fichier album.csv.</blockquote><br /> | 
| LinkedTrackArtist_ArtistIDs | Oui | Liste d’entiers. La liste contient les ID d’artiste, séparés par des points-virgules. Exemple : 41322 ; 12321 ; 82123 ; | Liste d’ID correspondant aux artistes contributeurs. | 
| Composer | Non | Chaîne Unicode. Exemple : Beethoven | Compositeur de la piste. si le genre de la piste n’a pas le champ HasComposer défini, la valeur du champ Composer sera ignorée. Généralement utilisé uniquement pour les pistes Jazz ou classiques. | 
| Popularité | Oui | Entier non négatif ou float. exemple : 1252,6<br /> | Détermine la position de la piste dans la liste lorsqu’elle est triée par popularité. Un nombre inférieur indique une popularité plus élevée. | 
| StarRating | Non | Float. exemple : 4,21<br /> | l’évaluation de l’étoile sera arrondie à l’étoile 1/4 la plus proche par Lecteur Windows Media avant d’être affichée dans l’interface utilisateur de Lecteur Windows Media. | 




 

 

 






---
title: album.csv
description: album.csv
ms.assetid: 7308e849-7227-480e-937a-8e9091bdec98
keywords:
- Lecteur Windows Media des magasins en ligne, album.csv
- magasins en ligne, album.csv
- tapez 1 magasins en ligne, album.csv
- album.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750926a3d01f8d65d7ed11c69436049e39ea3dabf0e446ede8a8c9dcecc53bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004199"
---
# <a name="albumcsv"></a>album.csv

Ce fichier contient une entrée pour chaque album inclus dans le catalogue. Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

Tous les champs de album.csv sont requis.

La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme. Elle ne fait pas référence au type de données du contenu. Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.



| Champ             | Format                                                                   | Description                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlbumID           | Entier non négatif. Exemple : 789456<br/>                          | Identificateur de l’album, unique dans album.csv. Doit être inférieur à 2 ^ 32.                                                                                                                                                                           |
| AlbumName         | Chaîne Unicode. Exemple : meilleurs résultats<br/>                         | Titre de l’album                                                                                                                                                                                                                                          |
| AlbumArtist       | Entier non négatif. Exemple : 34331<br/>                           | ArtistID de l’artiste. Une seule valeur est autorisée. Peut être l’ID de « différents artistes » ou similaire.                                                                                                                                                    |
| AlbumLabel        | Chaîne Unicode. Doit être vide.                                         | Non utilisé dans cette version. Doit être vide.                                                                                                                                                                                                           |
| ReleaseDate       | Chaîne Unicode au format AAAA-MM-JJ. Exemple : 2005-0-0<br/>        | Date de publication. La valeur 0 est autorisée pour le jour ou le mois.                                                                                                                                                                                               |
| AlbumPrice        | StringExample Unicode : $12,49<br/>                                 | Prix de l’album. Le symbole monétaire doit être inclus. La chaîne vide, 0 et-ont une signification particulière. Une chaîne vide indique un prix inconnu. « 0 » indique que la piste est libre. Un trait d’Union (« - ») indique que l’album ne peut pas être acheté. |
| LinkedGenreID     | Entier non négatif. Exemple : 12<br/>                              | ID du genre principal de l’album. Une seule valeur est autorisée.                                                                                                                                                                                        |
| LinkedSubGenreIDs | Format : n ; n ; n ; Exemple : 32 ; 44 ; 663 ;<br/>                             | Liste des ID de sous-genres associés. Un point-virgule de fin est autorisé à la fin de la liste.                                                                                                                                                             |
| Popularité        | Il peut s’agir d’un entier non négatif ou d’une valeur décimale. Exemple : 1256,24<br/> | Niveau de popularité déterminé par le service. Peut être le classement de cet album dans la liste des albums triés par popularité. 0 est autorisé.                                                                                                              |
| IsRecentlyAdded   | Propriété booléenne. Peut avoir la valeur 0 ou 1.                                                  | Indicateur signalant que l’album a été ajouté récemment, tel que déterminé par le service.                                                                                                                                                                    |
| IsFeatured        | Propriété booléenne. Peut avoir la valeur 0 ou 1.                                                  | Indicateur signalant qu’il s’agit d’un album proposé.                                                                                                                                                                                                      |
| EditorialGlyph    | Entier non négatif. Doit correspondre à 0.                                       | La version n’est pas utilisée. Doit correspondre à 0.                                                                                                                                                                                                                    |
| FeedsAreAvailable | Propriété booléenne. Peut avoir la valeur 0 ou 1.                                                  | Non utilisé dans cette version. Doit correspondre à 0.                                                                                                                                                                                                               |



 

 

 






---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player Online stores, artist.csv
- magasins en ligne, artist.csv
- tapez 1 magasins en ligne, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311350"
---
# <a name="artistcsv"></a>artist.csv

Ce fichier contient une entrée pour chaque artiste dans le catalogue. Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

Tous les champs de artist.csv sont requis.

La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme. Elle ne fait pas référence au type de données du contenu. Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.



| Champ                  | Format                                            | Description                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ArtistID               | Entier non négatif. Exemple : 65832              | Identificateur unique de l’artiste, unique dans artist.csv. Doit être inférieur à 2 ^ 32.                        |
| ArtistName             | Chaîne Unicode. Exemple : Don Funk<br/>       | Nom complet de l’artiste.                                                                               |
| LinkedGenreID          | Entier non négatif. Exemple : 313<br/>      | GenreID du genre principal de l’artiste. Doit être un genre principal et non un sous-genre. Une seule valeur est autorisée. |
| LinkedSimilarArtistIDs | N/A                                               | Non utilisé dans cette version. Doit être vide.                                                                 |
| Popularité             | Il peut s’agir d’un entier ou d’une valeur décimale. Exemple : 1252,25 | Classement de la popularité. Peut être la position dans la liste lorsqu’elle est triée par popularité.                             |
| FeedsAvailable         | Propriété booléenne. Format : \[ 0 \| 1 \] exemple : 0<br/>    | Non utilisé dans cette version. Doit être vide.                                                                 |



 

 

 






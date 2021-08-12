---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Lecteur Windows Media des magasins en ligne, artist.csv
- magasins en ligne, artist.csv
- tapez 1 magasins en ligne, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4192d0817740ac872d1c08989f2f57b4715d65fea6b9a6c9a199dcdabe267e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583041"
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



 

 

 






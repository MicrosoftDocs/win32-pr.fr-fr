---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Lecteur Windows Media des magasins en ligne, genre.csv
- magasins en ligne, genre.csv
- tapez 1 magasins en ligne, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008431"
---
# <a name="genrecsv"></a>genre.csv

Ce fichier contient une entrée pour chaque genre représenté dans le catalogue. Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

Tous les champs de genre.csv sont requis.

La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme. Elle ne fait pas référence au type de données du contenu. Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.



| Champ             | Format                                                    | Description                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de genre \_         | Entier non négatif. Exemple : 22<br/>               | Identificateur de genre, unique dans genre.csv. Doit être inférieur à 2 ^ 32. Un maximum de 64 genres est possible.                                             |
| GenreTitle        | Chaîne Unicode. Exemple : Rock<br/>                   | Nom complet du genre.                                                                                                                                |
| FeedsAreAvailable | Boolean. format : \[ 0 \| 1\]<br/> Exemple : 0<br/> | Indique si le comportement « radio Play » est possible en sautant à un flux.                                                                          |
| HasComposer       | Boolean. format : \[ 0 \| 1\]<br/> Exemple : 1<br/> | True si ce genre doit enregistrer les informations de compositeur dans le catalogue. S’il n’est pas défini, les informations du compositeur sont ignorées et ne sont pas compilées dans le catalogue. |



 

 

 






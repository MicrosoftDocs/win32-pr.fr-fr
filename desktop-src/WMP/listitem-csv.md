---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Windows Media Player Online stores, listitem.csv
- magasins en ligne, listitem.csv
- tapez 1 magasins en ligne, listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379807"
---
# <a name="listitemcsv"></a>listitem.csv

Ce fichier contient des entrées pour chaque élément inclus dans une liste. Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

Tous les champs sont obligatoires.

La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme. Elle ne fait pas référence au type de données du contenu. Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.



| Champ              | Format                                          | Description                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| \_ListId liés     | Entier non négatif. Exemple : 465<br/>    | ID de la liste dont cet élément fait partie.                                                                               |
| \_ListItem lié   | Entier non négatif. Exemple : 684793<br/> | ID de l'élément. Il peut s’agir de l’ID d’une piste, d’un album, d’un artiste, d’un genre, d’un sous-genre, d’un flux radio ou d’une autre liste. |
| ItemPositionInList | Entier non négatif. Exemple : 5<br/>      | Position de l’élément dans sa liste. Le premier élément d’une liste est à la position 0.                                   |



 

 

 






---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player Online stores, subgenre.csv
- magasins en ligne, subgenre.csv
- tapez 1 magasins en ligne, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512063"
---
# <a name="subgenrecsv"></a>subgenre.csv

Ce fichier contient une entrée pour chaque sous-genre représenté dans le catalogue. Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme. Elle ne fait pas référence au type de données du contenu. Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.



| Champ             | Obligatoire | Format                                                                                            | Description                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SubGenreID        | Oui      | Entier non négatif.                                                                             | Identificateur de sous-genre (ID), unique dans subgenre.csv. Jusqu’à 1024 sous-genres sont autorisés.                                                                   |
| SubGenreTitle     | Oui      | Chaîne Unicode. Exemple : musique de danse intelligente (IDM)<br/>                                  | Nom complet du sous-genre.                                                                                                                                    |
| SubGenreSubtitle  | Non       | Chaîne Unicode. Exemple : nouvelle musique électronique à percussion, qui n’est pas très pure.<br/> | Décrivez la signification du nom d’affichage du sous-genre. Doit être inférieur à 64 caractères.                                                                     |
| FeedsAreAvailable | Oui      | Boolean. format : \[ 0 \| 1\]<br/> Exemple : 0<br/>                                         | Indique s’il est possible d’accéder à un flux.                                                                                          |
| \_GenreID liés   | Oui      | Entier non négatif (GenreID). Exemple : 12<br/>                                             | GenreID du genre parent. Un seul parent est autorisé.                                                                                              |
| SortOrderRank     | Oui      | Entier non négatif. Exemple : 23<br/>                                                       | Classement, idéalement unique, utilisé pour trier les sous-genres dans l’interface utilisateur. Si le genre parent a 10 sous-genres, il peut s’agir d’un entier compris entre 1 et 10. |



 

 

 






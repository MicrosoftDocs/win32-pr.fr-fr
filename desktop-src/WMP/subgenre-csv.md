---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Lecteur Windows Media des magasins en ligne, subgenre.csv
- magasins en ligne, subgenre.csv
- tapez 1 magasins en ligne, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10242e955423d75174d04899285dcd3dc20ea2ea4a761d2ab3ba53561c4d41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122939"
---
# <a name="subgenrecsv"></a>subgenre.csv

Ce fichier contient une entrée pour chaque sous-genre représenté dans le catalogue. Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme. Elle ne fait pas référence au type de données du contenu. Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.



| Champ             | Obligatoire | Format                                                                                            | Description                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SubGenreID        | Oui      | Entier non négatif.                                                                             | Identificateur de sous-genre (ID), unique dans subgenre.csv. Jusqu’à 1024 sous-genres sont autorisés.                                                                   |
| SubGenreTitle     | Oui      | Chaîne Unicode. exemple : Musique de danse Intelligent (IDM)<br/>                                  | Nom complet du sous-genre.                                                                                                                                    |
| SubGenreSubtitle  | Non       | Chaîne Unicode. Exemple : nouvelle musique électronique à percussion, qui n’est pas très pure.<br/> | Décrivez la signification du nom d’affichage du sous-genre. Doit être inférieur à 64 caractères.                                                                     |
| FeedsAreAvailable | Oui      | Boolean. format : \[ 0 \| 1\]<br/> Exemple : 0<br/>                                         | Indique s’il est possible d’accéder à un flux.                                                                                          |
| \_GenreID liés   | Oui      | Entier non négatif (GenreID). Exemple : 12<br/>                                             | GenreID du genre parent. Un seul parent est autorisé.                                                                                              |
| SortOrderRank     | Oui      | Entier non négatif. Exemple : 23<br/>                                                       | Classement, idéalement unique, utilisé pour trier les sous-genres dans l’interface utilisateur. Si le genre parent a 10 sous-genres, il peut s’agir d’un entier compris entre 1 et 10. |



 

 

 






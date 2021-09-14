---
title: radio.csv
description: radio.csv
ms.assetid: 8b0a1852-b6c9-4598-b1ab-c679362794b3
keywords:
- Lecteur Windows Media des magasins en ligne, radio.csv
- magasins en ligne, radio.csv
- tapez 1 magasins en ligne, radio.csv
- radio.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5271f3a87b32d27996f61e444723f537a09cb827
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010948"
---
# <a name="radiocsv"></a>radio.csv

Ce fichier contient des entrées pour chaque flux radio inclus dans le catalogue. Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous. Les champs doivent apparaître dans l’ordre indiqué.

La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme. Elle ne fait pas référence au type de données du contenu. Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.



| Champ              | Obligatoire | Format                                                                                                               | Description                                                                                                                        |
|--------------------|----------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| RadioID            | Oui      | Entier non négatif.                                                                                                | ID du flux radio qui est unique dans radio.csv.                                                                             |
| Radiotitre         | Oui      | Chaîne Unicode. Exemple : accès essentiels<br/>                                                                    | Titre du flux radio.                                                                                                                  |
| Sous-titre      | Non       | Chaîne Unicode. Exemple : Top 40.                                                                                     | Sous-titre du flux radio. Souvent un nom de genre ou de sous-genre.                                                                               |
| Manuel         | Oui      | Chaîne Unicode. Exemple : Terri Lee Duffy                                                                             | Nom du programmeur du flux radio. Il est recommandé de ne pas dépasser 32 caractères.                                     |
| PrimaryGenre       | Oui      | Entier non négatif.                                                                                                | ID du genre principal. Une seule valeur est autorisée.                                                                            |
| Humeur               | Oui      | Chaîne Unicode. Exemple : amusant ; amiable; énergique stylisé exuberant<br/>                                       | Une série d’adjectifs qui décrivent la musique. Aucun point-virgule de fin après le dernier adjectif.                                    |
| Category           | Oui      | chaîne Unicode                                                                                                       | Non utilisé dans cette version. Doit être vide.                                                                                         |
| Description        | Non       | Chaîne Unicode. Exemple : Upbeat-friendly Music pour les artistes ayant essayé et réel qui ne déçu pas.<br/> | Description conviviale de l’affichage dans les pages de propriétés. Il est recommandé de ne pas dépasser 256 caractères.                   |
| Popularité         | Oui      | Entier non négatif ou valeur décimale. Exemple : 31<br/>                                                         | Classement de la popularité parmi les alimentations radio. Peut avoir la valeur 0.                                                                                    |
| StarRating         | Non       | Float. exemple : 3,21<br/>                                                                                       | Optionnel. La valeur, généralement comprise entre 0 et 5, est arrondie au 1/4 le plus proche pour l’affichage dans l’interface utilisateur.                   |
| IsSubscriptionOnly | Oui      | Propriété booléenne. Peut avoir la valeur 0 ou 1.                                                                                              | Indique si le flux est disponible par abonnement uniquement.                                                                      |
| IsRecentlyAdded    | Oui      | Propriété booléenne. Peut avoir la valeur 0 ou 1.                                                                                              | Indique si ce flux a été ajouté récemment.                                                                                    |
| IsFeatured         | Oui      | Propriété booléenne. Peut avoir la valeur 0 ou 1.                                                                                              | Indique si le flux est en vedette.                                                                                            |
| EditorialGlyph     | Oui      | Entier non négatif. Doit correspondre à 0.                                                                                   | Non utilisé dans cette version. Doit correspondre à 0.                                                                                             |
| SortOrderRank      | Oui      | Entier non négatif.                                                                                                | Peut être utilisé pour déterminer l’ordre de tri lorsque toutes les stations sont répertoriées dans l’interface utilisateur. Doit avoir la valeur 0 si ce champ n’est pas utilisé. |



 

 

 






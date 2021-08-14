---
description: Dans une base de données relationnelle, les lignes retournées par une requête de recherche doivent répondre à toutes les conditions appelées par la requête. en revanche, une requête de recherche Windows peut retourner des documents qui remplissent les conditions de recherche à différents degrés.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Compréhension des valeurs de pertinence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d28efba26d12e0260d76e02fc4e042e72612df34d383a0e22a34f4be9d9fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226804"
---
# <a name="understanding-relevance-values"></a>Compréhension des valeurs de pertinence

Dans une base de données relationnelle, les lignes retournées par une requête de recherche doivent répondre à toutes les conditions appelées par la requête. en revanche, une requête de recherche Windows peut retourner des documents qui remplissent les conditions de recherche à différents degrés.

Par exemple, la recherche du terme « programme » dans une base de données relationnelle produit des enregistrements qui contiennent l’orthographe spécifique du mot. Si un enregistrement contient une ou 100 instances du mot n’a aucun impact sur les résultats. en revanche, Windows recherche renvoie une valeur de pertinence associée aux documents correspondants. La pertinence des documents dont le titre contient « Program » est supérieure à celles qui contiennent le mot uniquement dans le dernier paragraphe. De même, les documents contenant des variations du terme de recherche, par exemple « Programs » et « Programming », correspondent également à et sont retournés par la requête.

Windows Les requêtes de recherche retournent des valeurs de pertinence entières dans la colonne nommée « rank ».

De plus :

-   Les valeurs de classement retournées par la requête sont des entiers compris entre 0 et 1000.
-   Des valeurs de classement plus élevées indiquent des documents qui correspondent mieux aux conditions de recherche.
-   Les valeurs de classement s’appliquent uniquement à la requête actuelle. elles ne peuvent donc pas être comparées pour les résultats d’une requête à l’autre.
-   Les valeurs de classement sont relatives aux autres documents correspondant à la requête. Par conséquent, la valeur de classement d’un document particulier dépend des autres documents qui correspondent également à la requête.
-   Les valeurs de classement des éléments correspondant à un prédicat purement relationnel sont 1000.

Vous pouvez manipuler les valeurs de classement retournées en utilisant des pondérations de colonnes [dans les prédicats de clause](-search-sql-contains.md) WHERE et [FREETEXT](-search-sql-freetext.md) WHERE, et la clause Rank by.

 

 




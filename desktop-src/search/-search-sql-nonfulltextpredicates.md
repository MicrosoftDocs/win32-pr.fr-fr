---
description: Le langage de requête de recherche Microsoft Windows prend en charge six prédicats de recherche de texte non intégral. Les prédicats décrits dans cette section sont répertoriés dans le tableau suivant.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Prédicats de texte non intégral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544625"
---
# <a name="non-full-text-predicates"></a>Prédicats de texte non intégral

Le langage de requête de recherche Microsoft Windows prend en charge six prédicats de recherche de texte non intégral. Les prédicats décrits dans cette section sont répertoriés dans le tableau suivant.



| Prédicat de texte non intégral                                                    | Description                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Toutes les opérations de bits and au niveau du bit](all-bitwise.md)                            | Est un ensemble de mots clés qui concernent le test des bits dans un type intégral.                                                                                                               |
| [DATEADD, fonction](-search-sql-dateadd.md)                                | Effectue des calculs de date et d’heure pour les propriétés correspondantes ayant des types de date. Utilisez la fonction DATEADD pour obtenir des dates et des heures dans un laps de temps spécifié avant le présent.     |
| [Prédicat LIKE](-search-sql-like.md)                                     | Compare les valeurs de colonne à l’aide de critères spéciaux simples avec des caractères génériques.                                                                                                          |
| [Comparaison de valeurs littérales](-search-sql-literalvaluecomparison.md)         | Compare les valeurs de colonne à la chaîne, à la date, à l’horodatage, à la valeur numérique et à d’autres valeurs littérales. Ce prédicat prend en charge les inégales telles que supérieur à (' > ') et inférieur à (' < '). |
| [Comparaisons à valeurs multiples (tableau)](-search-sql-multivaluedcomparisons.md) | Compare des colonnes à valeurs multiples à un tableau de littéraux à valeurs multiples.                                                                                                                   |
| [Prédicat NULL](-search-sql-null.md)                                     | Détecte les valeurs de colonne qui ne sont pas définies pour le document.                                                                                                                              |



 

> [!IMPORTANT]
> Les requêtes de recherche utilisant le prédicat **null** peuvent exiger que la recherche Windows analyse le catalogue entier, ce qui peut ralentir les performances de la requête.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 




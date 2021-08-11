---
description: 'En savoir plus sur : clause ORDER BY'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Clause ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3815ddecc659a47d7cf2c8547b49e878c54ba6bf8537e2589eea4441d9d3f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227184"
---
# <a name="order-by-clause"></a>Clause ORDER BY

La clause ORDER BY trie les résultats en fonction de la valeur d’une ou plusieurs colonnes que vous spécifiez. Voici la syntaxe de la clause ORDER BY :


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



Le spécificateur de colonne doit être une colonne valide. Vous pouvez utiliser le spécificateur de colonne pour faire référence aux colonnes dans l’ordre dans lequel elles apparaissent dans la requête. La première colonne de la requête est numérotée 1. Vous pouvez inclure plusieurs colonnes dans la clause ORDER BY, séparées par des virgules.

Le spécificateur de direction facultatif peut être « ASC » pour l’ordre croissant (de faible à élevé) ou « DESC » pour l’ordre décroissant (de haut en bas). Si vous ne fournissez pas de spécificateur de direction, la valeur par défaut, par ordre croissant, est utilisée. Si vous spécifiez plusieurs colonnes, mais que vous ne spécifiez pas toutes les directions, la direction que vous spécifiez en dernier est appliquée à chaque colonne jusqu’à ce que vous modifiiez explicitement la direction.

Par exemple, dans la clause ORDER BY suivante, les colonnes A, B, C et G sont triées dans l’ordre croissant, tandis que les colonnes D, E et F sont triées dans l’ordre décroissant.


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[FROM, clause](-search-sql-from.md)
</dt> <dt>

[RANK BY, clause](-search-sql-rankby.md)
</dt> <dt>

[Instruction SELECT](-search-sql-select.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




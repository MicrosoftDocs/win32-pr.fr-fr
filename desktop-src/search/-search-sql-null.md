---
description: Le prédicat NULL indique si le document a une valeur pour la colonne indiquée.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Prédicat NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd80ea6cba2009b398c8cdd0a2926240e3ce78309ca3f8511fb6ba286f44a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058119"
---
# <a name="null-predicate"></a>Prédicat NULL

Le prédicat **null** indique si le document a une valeur pour la colonne indiquée.

Le prédicat **null** a la syntaxe suivante :


```
...WHERE <column> IS [NOT] NULL
```



Le mot clé NOT facultatif inverse le résultat. La colonne peut être un [identificateur](-search-sql-identifiers.md)standard ou délimité.

> [!IMPORTANT]
> Pour déterminer si une colonne a la valeur **null** , vous devez utiliser le prédicat **null** . L’utilisation de la valeur **null** dans un prédicat de comparaison n’est pas valide. « WHERE Column IS **null**» est correct. « WHERE column = **null**» n’est pas valide.

 

## <a name="example"></a>Exemple

L’exemple suivant retourne des documents qui n’ont pas de valeur System. Video. Director.


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Prédicat LIKE](-search-sql-like.md)
</dt> <dt>

[Comparaison de valeurs littérales](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Comparaisons à valeurs multiples (tableau)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




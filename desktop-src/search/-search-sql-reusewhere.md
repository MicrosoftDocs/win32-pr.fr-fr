---
description: La clause WHERE d’une requête spécifie un ensemble d’éléments pour lesquels faire correspondre les résultats.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: ReuseWhere fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f073a7ac0d5faf5973d08ff53ccebdacf8bead080a53e2d9a4a6ae9ed5724db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944659"
---
# <a name="reusewhere-function"></a>ReuseWhere fonction)

La clause [Where](-search-sql-where.md) d’une requête spécifie un ensemble d’éléments pour lesquels faire correspondre les résultats. Les requêtes suivantes peuvent partager le travail effectué pour une requête précédente à l’aide de la fonction ReuseWhere dans une nouvelle clause WHERE de la requête. Les requêtes qui tirent parti de cette fonction s’exécutent plus rapidement.

## <a name="examples"></a>Exemples

Le scénario suivant montre comment utiliser la fonction ReuseWhere :

1.  Vous exécutez la requête suivante :
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  À partir de l’ensemble de lignes retourné, vous recevez un [ID WHERE](-search-sql-rowset-properties.md), *Query1WhereID*.

    Où ID est une propriété d’ensemble de lignes avec PROPSET {aa6ee6b0-e828-11D0-B2-3e-00-AA-00-47-FC-01}, PROPID 8 et le type UI4.

3.  Vous émettez une deuxième requête avec la fonction ReuseWhere, en transmettant le *Query1WhereID* de l’étape 2 :
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

La deuxième requête équivaut à ce qui suit :


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



La fonction ReuseWhere peut être utilisée anwhere dans la clause [Where](-search-sql-where.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Clause WHERE](-search-sql-where.md)
</dt> <dt>

[Propriétés du rowset](-search-sql-rowset-properties.md)
</dt> </dl>

 

 




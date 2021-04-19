---
description: À la suite de l’instruction SELECT, vous utilisez la clause FROM pour spécifier l’emplacement où rechercher les documents correspondants.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: FROM, clause
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517459"
---
# <a name="from-clause"></a>FROM, clause

À la suite de l’instruction SELECT, vous utilisez la clause FROM pour spécifier l’emplacement où rechercher les documents correspondants. La syntaxe de la clause FROM pour une requête locale est la suivante :


```
FROM [<ComputerName>.]SystemIndex
```



Actuellement, Windows Search ne prend en charge qu’un seul catalogue, SystemIndex. Pour interroger le catalogue local d’un ordinateur distant, incluez le nom de l’ordinateur avant le catalogue et un chemin d’accès UNC (Universal Naming Convention) sur l’ordinateur distant dans la clause SCOPE ou DIRECTORY.

Vous spécifiez une étendue en tant que restriction dans la clause WHERE, comme décrit dans la rubrique relative aux [prédicats d’étendue et de répertoire](-search-sql-folderdepth.md) .

## <a name="examples"></a>Exemples


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



Dans le second des exemples précédents, la requête cible un ordinateur distant appelé « zarascomputer ». Notez que ce nom d’ordinateur apparaît dans les clauses FROM et SCOPE. Dans le troisième exemple, la requête cible un nom de partage « Users » sur un serveur nommé « Server » (où le chemin d’accès UNC est le \\ \\ serveur \\ users).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Vue d’ensemble de la syntaxe de recherche SQL](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[Instruction SELECT](-search-sql-select.md)
</dt> <dt>

[Clause WHERE](-search-sql-where.md)
</dt> <dt>

[Prédicats d’étendue et de répertoire](-search-sql-folderdepth.md)
</dt> </dl>

 

 




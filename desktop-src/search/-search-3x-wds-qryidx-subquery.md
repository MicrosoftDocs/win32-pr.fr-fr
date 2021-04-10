---
description: Une sous-requête est un fichier de recherche enregistré ( \* . search-ms) que vous pouvez utiliser comme filtre pour une nouvelle requête.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argument de sous-requête (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951033"
---
# <a name="subquery-argument-windows-search"></a>Argument de sous-requête (Windows Search)

Une sous-requête est un fichier de recherche enregistré ( \* . search-ms) que vous pouvez utiliser comme filtre pour une nouvelle requête. Les résultats de la sous-requête sont utilisés comme source pour la nouvelle requête. Par exemple, imaginons que vous ayez plusieurs fichiers de recherche enregistrés qui limitent une requête par liste de distribution de courrier électronique : myDepartment. search-ms, TeamProject. search-ms et corporatewide. search-ms. L’utilisation de l' `subquery` argument vous permet de limiter les recherches par courrier électronique à tout ou partie de ces recherches enregistrées.

Cette rubrique est organisée comme suit :

-   [Exemple](#example)
-   [Rubriques connexes](#related-topics)

## <a name="example"></a>Exemple


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec des arguments Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Arguments de l’identificateur de paramètres régionaux](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argument de navigation](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argument de syntaxe](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argument STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 




---
title: Liaison au point de départ de la recherche
description: Le point de départ d’une recherche est un conteneur qui contient directement ou indirectement les objets recherchés.
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- Active Directory des exemples Active Directory, liaison à un point de départ de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741986e651848c1d2a88ab016b63365db91b26b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461970"
---
# <a name="binding-to-the-search-start-point"></a>Liaison au point de départ de la recherche

Le point de départ d’une recherche est un conteneur qui contient directement ou indirectement les objets recherchés. La recherche ne sera pas effectuée dans les conteneurs au-dessus du point de départ de la recherche. Par exemple, prenez la structure de répertoire hypothétique suivante :

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

Si une recherche est effectuée pour tous les objets et que le point de départ de la recherche est « Container 2 », seuls « Object 3 » et « Object 4 » sont récupérés. Si la recherche a été effectuée avec le point de départ de recherche sur « Container 1 », « Object 1 » et « Object 2 » sont récupérés.

Pour établir une liaison avec le point de départ de la recherche, établissez une liaison avec l’ADsPath du conteneur qui sera le point de départ de la recherche.

 

 





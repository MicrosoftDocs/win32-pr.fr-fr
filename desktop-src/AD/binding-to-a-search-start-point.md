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
# <a name="binding-to-the-search-start-point"></a><span data-ttu-id="aeb5b-104">Liaison au point de départ de la recherche</span><span class="sxs-lookup"><span data-stu-id="aeb5b-104">Binding to the Search Start Point</span></span>

<span data-ttu-id="aeb5b-105">Le point de départ d’une recherche est un conteneur qui contient directement ou indirectement les objets recherchés.</span><span class="sxs-lookup"><span data-stu-id="aeb5b-105">The start point for a search is a container that directly or indirectly contains the objects searched for.</span></span> <span data-ttu-id="aeb5b-106">La recherche ne sera pas effectuée dans les conteneurs au-dessus du point de départ de la recherche.</span><span class="sxs-lookup"><span data-stu-id="aeb5b-106">The search will not be performed in containers above the search start point.</span></span> <span data-ttu-id="aeb5b-107">Par exemple, prenez la structure de répertoire hypothétique suivante :</span><span class="sxs-lookup"><span data-stu-id="aeb5b-107">For example, take the following hypothetical directory structure:</span></span>

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

<span data-ttu-id="aeb5b-108">Si une recherche est effectuée pour tous les objets et que le point de départ de la recherche est « Container 2 », seuls « Object 3 » et « Object 4 » sont récupérés.</span><span class="sxs-lookup"><span data-stu-id="aeb5b-108">If a search is performed for all objects and the search start point is "Container 2", only "Object 3" and "Object 4" would be retrieved.</span></span> <span data-ttu-id="aeb5b-109">Si la recherche a été effectuée avec le point de départ de recherche sur « Container 1 », « Object 1 » et « Object 2 » sont récupérés.</span><span class="sxs-lookup"><span data-stu-id="aeb5b-109">If the same search was performed with the search start point at "Container 1", "Object 1" and "Object 2" would be retrieved.</span></span>

<span data-ttu-id="aeb5b-110">Pour établir une liaison avec le point de départ de la recherche, établissez une liaison avec l’ADsPath du conteneur qui sera le point de départ de la recherche.</span><span class="sxs-lookup"><span data-stu-id="aeb5b-110">To bind to the search start point, bind to the ADsPath of the container that will be the search start point.</span></span>

 

 





---
title: Résolution de plusieurs composants d’agrégation prenant en charge la même interface
description: Il est rare que deux extensions exposent la même interface à ADSI.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Résolution de plusieurs composants d’agrégation prenant en charge la même interface ADSI
- résolution de plusieurs composants d’agrégation prenant en charge la même interface ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509363"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a><span data-ttu-id="f536f-105">Résolution de plusieurs composants d’agrégation prenant en charge la même interface</span><span class="sxs-lookup"><span data-stu-id="f536f-105">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>

<span data-ttu-id="f536f-106">Il est rare que deux extensions exposent la même interface à ADSI.</span><span class="sxs-lookup"><span data-stu-id="f536f-106">It is uncommon that two extensions expose the same interface to ADSI.</span></span> <span data-ttu-id="f536f-107">Dans ce cas, les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="f536f-107">If this happens, the following rules apply:</span></span>

-   <span data-ttu-id="f536f-108">Si une interface, telle que **IMyInterface**, est prise en charge par l’agrégateur (ADSI) et tous les objets d’extension, **QueryInterface** retourne toujours le **IMyInterface** pour ADSI.</span><span class="sxs-lookup"><span data-stu-id="f536f-108">If an interface, such as **IMyInterface**, is supported by both the aggregator (ADSI) and any extension objects, **QueryInterface** always returns the **IMyInterface** for ADSI.</span></span>
-   <span data-ttu-id="f536f-109">Si une interface, telle que **IMyInterface**, n’est pas prise en charge par l’agrégateur (ADSI), mais qu’elle est prise en charge par plus d’un objet d’extension, **QueryInterface** retourne le **IMyInterface** du premier objet d’extension listé dans le Registre qui prend en charge l’interface.</span><span class="sxs-lookup"><span data-stu-id="f536f-109">If an interface, such as **IMyInterface**, is not supported by the aggregator (ADSI), but is supported by more than one extension object, **QueryInterface** returns the **IMyInterface** of the first extension object listed in the registry that supports the interface.</span></span>

<span data-ttu-id="f536f-110">N’oubliez pas que l’ordre des composants dans le registre affecte également la résolution des conflits de noms dans Automation.</span><span class="sxs-lookup"><span data-stu-id="f536f-110">Be aware that the order of components in the registry also affects the resolution of name conflicts in Automation.</span></span> <span data-ttu-id="f536f-111">Pour plus d’informations, consultez [résolution des conflits de noms de fonctions/propriétés dans Automation dans les extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="f536f-111">For more information, see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>

 

 





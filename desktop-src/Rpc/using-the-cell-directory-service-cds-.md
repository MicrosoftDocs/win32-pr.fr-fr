---
title: Utilisation des service d’annuaire de cellules/service d’annuaires de cellules (CDS)
description: Si vous avez des CD, vous pouvez l’utiliser à la place de Microsoft Locator.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- Appel de procédure distante RPC, tâches, utilisation du service d’annuaire de cellules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0029bf78308d6963d615daa04eaf87f3617ebbb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673254"
---
# <a name="using-the-cell-directory-service-cds"></a><span data-ttu-id="63200-104">Utilisation des service d’annuaire de cellules/service d’annuaires de cellules (CDS)</span><span class="sxs-lookup"><span data-stu-id="63200-104">Using the Cell Directory Service (CDS)</span></span>

<span data-ttu-id="63200-105">Si vous avez des CD, vous pouvez l’utiliser à la place de Microsoft Locator.</span><span class="sxs-lookup"><span data-stu-id="63200-105">If you have CDS, you can use it instead of Microsoft Locator.</span></span> <span data-ttu-id="63200-106">Modifiez les entrées de Registre comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="63200-106">Change the registry entries as shown:</span></span>

``` syntax
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    NetworkAddress
 
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    Endpoint
```

<span data-ttu-id="63200-107">La modification de ces entrées pointera vers un ordinateur de passerelle qui exécute NSID.</span><span class="sxs-lookup"><span data-stu-id="63200-107">Changing these entries will point to a gateway computer that is running the NSID.</span></span> <span data-ttu-id="63200-108">Ce sera utilisé en tant que localisateur maître.</span><span class="sxs-lookup"><span data-stu-id="63200-108">This will be used as the master locator.</span></span> <span data-ttu-id="63200-109">En cas de panne, il n’y aura pas de recherche de remplacement.</span><span class="sxs-lookup"><span data-stu-id="63200-109">In the event of a crash, there will be no search for a replacement.</span></span>

 

 





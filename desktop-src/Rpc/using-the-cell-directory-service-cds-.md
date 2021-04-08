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
# <a name="using-the-cell-directory-service-cds"></a>Utilisation des service d’annuaire de cellules/service d’annuaires de cellules (CDS)

Si vous avez des CD, vous pouvez l’utiliser à la place de Microsoft Locator. Modifiez les entrées de Registre comme indiqué ci-dessous :

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

La modification de ces entrées pointera vers un ordinateur de passerelle qui exécute NSID. Ce sera utilisé en tant que localisateur maître. En cas de panne, il n’y aura pas de recherche de remplacement.

 

 





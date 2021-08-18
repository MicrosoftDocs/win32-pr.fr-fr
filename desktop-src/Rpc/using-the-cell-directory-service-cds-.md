---
title: Utilisation des service d’annuaire de cellules/service d’annuaires de cellules (CDS)
description: Si vous avez des CD, vous pouvez l’utiliser à la place de Microsoft Locator.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- Appel de procédure distante RPC, tâches, utilisation du service d’annuaire de cellules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df9058d917396a4e2e2dc3579768c3f3d5b46242b34c0fa5411c6d2204ed20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010636"
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

 

 





---
description: Windows charge et exécute la DLL Microsoft GINA standard (MSGina.dll). Pour charger une autre GINA, vous devez modifier une valeur de clé de registre.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Chargement et exécution d’une DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a4e8d68a1e1846a28e1db9402d730834768a132a7c502021fd101f20926f54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140952"
---
# <a name="loading-and-running-a-gina-dll"></a>Chargement et exécution d’une DLL GINA

Windows charge et exécute la DLL Microsoft GINA standard (MSGina.dll). Pour charger une autre [*Gina*](../secgloss/g-gly.md), vous devez modifier la valeur de clé de Registre suivante :

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

Si la valeur de clé GinaDLL est présente, elle doit contenir le nom d’une DLL GINA, que [*Winlogon*](../secgloss/w-gly.md) chargera et utilise.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération et test d’une DLL GINA](building-and-testing-a-gina-dll.md)
</dt> <dt>

[Fonctions d’exportation GINA](authentication-functions.md)
</dt> <dt>

[Structures GINA](authentication-structures.md)
</dt> <dt>

[Fonctions GINA des services Terminal Server](terminal-services-gina-functions.md)
</dt> </dl>

 

 

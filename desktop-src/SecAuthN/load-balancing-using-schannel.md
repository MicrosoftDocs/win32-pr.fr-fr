---
description: Chaque serveur peut définir une valeur de clé de Registre MachineID dans le Registre qui est définie comme partie fixe de l’ID de session.
ms.assetid: 1B373496-1C1B-4D4B-8CAC-B572C58E43A2
title: Équilibrage de charge à l’aide de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce190d665f4cc41eb0615a2ddc83e0ee54798d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865729"
---
# <a name="load-balancing-using-schannel"></a>Équilibrage de charge à l’aide de Schannel

Chaque serveur peut définir une valeur de clé de Registre MachineID dans le Registre qui est définie comme partie fixe de l’ID de session. La clé de Registre MachineID est un type de valeur **reg \_ DWORD** . L’équilibreur de charge peut utiliser cette partie de l’ID de session pour déterminer quel serveur a généré la session SSL et peut conserver le mappage vers ce serveur. L’ID de session fait partie de la négociation SSL/TLS envoyée sur le réseau. Le code d’équilibrage de charge doit utiliser la deuxième **valeur DWORD** dans l’ID de session lors de la reprise ou de la reconnexion au client. Le deuxième **DWORD** de l’ID de session aléatoire généré par un serveur Schannel est remplacé par le **DWORD** stocké dans le registre. La valeur de Registre pour la valeur **DWORD** ne peut pas être 0xFFFFFFFF.

La valeur de la clé de Registre est la suivante.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            SecurityProviders
               SCHANNEL
                  MachineID<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

 

 




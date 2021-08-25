---
title: Obtention de System Information MCI
description: Obtention de System Information MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- Commande MCI_SYSINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fa6cc0757bc09aa16216f2f20385bf31b44bb88e27ea64e091ff3909d8d57e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893219"
---
# <a name="obtaining-mci-system-information"></a>Obtention de System Information MCI

La commande [sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md)) obtient des informations système sur les périphériques MCI. MCI gère cette commande sans la transmettre à un appareil MCI. Pour l’interface de message de commande, MCI retourne les informations système dans la structure de [**MCI \_ sysinfo \_**](mci-sysinfo-parms.md) .

Vous pouvez utiliser la commande **sysinfo** (MCI \_ sysinfo) pour récupérer des informations telles que le nombre de périphériques MCI sur un système, le nombre de périphériques MCI d’un type particulier, le nombre d’appareils MCI ouverts et les noms des appareils. Cette commande est souvent appelée plusieurs fois pour récupérer une information particulière. Par exemple, vous pouvez récupérer le nombre d’appareils d’un type particulier dans le premier appel, puis énumérer les noms des appareils dans la suivante.

 

 





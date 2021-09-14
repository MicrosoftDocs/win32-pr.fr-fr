---
title: Obtention de System Information MCI
description: Obtention de System Information MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- Commande MCI_SYSINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119585"
---
# <a name="obtaining-mci-system-information"></a>Obtention de System Information MCI

La commande [sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md)) obtient des informations système sur les périphériques MCI. MCI gère cette commande sans la transmettre à un appareil MCI. Pour l’interface de message de commande, MCI retourne les informations système dans la structure de [**MCI \_ sysinfo \_**](mci-sysinfo-parms.md) .

Vous pouvez utiliser la commande **sysinfo** (MCI \_ sysinfo) pour récupérer des informations telles que le nombre de périphériques MCI sur un système, le nombre de périphériques MCI d’un type particulier, le nombre d’appareils MCI ouverts et les noms des appareils. Cette commande est souvent appelée plusieurs fois pour récupérer une information particulière. Par exemple, vous pouvez récupérer le nombre d’appareils d’un type particulier dans le premier appel, puis énumérer les noms des appareils dans la suivante.

 

 





---
title: Récupération d’informations sur un appareil
description: Récupération d’informations sur un appareil
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- Commande MCI_GETDEVCAPS
- Commande MCI_STATUS
- Commande MCI_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10acb53fa1a961fe7a70042350f8d889d9fdf572
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940286"
---
# <a name="retrieving-information-about-a-device"></a>Récupération d’informations sur un appareil

Chaque appareil répond aux commandes de [**capacité**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)), d' [**État**](status.md) ([**\_ État MCI**](mci-status.md)) et d' [**informations**](info.md) ([**MCI \_ info**](mci-info.md)). Ces commandes obtiennent des informations sur l’appareil. Par exemple, la commande suivante retourne « true » si un appareil **cdaudio** peut éjecter le disque :


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Les indicateurs indiqués pour les commandes obligatoires et de base fournissent une quantité minimale d’informations sur un appareil. De nombreux appareils complètent les commandes requises et de base avec des indicateurs étendus pour fournir des informations supplémentaires sur l’appareil.

 

 





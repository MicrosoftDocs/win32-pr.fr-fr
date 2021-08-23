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
ms.openlocfilehash: 412ccfb8819ac1c76cd3f0114fa114c877280de959f605535fd4bb83d224a91e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689089"
---
# <a name="retrieving-information-about-a-device"></a>Récupération d’informations sur un appareil

Chaque appareil répond aux commandes de [**capacité**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)), d' [**État**](status.md) ([**\_ État MCI**](mci-status.md)) et d' [**informations**](info.md) ([**MCI \_ info**](mci-info.md)). Ces commandes obtiennent des informations sur l’appareil. Par exemple, la commande suivante retourne « true » si un appareil **cdaudio** peut éjecter le disque :


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Les indicateurs indiqués pour les commandes obligatoires et de base fournissent une quantité minimale d’informations sur un appareil. De nombreux appareils complètent les commandes requises et de base avec des indicateurs étendus pour fournir des informations supplémentaires sur l’appareil.

 

 





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
# <a name="retrieving-information-about-a-device"></a><span data-ttu-id="2a9f7-106">Récupération d’informations sur un appareil</span><span class="sxs-lookup"><span data-stu-id="2a9f7-106">Retrieving Information About a Device</span></span>

<span data-ttu-id="2a9f7-107">Chaque appareil répond aux commandes de [**capacité**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)), d' [**État**](status.md) ([**\_ État MCI**](mci-status.md)) et d' [**informations**](info.md) ([**MCI \_ info**](mci-info.md)).</span><span class="sxs-lookup"><span data-stu-id="2a9f7-107">Every device responds to the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)), and [**info**](info.md) ([**MCI\_INFO**](mci-info.md)) commands.</span></span> <span data-ttu-id="2a9f7-108">Ces commandes obtiennent des informations sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-108">These commands obtain information about the device.</span></span> <span data-ttu-id="2a9f7-109">Par exemple, la commande suivante retourne « true » si un appareil **cdaudio** peut éjecter le disque :</span><span class="sxs-lookup"><span data-stu-id="2a9f7-109">For example, the following command returns "true" if a **cdaudio** device can eject the disc:</span></span>


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="2a9f7-110">Les indicateurs indiqués pour les commandes obligatoires et de base fournissent une quantité minimale d’informations sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-110">The flags listed for the required and basic commands provide a minimum amount of information about a device.</span></span> <span data-ttu-id="2a9f7-111">De nombreux appareils complètent les commandes requises et de base avec des indicateurs étendus pour fournir des informations supplémentaires sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-111">Many devices supplement the required and basic commands with extended flags to provide additional information about the device.</span></span>

 

 





---
title: Obtention d’informations sur le système MCI
description: Obtention d’informations sur le système MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- Commande MCI_SYSINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939866"
---
# <a name="obtaining-mci-system-information"></a><span data-ttu-id="1ee3a-104">Obtention d’informations sur le système MCI</span><span class="sxs-lookup"><span data-stu-id="1ee3a-104">Obtaining MCI System Information</span></span>

<span data-ttu-id="1ee3a-105">La commande [sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md)) obtient des informations système sur les périphériques MCI.</span><span class="sxs-lookup"><span data-stu-id="1ee3a-105">The [sysinfo](sysinfo.md) ([**MCI\_SYSINFO**](mci-sysinfo.md)) command obtains system information about MCI devices.</span></span> <span data-ttu-id="1ee3a-106">MCI gère cette commande sans la transmettre à un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="1ee3a-106">MCI handles this command without relaying it to any MCI device.</span></span> <span data-ttu-id="1ee3a-107">Pour l’interface de message de commande, MCI retourne les informations système dans la structure de [**MCI \_ sysinfo \_**](mci-sysinfo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee3a-107">For the command-message interface, MCI returns the system information in the [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

<span data-ttu-id="1ee3a-108">Vous pouvez utiliser la commande **sysinfo** (MCI \_ sysinfo) pour récupérer des informations telles que le nombre de périphériques MCI sur un système, le nombre de périphériques MCI d’un type particulier, le nombre d’appareils MCI ouverts et les noms des appareils.</span><span class="sxs-lookup"><span data-stu-id="1ee3a-108">You can use the **sysinfo** (MCI\_SYSINFO) command to retrieve information such as the number of MCI devices on a system, the number of MCI devices of a particular type, the number of open MCI devices, and the names of the devices.</span></span> <span data-ttu-id="1ee3a-109">Cette commande est souvent appelée plusieurs fois pour récupérer une information particulière.</span><span class="sxs-lookup"><span data-stu-id="1ee3a-109">This command is often called more than once to retrieve a particular piece of information.</span></span> <span data-ttu-id="1ee3a-110">Par exemple, vous pouvez récupérer le nombre d’appareils d’un type particulier dans le premier appel, puis énumérer les noms des appareils dans la suivante.</span><span class="sxs-lookup"><span data-stu-id="1ee3a-110">For example, you might retrieve the number of devices of a particular type in the first call and then enumerate the names of the devices in the next.</span></span>

 

 





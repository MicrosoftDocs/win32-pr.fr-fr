---
title: Codes de contrôle d’e/s de périphérique
description: Codes de contrôle d’e/s de périphérique
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player, codes de contrôle d’e/s de périphérique
- Windows Media Player, codes de contrôle
- Gestionnaire de périphériques Windows Media
- codes de contrôle d’e/s de périphérique
- codes de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517966"
---
# <a name="device-io-control-codes"></a><span data-ttu-id="7ded7-108">Codes de contrôle d’e/s de périphérique</span><span class="sxs-lookup"><span data-stu-id="7ded7-108">Device I/O Control Codes</span></span>

<span data-ttu-id="7ded7-109">Le lecteur Windows Media 10 ou version ultérieure définit les codes de contrôle d’e/s des appareils Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="7ded7-109">Windows Media Player 10 or later defines Windows Media Device Manager device I/O control codes.</span></span> <span data-ttu-id="7ded7-110">Le tableau suivant contient les codes de contrôle et leurs descriptions.</span><span class="sxs-lookup"><span data-stu-id="7ded7-110">The following table contains the control codes and their descriptions.</span></span>



| <span data-ttu-id="7ded7-111">Code de contrôle d’e/s</span><span class="sxs-lookup"><span data-stu-id="7ded7-111">I/O control code</span></span>                      | <span data-ttu-id="7ded7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ded7-112">Value</span></span>      | <span data-ttu-id="7ded7-113">Description</span><span class="sxs-lookup"><span data-stu-id="7ded7-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ded7-114">**aller \_ - \_ retour des métadonnées IOCTL WMP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ded7-114">**IOCTL\_WMP\_METADATA\_ROUND\_TRIP**</span></span> | <span data-ttu-id="7ded7-115">0x31504d57</span><span class="sxs-lookup"><span data-stu-id="7ded7-115">0x31504d57</span></span> | <span data-ttu-id="7ded7-116">Gère le transfert des informations relatives aux modifications apportées aux valeurs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="7ded7-116">Manages transfer of information about changes that occurred to metadata values.</span></span> <span data-ttu-id="7ded7-117">Consultez [extensions de périphérique pour le transfert de métadonnées accéléré](device-extensions-for-accelerated-metadata-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="7ded7-117">See [Device Extensions for Accelerated Metadata Transfer](device-extensions-for-accelerated-metadata-transfer.md).</span></span>                                                                                                                                                                          |
| <span data-ttu-id="7ded7-118">**synchronisation de l' \_ appareil WMP avec IOCTL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ded7-118">**IOCTL\_WMP\_DEVICE\_CAN\_SYNC**</span></span>     | <span data-ttu-id="7ded7-119">0x32504d57</span><span class="sxs-lookup"><span data-stu-id="7ded7-119">0x32504d57</span></span> | <span data-ttu-id="7ded7-120">Indique si un périphérique portable prend en charge la synchronisation automatique.</span><span class="sxs-lookup"><span data-stu-id="7ded7-120">Indicates whether a portable device supports automatic synchronization.</span></span> <span data-ttu-id="7ded7-121">Le lecteur Windows Media 10 ou version ultérieure ne fournit aucune mémoire tampon d’entrée. La mémoire tampon de sortie doit retourner une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7ded7-121">Windows Media Player 10 or later provides no input buffer.The output buffer must return a **DWORD** value.</span></span> <span data-ttu-id="7ded7-122">La valeur 1 signifie que l’appareil prend en charge la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="7ded7-122">A value of 1 means the device supports synchronization.</span></span> <span data-ttu-id="7ded7-123">La valeur 0 signifie que l’appareil ne prend pas en charge la synchronisation automatique.</span><span class="sxs-lookup"><span data-stu-id="7ded7-123">A value of 0 means the device does not support automatic synchronization.</span></span><br/> <span data-ttu-id="7ded7-124">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="7ded7-124">See Remarks for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ded7-125">Notes</span><span class="sxs-lookup"><span data-stu-id="7ded7-125">Remarks</span></span>

<span data-ttu-id="7ded7-126">Ces codes de contrôle sont définis dans wmpdevices. h.</span><span class="sxs-lookup"><span data-stu-id="7ded7-126">These control codes are defined in wmpdevices.h.</span></span>

<span data-ttu-id="7ded7-127">Si l’appareil ne prend pas en charge la synchronisation des **appareils par IOCTL \_ WMP \_ \_ \_**, le lecteur Windows Media 10 ou version ultérieure suppose que l’appareil prend en charge la synchronisation automatique.</span><span class="sxs-lookup"><span data-stu-id="7ded7-127">If the device does not support **IOCTL\_WMP\_DEVICE\_CAN\_SYNC**, Windows Media Player 10 or later assumes the device supports automatic synchronization.</span></span> <span data-ttu-id="7ded7-128">Notez que même si cette valeur peut interdire la synchronisation automatique, des critères supplémentaires sont utilisés pour déterminer si l’appareil prend en charge la synchronisation automatique.</span><span class="sxs-lookup"><span data-stu-id="7ded7-128">Note that while this value can disallow automatic synchronization, there are additional criteria used to determine whether the device supports automatic synchronization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ded7-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ded7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ded7-130">**Extensions d’appareil pour le transfert de métadonnées accéléré**</span><span class="sxs-lookup"><span data-stu-id="7ded7-130">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[<span data-ttu-id="7ded7-131">**Lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7ded7-131">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 






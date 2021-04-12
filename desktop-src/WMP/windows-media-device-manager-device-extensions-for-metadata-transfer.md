---
title: Extensions d’appareils Windows Media Gestionnaire de périphériques pour le transfert de métadonnées
description: Extensions d’appareils Windows Media Gestionnaire de périphériques pour le transfert de métadonnées
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player, extensions d’appareils
- Windows Media Player, extensions
- Lecteur Windows Media, métadonnées
- Windows Media Player, transfert de métadonnées accéléré
- Lecteur Windows Media, transfert des métadonnées accéléré
- métadonnées, extensions de périphérique
- métadonnées, extensions
- extensions d’appareils, transfert de métadonnées
- extensions, transfert de métadonnées
- transfert de métadonnées accéléré
- métadonnées, transfert accéléré
- extensions d’appareils, transfert de métadonnées accéléré
- extensions, transfert de métadonnées accéléré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462306"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a><span data-ttu-id="04ba9-116">Extensions d’appareils Windows Media Gestionnaire de périphériques pour le transfert de métadonnées</span><span class="sxs-lookup"><span data-stu-id="04ba9-116">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>

<span data-ttu-id="04ba9-117">Pour activer le transfert de métadonnées accéléré, les fabricants d’appareils qui ne prennent pas en charge MTP doivent effectuer les opérations suivantes dans le code source :</span><span class="sxs-lookup"><span data-stu-id="04ba9-117">To enable accelerated metadata transfer, manufacturers of devices that do not support MTP must do the following in source code:</span></span>

-   <span data-ttu-id="04ba9-118">Définir **la \_ \_ \_ prise en charge des appareils WMDM WMP**.</span><span class="sxs-lookup"><span data-stu-id="04ba9-118">Define **WMP\_WMDM\_DEVICE\_SUPPORT**.</span></span>
-   <span data-ttu-id="04ba9-119">Incluez wmpdevices. h, qui est installé dans le cadre du kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="04ba9-119">Include wmpdevices.h, which is installed as part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="04ba9-120">Wmpdevices. h définit les structures suivantes.</span><span class="sxs-lookup"><span data-stu-id="04ba9-120">Wmpdevices.h defines the following structures.</span></span>



| <span data-ttu-id="04ba9-121">Structure</span><span class="sxs-lookup"><span data-stu-id="04ba9-121">Structure</span></span>                                                                                 | <span data-ttu-id="04ba9-122">Description</span><span class="sxs-lookup"><span data-stu-id="04ba9-122">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04ba9-123">WMP \_ WMDM \_ métadonnées aller- \_ \_ retour \_ PC2DEVICE</span><span class="sxs-lookup"><span data-stu-id="04ba9-123">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | <span data-ttu-id="04ba9-124">Structure utilisée par le lecteur Windows Media pour demander des informations de synchronisation des métadonnées accélérées à partir d’appareils portables qui ne prennent pas en charge MTP.</span><span class="sxs-lookup"><span data-stu-id="04ba9-124">Structure used by Windows Media Player to request accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |
| [<span data-ttu-id="04ba9-125">WMP \_ WMDM \_ métadonnées aller- \_ \_ retour \_ DEVICE2PC</span><span class="sxs-lookup"><span data-stu-id="04ba9-125">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | <span data-ttu-id="04ba9-126">Structure utilisée par le lecteur Windows Media pour recevoir des informations de synchronisation des métadonnées accélérées à partir d’appareils portables qui ne prennent pas en charge MTP.</span><span class="sxs-lookup"><span data-stu-id="04ba9-126">Structure used by Windows Media Player to receive accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |



 

<span data-ttu-id="04ba9-127">Pour demander des informations à l’appareil sur les métadonnées qui ont changé, le lecteur Windows Media 10 ou version ultérieure appelle la méthode Gestionnaire de périphériques Windows Media **IWMDMDevice3 ::D eviceiocontrol**.</span><span class="sxs-lookup"><span data-stu-id="04ba9-127">To request information from the device about metadata that has changed, Windows Media Player 10 or later calls the Windows Media Device Manager method **IWMDMDevice3::DeviceIoControl**.</span></span> <span data-ttu-id="04ba9-128">Lorsque vous effectuez cet appel, le lecteur suit des étapes spécifiques, comme suit :</span><span class="sxs-lookup"><span data-stu-id="04ba9-128">When making this call, the Player follows specific steps, as follows:</span></span>

-   <span data-ttu-id="04ba9-129">Le premier paramètre, *dwIoControlCode*, contient l’aller **- \_ \_ \_ \_ retour de métadonnées IOCTL WMP** constant.</span><span class="sxs-lookup"><span data-stu-id="04ba9-129">The first parameter, *dwIoControlCode*, contains the constant **IOCTL\_WMP\_METADATA\_ROUND\_TRIP**.</span></span> <span data-ttu-id="04ba9-130">Cette constante est définie dans wmpdevices. h.</span><span class="sxs-lookup"><span data-stu-id="04ba9-130">This constant is defined in wmpdevices.h.</span></span>
-   <span data-ttu-id="04ba9-131">Le deuxième paramètre, *lpInBuffer*, pointe vers une structure de **\_ WMDM de \_ métadonnées d’aller- \_ \_ retour \_ WMP** .</span><span class="sxs-lookup"><span data-stu-id="04ba9-131">The second parameter, *lpInBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE** structure.</span></span>
-   <span data-ttu-id="04ba9-132">Le troisième paramètre, *nInBufferSize*, contient la taille de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="04ba9-132">The third parameter, *nInBufferSize*, contains the size of the input buffer.</span></span>
-   <span data-ttu-id="04ba9-133">Le quatrième paramètre, *lpOutBuffer*, pointe vers une structure de boucles de **\_ WMDM de \_ métadonnées \_ \_ \_ WMP** .</span><span class="sxs-lookup"><span data-stu-id="04ba9-133">The fourth parameter, *lpOutBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC** structure.</span></span> <span data-ttu-id="04ba9-134">L’appareil doit remplir cette structure avec des informations sur les modifications.</span><span class="sxs-lookup"><span data-stu-id="04ba9-134">The device must fill in this structure with information about changes.</span></span>
-   <span data-ttu-id="04ba9-135">Le cinquième paramètre, *pnOutBufferSize*, reçoit la taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="04ba9-135">The fifth parameter, *pnOutBufferSize*, receives the size of the output buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04ba9-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04ba9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04ba9-137">**Extensions d’appareil pour le transfert de métadonnées accéléré**</span><span class="sxs-lookup"><span data-stu-id="04ba9-137">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 





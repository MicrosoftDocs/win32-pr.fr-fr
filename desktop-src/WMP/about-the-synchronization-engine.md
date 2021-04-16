---
title: À propos du moteur de synchronisation
description: À propos du moteur de synchronisation
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Lecteur Windows Media, moteur de synchronisation
- Modèle objet du lecteur Windows Media, moteur de synchronisation
- modèle objet, moteur de synchronisation
- Contrôle Windows Media Player ActiveX, moteur de synchronisation
- Contrôle ActiveX, moteur de synchronisation
- Contrôle ActiveX Windows Media Player Mobile, moteur de synchronisation
- Lecteur Windows Media Mobile, moteur de synchronisation
- synchronisation des appareils, moteur de synchronisation
- synchronisation des appareils, moteur de synchronisation
- moteur de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381533"
---
# <a name="about-the-synchronization-engine"></a><span data-ttu-id="4efe3-113">À propos du moteur de synchronisation</span><span class="sxs-lookup"><span data-stu-id="4efe3-113">About the Synchronization Engine</span></span>

<span data-ttu-id="4efe3-114">Le moteur de synchronisation est le composant du lecteur Windows Media qui gère la copie de contenu multimédia numérique sur des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="4efe3-114">The synchronization engine is the component of Windows Media Player that manages copying digital media content to portable devices.</span></span> <span data-ttu-id="4efe3-115">Le lecteur Windows Media prend en charge une seule instance du moteur de synchronisation pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="4efe3-115">Windows Media Player supports a single instance of the synchronization engine for each device.</span></span> <span data-ttu-id="4efe3-116">Vous devez utiliser une instance distante du contrôle du lecteur Windows Media pour effectuer des tâches de synchronisation par programme.</span><span class="sxs-lookup"><span data-stu-id="4efe3-116">You must use a remoted instance of the Windows Media Player control to perform synchronization tasks programmatically.</span></span> <span data-ttu-id="4efe3-117">En effet, votre programme partage les instances du moteur de synchronisation avec le lecteur Windows Media et tous les autres programmes qui utilisent les interfaces du lecteur pour la synchronisation des appareils.</span><span class="sxs-lookup"><span data-stu-id="4efe3-117">In effect, your program shares the synchronization engine instances with Windows Media Player and all other programs that use the Player interfaces for device synchronization.</span></span>

<span data-ttu-id="4efe3-118">Vous pouvez utiliser [IWMPSyncDevice :: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) et [IWMPSyncDevice :: Stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) pour contrôler le moment où le moteur de synchronisation effectue son travail.</span><span class="sxs-lookup"><span data-stu-id="4efe3-118">You can use [IWMPSyncDevice::start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) and [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) to control when the synchronization engine does its work.</span></span> <span data-ttu-id="4efe3-119">Dans la plupart des cas, vous ne devez pas utiliser ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4efe3-119">In most cases, you should not use these methods.</span></span> <span data-ttu-id="4efe3-120">Au lieu de cela, vous devez laisser le moteur de synchronisation planifier son travail automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4efe3-120">Instead, you should let the synchronization engine schedule its work automatically.</span></span> <span data-ttu-id="4efe3-121">Les méthodes de **démarrage** et d' **arrêt** existent afin que vous puissiez les utiliser si votre programme est conçu pour remplacer l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4efe3-121">The **start** and **stop** methods exist so that you can use them if your program is designed to replace the Windows Media Player user interface.</span></span> <span data-ttu-id="4efe3-122">Dans ce cas, vous souhaiterez peut-être fournir un bouton Démarrer/arrêter similaire à celui fourni par le lecteur Windows Media dans l’onglet **périphériques** .</span><span class="sxs-lookup"><span data-stu-id="4efe3-122">In this case, you might want to provide a start/stop button similar to the one Windows Media Player provides in the **Devices** tab.</span></span>

<span data-ttu-id="4efe3-123">Vous pouvez surveiller la progression de la synchronisation d’un appareil en interrogeant [IWMPSyncDevice :: obtenir la \_ progression](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span><span class="sxs-lookup"><span data-stu-id="4efe3-123">You can monitor the synchronization progress for a device by polling [IWMPSyncDevice::get\_progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span></span> <span data-ttu-id="4efe3-124">Cette méthode récupère une valeur de progression pour l’ensemble du processus de synchronisation avec un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="4efe3-124">This method retrieves a progress value for the entire synchronization process with a particular device.</span></span> <span data-ttu-id="4efe3-125">La valeur récupérée est un nombre qui représente le pourcentage de synchronisation terminée.</span><span class="sxs-lookup"><span data-stu-id="4efe3-125">The value retrieved is a number that represents the percentage of synchronization complete.</span></span> <span data-ttu-id="4efe3-126">Vous pouvez recevoir deux événements liés à la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="4efe3-126">There are two events you can receive that are related to synchronization.</span></span> <span data-ttu-id="4efe3-127">L’événement **DeviceSyncError** vous avertit lorsqu’un problème se produit.</span><span class="sxs-lookup"><span data-stu-id="4efe3-127">The **DeviceSyncError** event notifies you when a problem occurs.</span></span> <span data-ttu-id="4efe3-128">L’événement **DeviceSyncStateChange** vous avertit lorsque le moteur de synchronisation a changé d’État pour l’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="4efe3-128">The **DeviceSyncStateChange** event alerts you when the synchronization engine has changed state for the current device.</span></span>

<span data-ttu-id="4efe3-129">Vous pouvez limiter la quantité de stockage des appareils que le lecteur Windows Media utilise pour la synchronisation en appelant [IWMPSyncDevice2 :: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) avec l’attribut **PercentSpaceReserved** .</span><span class="sxs-lookup"><span data-stu-id="4efe3-129">You can limit the amount of device storage that Windows Media Player uses for synchronization by calling [IWMPSyncDevice2::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) with the **PercentSpaceReserved** attribute.</span></span> <span data-ttu-id="4efe3-130">L’utilisation de cette interface requiert le lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="4efe3-130">Using this interface requires Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4efe3-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4efe3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4efe3-132">**À propos de la synchronisation des appareils**</span><span class="sxs-lookup"><span data-stu-id="4efe3-132">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="4efe3-133">**Interface IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="4efe3-133">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="4efe3-134">**Indication de la progression de la synchronisation**</span><span class="sxs-lookup"><span data-stu-id="4efe3-134">**Showing Synchronization Progress**</span></span>](showing-synchronization-progress.md)
</dt> </dl>

 

 





---
title: À propos des appareils
description: À propos des appareils
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Lecteur Windows Media, synchronisation des appareils
- Modèle objet du lecteur Windows Media, synchronisation des appareils
- modèle objet, synchronisation des appareils
- Contrôle ActiveX du lecteur Windows Media, synchronisation des appareils
- Contrôle ActiveX, synchronisation des appareils
- Windows Media Player Mobile contrôle ActiveX, synchronisation des appareils
- Windows Media Player Mobile, synchronisation des appareils
- synchronisation des appareils, à propos de
- synchronisation des appareils, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509237"
---
# <a name="about-devices"></a><span data-ttu-id="0e9ca-112">À propos des appareils</span><span class="sxs-lookup"><span data-stu-id="0e9ca-112">About Devices</span></span>

<span data-ttu-id="0e9ca-113">Les périphériques portables sont des périphériques matériels que les utilisateurs utilisent pour profiter d’un contenu multimédia numérique lorsqu’ils sont à l’extérieur de leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-113">Portable devices are hardware devices that users carry to enjoy digital media content when they are away from their computer.</span></span> <span data-ttu-id="0e9ca-114">En règle générale, les périphériques portables sont exploités par une batterie.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-114">Typically, portable devices are battery operated.</span></span> <span data-ttu-id="0e9ca-115">Certains appareils peuvent lire uniquement de la musique.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-115">Some devices can play music only.</span></span> <span data-ttu-id="0e9ca-116">D’autres appareils peuvent lire des vidéos et de la musique.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-116">Other devices can play video and music.</span></span>

<span data-ttu-id="0e9ca-117">Certains appareils prennent en charge la synchronisation automatique du contenu multimédia numérique avec le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-117">Some devices support automatic synchronization of digital media content with Windows Media Player.</span></span> <span data-ttu-id="0e9ca-118">Les autres périphériques prennent uniquement en charge le transfert manuel.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-118">Other devices support only manual transfer.</span></span> <span data-ttu-id="0e9ca-119">Vous pouvez déterminer si un appareil particulier prend en charge la synchronisation automatique en appelant [IWMPSyncDevice :: obtenir l' \_ État](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) et en inspectant la valeur [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) récupérée.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-119">You can determine whether a particular device supports automatic synchronization by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="0e9ca-120">Si la valeur récupérée est **wmpdsManualDevice**, l’appareil ne prend pas en charge la synchronisation automatique.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-120">If the retrieved value is **wmpdsManualDevice**, the device does not support automatic synchronization.</span></span>

<span data-ttu-id="0e9ca-121">Vous pouvez énumérer les appareils connectés à l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-121">You can enumerate the devices connected to the user's computer.</span></span> <span data-ttu-id="0e9ca-122">Pour ce faire, utilisez d’abord [IWMPSyncServices :: obtenir \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) pour récupérer le nombre d’appareils.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-122">To do this, first use [IWMPSyncServices::get\_deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) to retrieve the count of devices.</span></span> <span data-ttu-id="0e9ca-123">Ensuite, dans une boucle, appelez [IWMPSyncServices :: getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), en passant chaque fois la valeur d’index appropriée.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-123">Then, in a loop, call [IWMPSyncServices::getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passing the appropriate index value each time.</span></span> <span data-ttu-id="0e9ca-124">Vous pouvez utiliser [IWMPSyncDevice :: obtenir la \_ connexion](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) pour évaluer si un appareil particulier est actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-124">You can use [IWMPSyncDevice::get\_connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) to evaluate whether a particular device is currently connected.</span></span>

<span data-ttu-id="0e9ca-125">Pour savoir quand les appareils se connectent ou se déconnectent, vous pouvez recevoir les événements **DeviceConnect** et **DeviceDisconnect** .</span><span class="sxs-lookup"><span data-stu-id="0e9ca-125">To know when devices connect or disconnect, you can receive the **DeviceConnect** and **DeviceDisconnect** events.</span></span> <span data-ttu-id="0e9ca-126">Ces événements sont reçus via l’interface **IWMPEvents2** .</span><span class="sxs-lookup"><span data-stu-id="0e9ca-126">These events are received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="0e9ca-127">L’interface **IWMPSyncDevice** fournit des méthodes supplémentaires pour vous permettre d’obtenir ou de définir des informations sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-127">The **IWMPSyncDevice** interface provides additional methods to enable you to get or set information about a device.</span></span> <span data-ttu-id="0e9ca-128">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0e9ca-128">For example:</span></span>

-   <span data-ttu-id="0e9ca-129">Les méthodes **obtenir \_ FriendlyName** et **put \_ FriendlyName** vous permettent de récupérer et de spécifier le nom de périphérique défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-129">The **get\_FriendlyName** and **put\_FriendlyName** methods enable you to retrieve and specify the user-defined device name.</span></span>
-   <span data-ttu-id="0e9ca-130">La méthode **obtenir \_ DeviceName** vous permet de récupérer le nom de l’appareil que les utilisateurs voient dans le shell Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-130">The **get\_deviceName** method enables you to retrieve the device name that users see in the Windows XP shell.</span></span>
-   <span data-ttu-id="0e9ca-131">La méthode **getItemInfo** vous permet de récupérer les métadonnées des appareils.</span><span class="sxs-lookup"><span data-stu-id="0e9ca-131">The **getItemInfo** method enables you to retrieve metadata from devices.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e9ca-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e9ca-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e9ca-133">**À propos de la synchronisation des appareils**</span><span class="sxs-lookup"><span data-stu-id="0e9ca-133">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="0e9ca-134">**Interface IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="0e9ca-134">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="0e9ca-135">**Interface IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="0e9ca-135">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="0e9ca-136">**Utilisation d’appareils mobiles**</span><span class="sxs-lookup"><span data-stu-id="0e9ca-136">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 





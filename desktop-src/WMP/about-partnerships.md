---
title: À propos des partenariats
description: À propos des partenariats
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, partenariats
- Modèle objet du lecteur Windows Media, partenariats
- modèle objet, partenariats
- Contrôle ActiveX du lecteur Windows Media, partenariats
- Contrôle ActiveX, partenariats
- Contrôle ActiveX Windows Media Player Mobile, partenariats
- Windows Media Player Mobile, partenariats
- synchronisation des appareils, partenariats
- synchronisation des appareils, partenariats
- partenariats entre les appareils et le lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104462707"
---
# <a name="about-partnerships"></a><span data-ttu-id="7f5df-113">À propos des partenariats</span><span class="sxs-lookup"><span data-stu-id="7f5df-113">About Partnerships</span></span>

<span data-ttu-id="7f5df-114">Un partenariat est une relation spéciale entre un appareil portable et le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7f5df-114">A partnership is a special relationship between a portable device and Windows Media Player.</span></span> <span data-ttu-id="7f5df-115">Les utilisateurs peuvent établir un partenariat pour un appareil particulier à l’aide de l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7f5df-115">Users can establish a partnership for a particular device by using the Windows Media Player user interface.</span></span> <span data-ttu-id="7f5df-116">Vous pouvez gérer les partenariats par programmation à l’aide de [IWMPSyncDevice :: createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) et [IWMPSyncDevice ::d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span><span class="sxs-lookup"><span data-stu-id="7f5df-116">You can programmatically manage partnerships by using [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) and [IWMPSyncDevice::deletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span></span> <span data-ttu-id="7f5df-117">La méthode **createPartnership** démarre un processus asynchrone qui se termine lorsque l’événement **CreatePartnershipComplete** est reçu par le biais de l’interface **IWMPEvents2** .</span><span class="sxs-lookup"><span data-stu-id="7f5df-117">The **createPartnership** method starts an asynchronous process that ends when the **CreatePartnershipComplete** event is received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="7f5df-118">Le lecteur Windows Media 10 ou une version ultérieure prend en charge la création de partenariats avec jusqu’à 16 appareils.</span><span class="sxs-lookup"><span data-stu-id="7f5df-118">Windows Media Player 10 or later supports creating partnerships with up to 16 devices.</span></span> <span data-ttu-id="7f5df-119">Chaque partenariat est associé à un index de partenariat.</span><span class="sxs-lookup"><span data-stu-id="7f5df-119">Each partnership has an associated partnership index.</span></span> <span data-ttu-id="7f5df-120">Vous pouvez récupérer l’index de partenariat pour un appareil particulier en appelant [IWMPSyncDevice :: obtenir \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span><span class="sxs-lookup"><span data-stu-id="7f5df-120">You can retrieve the partnership index for a particular device by calling [IWMPSyncDevice::get\_partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span></span> <span data-ttu-id="7f5df-121">Les indices de partenariat sont numérotés de 1 à 16.</span><span class="sxs-lookup"><span data-stu-id="7f5df-121">Partnership indices are numbered from 1 to 16.</span></span> <span data-ttu-id="7f5df-122">Quand un appareil particulier n’a pas de partenariat avec le lecteur Windows Media, **getPartnershipIndex** retourne zéro pour l’index.</span><span class="sxs-lookup"><span data-stu-id="7f5df-122">When a particular device does not have a partnership with Windows Media Player, **getPartnershipIndex** returns zero for the index.</span></span>

<span data-ttu-id="7f5df-123">Vous pouvez récupérer l’état du partenariat d’un appareil particulier en appelant [IWMPSyncDevice :: obtenir l' \_ État](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) et en inspectant la valeur [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) récupérée.</span><span class="sxs-lookup"><span data-stu-id="7f5df-123">You can retrieve the partnership status of a particular device by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="7f5df-124">Le lecteur Windows Media autorise un partenariat avec la bibliothèque d’un utilisateur sur un ordinateur pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="7f5df-124">Windows Media Player allows one partnership with one user's library on one computer for each device.</span></span> <span data-ttu-id="7f5df-125">Cela signifie que la création d’un partenariat détruit tout partenariat existant que l’appareil actuel peut avoir avec un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f5df-125">This means that creating a new partnership destroys any existing partnership the current device might have with another computer.</span></span> <span data-ttu-id="7f5df-126">Pour savoir quand l’état change pour un appareil, vous pouvez recevoir l’événement **DeviceStatusChange** .</span><span class="sxs-lookup"><span data-stu-id="7f5df-126">To know when the status changes for a device, you can receive the **DeviceStatusChange** event.</span></span>

<span data-ttu-id="7f5df-127">Le lecteur Windows Media ne peut pas créer de partenariat avec un appareil dont l’État est **wmpdsManualDevice**.</span><span class="sxs-lookup"><span data-stu-id="7f5df-127">Windows Media Player cannot create a partnership with a device having the status **wmpdsManualDevice**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f5df-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f5df-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f5df-129">**À propos de la synchronisation des appareils**</span><span class="sxs-lookup"><span data-stu-id="7f5df-129">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="7f5df-130">**Interface IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="7f5df-130">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="7f5df-131">**Utilisation d’appareils mobiles**</span><span class="sxs-lookup"><span data-stu-id="7f5df-131">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 





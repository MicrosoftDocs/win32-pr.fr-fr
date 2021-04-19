---
title: Attribut SyncState
description: L’attribut SyncState est une représentation sous forme de chaîne d’une valeur 32 bits que le lecteur Windows Media utilise lorsqu’il synchronise des sélections avec des appareils portables.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- Attribut SyncState lecteur Windows Media
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535888"
---
# <a name="syncstate-attribute"></a><span data-ttu-id="ef306-104">Attribut SyncState</span><span class="sxs-lookup"><span data-stu-id="ef306-104">SyncState Attribute</span></span>

<span data-ttu-id="ef306-105">L’attribut **SyncState** est une représentation sous forme de chaîne d’une valeur 32 bits que le lecteur Windows Media utilise lorsqu’il synchronise des sélections avec des appareils portables.</span><span class="sxs-lookup"><span data-stu-id="ef306-105">The **SyncState** attribute is a string representation of a 32-bit value that Windows Media Player uses when it synchronizes playlists with portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ef306-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="ef306-106">Applies To</span></span>

-   [<span data-ttu-id="ef306-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="ef306-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="ef306-108">Autres éléments</span><span class="sxs-lookup"><span data-stu-id="ef306-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="ef306-109">Éléments de photo</span><span class="sxs-lookup"><span data-stu-id="ef306-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="ef306-110">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="ef306-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="ef306-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ef306-111">Remarks</span></span>

<span data-ttu-id="ef306-112">Cet attribut se compose de valeurs 16 2 bits, chacune spécifiant l’état de synchronisation d’un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="ef306-112">This attribute consists of sixteen 2-bit values, each of which specifies the synchronization state of a portable device.</span></span> <span data-ttu-id="ef306-113">Le bit le plus significatif (MSB) de cette valeur de 32 bits correspond à l’appareil 16.</span><span class="sxs-lookup"><span data-stu-id="ef306-113">The most significant bit (MSB) of this 32-bit value corresponds to device 16.</span></span> <span data-ttu-id="ef306-114">Le bit le moins significatif (LSB) correspond à l’appareil 1.</span><span class="sxs-lookup"><span data-stu-id="ef306-114">The least significant bit (LSB) corresponds to device 1.</span></span>

<span data-ttu-id="ef306-115">L’octet de poids fort de chaque valeur de 2 bits indique si le lecteur Windows Media a synchronisé le contenu avec l’appareil correspondant.</span><span class="sxs-lookup"><span data-stu-id="ef306-115">The MSB of each 2-bit value indicates whether Windows Media Player synchronized the content with the corresponding device.</span></span> <span data-ttu-id="ef306-116">La valeur 1 indique qu’elle a été exécutée.</span><span class="sxs-lookup"><span data-stu-id="ef306-116">A value of 1 indicates that it did.</span></span> <span data-ttu-id="ef306-117">La valeur 0 indique qu’elle ne l’a pas fait.</span><span class="sxs-lookup"><span data-stu-id="ef306-117">A value of 0 indicates that it did not.</span></span>

<span data-ttu-id="ef306-118">Si le MSB est 0, le LSB spécifie la raison de l’échec de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="ef306-118">If the MSB is 0, the LSB specifies why the synchronization failed.</span></span> <span data-ttu-id="ef306-119">La valeur 1 dans le LSB indique qu’il n’y avait pas suffisamment d’espace libre pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="ef306-119">A value of 1 in the LSB indicates that there was not enough free space for the content.</span></span> <span data-ttu-id="ef306-120">La valeur 0 dans le LSB indique une autre raison empêchait la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="ef306-120">A value of 0 in the LSB indicates some other reason prevented synchronization.</span></span>

<span data-ttu-id="ef306-121">Pour récupérer l’état de synchronisation d’un appareil donné, vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ef306-121">To retrieve the synchronization state of a given device, you should do the following:</span></span>

1.  <span data-ttu-id="ef306-122">Appelez **IWMPSyncDevice :: obtenir l' \_ État** pour déterminer si un appareil donné est synchronisé.</span><span class="sxs-lookup"><span data-stu-id="ef306-122">Invoke **IWMPSyncDevice::get\_status** to determine whether a given device is synchronized.</span></span>
2.  <span data-ttu-id="ef306-123">Si elle est synchronisée, appelez **IWMPSyncDevice :: obtenir \_ partnershipIndex** pour récupérer l’index de la paire de bits de l’appareil dans l’attribut **SyncState** .</span><span class="sxs-lookup"><span data-stu-id="ef306-123">If it is synchronized, invoke **IWMPSyncDevice::get\_partnershipIndex** to retrieve the index of the device's bit pair in the **SyncState** attribute.</span></span>
3.  <span data-ttu-id="ef306-124">À l’aide de cet index, masquez la paire de bits correspondante de l’attribut **SyncState** et examinez le résultat pour déterminer l’état de synchronisation de la playlist avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ef306-124">Using this index, mask the corresponding bit pair of the **SyncState** attribute and examine the result to determine the synchronization state of the playlist with the device.</span></span>

<span data-ttu-id="ef306-125">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ef306-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef306-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef306-126">Requirements</span></span>



| <span data-ttu-id="ef306-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef306-127">Requirement</span></span> | <span data-ttu-id="ef306-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef306-128">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="ef306-129">Version</span><span class="sxs-lookup"><span data-stu-id="ef306-129">Version</span></span><br/> | <span data-ttu-id="ef306-130">Lecteur Windows Media 10 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ef306-130">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef306-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef306-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef306-132">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="ef306-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="ef306-133">**Détermination de l’état de synchronisation des sélections**</span><span class="sxs-lookup"><span data-stu-id="ef306-133">**Determining Playlist Synchronization State**</span></span>](determining-playlist-synchronization-state.md)
</dt> <dt>

[<span data-ttu-id="ef306-134">**IWMPSyncDevice :: obtient \_ partnershipIndex**</span><span class="sxs-lookup"><span data-stu-id="ef306-134">**IWMPSyncDevice::get\_partnershipIndex**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[<span data-ttu-id="ef306-135">**IWMPSyncDevice :: obtient l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="ef306-135">**IWMPSyncDevice::get\_status**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 






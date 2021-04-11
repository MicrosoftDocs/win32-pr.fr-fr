---
description: Les \_ \_ \_ constantes support matériel de point de terminaison xxx sont des indicateurs de support matériel pour un périphérique de point de terminaison audio.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: Constantes ENDPOINT_HARDWARE_SUPPORT_XXX (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111550"
---
# <a name="endpoint_hardware_support_xxx-constants"></a><span data-ttu-id="255e8-103">SUPPORT matériel de point de terminaison \_ \_ xxx, \_ constantes</span><span class="sxs-lookup"><span data-stu-id="255e8-103">ENDPOINT\_HARDWARE\_SUPPORT\_XXX Constants</span></span>

<span data-ttu-id="255e8-104">Les \_ \_ \_ constantes support matériel de point de terminaison xxx sont des indicateurs de support matériel pour un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="255e8-104">The ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants are hardware support flags for an audio endpoint device.</span></span>



| <span data-ttu-id="255e8-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="255e8-105">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="255e8-106">Description</span><span class="sxs-lookup"><span data-stu-id="255e8-106">Description</span></span>                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <span data-ttu-id="255e8-107"><dt>**Point de terminaison \_ \_ \_ Volume de support matériel**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="255e8-107"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_VOLUME**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="255e8-108">L’appareil de point de terminaison audio prend en charge un contrôle de volume matériel.</span><span class="sxs-lookup"><span data-stu-id="255e8-108">The audio endpoint device supports a hardware volume control.</span></span><br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <span data-ttu-id="255e8-109"><dt>**Point de terminaison \_ \_Support matériel \_ muet**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="255e8-109"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_MUTE**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="255e8-110">L’appareil de point de terminaison audio prend en charge un contrôle matériel muet.</span><span class="sxs-lookup"><span data-stu-id="255e8-110">The audio endpoint device supports a hardware mute control.</span></span><br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <span data-ttu-id="255e8-111"><dt>**Point de terminaison \_ MATÉRIEL \_ pris \_ en charge**</dt> par le compteur <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="255e8-111"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_METER**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="255e8-112">L’appareil de point de terminaison audio prend en charge un indicateur de pic matériel.</span><span class="sxs-lookup"><span data-stu-id="255e8-112">The audio endpoint device supports a hardware peak meter.</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="255e8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="255e8-113">Remarks</span></span>

<span data-ttu-id="255e8-114">Les méthodes [**IAudioEndpointVolume :: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) et [**IAudioMeterInformation :: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) utilisent les \_ constantes support matériel de point de terminaison \_ \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="255e8-114">The [**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) and [**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) methods use the ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span>

<span data-ttu-id="255e8-115">Un masque de support matériel indique les fonctions qu’un périphérique de point de terminaison audio implémente dans le matériel.</span><span class="sxs-lookup"><span data-stu-id="255e8-115">A hardware support mask indicates which functions an audio endpoint device implements in hardware.</span></span> <span data-ttu-id="255e8-116">Le masque peut avoir la valeur 0 ou la combinaison or au niveau du bit (or) d’une ou de plusieurs \_ \_ constantes support matériel de point de terminaison \_ .</span><span class="sxs-lookup"><span data-stu-id="255e8-116">The mask can be either 0 or the bitwise-OR combination of one or more ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span> <span data-ttu-id="255e8-117">Si un bit qui correspond à une constante particulière support matériel de point de terminaison \_ \_ \_ est défini dans le masque, la signification est que la fonction représentée par cette constante est implémentée dans le matériel par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="255e8-117">If a bit that corresponds to a particular ENDPOINT\_HARDWARE\_SUPPORT\_XXX constant is set in the mask, then the meaning is that the function represented by that constant is implemented in hardware by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="255e8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="255e8-118">Requirements</span></span>



| <span data-ttu-id="255e8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="255e8-119">Requirement</span></span> | <span data-ttu-id="255e8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="255e8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="255e8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="255e8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="255e8-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="255e8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="255e8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="255e8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="255e8-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="255e8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="255e8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="255e8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="255e8-126"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="255e8-126"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="255e8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="255e8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="255e8-128">Constantes audio principales</span><span class="sxs-lookup"><span data-stu-id="255e8-128">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="255e8-129">**IAudioEndpointVolume::QueryHardwareSupport**</span><span class="sxs-lookup"><span data-stu-id="255e8-129">**IAudioEndpointVolume::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[<span data-ttu-id="255e8-130">**IAudioMeterInformation::QueryHardwareSupport**</span><span class="sxs-lookup"><span data-stu-id="255e8-130">**IAudioMeterInformation::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 





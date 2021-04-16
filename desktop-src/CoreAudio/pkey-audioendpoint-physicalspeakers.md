---
description: 'En savoir plus sur : PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524079"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a><span data-ttu-id="65a10-103">\_AudioEndpoint \_ PhysicalSpeakers</span><span class="sxs-lookup"><span data-stu-id="65a10-103">PKEY\_AudioEndpoint\_PhysicalSpeakers</span></span>

<span data-ttu-id="65a10-104">La **propriété \_ \_ PhysicalSpeakers AudioEndpoint** spécifie le masque de configuration de canal pour l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="65a10-104">The **PKEY\_AudioEndpoint\_PhysicalSpeakers** property specifies the channel-configuration mask for the audio endpoint device.</span></span> <span data-ttu-id="65a10-105">Le masque indique la configuration physique d’un ensemble de haut-parleurs et spécifie l’attribution de canaux aux orateurs.</span><span class="sxs-lookup"><span data-stu-id="65a10-105">The mask indicates the physical configuration of a set of speakers and specifies the assignment of channels to speakers.</span></span> <span data-ttu-id="65a10-106">Pour plus d’informations sur les masques de configuration de canal, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="65a10-106">For more information about channel-configuration masks, see the following:</span></span>

1.  <span data-ttu-id="65a10-107">Description de la propriété de \_ configuration de canal audio KSPROPERTY \_ \_ dans la documentation de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="65a10-107">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
2.  <span data-ttu-id="65a10-108">Le livre blanc intitulé « prise en charge du pilote audio pour les configurations du locuteur Home Cinema » sur le site Web [des technologies de périphériques audio pour Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="65a10-108">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="65a10-109">Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="65a10-109">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="65a10-110">Le membre **uintVal** de la structure **PROPVARIANT** contient un masque de configuration de canal qui est converti en type **uint**.</span><span class="sxs-lookup"><span data-stu-id="65a10-110">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="65a10-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65a10-111">Requirements</span></span>



| <span data-ttu-id="65a10-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65a10-112">Requirement</span></span> | <span data-ttu-id="65a10-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="65a10-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65a10-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65a10-114">Minimum supported client</span></span><br/> | <span data-ttu-id="65a10-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65a10-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="65a10-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65a10-116">Minimum supported server</span></span><br/> | <span data-ttu-id="65a10-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65a10-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="65a10-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="65a10-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="65a10-119"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="65a10-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65a10-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65a10-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a10-121">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="65a10-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="65a10-122">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="65a10-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 





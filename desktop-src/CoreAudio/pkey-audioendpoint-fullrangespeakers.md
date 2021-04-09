---
description: La \_ propriété hyperAudioEndpoint \_ FullRangeSpeakers spécifie le masque de configuration de canal pour les haut-parleurs complets connectés à l’appareil de point de terminaison audio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111326"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a><span data-ttu-id="91d6e-103">\_AudioEndpoint \_ FullRangeSpeakers</span><span class="sxs-lookup"><span data-stu-id="91d6e-103">PKEY\_AudioEndpoint\_FullRangeSpeakers</span></span>

<span data-ttu-id="91d6e-104">La **propriété \_ hyperAudioEndpoint \_ FullRangeSpeakers** spécifie le masque de configuration de canal pour les haut-parleurs complets connectés à l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="91d6e-104">The **PKEY\_AudioEndpoint\_FullRangeSpeakers** property specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span> <span data-ttu-id="91d6e-105">Le masque indique la configuration physique des haut-parleurs complets et spécifie l’affectation des canaux à ces intervenants.</span><span class="sxs-lookup"><span data-stu-id="91d6e-105">The mask indicates the physical configuration of the full-range speakers and specifies the assignment of channels to those speakers.</span></span>

<span data-ttu-id="91d6e-106">Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="91d6e-106">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="91d6e-107">Le membre **uintVal** de la structure **PROPVARIANT** contient un masque de configuration de canal qui est converti en type **uint**.</span><span class="sxs-lookup"><span data-stu-id="91d6e-107">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

<span data-ttu-id="91d6e-108">Un orateur complet est en train de jouer des sons sur la plage complète, de graves à aigus.</span><span class="sxs-lookup"><span data-stu-id="91d6e-108">A full-range speaker is capable of playing sounds over the full range from bass to treble.</span></span> <span data-ttu-id="91d6e-109">En règle générale, les haut-parleurs sont de gamme complète, mais les plus petits sont beaucoup moins aptes à jouer des basses.</span><span class="sxs-lookup"><span data-stu-id="91d6e-109">Typically, larger speakers are full range but smaller speakers are significantly less capable of playing bass sounds.</span></span> <span data-ttu-id="91d6e-110">Dans Windows Vista, le moteur audio utilise cette propriété pour gérer les niveaux de basses dans le flux de sortie audio joué par l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="91d6e-110">In Windows Vista, the audio engine uses this property to manage bass levels in the audio output stream that is played by the audio endpoint device.</span></span>

<span data-ttu-id="91d6e-111">Le masque de configuration de canal pour cette propriété est au même format que le masque de configuration de canal pour la propriété [**\_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) .</span><span class="sxs-lookup"><span data-stu-id="91d6e-111">The channel-configuration mask for this property is in the same format as the channel-configuration mask for the [**PKEY\_AudioEndpoint\_PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) property.</span></span> <span data-ttu-id="91d6e-112">Pour plus d’informations sur les masques de configuration de canal, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="91d6e-112">For more information about channel-configuration masks, see the following:</span></span>

-   <span data-ttu-id="91d6e-113">Description de la propriété de \_ configuration de canal audio KSPROPERTY \_ \_ dans la documentation de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="91d6e-113">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
-   <span data-ttu-id="91d6e-114">Le livre blanc intitulé « prise en charge du pilote audio pour les configurations du locuteur Home Cinema » sur le site Web [des technologies de périphériques audio pour Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="91d6e-114">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="91d6e-115">Le système obtient le masque de configuration de canal pour la \_ propriété AudioEndpoint \_ FullRangeSpeakers de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="91d6e-115">The system obtains the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property from the user.</span></span> <span data-ttu-id="91d6e-116">L’utilisateur entre ces informations par le biais du panneau de configuration multimédia de Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="91d6e-116">The user enters this information through the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="91d6e-117">Pour plus d’informations sur Mmsys.cpl, consultez la documentation de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="91d6e-117">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="91d6e-118">Le masque de configuration de canal pour la \_ \_ propriété AudioEndpoint FullRangeSpeakers d’un appareil de point de terminaison audio est un sous-ensemble du masque de configuration de canal pour la \_ \_ propriété PhysicalSpeakers AudioEndpoint du même appareil.</span><span class="sxs-lookup"><span data-stu-id="91d6e-118">The channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property of an audio endpoint device is a subset of the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property of the same device.</span></span>

<span data-ttu-id="91d6e-119">Par exemple, si un périphérique de point de terminaison audio pilote un ensemble de haut-parleurs de son surround 5,1, le masque de configuration de canal pour la \_ \_ propriété AudioEndpoint PHYSICALSPEAKERS est KSAUDIO \_ Speaker \_ 5POINT1.</span><span class="sxs-lookup"><span data-stu-id="91d6e-119">For example, if an audio endpoint device drives a set of 5.1 surround-sound speakers, then the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property is KSAUDIO\_SPEAKER\_5POINT1.</span></span> <span data-ttu-id="91d6e-120">Ce masque indique la présence de haut-parleurs de l’avant-plan, du front-droit, du front-Center, du côté gauche et du côté droit, ainsi qu’un caisson de basses.</span><span class="sxs-lookup"><span data-stu-id="91d6e-120">This mask indicates the presence of front-left, front-right, front-center, side-left, and side-right speakers—plus a subwoofer.</span></span> <span data-ttu-id="91d6e-121">Si les haut-parleurs de l’avant-plan et de l’avant-plan sont suffisamment grands pour produire des basses, mais que les haut-parleurs plus petits et les haut-parleurs latéraux ne le sont pas, le masque de configuration de canal pour la \_ \_ propriété AudioEndpoint FULLRANGESPEAKERS est KSAUDIO \_ Speaker \_ , qui indique uniquement les haut-parleurs avant gauche et avant.</span><span class="sxs-lookup"><span data-stu-id="91d6e-121">If the front-left and front-right speakers are large enough to produce bass sounds but the smaller front-center and side speakers are not, then the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property is KSAUDIO\_SPEAKER\_STEREO, which indicates only the front-left and front-right speakers.</span></span> <span data-ttu-id="91d6e-122">Les masques de configuration de canaux KSAUDIO \_ Speaker \_ 5POINT1 et KSAUDIO \_ Speaker \_ Stereo sont définis dans le fichier d’en-tête Ksmedia. h.</span><span class="sxs-lookup"><span data-stu-id="91d6e-122">Channel-configuration masks KSAUDIO\_SPEAKER\_5POINT1 and KSAUDIO\_SPEAKER\_STEREO are defined in header file Ksmedia.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="91d6e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91d6e-123">Requirements</span></span>



| <span data-ttu-id="91d6e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91d6e-124">Requirement</span></span> | <span data-ttu-id="91d6e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="91d6e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d6e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91d6e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="91d6e-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91d6e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="91d6e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91d6e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="91d6e-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91d6e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="91d6e-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="91d6e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d6e-131"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="91d6e-131"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91d6e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91d6e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d6e-133">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="91d6e-133">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="91d6e-134">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="91d6e-134">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="91d6e-135">**\_Propriété AudioEndpoint \_ PhysicalSpeakers**</span><span class="sxs-lookup"><span data-stu-id="91d6e-135">**PKEY\_AudioEndpoint\_PhysicalSpeakers Property**</span></span>](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 





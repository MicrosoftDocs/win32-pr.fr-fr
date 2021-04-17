---
title: Modification du pas et de la vitesse de lecture
description: Modification du pas et de la vitesse de lecture
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- sons Waveform, pas de tonalité
- Waveform-interface audio, inclinaison
- audio Wave, vitesse de lecture
- Waveform-interface audio, vitesse de lecture
- son de forme d’onde, modification du pas
- Waveform-interface audio, modification du pas
- audio Wave, modification de la vitesse de lecture
- Waveform-interface audio, modification de la vitesse de lecture
- modification de la vitesse de lecture Waveform-Audio
- modification du ton de la forme d’onde-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463147"
---
# <a name="changing-pitch-and-playback-rate"></a><span data-ttu-id="92211-113">Modification du pas et de la vitesse de lecture</span><span class="sxs-lookup"><span data-stu-id="92211-113">Changing Pitch and Playback Rate</span></span>

<span data-ttu-id="92211-114">Certains périphériques de sortie Waveform-Audio peuvent varier le pas et la vitesse de lecture des données audio Waveform.</span><span class="sxs-lookup"><span data-stu-id="92211-114">Some waveform-audio output devices can vary the pitch and the playback rate of waveform-audio data.</span></span> <span data-ttu-id="92211-115">Tous les périphériques audio Waveform ne prennent pas en charge la tonalité et les changements de vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="92211-115">Not all waveform-audio devices support pitch and playback-rate changes.</span></span> <span data-ttu-id="92211-116">Pour plus d’informations sur la façon de déterminer si un périphérique Wave-Audio particulier prend en charge les changements de taux de lecture et de tonalité, consultez [périphériques et types de données](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="92211-116">For information about how to determine whether a particular waveform-audio device supports pitch and playback rate changes, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="92211-117">Les différences entre la variation du pas et la vitesse de lecture sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="92211-117">The differences between changing pitch and playback rate are as follows:</span></span>

-   <span data-ttu-id="92211-118">La modification de la vitesse de lecture est effectuée par le pilote de périphérique et ne nécessite pas de matériel spécialisé.</span><span class="sxs-lookup"><span data-stu-id="92211-118">Changing the playback rate is performed by the device driver and does not require specialized hardware.</span></span> <span data-ttu-id="92211-119">Le taux d’échantillonnage n’est pas modifié, mais le pilote interpole en ignorant ou en synthétisant les exemples.</span><span class="sxs-lookup"><span data-stu-id="92211-119">The sample rate is not changed, but the driver interpolates by skipping or synthesizing samples.</span></span> <span data-ttu-id="92211-120">Par exemple, si la vitesse de lecture est modifiée par un facteur de deux, le pilote ignore chaque autre échantillon.</span><span class="sxs-lookup"><span data-stu-id="92211-120">For example, if the playback rate is changed by a factor of two, the driver skips every other sample.</span></span>
-   <span data-ttu-id="92211-121">La modification du pas à pas nécessite un matériel spécialisé.</span><span class="sxs-lookup"><span data-stu-id="92211-121">Changing the pitch requires specialized hardware.</span></span> <span data-ttu-id="92211-122">La vitesse de lecture et le taux d’échantillonnage ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="92211-122">The playback rate and sample rate are not changed.</span></span>

<span data-ttu-id="92211-123">Windows fournit les fonctions suivantes pour interroger et définir le taux de lecture et le ton de la forme d’onde audio.</span><span class="sxs-lookup"><span data-stu-id="92211-123">Windows provides the following functions to query and set waveform-audio pitch and playback rates.</span></span>



| <span data-ttu-id="92211-124">Fonction</span><span class="sxs-lookup"><span data-stu-id="92211-124">Function</span></span>                                                 | <span data-ttu-id="92211-125">Description</span><span class="sxs-lookup"><span data-stu-id="92211-125">Description</span></span>                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="92211-126">**waveOutGetPitch**</span><span class="sxs-lookup"><span data-stu-id="92211-126">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | <span data-ttu-id="92211-127">Récupère le pas du périphérique de sortie Waveform-Audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="92211-127">Retrieves the pitch for the specified waveform-audio output device.</span></span>         |
| [<span data-ttu-id="92211-128">**waveOutGetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="92211-128">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | <span data-ttu-id="92211-129">Récupère la vitesse de lecture pour le périphérique de sortie Waveform-Audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="92211-129">Retrieves the playback rate for the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="92211-130">**waveOutSetPitch**</span><span class="sxs-lookup"><span data-stu-id="92211-130">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | <span data-ttu-id="92211-131">Définit le pas du périphérique de sortie Waveform-Audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="92211-131">Sets the pitch for the specified waveform-audio output device.</span></span>              |
| [<span data-ttu-id="92211-132">**waveOutSetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="92211-132">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | <span data-ttu-id="92211-133">Définit la vitesse de lecture pour le périphérique de sortie Waveform-Audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="92211-133">Sets the playback rate for the specified waveform-audio output device.</span></span>      |



 

<span data-ttu-id="92211-134">Les taux de pas et de lecture sont modifiés par un facteur spécifié avec un nombre à virgule fixe compacté dans une valeur de mot double.</span><span class="sxs-lookup"><span data-stu-id="92211-134">The pitch and playback rates are changed by a factor specified with a fixed-point number packed into a doubleword value.</span></span> <span data-ttu-id="92211-135">Les 16 bits supérieurs spécifient la partie entière du nombre ; les 16 bits de poids faible spécifient la partie fractionnaire.</span><span class="sxs-lookup"><span data-stu-id="92211-135">The upper 16 bits specify the integer part of the number; the lower 16 bits specify the fractional part.</span></span> <span data-ttu-id="92211-136">Par exemple, la valeur 1,5 est représentée sous la forme 0x00018000L.</span><span class="sxs-lookup"><span data-stu-id="92211-136">For example, the value 1.5 is represented as 0x00018000L.</span></span> <span data-ttu-id="92211-137">La valeur 0,75 est représentée sous la forme 0x0000C000L.</span><span class="sxs-lookup"><span data-stu-id="92211-137">The value 0.75 is represented as 0x0000C000L.</span></span> <span data-ttu-id="92211-138">Une valeur de 1,0 (0x00010000) signifie que le pas à pas ou la vitesse de lecture est inchangée.</span><span class="sxs-lookup"><span data-stu-id="92211-138">A value of 1.0 (0x00010000) means the pitch or playback rate is unchanged.</span></span>

 

 
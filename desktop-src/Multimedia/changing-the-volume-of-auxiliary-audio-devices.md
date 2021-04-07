---
title: Modification du volume de Audio-Devices auxiliaires
description: Modification du volume de Audio-Devices auxiliaires
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- audio Wave, modification du volume du périphérique audio auxiliaire
- modification du volume du périphérique audio auxiliaire
- audio auxiliaire, modification du volume de l’appareil
- interface audio auxiliaire
- périphériques audio auxiliaires, modification du volume
- audio auxiliaire, interface
- audio auxiliaire, appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727317"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a><span data-ttu-id="6b93f-110">Modification du volume de Audio-Devices auxiliaires</span><span class="sxs-lookup"><span data-stu-id="6b93f-110">Changing the Volume of Auxiliary Audio-Devices</span></span>

<span data-ttu-id="6b93f-111">Windows fournit les fonctions suivantes pour interroger et définir le volume des périphériques audio auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="6b93f-111">Windows provides the following functions to query and set the volume for auxiliary audio devices.</span></span>



| <span data-ttu-id="6b93f-112">Fonction</span><span class="sxs-lookup"><span data-stu-id="6b93f-112">Function</span></span>                             | <span data-ttu-id="6b93f-113">Description</span><span class="sxs-lookup"><span data-stu-id="6b93f-113">Description</span></span>                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="6b93f-114">**auxGetVolume**</span><span class="sxs-lookup"><span data-stu-id="6b93f-114">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | <span data-ttu-id="6b93f-115">Récupère le paramètre de volume actuel du périphérique de sortie auxiliaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="6b93f-115">Retrieves the current volume setting of the specified auxiliary output device.</span></span> |
| [<span data-ttu-id="6b93f-116">**auxSetVolume**</span><span class="sxs-lookup"><span data-stu-id="6b93f-116">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | <span data-ttu-id="6b93f-117">Définit le volume du périphérique de sortie auxiliaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="6b93f-117">Sets the volume of the specified auxiliary output device.</span></span>                      |



 

<span data-ttu-id="6b93f-118">Tous les périphériques audio auxiliaires ne prennent pas en charge les modifications de volume.</span><span class="sxs-lookup"><span data-stu-id="6b93f-118">Not all auxiliary audio devices support volume changes.</span></span> <span data-ttu-id="6b93f-119">Certains appareils peuvent prendre en charge des modifications de volume individuelles sur les canaux gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="6b93f-119">Some devices can support individual volume changes on both the left and the right channels.</span></span>

<span data-ttu-id="6b93f-120">Le volume est spécifié dans une valeur de mot double, comme avec les fonctions Wave-audio et de contrôle de volume MIDI.</span><span class="sxs-lookup"><span data-stu-id="6b93f-120">Volume is specified in a doubleword value, as with the waveform-audio and MIDI volume-control functions.</span></span> <span data-ttu-id="6b93f-121">Lorsque le format audio est stéréo, les 16 bits supérieurs spécifient le volume relatif du canal droit et les 16 bits inférieurs spécifient le volume relatif du canal de gauche.</span><span class="sxs-lookup"><span data-stu-id="6b93f-121">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="6b93f-122">Pour les appareils qui ne prennent pas en charge le contrôle du volume de canal droit et gauche, les 16 bits de poids faible spécifient le niveau de volume et les 16 bits supérieurs sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="6b93f-122">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="6b93f-123">Les valeurs au niveau du volume sont comprises entre 0x0 (silence) et 0xFFFF (volume maximal) et sont interprétées de façon logarithmique.</span><span class="sxs-lookup"><span data-stu-id="6b93f-123">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="6b93f-124">L’augmentation du volume perçu est la même lors de l’augmentation du niveau de volume de 0x5000 à 0x6000, comme c’est le cas de 0x4000 à 0x5000.</span><span class="sxs-lookup"><span data-stu-id="6b93f-124">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 
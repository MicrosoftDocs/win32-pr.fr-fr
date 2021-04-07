---
title: Modification du volume de Waveform-Audio lecture
description: Modification du volume de Waveform-Audio lecture
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- audio Wave, modification du volume de lecture
- Waveform-interface audio, modification du volume de lecture
- audio Wave, volume de lecture
- Waveform-interface audio, volume de lecture
- modification du volume de lecture Waveform-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f972b5bd8e6f0d4a0d7d5964f164429c5632b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727316"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a><span data-ttu-id="22707-108">Modification du volume de Waveform-Audio lecture</span><span class="sxs-lookup"><span data-stu-id="22707-108">Changing the Volume of Waveform-Audio Playback</span></span>

<span data-ttu-id="22707-109">Windows fournit les fonctions suivantes pour interroger et définir le niveau de volume des périphériques de sortie Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="22707-109">Windows provides the following functions to query and set the volume level of waveform-audio output devices.</span></span>



| <span data-ttu-id="22707-110">Fonction</span><span class="sxs-lookup"><span data-stu-id="22707-110">Function</span></span>                                     | <span data-ttu-id="22707-111">Description</span><span class="sxs-lookup"><span data-stu-id="22707-111">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="22707-112">**waveOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="22707-112">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | <span data-ttu-id="22707-113">Récupère le niveau de volume actuel du périphérique de sortie Waveform-Audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="22707-113">Retrieves the current volume level of the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="22707-114">**waveOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="22707-114">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | <span data-ttu-id="22707-115">Définit le niveau de volume du périphérique de sortie Wave-audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="22707-115">Sets the volume level of the specified waveform-audio output device.</span></span>              |



 

<span data-ttu-id="22707-116">Tous les périphériques audio Waveform ne prennent pas en charge les modifications de volume.</span><span class="sxs-lookup"><span data-stu-id="22707-116">Not all waveform-audio devices support volume changes.</span></span> <span data-ttu-id="22707-117">Certains périphériques prennent en charge le contrôle de volume individuel sur les canaux gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="22707-117">Some devices support individual volume control on both the left and right channels.</span></span> <span data-ttu-id="22707-118">Pour plus d’informations sur la façon de déterminer les capacités de contrôle de volume des périphériques Wave-audio, consultez [périphériques et types de données](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="22707-118">For information about how to determine the volume-control capabilities of waveform-audio devices, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="22707-119">Certaines applications permettent à l’utilisateur de contrôler le volume de tous les périphériques audio d’un système.</span><span class="sxs-lookup"><span data-stu-id="22707-119">Some applications allow the user to control the volume for all audio devices in a system.</span></span> <span data-ttu-id="22707-120">(De nombreuses applications de ce type utilisent les services de mixage audio. pour plus d’informations, consultez [mixages audio](audio-mixers.md)). À moins que votre application ne soit en capacité de prendre en charge ce type de contrôle de volume principal, vous devez ouvrir un périphérique audio avant de modifier son volume.</span><span class="sxs-lookup"><span data-stu-id="22707-120">(Many applications of this type use the audio mixer services; for more information, see [Audio Mixers](audio-mixers.md).) Unless your application is capable of this kind of master volume control, you should open an audio device before changing its volume.</span></span> <span data-ttu-id="22707-121">Vous devez également interroger le niveau de volume avant de le modifier et restaurer le niveau de volume précédent le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="22707-121">You should also query the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="22707-122">Le volume est spécifié dans une valeur de mot double.</span><span class="sxs-lookup"><span data-stu-id="22707-122">Volume is specified in a doubleword value.</span></span> <span data-ttu-id="22707-123">Lorsque le format audio est stéréo, les 16 bits supérieurs spécifient le volume relatif du canal droit et les 16 bits inférieurs spécifient le volume relatif du canal de gauche.</span><span class="sxs-lookup"><span data-stu-id="22707-123">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="22707-124">Pour les appareils qui ne prennent pas en charge le contrôle du volume de canal droit et gauche, les 16 bits de poids faible spécifient le niveau de volume et les 16 bits supérieurs sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="22707-124">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="22707-125">Les valeurs au niveau du volume sont comprises entre 0x0 (silence) et 0xFFFF (volume maximal) et sont interprétées de façon logarithmique.</span><span class="sxs-lookup"><span data-stu-id="22707-125">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="22707-126">L’augmentation du volume perçu est la même lors de l’augmentation du niveau de volume de 0x5000 à 0x6000, comme c’est le cas de 0x4000 à 0x5000.</span><span class="sxs-lookup"><span data-stu-id="22707-126">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 
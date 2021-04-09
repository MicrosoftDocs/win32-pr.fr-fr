---
title: Modification du volume du synthétiseur MIDI interne
description: Modification du volume du synthétiseur MIDI interne
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), synthétiseurs internes
- MIDI (Musical Instrument Digital Interface), synthétiseurs internes
- lire des fichiers MIDI, des synthétiseurs internes
- synthétiseurs MIDI internes
- MIDI (Musical Instrument Digital Interface), modification du volume
- MIDI (Musical Instrument Digital Interface), modification du volume
- Jeux de fichiers MIDI, modification du volume
- modification du volume MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940961"
---
# <a name="changing-internal-midi-synthesizer-volume"></a><span data-ttu-id="f4868-111">Modification du volume du synthétiseur MIDI interne</span><span class="sxs-lookup"><span data-stu-id="f4868-111">Changing Internal MIDI Synthesizer Volume</span></span>

<span data-ttu-id="f4868-112">Windows fournit les fonctions suivantes pour récupérer et définir le niveau de volume des appareils de synthétiseur MIDI internes :</span><span class="sxs-lookup"><span data-stu-id="f4868-112">Windows provides the following functions to retrieve and set the volume level of internal MIDI synthesizer devices:</span></span>



| <span data-ttu-id="f4868-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4868-113">Value</span></span>                                        | <span data-ttu-id="f4868-114">Signification</span><span class="sxs-lookup"><span data-stu-id="f4868-114">Meaning</span></span>                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="f4868-115">**midiOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="f4868-115">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | <span data-ttu-id="f4868-116">Récupère le niveau de volume du périphérique de synthétiseur MIDI interne spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4868-116">Retrieves the volume level of the specified internal MIDI synthesizer device.</span></span> |
| [<span data-ttu-id="f4868-117">**midiOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="f4868-117">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | <span data-ttu-id="f4868-118">Définit le niveau de volume du périphérique de synthétiseur MIDI interne spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4868-118">Sets the volume level of the specified internal MIDI synthesizer device.</span></span>      |



 

<span data-ttu-id="f4868-119">Tous les périphériques de sortie MIDI ne prennent pas en charge les modifications de volume.</span><span class="sxs-lookup"><span data-stu-id="f4868-119">Not all MIDI output devices support volume changes.</span></span> <span data-ttu-id="f4868-120">Certains appareils peuvent prendre en charge des modifications de volume individuelles sur les canaux gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="f4868-120">Some devices can support individual volume changes on both the left and right channels.</span></span> <span data-ttu-id="f4868-121">Pour plus d’informations sur la façon de déterminer si un appareil particulier prend en charge les modifications de volume, consultez [interrogation des périphériques de sortie MIDI](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="f4868-121">For information on how to determine if a particular device supports volume changes, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

<span data-ttu-id="f4868-122">À moins que votre application ne soit conçue pour être une application de contrôle de volume maître (fournit à l’utilisateur un contrôle du volume pour tous les périphériques audio d’un système), vous devez ouvrir un périphérique audio avant de modifier son volume.</span><span class="sxs-lookup"><span data-stu-id="f4868-122">Unless your application is designed to be a master volume-control application (provides the user with volume control for all audio devices in a system), you should open an audio device before changing its volume.</span></span> <span data-ttu-id="f4868-123">Vous devez également vérifier le niveau de volume avant de le modifier et restaurer le niveau de volume précédent le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="f4868-123">You should also check the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="f4868-124">Le volume est spécifié sous la forme d’une valeur de mot double.</span><span class="sxs-lookup"><span data-stu-id="f4868-124">Volume is specified as a doubleword value.</span></span> <span data-ttu-id="f4868-125">Les 16 bits supérieurs spécifient le volume relatif du canal droit, tandis que les 16 bits inférieurs spécifient le volume relatif du canal de gauche.</span><span class="sxs-lookup"><span data-stu-id="f4868-125">The upper 16 bits specify the relative volume of the right channel, and the lower 16 bits specify the relative volume of the left channel.</span></span>

<span data-ttu-id="f4868-126">Pour les appareils qui ne prennent pas en charge les modifications de volume individuelles sur les canaux gauche et droit, les 16 bits de poids faible spécifient le niveau de volume et les 16 bits supérieurs sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="f4868-126">For devices that do not support individual volume changes on both the left and right channels, the lower 16 bits specify the volume level and the upper 16 bits are ignored.</span></span> <span data-ttu-id="f4868-127">Les valeurs de la plage de niveau de volume 0x0 (silence) à 0xFFFF (volume maximal) et sont interprétées de façon logarithmique.</span><span class="sxs-lookup"><span data-stu-id="f4868-127">Values for the volume level range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="f4868-128">L’augmentation du volume perçu est la même lors de l’augmentation du niveau de volume de 0x5000 à 0x6000, comme c’est le cas de 0x4000 à 0x5000.</span><span class="sxs-lookup"><span data-stu-id="f4868-128">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 
---
title: Erreurs de Waveform-Audio
description: Erreurs de Waveform-Audio
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- MCIERR les valeurs de retour, erreurs Waveform-Audio
- Référence multimédia, erreurs Waveform-Audio
- référence pour les erreurs multimédias, Waveform-Audio
- Erreurs MCI (Media Control Interface), Waveform-Audio
- MCI (interface de contrôle multimédia), erreurs Waveform-Audio
- référence pour les erreurs MCI, Waveform-Audio
- Référence MCI, erreurs Waveform-Audio
- MCI (Media Control Interface), Erreurs
- MCI (interface de contrôle multimédia), Erreurs
- informations de référence sur MCI, Erreurs
- Informations de référence sur MCI, Erreurs
- Erreurs Waveform-Audio
- Erreurs Waveform MCI-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028805"
---
# <a name="waveform-audio-errors"></a><span data-ttu-id="f8deb-116">Erreurs de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="f8deb-116">Waveform-Audio Errors</span></span>

<span data-ttu-id="f8deb-117">Les valeurs de retour supplémentaires suivantes sont définies pour les périphériques MCI Waveform-Audio :</span><span class="sxs-lookup"><span data-stu-id="f8deb-117">The following additional return values are defined for MCI waveform-audio devices:</span></span>



| <span data-ttu-id="f8deb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8deb-118">Value</span></span>                             | <span data-ttu-id="f8deb-119">Signification</span><span class="sxs-lookup"><span data-stu-id="f8deb-119">Meaning</span></span>                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8deb-120">MCIERR \_ Wave \_ INPUTSINUSE</span><span class="sxs-lookup"><span data-stu-id="f8deb-120">MCIERR\_WAVE\_INPUTSINUSE</span></span>         | <span data-ttu-id="f8deb-121">Tous les périphériques Waveform qui peuvent enregistrer des fichiers dans le format actuel sont en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f8deb-121">All waveform devices that can record files in the current format are in use.</span></span> <span data-ttu-id="f8deb-122">Attendez que l’un de ces appareils soit libre. Ensuite, réessayez.</span><span class="sxs-lookup"><span data-stu-id="f8deb-122">Wait until one of these devices is free; then, try again.</span></span>                              |
| <span data-ttu-id="f8deb-123">MCIERR \_ Wave \_ INPUTSUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="f8deb-123">MCIERR\_WAVE\_INPUTSUNSUITABLE</span></span>    | <span data-ttu-id="f8deb-124">Aucun périphérique Waveform installé ne peut enregistrer des fichiers au format actuel.</span><span class="sxs-lookup"><span data-stu-id="f8deb-124">No installed waveform device can record files in the current format.</span></span> <span data-ttu-id="f8deb-125">Utilisez l’option pilotes du panneau de configuration pour installer un périphérique d’enregistrement de la forme d’onde approprié.</span><span class="sxs-lookup"><span data-stu-id="f8deb-125">Use the Drivers option from the Control Panel to install a suitable waveform recording device.</span></span> |
| <span data-ttu-id="f8deb-126">MCIERR \_ Wave \_ INPUTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="f8deb-126">MCIERR\_WAVE\_INPUTUNSPECIFIED</span></span>    | <span data-ttu-id="f8deb-127">Vous pouvez spécifier n’importe quel appareil d’enregistrement de la forme d’onde compatible.</span><span class="sxs-lookup"><span data-stu-id="f8deb-127">You can specify any compatible waveform recording device.</span></span>                                                                                                           |
| <span data-ttu-id="f8deb-128">MCIERR \_ Wave \_ OUTPUTSINUSE</span><span class="sxs-lookup"><span data-stu-id="f8deb-128">MCIERR\_WAVE\_OUTPUTSINUSE</span></span>        | <span data-ttu-id="f8deb-129">Tous les périphériques Waveform capables de lire des fichiers dans le format actuel sont en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f8deb-129">All waveform devices that can play files in the current format are in use.</span></span> <span data-ttu-id="f8deb-130">Attendez que l’un de ces appareils soit libre. Ensuite, réessayez.</span><span class="sxs-lookup"><span data-stu-id="f8deb-130">Wait until one of these devices is free; then, try again.</span></span>                                |
| <span data-ttu-id="f8deb-131">MCIERR \_ Wave \_ OUTPUTSUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="f8deb-131">MCIERR\_WAVE\_OUTPUTSUNSUITABLE</span></span>   | <span data-ttu-id="f8deb-132">Aucun périphérique Waveform installé ne peut lire des fichiers au format actuel.</span><span class="sxs-lookup"><span data-stu-id="f8deb-132">No installed waveform device can play files in the current format.</span></span> <span data-ttu-id="f8deb-133">Utilisez l’option pilotes du panneau de configuration pour installer un périphérique de forme d’onde approprié.</span><span class="sxs-lookup"><span data-stu-id="f8deb-133">Use the Drivers option from the Control Panel to install a suitable waveform device.</span></span>             |
| <span data-ttu-id="f8deb-134">MCIERR \_ Wave \_ OUTPUTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="f8deb-134">MCIERR\_WAVE\_OUTPUTUNSPECIFIED</span></span>   | <span data-ttu-id="f8deb-135">Vous pouvez spécifier n’importe quel périphérique de lecture de la forme d’onde compatible.</span><span class="sxs-lookup"><span data-stu-id="f8deb-135">You can specify any compatible waveform playback device.</span></span>                                                                                                            |
| <span data-ttu-id="f8deb-136">MCIERR \_ Wave \_ SETINPUTINUSE</span><span class="sxs-lookup"><span data-stu-id="f8deb-136">MCIERR\_WAVE\_SETINPUTINUSE</span></span>       | <span data-ttu-id="f8deb-137">L’appareil Waveform actuel est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f8deb-137">The current waveform device is in use.</span></span> <span data-ttu-id="f8deb-138">Attendez que l’appareil soit libre. Ensuite, réessayez de configurer l’appareil pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f8deb-138">Wait until the device is free; then, try again to set the device for recording.</span></span>                                              |
| <span data-ttu-id="f8deb-139">MCIERR \_ Wave \_ SETINPUTUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="f8deb-139">MCIERR\_WAVE\_SETINPUTUNSUITABLE</span></span>  | <span data-ttu-id="f8deb-140">L’appareil que vous utilisez pour enregistrer une forme d’onde ne peut pas reconnaître le format des données.</span><span class="sxs-lookup"><span data-stu-id="f8deb-140">The device you are using to record a waveform cannot recognize the data format.</span></span>                                                                                     |
| <span data-ttu-id="f8deb-141">MCIERR \_ Wave \_ SETOUTPUTINUSE</span><span class="sxs-lookup"><span data-stu-id="f8deb-141">MCIERR\_WAVE\_SETOUTPUTINUSE</span></span>      | <span data-ttu-id="f8deb-142">L’appareil Waveform actuel est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f8deb-142">The current waveform device is in use.</span></span> <span data-ttu-id="f8deb-143">Attendez que l’appareil soit libre. Ensuite, réessayez de configurer l’appareil pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="f8deb-143">Wait until the device is free; then, try again to set the device for playback.</span></span>                                               |
| <span data-ttu-id="f8deb-144">MCIERR \_ Wave \_ SETOUTPUTUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="f8deb-144">MCIERR\_WAVE\_SETOUTPUTUNSUITABLE</span></span> | <span data-ttu-id="f8deb-145">L’appareil que vous utilisez pour lire une forme d’onde ne peut pas reconnaître le format des données.</span><span class="sxs-lookup"><span data-stu-id="f8deb-145">The device you are using to playback a waveform cannot recognize the data format.</span></span>                                                                                   |



 

 

 





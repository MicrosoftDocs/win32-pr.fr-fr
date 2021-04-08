---
title: Erreurs de Sequencer
description: Erreurs de Sequencer
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- MCIERR les valeurs de retour, erreurs de Sequencer
- Référence multimédia, erreurs de Sequencer
- référence pour les éléments multimédias, les erreurs Sequencer
- MCI (Media Control Interface), erreurs Sequencer
- MCI (Media Control Interface), erreurs Sequencer
- informations de référence sur MCI, erreurs Sequencer
- Référence MCI, erreurs de Sequencer
- MCI (Media Control Interface), Erreurs
- MCI (interface de contrôle multimédia), Erreurs
- informations de référence sur MCI, Erreurs
- Informations de référence sur MCI, Erreurs
- Erreurs de Sequencer
- Erreurs de séquenceur MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673161"
---
# <a name="sequencer-errors"></a><span data-ttu-id="65ff3-116">Erreurs de Sequencer</span><span class="sxs-lookup"><span data-stu-id="65ff3-116">Sequencer Errors</span></span>

<span data-ttu-id="65ff3-117">Les valeurs de retour supplémentaires suivantes sont définies pour les séquenceurs MCI :</span><span class="sxs-lookup"><span data-stu-id="65ff3-117">The following additional return values are defined for MCI sequencers:</span></span>



| <span data-ttu-id="65ff3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="65ff3-118">Value</span></span>                          | <span data-ttu-id="65ff3-119">Signification</span><span class="sxs-lookup"><span data-stu-id="65ff3-119">Meaning</span></span>                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ff3-120">MCIERR \_ Seq \_ div \_ incompatible</span><span class="sxs-lookup"><span data-stu-id="65ff3-120">MCIERR\_SEQ\_DIV\_INCOMPATIBLE</span></span> | <span data-ttu-id="65ff3-121">Les formats d’heure du pointeur de la chanson et du SMPTE sont singuliers.</span><span class="sxs-lookup"><span data-stu-id="65ff3-121">The time formats of the "song pointer" and SMPTE are singular.</span></span> <span data-ttu-id="65ff3-122">Vous ne pouvez pas les utiliser ensemble.</span><span class="sxs-lookup"><span data-stu-id="65ff3-122">You can't use them together.</span></span>                                                              |
| <span data-ttu-id="65ff3-123">MCIERR \_ Seq \_ NOMIDIPRESENT</span><span class="sxs-lookup"><span data-stu-id="65ff3-123">MCIERR\_SEQ\_NOMIDIPRESENT</span></span>     | <span data-ttu-id="65ff3-124">Aucun périphérique MIDI n’est installé sur ce système.</span><span class="sxs-lookup"><span data-stu-id="65ff3-124">This system has no installed MIDI devices.</span></span> <span data-ttu-id="65ff3-125">Utilisez l’option pilotes du panneau de configuration pour installer un pilote MIDI.</span><span class="sxs-lookup"><span data-stu-id="65ff3-125">Use the Drivers option from the Control Panel to install a MIDI driver.</span></span>                                       |
| <span data-ttu-id="65ff3-126">MCIERR \_ Seq \_ port \_ Inuse</span><span class="sxs-lookup"><span data-stu-id="65ff3-126">MCIERR\_SEQ\_PORT\_INUSE</span></span>       | <span data-ttu-id="65ff3-127">Le port MIDI spécifié est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="65ff3-127">The specified MIDI port is already in use.</span></span> <span data-ttu-id="65ff3-128">Attendez qu’il soit libre ; Ensuite, réessayez.</span><span class="sxs-lookup"><span data-stu-id="65ff3-128">Wait until it is free; then, try again.</span></span>                                                                       |
| <span data-ttu-id="65ff3-129">MCIERR \_ Seq \_ port \_ MAPNODEVICE</span><span class="sxs-lookup"><span data-stu-id="65ff3-129">MCIERR\_SEQ\_PORT\_MAPNODEVICE</span></span> | <span data-ttu-id="65ff3-130">Le programme d’installation du mappeur MIDI en cours fait référence à un périphérique MIDI qui n’est pas installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="65ff3-130">The current MIDI Mapper setup refers to a MIDI device that is not installed on the system.</span></span> <span data-ttu-id="65ff3-131">Utilisez le Mappeur MIDI à partir du panneau de configuration pour modifier l’installation.</span><span class="sxs-lookup"><span data-stu-id="65ff3-131">Use the MIDI Mapper from the Control Panel to edit the setup.</span></span> |
| <span data-ttu-id="65ff3-132">MCIERR \_ Seq \_ port \_ MISCERROR</span><span class="sxs-lookup"><span data-stu-id="65ff3-132">MCIERR\_SEQ\_PORT\_MISCERROR</span></span>   | <span data-ttu-id="65ff3-133">Une erreur s’est produite avec le port spécifié.</span><span class="sxs-lookup"><span data-stu-id="65ff3-133">An error occurred with specified port.</span></span>                                                                                                                   |
| <span data-ttu-id="65ff3-134">\_port MCIERR \_ Seq \_ inexistant</span><span class="sxs-lookup"><span data-stu-id="65ff3-134">MCIERR\_SEQ\_PORT\_NONEXISTENT</span></span> | <span data-ttu-id="65ff3-135">L’appareil MIDI spécifié n’est pas installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="65ff3-135">The specified MIDI device is not installed on the system.</span></span> <span data-ttu-id="65ff3-136">Utilisez l’option pilotes du panneau de configuration pour installer un appareil MIDI.</span><span class="sxs-lookup"><span data-stu-id="65ff3-136">Use the Drivers option from the Control Panel to install a MIDI device.</span></span>                        |
| <span data-ttu-id="65ff3-137">MCIERR \_ Seq \_ PORTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="65ff3-137">MCIERR\_SEQ\_PORTUNSPECIFIED</span></span>   | <span data-ttu-id="65ff3-138">Le système n’a pas de port MIDI en cours spécifié.</span><span class="sxs-lookup"><span data-stu-id="65ff3-138">The system does not have a current MIDI port specified.</span></span>                                                                                                  |
| <span data-ttu-id="65ff3-139">MCIERR \_ Seq \_ Timer</span><span class="sxs-lookup"><span data-stu-id="65ff3-139">MCIERR\_SEQ\_TIMER</span></span>             | <span data-ttu-id="65ff3-140">Toutes les minuteries multimédias sont utilisées par d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="65ff3-140">All multimedia timers are being used by other applications.</span></span> <span data-ttu-id="65ff3-141">Quittez l’une de ces applications ; Ensuite, réessayez.</span><span class="sxs-lookup"><span data-stu-id="65ff3-141">Quit one of these applications; then, try again.</span></span>                                             |



 

 

 





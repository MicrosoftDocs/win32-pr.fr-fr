---
title: Commande MCI_CUE (mmsystem. h)
description: La \_ commande MCI CUE signale un appareil afin que la lecture ou l’enregistrement commence par un délai minimal. Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- Commande MCI_CUE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510551"
---
# <a name="mci_cue-command"></a><span data-ttu-id="728d3-105">\_Commande MCI CUE</span><span class="sxs-lookup"><span data-stu-id="728d3-105">MCI\_CUE command</span></span>

<span data-ttu-id="728d3-106">La \_ commande MCI CUE signale un appareil afin que la lecture ou l’enregistrement commence par un délai minimal.</span><span class="sxs-lookup"><span data-stu-id="728d3-106">The MCI\_CUE command cues a device so that playback or recording begins with minimum delay.</span></span> <span data-ttu-id="728d3-107">Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="728d3-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="728d3-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="728d3-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
);
```



## <a name="parameters"></a><span data-ttu-id="728d3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="728d3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="728d3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="728d3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="728d3-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="728d3-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="728d3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="728d3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="728d3-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="728d3-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="728d3-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="728d3-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="728d3-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span><span class="sxs-lookup"><span data-stu-id="728d3-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span></span>
</dt> <dd>

<span data-ttu-id="728d3-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="728d3-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="728d3-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="728d3-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="728d3-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="728d3-118">Return Value</span></span>

<span data-ttu-id="728d3-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="728d3-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="728d3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="728d3-120">Remarks</span></span>

<span data-ttu-id="728d3-121">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="728d3-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="728d3-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>\_entrée de \_ signal MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="728d3-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI\_DGV\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="728d3-123">Une instance de vidéo numérique doit préparer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="728d3-123">A digital-video instance should prepare for recording.</span></span> <span data-ttu-id="728d3-124">Si l’application n’a pas d’espace disque réservé, l’appareil réserve l’espace disque à l’aide de ses paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="728d3-124">If the application has not reserved disk space, the device reserves the disk space using its default parameters.</span></span> <span data-ttu-id="728d3-125">L’application peut omettre cet indicateur si la source de présentation actuelle est déjà l’entrée externe.</span><span class="sxs-lookup"><span data-stu-id="728d3-125">The application can omit this flag if the current presentation source is already the external input.</span></span> <span data-ttu-id="728d3-126">(Cet indicateur n’a aucun effet sur la sélection de la source de présentation.)</span><span class="sxs-lookup"><span data-stu-id="728d3-126">(This flag has no effect on selecting the presentation source.)</span></span>

</dd> <dt>

<span data-ttu-id="728d3-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI \_ DGV \_ CUE \_ NoShow</span><span class="sxs-lookup"><span data-stu-id="728d3-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI\_DGV\_CUE\_NOSHOW</span></span>
</dt> <dd>

<span data-ttu-id="728d3-128">Une instance de vidéo numérique doit préparer la diffusion du frame spécifié avec la commande sans l’afficher.</span><span class="sxs-lookup"><span data-stu-id="728d3-128">A digital-video instance should prepare for playing the frame specified with the command without displaying it.</span></span> <span data-ttu-id="728d3-129">Lorsque cet indicateur est spécifié, l’affichage continue d’afficher l’image dans la mémoire tampon de trame, même si son frame correspondant n’est pas la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="728d3-129">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="728d3-130">Par exemple, si la mémoire tampon de trame contient l’image du frame 7, l’appareil continue à afficher le cadre 7 lorsque cet indicateur est utilisé pour signaler l’appareil à une autre position.</span><span class="sxs-lookup"><span data-stu-id="728d3-130">For example, if the frame buffer contains the image from frame 7, the device continues to show frame 7 when this flag is used to cue the device to any other position.</span></span> <span data-ttu-id="728d3-131">Une commande de pile ultérieure sans cet indicateur et sans l' \_ indicateur MCI pour affiche le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="728d3-131">A subsequent cue command without this flag and without the MCI\_TO flag displays the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="728d3-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>sortie de la \_ pile MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="728d3-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI\_DGV\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="728d3-133">Une instance de vidéo numérique doit se préparer à être lue.</span><span class="sxs-lookup"><span data-stu-id="728d3-133">A digital-video instance should prepare for playing.</span></span> <span data-ttu-id="728d3-134">Si l’espace de travail est suspendu, aucun positionnement ne se produit.</span><span class="sxs-lookup"><span data-stu-id="728d3-134">If the workspace is paused, no positioning occurs.</span></span> <span data-ttu-id="728d3-135">Si l’espace de travail est arrêté, la position peut passer à une image d’image clé précédente.</span><span class="sxs-lookup"><span data-stu-id="728d3-135">If the workspace is stopped, the position might change to a previous key-frame image.</span></span> <span data-ttu-id="728d3-136">L’application peut omettre cet indicateur si la source de présentation actuelle est déjà l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="728d3-136">The application can omit this flag if the current presentation source is already the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="728d3-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers</span><span class="sxs-lookup"><span data-stu-id="728d3-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="728d3-138">La position d’un espace de travail est incluse dans le membre **dwTo** de la structure identifiée par *lpCue*.</span><span class="sxs-lookup"><span data-stu-id="728d3-138">A workspace position is included in the **dwTo** member of the structure identified by *lpCue*.</span></span> <span data-ttu-id="728d3-139">Les unités affectées aux valeurs de position sont spécifiées à l’aide \_ \_ de l' \_ indicateur de format de temps Set MCI de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="728d3-139">The units assigned to position values are specified using the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="728d3-140">Cela équivaut à la recherche d’une position, sauf que l’appareil est suspendu après la commande.</span><span class="sxs-lookup"><span data-stu-id="728d3-140">This is equivalent to seeking to a position, except the device is paused after the command.</span></span>

</dd> </dl>

<span data-ttu-id="728d3-141">Pour les appareils **Digitalvideo** , le paramètre *lpCue* pointe vers une structure [**MCI \_ DGV \_ CUE \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) .</span><span class="sxs-lookup"><span data-stu-id="728d3-141">For **digitalvideo** devices, the *lpCue* parameter points to an [**MCI\_DGV\_CUE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) structure.</span></span>

<span data-ttu-id="728d3-142">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="728d3-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="728d3-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de</span><span class="sxs-lookup"><span data-stu-id="728d3-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="728d3-144">Le membre **dwFrom** de la structure vers laquelle pointe *lpCue* contient l’emplacement de départ spécifié dans le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="728d3-144">The **dwFrom** member of the structure pointed to by *lpCue* contains the starting location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="728d3-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers</span><span class="sxs-lookup"><span data-stu-id="728d3-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="728d3-146">Le membre **dwTo** de la structure vers laquelle pointe *lpCue* contient l’emplacement de fin (suspension) spécifié dans le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="728d3-146">The **dwTo** member of the structure pointed to by *lpCue* contains the ending (pausing) location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="728d3-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>\_entrée de \_ signal de magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="728d3-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI\_VCR\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="728d3-148">Préparez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="728d3-148">Prepare for recording.</span></span>

</dd> <dt>

<span data-ttu-id="728d3-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>\_sortie de magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="728d3-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI\_VCR\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="728d3-150">Préparez-vous à la diffusion.</span><span class="sxs-lookup"><span data-stu-id="728d3-150">Prepare for playing.</span></span> <span data-ttu-id="728d3-151">Si aucune \_ \_ entrée de la file d’attente MCI magnétoscope et aucune \_ \_ \_ sortie de magnétoscope MCI \_ n’est spécifiée, la sortie de la \_ file d’attente MCI \_ \_ est supposée.</span><span class="sxs-lookup"><span data-stu-id="728d3-151">If neither MCI\_VCR\_CUE\_INPUT nor MCI\_VCR\_CUE\_OUTPUT is specified, MCI\_VCR\_CUE\_OUTPUT is assumed.</span></span>

</dd> <dt>

<span data-ttu-id="728d3-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>préroll de \_ magnétoscope MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="728d3-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI\_VCR\_CUE\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="728d3-153">Signalez l’appareil à la position actuelle ou à la position **dwFrom** , moins la durée du préroll.</span><span class="sxs-lookup"><span data-stu-id="728d3-153">Cue the device to the current position, or the **dwFrom** position, minus the preroll duration.</span></span> <span data-ttu-id="728d3-154">Cela permettra à l’appareil de se préparer lui-même avant d’entrer en mode enregistrement ou lecture.</span><span class="sxs-lookup"><span data-stu-id="728d3-154">This will allow the device to prepare itself before entering record or playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="728d3-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>\_magnétoscope de \_ signal MCI \_ inversé</span><span class="sxs-lookup"><span data-stu-id="728d3-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI\_VCR\_CUE\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="728d3-156">La direction de la commande de lecture ou d’enregistrement suivante est inversée.</span><span class="sxs-lookup"><span data-stu-id="728d3-156">The direction of the next play or record command is reverse.</span></span>

</dd> </dl>

<span data-ttu-id="728d3-157">Quand vous cueing pour la lecture à l’aide de la \_ commande MCI CUE avec l' \_ indicateur de sortie MCI VCR \_ \_ , vous pouvez annuler \_ la pile MCI en émettant la commande MCI [ \_ Play](mci-play.md) avec MCI à \_ partir de, MCI \_ à ou \_ magnétoscope MCI \_ Play \_ .</span><span class="sxs-lookup"><span data-stu-id="728d3-157">When cueing for playback by using the MCI\_CUE command with the MCI\_VCR\_CUE\_OUTPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_PLAY](mci-play.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_PLAY\_REVERSE.</span></span>

<span data-ttu-id="728d3-158">Quand vous cueing à l’enregistrement à l’aide de l' \_ indicateur MCI avec l' \_ \_ indicateur d’entrée de la file d’attente MCI \_ , vous pouvez annuler \_ la pile MCI en émettant la commande d' [ \_ enregistrement MCI](mci-record.md) avec MCI \_ de, MCI \_ à ou \_ \_ l’enregistrement magnétoscope MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="728d3-158">When cueing for recording by using MCI\_CUE with the MCI\_VCR\_CUE\_INPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_RECORD](mci-record.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_RECORD\_INITIALIZE.</span></span>

<span data-ttu-id="728d3-159">Pour les périphériques **VCR** , le paramètre *lpCue* pointe vers une structure de [**file d' \_ \_ attente \_ de magnétoscope MCI**](mci-vcr-cue-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="728d3-159">For **vcr** devices, the *lpCue* parameter points to an [**MCI\_VCR\_CUE\_PARMS**](mci-vcr-cue-parms.md) structure.</span></span>

<span data-ttu-id="728d3-160">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="728d3-160">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="728d3-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrée MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="728d3-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="728d3-162">Un appareil d’entrée Waveform-Audio doit être en signal.</span><span class="sxs-lookup"><span data-stu-id="728d3-162">A waveform-audio input device should be cued.</span></span>

</dd> <dt>

<span data-ttu-id="728d3-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_sortie MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="728d3-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="728d3-164">Un périphérique de sortie Waveform-Audio doit être en signal.</span><span class="sxs-lookup"><span data-stu-id="728d3-164">A waveform-audio output device should be cued.</span></span> <span data-ttu-id="728d3-165">Il s’agit de l’indicateur par défaut si aucun indicateur n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="728d3-165">This is the default flag if a flag is not specified.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="728d3-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="728d3-166">Requirements</span></span>



| <span data-ttu-id="728d3-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="728d3-167">Requirement</span></span> | <span data-ttu-id="728d3-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="728d3-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="728d3-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="728d3-169">Minimum supported client</span></span><br/> | <span data-ttu-id="728d3-170">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="728d3-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="728d3-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="728d3-171">Minimum supported server</span></span><br/> | <span data-ttu-id="728d3-172">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="728d3-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="728d3-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="728d3-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="728d3-174"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="728d3-174"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="728d3-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="728d3-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="728d3-176">MCI</span><span class="sxs-lookup"><span data-stu-id="728d3-176">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="728d3-177">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="728d3-177">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


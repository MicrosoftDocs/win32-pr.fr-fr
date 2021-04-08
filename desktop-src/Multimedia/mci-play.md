---
title: Commande MCI_PLAY (mmsystem. h)
description: La \_ commande MCI Play signale à l’appareil qu’il doit commencer à transmettre des données de sortie. Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- Commande MCI_PLAY Windows multimédia
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844405"
---
# <a name="mci_play-command"></a><span data-ttu-id="7c7ee-105">\_Commande MCI Play</span><span class="sxs-lookup"><span data-stu-id="7c7ee-105">MCI\_PLAY command</span></span>

<span data-ttu-id="7c7ee-106">La \_ commande MCI Play signale à l’appareil qu’il doit commencer à transmettre des données de sortie.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-106">The MCI\_PLAY command signals the device to begin transmitting output data.</span></span> <span data-ttu-id="7c7ee-107">Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="7c7ee-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
);
```



## <a name="parameters"></a><span data-ttu-id="7c7ee-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c7ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c7ee-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7c7ee-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7c7ee-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="7c7ee-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="7c7ee-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7c7ee-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span><span class="sxs-lookup"><span data-stu-id="7c7ee-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-116">Pointeur vers une structure de [**\_ \_ lecture MCI**](mci-play-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7c7ee-116">Pointer to an [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure.</span></span> <span data-ttu-id="7c7ee-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="7c7ee-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c7ee-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7c7ee-118">Return Value</span></span>

<span data-ttu-id="7c7ee-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c7ee-120">Notes</span><span class="sxs-lookup"><span data-stu-id="7c7ee-120">Remarks</span></span>

<span data-ttu-id="7c7ee-121">Les indicateurs supplémentaires suivants s’appliquent à tous les appareils prenant en charge MCI \_ Play :</span><span class="sxs-lookup"><span data-stu-id="7c7ee-121">The following additional flags apply to all devices supporting MCI\_PLAY:</span></span>

<dl> <dt>

<span data-ttu-id="7c7ee-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de</span><span class="sxs-lookup"><span data-stu-id="7c7ee-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-123">Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-123">A starting location is included in the **dwFrom** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="7c7ee-124">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="7c7ee-124">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="7c7ee-125">Si MCI \_ à partir de n’est pas spécifié, l’emplacement de départ prend par défaut la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-125">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers</span><span class="sxs-lookup"><span data-stu-id="7c7ee-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-127">Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-127">An ending location is included in the **dwTo** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="7c7ee-128">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de l' \_ ensemble MCI.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-128">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span> <span data-ttu-id="7c7ee-129">Si \_ vous ne spécifiez pas l’option MCI à, l’emplacement de fin est défini par défaut à la fin du support.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-129">If MCI\_TO is not specified, the ending location defaults to the end of the media.</span></span>

</dd> </dl>

<span data-ttu-id="7c7ee-130">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="7c7ee-130">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7c7ee-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>\_ \_ lecture \_ répétée MCI DGV</span><span class="sxs-lookup"><span data-stu-id="7c7ee-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI\_DGV\_PLAY\_REPEAT</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-132">La lecture doit redémarrer à partir du début lorsque la fin du contenu est atteinte.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-132">Playback should start again at the beginning when the end of the content is reached.</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>\_ \_ lecture \_ inversée MCI DGV</span><span class="sxs-lookup"><span data-stu-id="7c7ee-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI\_DGV\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-134">La lecture doit être effectuée en sens inverse.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-134">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>\_fenêtre de \_ lecture MCI MCIAVI \_</span><span class="sxs-lookup"><span data-stu-id="7c7ee-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI\_MCIAVI\_PLAY\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-136">La lecture doit se produire dans la fenêtre associée à une instance d’appareil (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="7c7ee-136">Playback should occur in the window associated with a device instance (the default).</span></span> <span data-ttu-id="7c7ee-137">(Cet indicateur est spécifique à MCIAVI. DRV.)</span><span class="sxs-lookup"><span data-stu-id="7c7ee-137">(This flag is specific to MCIAVI.DRV.)</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI \_ MCIAVI \_ Play \_ fullscreen</span><span class="sxs-lookup"><span data-stu-id="7c7ee-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI\_MCIAVI\_PLAY\_FULLSCREEN</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-139">La lecture doit utiliser un affichage plein écran.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-139">Playback should use a full-screen display.</span></span> <span data-ttu-id="7c7ee-140">Utilisez cet indicateur uniquement lors de la diffusion de fichiers compressés ou 8 bits.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-140">Use this flag only when playing compressed or 8-bit files.</span></span>

</dd> </dl>

<span data-ttu-id="7c7ee-141">Pour les périphériques vidéo numériques, *lpPlay* pointe vers une structure [**MCI \_ DGV \_ Play \_ PARMS**](/previous-versions//dd743396(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7c7ee-141">For digital-video devices, *lpPlay* points to an [**MCI\_DGV\_PLAY\_PARMS**](/previous-versions//dd743396(v=vs.85)) structure.</span></span>

<span data-ttu-id="7c7ee-142">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="7c7ee-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7c7ee-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>\_magnétoscope MCI \_ lu \_ à</span><span class="sxs-lookup"><span data-stu-id="7c7ee-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI\_VCR\_PLAY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-144">Le membre **dwAt** de la structure identifiée par *lpPlay* contient une heure à laquelle l’intégralité de la commande commence ou, si l’appareil est reçu, lorsque l’appareil atteint la position à partir de la commande [MCI \_ CUE](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="7c7ee-144">The **dwAt** member of the structure identified by *lpPlay* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the [MCI\_CUE](mci-cue.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>\_ \_ Lecture inversée des MAGNÉTOSCOPEs MCI \_</span><span class="sxs-lookup"><span data-stu-id="7c7ee-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI\_VCR\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-146">La lecture doit être effectuée en sens inverse.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-146">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>\_analyse de \_ lecture \_ magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="7c7ee-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI\_VCR\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-148">La lecture doit être aussi rapide que possible tout en conservant la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-148">Playback should be as fast as possible while maintaining video output.</span></span>

</dd> </dl>

<span data-ttu-id="7c7ee-149">Pour les périphériques VCR, *lpPlay* pointe vers une structure de [**\_ \_ lecture \_ de magnétoscope MCI**](mci-vcr-play-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7c7ee-149">For VCR devices, *lpPlay* points to an [**MCI\_VCR\_PLAY\_PARMS**](mci-vcr-play-parms.md) structure.</span></span>

<span data-ttu-id="7c7ee-150">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **videodisc** :</span><span class="sxs-lookup"><span data-stu-id="7c7ee-150">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7c7ee-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI \_ VD \_ Play \_ Fast</span><span class="sxs-lookup"><span data-stu-id="7c7ee-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI\_VD\_PLAY\_FAST</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-152">Jouez rapidement.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-152">Play fast.</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>\_ \_ lecture \_ inversée MCI VD</span><span class="sxs-lookup"><span data-stu-id="7c7ee-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI\_VD\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-154">Jouez en sens inverse.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-154">Play in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>\_analyse de \_ lecture MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="7c7ee-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI\_VD\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-156">Analyser rapidement.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-156">Scan quickly.</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI \_ VD \_ Play \_ lent</span><span class="sxs-lookup"><span data-stu-id="7c7ee-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI\_VD\_PLAY\_SLOW</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-158">Jouez lentement.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-158">Play slowly.</span></span>

</dd> <dt>

<span data-ttu-id="7c7ee-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>\_vitesse de \_ lecture MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="7c7ee-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI\_VD\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="7c7ee-160">La vitesse de lecture est incluse dans le membre **dwSpeed** de la structure identifiée par *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="7c7ee-160">The play speed is included in the **dwSpeed** member in the structure identified by *lpPlay*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c7ee-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c7ee-161">Requirements</span></span>



| <span data-ttu-id="7c7ee-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c7ee-162">Requirement</span></span> | <span data-ttu-id="7c7ee-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c7ee-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c7ee-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c7ee-164">Minimum supported client</span></span><br/> | <span data-ttu-id="7c7ee-165">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c7ee-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c7ee-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c7ee-166">Minimum supported server</span></span><br/> | <span data-ttu-id="7c7ee-167">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c7ee-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7c7ee-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c7ee-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c7ee-169"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c7ee-169"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c7ee-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c7ee-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c7ee-171">MCI</span><span class="sxs-lookup"><span data-stu-id="7c7ee-171">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7c7ee-172">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="7c7ee-172">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


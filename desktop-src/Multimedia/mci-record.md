---
title: Commande MCI_RECORD (mmsystem. h)
description: La \_ commande d’enregistrement MCI démarre l’enregistrement à partir de la position actuelle ou d’un emplacement spécifié vers un autre emplacement spécifié.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- Commande MCI_RECORD Windows multimédia
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104011"
---
# <a name="mci_record-command"></a><span data-ttu-id="a8e46-104">\_Commande d’enregistrement MCI</span><span class="sxs-lookup"><span data-stu-id="a8e46-104">MCI\_RECORD command</span></span>

<span data-ttu-id="a8e46-105">La commande d' [**\_ enregistrement MCI**](mci-record-parms.md) démarre l’enregistrement à partir de la position actuelle ou d’un emplacement spécifié vers un autre emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="a8e46-105">The [**MCI\_RECORD**](mci-record-parms.md) command starts recording from the current position or from one specified location to another specified location.</span></span> <span data-ttu-id="a8e46-106">Les périphériques VCR et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="a8e46-106">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="a8e46-107">Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne les implémentent pas.</span><span class="sxs-lookup"><span data-stu-id="a8e46-107">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="a8e46-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="a8e46-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
);
```



## <a name="parameters"></a><span data-ttu-id="a8e46-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8e46-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8e46-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a8e46-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="a8e46-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a8e46-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a8e46-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a8e46-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="a8e46-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a8e46-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8e46-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span><span class="sxs-lookup"><span data-stu-id="a8e46-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-116">Pointeur vers une structure d' [**\_ \_ enregistrement MCI**](mci-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e46-116">Pointer to an [**MCI\_RECORD\_PARMS**](mci-record-parms.md) structure.</span></span> <span data-ttu-id="a8e46-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="a8e46-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8e46-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a8e46-118">Return Value</span></span>

<span data-ttu-id="a8e46-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="a8e46-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8e46-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a8e46-120">Remarks</span></span>

<span data-ttu-id="a8e46-121">Cette commande est prise en charge par les appareils qui renvoient la **valeur true** lorsque vous appelez la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) avec l' \_ indicateur d’enregistrement MCI GETDEVCAPS \_ CAN \_ .</span><span class="sxs-lookup"><span data-stu-id="a8e46-121">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_RECORD flag.</span></span> <span data-ttu-id="a8e46-122">Pour le pilote MCIWAVE, toutes les données enregistrées après l’ouverture d’un fichier sont ignorées si le fichier est fermé sans l’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="a8e46-122">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="a8e46-123">Les indicateurs supplémentaires suivants s’appliquent à tous les appareils prenant en charge l' \_ enregistrement MCI :</span><span class="sxs-lookup"><span data-stu-id="a8e46-123">The following additional flags apply to all devices supporting MCI\_RECORD:</span></span>

<dl> <dt>

<span data-ttu-id="a8e46-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de</span><span class="sxs-lookup"><span data-stu-id="a8e46-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-125">Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="a8e46-125">A starting location is included in the **dwFrom** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="a8e46-126">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e46-126">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="a8e46-127">Si MCI \_ à partir de n’est pas spécifié, l’emplacement de départ prend par défaut la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="a8e46-127">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="a8e46-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>\_insertion d’enregistrement MCI \_</span><span class="sxs-lookup"><span data-stu-id="a8e46-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI\_RECORD\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-129">Les informations nouvellement enregistrées doivent être insérées ou collées dans les données existantes.</span><span class="sxs-lookup"><span data-stu-id="a8e46-129">Newly recorded information should be inserted or pasted into the existing data.</span></span> <span data-ttu-id="a8e46-130">Il se peut que certains appareils ne prennent pas en charge cette opération.</span><span class="sxs-lookup"><span data-stu-id="a8e46-130">Some devices might not support this.</span></span> <span data-ttu-id="a8e46-131">S’il est pris en charge, il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a8e46-131">If supported, this is the default.</span></span>

</dd> <dt>

<span data-ttu-id="a8e46-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>\_remplacement d’enregistrement MCI \_</span><span class="sxs-lookup"><span data-stu-id="a8e46-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI\_RECORD\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-133">Les données doivent remplacer les données existantes.</span><span class="sxs-lookup"><span data-stu-id="a8e46-133">Data should overwrite existing data.</span></span> <span data-ttu-id="a8e46-134">MCIWAVE. L’appareil DRV retourne une \_ fonction non prise en charge MCIERR \_ en réponse à cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="a8e46-134">The MCIWAVE.DRV device returns MCIERR\_UNSUPPORTED\_FUNCTION in response to this flag.</span></span>

</dd> <dt>

<span data-ttu-id="a8e46-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers</span><span class="sxs-lookup"><span data-stu-id="a8e46-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-136">Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="a8e46-136">An ending location is included in the **dwTo** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="a8e46-137">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e46-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="a8e46-138">Si MCI \_ à n’est pas spécifié, l’emplacement de fin se trouve par défaut à la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="a8e46-138">If MCI\_TO is not specified, the ending location defaults to the end of the content.</span></span>

</dd> </dl>

<span data-ttu-id="a8e46-139">Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="a8e46-139">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a8e46-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI \_ DGV \_ enregistrement \_ audio \_ Stream</span><span class="sxs-lookup"><span data-stu-id="a8e46-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI\_DGV\_RECORD\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-141">Un numéro de flux audio est inclus dans le membre **dwAudioStream** de la structure identifiée par *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="a8e46-141">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="a8e46-142">Si vous omettez cet indicateur, les données audio sont enregistrées dans le premier flux physique.</span><span class="sxs-lookup"><span data-stu-id="a8e46-142">If you omit this flag, audio data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="a8e46-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>\_blocage d' \_ enregistrement \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="a8e46-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI\_DGV\_RECORD\_HOLD</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-144">Lorsque l’enregistrement s’arrête, l’écran contiendra la dernière image et ne reprend pas l’affichage de la vidéo tant qu’une commande [MCI \_ Monitor](mci-monitor.md) n’est pas émise.</span><span class="sxs-lookup"><span data-stu-id="a8e46-144">When recording stops, the screen will hold the last image and will not resume showing the video until an [MCI\_MONITOR](mci-monitor.md) command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="a8e46-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>\_ \_ \_ flux vidéo de l’enregistrement DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a8e46-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI\_DGV\_RECORD\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-146">Un numéro de flux vidéo est inclus dans le membre **dwVideoStream** de la structure identifiée par *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="a8e46-146">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="a8e46-147">Si vous omettez cet indicateur, les données vidéo sont enregistrées dans le premier flux physique.</span><span class="sxs-lookup"><span data-stu-id="a8e46-147">If you omit this flag, video data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="a8e46-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a8e46-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-149">Un rectangle est spécifié dans le membre **RC** de la structure identifiée par *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="a8e46-149">A rectangle is specified in the **rc** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="a8e46-150">Le rectangle spécifie la région de l’entrée externe utilisée comme source pour les pixels compressés et enregistrés.</span><span class="sxs-lookup"><span data-stu-id="a8e46-150">The rectangle specifies the region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="a8e46-151">Par défaut, ce rectangle est le rectangle spécifié (ou par défaut) par l' \_ indicateur MCI DGV \_ put \_ Video pour la commande [ \_ put MCI](mci-put.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e46-151">This rectangle defaults to the rectangle specified (or defaulted) by the MCI\_DGV\_PUT\_VIDEO flag for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="a8e46-152">Lorsqu’il est défini différemment du rectangle vidéo, ce qui est affiché n’est pas ce qui est enregistré</span><span class="sxs-lookup"><span data-stu-id="a8e46-152">When it is set differently than the video rectangle, what is displayed is not what is recorded</span></span>

</dd> </dl>

<span data-ttu-id="a8e46-153">Pour les périphériques vidéo numériques, *lpRecord* pointe vers une structure de gestion des [**\_ \_ enregistrements \_ MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) .</span><span class="sxs-lookup"><span data-stu-id="a8e46-153">For digital-video devices, *lpRecord* points to an [**MCI\_DGV\_RECORD\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) structure.</span></span>

<span data-ttu-id="a8e46-154">Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="a8e46-154">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a8e46-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>\_enregistrement magnétoscope \_ MCI \_ à l’adresse</span><span class="sxs-lookup"><span data-stu-id="a8e46-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI\_VCR\_RECORD\_AT</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-156">Le membre **dwAt** de la structure identifiée par *lpRecord* contient une heure à laquelle l’intégralité de la commande commence ou, si l’appareil est reçu, lorsque l’appareil atteint la position à partir de la commande CUE.</span><span class="sxs-lookup"><span data-stu-id="a8e46-156">The **dwAt** member of the structure identified by *lpRecord* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the cue command.</span></span>

</dd> <dt>

<span data-ttu-id="a8e46-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>\_initialisation de \_ l’enregistrement magnétoscope \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a8e46-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI\_VCR\_RECORD\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="a8e46-158">Recherchez l’appareil au début du support, commencez l’enregistrement de la vidéo et de l’audio vides, puis enregistrez le code temporel, si possible.</span><span class="sxs-lookup"><span data-stu-id="a8e46-158">Seek the device to the start of the media, begin recording blank video and audio, and record timecode, if possible.</span></span>

</dd> </dl>

<span data-ttu-id="a8e46-159">Pour les périphériques VCR, *lpRecord* pointe vers une structure d' [**\_ \_ enregistrement \_ de magnétoscope MCI**](mci-vcr-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e46-159">For VCR devices, *lpRecord* points to an [**MCI\_VCR\_RECORD\_PARMS**](mci-vcr-record-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e46-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8e46-160">Requirements</span></span>



| <span data-ttu-id="a8e46-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8e46-161">Requirement</span></span> | <span data-ttu-id="a8e46-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8e46-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e46-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8e46-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e46-164">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8e46-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a8e46-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8e46-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e46-166">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8e46-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a8e46-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8e46-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8e46-168"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8e46-168"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8e46-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8e46-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e46-170">MCI</span><span class="sxs-lookup"><span data-stu-id="a8e46-170">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a8e46-171">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="a8e46-171">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


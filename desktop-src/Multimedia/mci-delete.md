---
title: Commande MCI_DELETE (mmsystem. h)
description: La \_ commande MCI Delete supprime les données du fichier. Les périphériques vidéo numériques et Waveform-Audio reconnaissent cette commande.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- Commande MCI_DELETE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942437"
---
# <a name="mci_delete-command"></a><span data-ttu-id="ddfc9-105">\_Commande de suppression MCI</span><span class="sxs-lookup"><span data-stu-id="ddfc9-105">MCI\_DELETE command</span></span>

<span data-ttu-id="ddfc9-106">La \_ commande MCI Delete supprime les données du fichier.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-106">The MCI\_DELETE command removes data from the file.</span></span> <span data-ttu-id="ddfc9-107">Les périphériques vidéo numériques et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="ddfc9-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
);
```



## <a name="parameters"></a><span data-ttu-id="ddfc9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddfc9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddfc9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ddfc9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ddfc9-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ddfc9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ddfc9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ddfc9-113">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="ddfc9-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="ddfc9-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ddfc9-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddfc9-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span><span class="sxs-lookup"><span data-stu-id="ddfc9-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span></span>
</dt> <dd>

<span data-ttu-id="ddfc9-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ddfc9-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="ddfc9-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="ddfc9-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddfc9-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ddfc9-118">Return Value</span></span>

<span data-ttu-id="ddfc9-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddfc9-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ddfc9-120">Remarks</span></span>

<span data-ttu-id="ddfc9-121">Les indicateurs suivants s’appliquent au type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="ddfc9-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ddfc9-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ supprimer \_ à</span><span class="sxs-lookup"><span data-stu-id="ddfc9-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI\_DGV\_DELETE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="ddfc9-123">Un rectangle est inclus dans le membre **RC** de la structure identifiée par *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-123">A rectangle is included in the **rc** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="ddfc9-124">Le rectangle spécifie la partie de chaque cadre à supprimer.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-124">The rectangle specifies the portion of each frame to delete.</span></span> <span data-ttu-id="ddfc9-125">Lorsque cet indicateur est utilisé, le frame est conservé dans l’espace de travail et la zone spécifiée par le rectangle devient noire.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-125">When this flag is used, the frame is retained in the workspace and the area specified by the rectangle becomes black.</span></span> <span data-ttu-id="ddfc9-126">Si l’indicateur est omis, MCI \_ supprime par défaut l’ensemble du frame et supprime le frame de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-126">If the flag is omitted, MCI\_DELETE defaults to the entire frame and removes the frame from the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="ddfc9-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ supprimer \_ le \_ flux audio</span><span class="sxs-lookup"><span data-stu-id="ddfc9-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI\_DGV\_DELETE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="ddfc9-128">Un numéro de flux audio est inclus dans le membre **dwAudioStream** de la structure identifiée par *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-128">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="ddfc9-129">Si vous utilisez cet indicateur et que vous souhaitez également supprimer la vidéo, vous devez également utiliser \_ l' \_ indicateur MCI DGV supprimer le \_ \_ flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-129">If you use this flag and also want to delete video, you must also use the MCI\_DGV\_DELETE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="ddfc9-130">(Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont supprimées.)</span><span class="sxs-lookup"><span data-stu-id="ddfc9-130">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="ddfc9-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>\_ \_ flux vidéo de suppression de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ddfc9-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI\_DGV\_DELETE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="ddfc9-132">Un numéro de flux vidéo est inclus dans le membre **dwVideoStream** de la structure identifiée par *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-132">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="ddfc9-133">Si vous utilisez cet indicateur et que vous souhaitez également supprimer l’audio, vous devez également utiliser \_ l' \_ indicateur MCI DGV supprimer le \_ \_ flux audio.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-133">If you use this flag and also want to delete audio, you must also use the MCI\_DGV\_DELETE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="ddfc9-134">(Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont supprimées.)</span><span class="sxs-lookup"><span data-stu-id="ddfc9-134">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="ddfc9-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de</span><span class="sxs-lookup"><span data-stu-id="ddfc9-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="ddfc9-136">Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-136">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="ddfc9-137">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="ddfc9-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="ddfc9-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers</span><span class="sxs-lookup"><span data-stu-id="ddfc9-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="ddfc9-139">Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-139">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="ddfc9-140">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de l' \_ ensemble MCI.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-140">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="ddfc9-141">Pour les périphériques vidéo numériques, le paramètre *lpDelete* pointe vers une structure [**MCI \_ DGV \_ Delete \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) .</span><span class="sxs-lookup"><span data-stu-id="ddfc9-141">For digital-video devices, the *lpDelete* parameter points to an [**MCI\_DGV\_DELETE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) structure.</span></span>

<span data-ttu-id="ddfc9-142">Les indicateurs suivants s’appliquent au type d’appareil **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="ddfc9-142">The following flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ddfc9-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de</span><span class="sxs-lookup"><span data-stu-id="ddfc9-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="ddfc9-144">Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-144">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="ddfc9-145">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de l' [ \_ ensemble MCI](mci-set.md).</span><span class="sxs-lookup"><span data-stu-id="ddfc9-145">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of [MCI\_SET](mci-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="ddfc9-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers</span><span class="sxs-lookup"><span data-stu-id="ddfc9-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="ddfc9-147">Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-147">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="ddfc9-148">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de l' \_ ensemble MCI.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-148">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="ddfc9-149">Pour les périphériques audio Waveform, le paramètre *lpDelete* pointe vers une structure [**MCI \_ Wave \_ supprimer \_ PARMS**](mci-wave-delete-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ddfc9-149">For waveform-audio devices, the *lpDelete* parameter points to an [**MCI\_WAVE\_DELETE\_PARMS**](mci-wave-delete-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddfc9-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddfc9-150">Requirements</span></span>



| <span data-ttu-id="ddfc9-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddfc9-151">Requirement</span></span> | <span data-ttu-id="ddfc9-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddfc9-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddfc9-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddfc9-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ddfc9-154">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddfc9-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ddfc9-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddfc9-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ddfc9-156">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddfc9-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ddfc9-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddfc9-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddfc9-158"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc9-158"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddfc9-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddfc9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddfc9-160">MCI</span><span class="sxs-lookup"><span data-stu-id="ddfc9-160">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ddfc9-161">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="ddfc9-161">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


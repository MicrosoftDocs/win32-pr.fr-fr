---
title: Commande MCI_COPY (mmsystem. h)
description: La \_ commande de copie MCI copie les données dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- Commande MCI_COPY Windows multimédia
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942188"
---
# <a name="mci_copy-command"></a><span data-ttu-id="41f83-105">\_Commande de copie MCI</span><span class="sxs-lookup"><span data-stu-id="41f83-105">MCI\_COPY command</span></span>

<span data-ttu-id="41f83-106">La \_ commande de copie MCI copie les données dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="41f83-106">The MCI\_COPY command copies data to the clipboard.</span></span> <span data-ttu-id="41f83-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="41f83-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="41f83-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="41f83-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
);
```



## <a name="parameters"></a><span data-ttu-id="41f83-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41f83-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41f83-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="41f83-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="41f83-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="41f83-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="41f83-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="41f83-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="41f83-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="41f83-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="41f83-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="41f83-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="41f83-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span><span class="sxs-lookup"><span data-stu-id="41f83-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span></span>
</dt> <dd>

<span data-ttu-id="41f83-116">Pointeur vers une structure de [**\_ DGV de \_ copie \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .</span><span class="sxs-lookup"><span data-stu-id="41f83-116">Pointer to an [**MCI\_DGV\_COPY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41f83-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41f83-117">Return Value</span></span>

<span data-ttu-id="41f83-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="41f83-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41f83-119">Notes</span><span class="sxs-lookup"><span data-stu-id="41f83-119">Remarks</span></span>

<span data-ttu-id="41f83-120">Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :</span><span class="sxs-lookup"><span data-stu-id="41f83-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="41f83-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>\_ \_ copie de DGV MCI à l' \_ adresse</span><span class="sxs-lookup"><span data-stu-id="41f83-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI\_DGV\_COPY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="41f83-122">Un rectangle est inclus dans le membre **RC** de la structure identifiée par *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="41f83-122">A rectangle is included in the **rc** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="41f83-123">Le rectangle spécifie la partie de chaque cadre à copier.</span><span class="sxs-lookup"><span data-stu-id="41f83-123">The rectangle specifies the portion of each frame to copy.</span></span> <span data-ttu-id="41f83-124">Si l’indicateur est omis, la \_ copie MCI copie l’intégralité du frame.</span><span class="sxs-lookup"><span data-stu-id="41f83-124">If the flag is omitted, MCI\_COPY copies the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="41f83-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI \_ DGV \_ copier \_ un \_ flux audio</span><span class="sxs-lookup"><span data-stu-id="41f83-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI\_DGV\_COPY\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="41f83-126">Un numéro de flux audio est inclus dans le membre **dwAudioStream** de la structure identifiée par *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="41f83-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="41f83-127">Si vous utilisez cet indicateur et que vous souhaitez également copier la vidéo, vous devez également utiliser \_ l' \_ indicateur MCI DGV copier le \_ \_ flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="41f83-127">If you use this flag and also want to copy video, you must also use the MCI\_DGV\_COPY\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="41f83-128">(Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont copiées.)</span><span class="sxs-lookup"><span data-stu-id="41f83-128">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="41f83-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>\_ \_ flux vidéo de copie MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="41f83-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI\_DGV\_COPY\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="41f83-130">Un numéro de flux vidéo est inclus dans le membre **dwVideoStream** de la structure identifiée par *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="41f83-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="41f83-131">Si vous utilisez cet indicateur et que vous souhaitez également copier l’audio, vous devez également utiliser \_ l' \_ indicateur MCI DGV copier le \_ \_ flux audio.</span><span class="sxs-lookup"><span data-stu-id="41f83-131">If you use this flag and also want to copy audio, you must also use the MCI\_DGV\_COPY\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="41f83-132">(Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont copiées.)</span><span class="sxs-lookup"><span data-stu-id="41f83-132">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="41f83-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de</span><span class="sxs-lookup"><span data-stu-id="41f83-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="41f83-134">Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="41f83-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="41f83-135">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="41f83-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="41f83-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers</span><span class="sxs-lookup"><span data-stu-id="41f83-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="41f83-137">Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="41f83-137">An ending location is included in the **dwTo** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="41f83-138">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la \_ commande Set MCI.</span><span class="sxs-lookup"><span data-stu-id="41f83-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the MCI\_SET command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41f83-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41f83-139">Requirements</span></span>



| <span data-ttu-id="41f83-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41f83-140">Requirement</span></span> | <span data-ttu-id="41f83-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="41f83-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f83-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41f83-142">Minimum supported client</span></span><br/> | <span data-ttu-id="41f83-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41f83-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="41f83-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41f83-144">Minimum supported server</span></span><br/> | <span data-ttu-id="41f83-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41f83-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="41f83-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="41f83-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="41f83-147"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41f83-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41f83-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41f83-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f83-149">MCI</span><span class="sxs-lookup"><span data-stu-id="41f83-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="41f83-150">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="41f83-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


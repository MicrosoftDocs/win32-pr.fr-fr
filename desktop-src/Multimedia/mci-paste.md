---
title: Commande MCI_PASTE (mmsystem. h)
description: La \_ commande de collage MCI colle les données du presse-papiers dans un fichier. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- Commande MCI_PASTE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739828"
---
# <a name="mci_paste-command"></a><span data-ttu-id="d36d4-105">\_Commande de collage MCI</span><span class="sxs-lookup"><span data-stu-id="d36d4-105">MCI\_PASTE command</span></span>

<span data-ttu-id="d36d4-106">La \_ commande de collage MCI colle les données du presse-papiers dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="d36d4-106">The MCI\_PASTE command pastes data from the clipboard into a file.</span></span> <span data-ttu-id="d36d4-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="d36d4-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d36d4-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="d36d4-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
);
```



## <a name="parameters"></a><span data-ttu-id="d36d4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d36d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d36d4-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d36d4-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d36d4-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="d36d4-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d36d4-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d36d4-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d36d4-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="d36d4-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="d36d4-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d36d4-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d36d4-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span><span class="sxs-lookup"><span data-stu-id="d36d4-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span></span>
</dt> <dd>

<span data-ttu-id="d36d4-116">Pointeur vers une structure [**MCI \_ DGV \_ coller \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) .</span><span class="sxs-lookup"><span data-stu-id="d36d4-116">Pointer to an [**MCI\_ DGV\_ PASTE\_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d36d4-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d36d4-117">Return Value</span></span>

<span data-ttu-id="d36d4-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="d36d4-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d36d4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d36d4-119">Remarks</span></span>

<span data-ttu-id="d36d4-120">Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :</span><span class="sxs-lookup"><span data-stu-id="d36d4-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="d36d4-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>DGV MCI, \_ \_ coller \_ à l’adresse</span><span class="sxs-lookup"><span data-stu-id="d36d4-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI\_DGV\_PASTE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="d36d4-122">Un rectangle est inclus dans le membre **RC** de la structure identifiée par *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="d36d4-122">A rectangle is included in the **rc** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="d36d4-123">Les deux premières valeurs du rectangle spécifient le point dans le frame où placer les informations du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="d36d4-123">The first two values of the rectangle specify the point within the frame to place the clipboard information.</span></span> <span data-ttu-id="d36d4-124">Si la hauteur et la largeur du rectangle sont différente de zéro, le contenu du presse-papiers est mis à l’échelle avec ces dimensions lorsqu’elles sont collées dans le cadre.</span><span class="sxs-lookup"><span data-stu-id="d36d4-124">If the rectangle height and width are nonzero, the clipboard contents are scaled to those dimensions when they are pasted in the frame.</span></span> <span data-ttu-id="d36d4-125">Si l’indicateur est omis, MCI \_ colle par défaut le rectangle de cadre entier.</span><span class="sxs-lookup"><span data-stu-id="d36d4-125">If the flag is omitted, MCI\_PASTE defaults to the entire frame rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d36d4-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ coller \_ un \_ flux audio</span><span class="sxs-lookup"><span data-stu-id="d36d4-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI\_DGV\_PASTE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="d36d4-127">Un numéro de flux audio est inclus dans le membre **dwAudioStream** de la structure identifiée par *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="d36d4-127">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="d36d4-128">S’il n’existe qu’un seul flux audio dans le presse-papiers, les données audio sont collées dans le flux désigné.</span><span class="sxs-lookup"><span data-stu-id="d36d4-128">If only one audio stream exists on the clipboard, the audio data is pasted into the designated stream.</span></span> <span data-ttu-id="d36d4-129">Si plusieurs flux audio existent dans le presse-papiers, le flux indique le numéro de départ des séquences de flux.</span><span class="sxs-lookup"><span data-stu-id="d36d4-129">If more than one audio stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="d36d4-130">Si vous utilisez cet indicateur et que vous souhaitez également coller la vidéo, vous devez également utiliser \_ l' \_ indicateur MCI DGV coller la \_ vidéo \_ .</span><span class="sxs-lookup"><span data-stu-id="d36d4-130">If you use this flag and also want to paste video, you must also use the MCI\_DGV\_PASTE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="d36d4-131">(Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont collés à partir du premier flux audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="d36d4-131">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="d36d4-132">Chaque flux collé conserve son numéro de flux d’origine.)</span><span class="sxs-lookup"><span data-stu-id="d36d4-132">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="d36d4-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>\_DGV MCI \_ \_ Insérer</span><span class="sxs-lookup"><span data-stu-id="d36d4-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI\_DGV\_PASTE\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="d36d4-134">Les données du presse-papiers doivent être insérées dans l’espace de travail existant à l’emplacement spécifié par l’MCI \_ pour l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="d36d4-134">Clipboard data should be inserted in the existing workspace at the position specified by the MCI\_TO flag.</span></span> <span data-ttu-id="d36d4-135">Toutes les données existantes après le point d’insertion sont déplacées dans l’espace de travail pour faire de la place.</span><span class="sxs-lookup"><span data-stu-id="d36d4-135">Any existing data after the insertion point is moved in the workspace to make room.</span></span> <span data-ttu-id="d36d4-136">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d36d4-136">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="d36d4-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>REMPLACEMENT de DGV MCI par le \_ \_ Collage \_</span><span class="sxs-lookup"><span data-stu-id="d36d4-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI\_DGV\_PASTE\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="d36d4-138">Les données du presse-papiers doivent remplacer les données déjà présentes dans l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="d36d4-138">Clipboard data should replace data already present in the workspace.</span></span> <span data-ttu-id="d36d4-139">Les données de l’espace de travail remplacées suivent le point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="d36d4-139">The workspace data replaced follows the insertion point.</span></span>

</dd> <dt>

<span data-ttu-id="d36d4-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>\_DGV MCI \_ coller \_ le \_ flux vidéo</span><span class="sxs-lookup"><span data-stu-id="d36d4-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI\_DGV\_PASTE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="d36d4-141">Un numéro de flux vidéo est inclus dans le membre **dwVideoStream** de la structure identifiée par *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="d36d4-141">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="d36d4-142">S’il n’existe qu’un seul flux vidéo dans le presse-papiers, les données vidéo sont collées dans le flux désigné.</span><span class="sxs-lookup"><span data-stu-id="d36d4-142">If only one video stream exists on the clipboard, the video data is pasted into the designated stream.</span></span> <span data-ttu-id="d36d4-143">Si plusieurs flux vidéo existent dans le presse-papiers, le flux indique le numéro de départ des séquences de flux.</span><span class="sxs-lookup"><span data-stu-id="d36d4-143">If more than one video stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="d36d4-144">Si vous utilisez cet indicateur et que vous souhaitez également coller l’audio, vous devez également utiliser \_ l' \_ indicateur MCI DGV coller le \_ \_ flux audio.</span><span class="sxs-lookup"><span data-stu-id="d36d4-144">If you use this flag and also want to paste audio, you must also use the MCI\_DGV\_PASTE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="d36d4-145">(Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont collés à partir du premier flux audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="d36d4-145">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="d36d4-146">Chaque flux collé conserve son numéro de flux d’origine.)</span><span class="sxs-lookup"><span data-stu-id="d36d4-146">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="d36d4-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers</span><span class="sxs-lookup"><span data-stu-id="d36d4-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="d36d4-148">Une valeur position est incluse dans le membre **dwTo** de la structure identifiée par *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="d36d4-148">A position value is included in the **dwTo** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="d36d4-149">La valeur position spécifie la position à partir de laquelle commencer le collage des données dans l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="d36d4-149">The position value specifies the position to begin pasting data into the workspace.</span></span> <span data-ttu-id="d36d4-150">Si cet indicateur est omis, la position par défaut correspond à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="d36d4-150">If this flag is omitted, the position defaults to the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d36d4-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d36d4-151">Requirements</span></span>



| <span data-ttu-id="d36d4-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d36d4-152">Requirement</span></span> | <span data-ttu-id="d36d4-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="d36d4-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d36d4-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d36d4-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d36d4-155">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d36d4-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d36d4-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d36d4-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d36d4-157">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d36d4-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d36d4-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="d36d4-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d36d4-159"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d36d4-159"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d36d4-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d36d4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d36d4-161">MCI</span><span class="sxs-lookup"><span data-stu-id="d36d4-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d36d4-162">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="d36d4-162">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


---
title: Commande MCI_CUT (mmsystem. h)
description: La \_ commande MCI Cut supprime les données du fichier et les copie dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- Commande MCI_CUT Windows multimédia
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942438"
---
# <a name="mci_cut-command"></a><span data-ttu-id="5ac64-105">\_Commande MCI Cut</span><span class="sxs-lookup"><span data-stu-id="5ac64-105">MCI\_CUT command</span></span>

<span data-ttu-id="5ac64-106">La \_ commande MCI Cut supprime les données du fichier et les copie dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="5ac64-106">The MCI\_CUT command removes data from the file and copies it to the clipboard.</span></span> <span data-ttu-id="5ac64-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="5ac64-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="5ac64-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="5ac64-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
);
```



## <a name="parameters"></a><span data-ttu-id="5ac64-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ac64-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac64-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5ac64-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5ac64-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="5ac64-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5ac64-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5ac64-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5ac64-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="5ac64-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="5ac64-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5ac64-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ac64-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span><span class="sxs-lookup"><span data-stu-id="5ac64-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span></span>
</dt> <dd>

<span data-ttu-id="5ac64-116">Pointeur vers une structure [**MCI \_ DGV \_ Cut \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) .</span><span class="sxs-lookup"><span data-stu-id="5ac64-116">Pointer to an [**MCI\_DGV\_CUT\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac64-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5ac64-117">Return Value</span></span>

<span data-ttu-id="5ac64-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="5ac64-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac64-119">Notes</span><span class="sxs-lookup"><span data-stu-id="5ac64-119">Remarks</span></span>

<span data-ttu-id="5ac64-120">Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :</span><span class="sxs-lookup"><span data-stu-id="5ac64-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="5ac64-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>\_DGV MCI \_ \_ à</span><span class="sxs-lookup"><span data-stu-id="5ac64-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI\_DGV\_CUT\_AT</span></span>
</dt> <dd>

<span data-ttu-id="5ac64-122">Un rectangle est inclus dans le membre **RC** de la structure identifiée par *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="5ac64-122">A rectangle is included in the **rc** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="5ac64-123">Le rectangle spécifie la partie de chaque cadre à couper.</span><span class="sxs-lookup"><span data-stu-id="5ac64-123">The rectangle specifies the portion of each frame to cut.</span></span> <span data-ttu-id="5ac64-124">Si l’indicateur est omis, MCI \_ coupe le cadre entier.</span><span class="sxs-lookup"><span data-stu-id="5ac64-124">If the flag is omitted, MCI\_CUT cuts the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="5ac64-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI \_ DGV \_ couper \_ le \_ flux audio</span><span class="sxs-lookup"><span data-stu-id="5ac64-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI\_DGV\_CUT\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="5ac64-126">Un numéro de flux audio est inclus dans le membre **dwAudioStream** de la structure identifiée par *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="5ac64-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="5ac64-127">Si vous utilisez cet indicateur et que vous souhaitez également couper la vidéo, vous devez également utiliser \_ l' \_ indicateur MCI DGV Cut \_ Video \_ Stream.</span><span class="sxs-lookup"><span data-stu-id="5ac64-127">If you use this flag and also want to cut video, you must also use the MCI\_DGV\_CUT\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="5ac64-128">(Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont coupées.)</span><span class="sxs-lookup"><span data-stu-id="5ac64-128">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="5ac64-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>\_ \_ flux vidéo de coupure MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="5ac64-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>MCI\_DGV\_CUT\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="5ac64-130">Un numéro de flux vidéo est inclus dans le membre **dwVideoStream** de la structure identifiée par *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="5ac64-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="5ac64-131">Si vous utilisez cet indicateur et que vous souhaitez également couper le son, vous devez également utiliser \_ l' \_ indicateur MCI DGV couper le \_ \_ flux audio.</span><span class="sxs-lookup"><span data-stu-id="5ac64-131">If you use this flag and also want to cut audio, you must also use the MCI\_DGV\_CUT\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="5ac64-132">(Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont coupées.)</span><span class="sxs-lookup"><span data-stu-id="5ac64-132">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="5ac64-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de</span><span class="sxs-lookup"><span data-stu-id="5ac64-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="5ac64-134">Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="5ac64-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="5ac64-135">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="5ac64-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="5ac64-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers</span><span class="sxs-lookup"><span data-stu-id="5ac64-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="5ac64-137">Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="5ac64-137">An ending location is included in the **dwTo** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="5ac64-138">Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de l' \_ ensemble MCI.</span><span class="sxs-lookup"><span data-stu-id="5ac64-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ac64-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ac64-139">Requirements</span></span>



| <span data-ttu-id="5ac64-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ac64-140">Requirement</span></span> | <span data-ttu-id="5ac64-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ac64-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac64-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ac64-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac64-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ac64-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5ac64-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ac64-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac64-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ac64-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5ac64-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ac64-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac64-147"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ac64-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac64-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ac64-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac64-149">MCI</span><span class="sxs-lookup"><span data-stu-id="5ac64-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5ac64-150">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="5ac64-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


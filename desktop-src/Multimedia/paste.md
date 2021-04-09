---
title: commande Coller
description: La commande Coller copie le contenu du presse-papiers dans l’espace de travail. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- commande Coller Windows Multimedia
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032546"
---
# <a name="paste-command"></a><span data-ttu-id="f959d-105">commande Coller</span><span class="sxs-lookup"><span data-stu-id="f959d-105">paste command</span></span>

<span data-ttu-id="f959d-106">La commande Coller copie le contenu du presse-papiers dans l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="f959d-106">The paste command copies the contents of the clipboard into the workspace.</span></span> <span data-ttu-id="f959d-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="f959d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="f959d-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="f959d-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f959d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f959d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f959d-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f959d-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f959d-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="f959d-111">Identifier of an MCI device.</span></span> <span data-ttu-id="f959d-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="f959d-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f959d-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="f959d-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="f959d-114">Un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="f959d-114">One or more of the following flags.</span></span>



| <span data-ttu-id="f959d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f959d-115">Value</span></span>                 | <span data-ttu-id="f959d-116">Signification</span><span class="sxs-lookup"><span data-stu-id="f959d-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f959d-117">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="f959d-117">at *rectangle*</span></span>        | <span data-ttu-id="f959d-118">Spécifie l’emplacement dans le frame où les données sont collées.</span><span class="sxs-lookup"><span data-stu-id="f959d-118">Specifies the location within the frame where the data is pasted.</span></span> <span data-ttu-id="f959d-119">L’angle supérieur gauche du *rectangle* correspond au coin supérieur gauche des données ajoutées.</span><span class="sxs-lookup"><span data-stu-id="f959d-119">The upper left corner of the *rectangle* corresponds to the upper left corner of the added data.</span></span> <span data-ttu-id="f959d-120">Si le rectangle a une taille différente de zéro dans X ou Y, le contenu du presse-papiers est mis à l’échelle dans ces dimensions lorsqu’elles sont collées dans le cadre.</span><span class="sxs-lookup"><span data-stu-id="f959d-120">If the rectangle has a nonzero size in X or Y, the contents of the clipboard are scaled in those dimensions when they are pasted into the frame.</span></span> <span data-ttu-id="f959d-121">En cas d’omission, le *rectangle* a comme valeur par défaut l’ensemble du frame.</span><span class="sxs-lookup"><span data-stu-id="f959d-121">If omitted, the *rectangle* defaults to the entire frame.</span></span> <span data-ttu-id="f959d-122">Si cet indicateur est spécifié en mode « Insert » (valeur par défaut), toute région située à l’extérieur du rectangle est peinte avec une couleur unie.</span><span class="sxs-lookup"><span data-stu-id="f959d-122">If this flag is specified in "insert" mode (the default), any region outside the rectangle is painted a solid color.</span></span>                       |
| <span data-ttu-id="f959d-123">*flux* de flux audio</span><span class="sxs-lookup"><span data-stu-id="f959d-123">audio stream *stream*</span></span> | <span data-ttu-id="f959d-124">Spécifie le flux audio dans l’espace de travail affecté par la commande.</span><span class="sxs-lookup"><span data-stu-id="f959d-124">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="f959d-125">S’il n’existe qu’un seul flux audio dans le presse-papiers, les données audio sont collées dans le *flux* désigné.</span><span class="sxs-lookup"><span data-stu-id="f959d-125">If only one audio stream exists on the clipboard, the audio data is pasted into the designated *stream*.</span></span> <span data-ttu-id="f959d-126">Si plusieurs flux audio existent dans le presse-papiers, le *flux* indique le numéro de départ des séquences de flux.</span><span class="sxs-lookup"><span data-stu-id="f959d-126">If more than one audio stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="f959d-127">Si vous utilisez cet indicateur et que vous souhaitez également coller la vidéo, vous devez également utiliser l’indicateur « flux vidéo ».</span><span class="sxs-lookup"><span data-stu-id="f959d-127">If you use this flag and also want to paste video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="f959d-128">(Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont collés et conservent leurs numéros de flux d’origine.)</span><span class="sxs-lookup"><span data-stu-id="f959d-128">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |
| <span data-ttu-id="f959d-129">insert</span><span class="sxs-lookup"><span data-stu-id="f959d-129">insert</span></span>                | <span data-ttu-id="f959d-130">Spécifie que les données sont insérées dans l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="f959d-130">Specifies that the data is inserted into the workspace.</span></span> <span data-ttu-id="f959d-131">Toutes les données qui suivent le point d’insertion sont déplacées vers l’avant dans l’espace de travail pour faire de la place.</span><span class="sxs-lookup"><span data-stu-id="f959d-131">Any data after the insertion point is moved forward in the workspace to make room.</span></span> <span data-ttu-id="f959d-132">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f959d-132">This is the default value.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f959d-133">overwrite</span><span class="sxs-lookup"><span data-stu-id="f959d-133">overwrite</span></span>             | <span data-ttu-id="f959d-134">Spécifie que les données sont copiées dans l’espace de travail en écrivant sur les données existantes après le point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="f959d-134">Specifies that the data is copied into the workspace by writing over any existing data after the insertion point.</span></span> <span data-ttu-id="f959d-135">Les indicateurs « Insert » et « overwrite » déterminent si les images sont détruites ou déplacées pendant l’opération de collage, et non la manière dont les données sont collées dans chaque image.</span><span class="sxs-lookup"><span data-stu-id="f959d-135">The "insert" and "overwrite" flags affect whether frames are destroyed or moved during the paste operation, not how the data is pasted within each frame.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="f959d-136">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="f959d-136">to *position*</span></span>         | <span data-ttu-id="f959d-137">Spécifie la position dans l’espace de travail à laquelle les données sont collées.</span><span class="sxs-lookup"><span data-stu-id="f959d-137">Specifies the position in the workspace at which the data is pasted.</span></span> <span data-ttu-id="f959d-138">En cas d’omission, sa valeur par défaut est la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="f959d-138">If omitted, it defaults to the current position.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f959d-139">*flux* de flux vidéo</span><span class="sxs-lookup"><span data-stu-id="f959d-139">video stream *stream*</span></span> | <span data-ttu-id="f959d-140">Spécifie le flux vidéo dans l’espace de travail affecté par la commande.</span><span class="sxs-lookup"><span data-stu-id="f959d-140">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="f959d-141">S’il n’existe qu’un seul flux vidéo dans le presse-papiers, les données vidéo sont collées dans le *flux* désigné.</span><span class="sxs-lookup"><span data-stu-id="f959d-141">If only one video stream exists on the clipboard, the video data is pasted into the designated *stream*.</span></span> <span data-ttu-id="f959d-142">Si plusieurs flux vidéo existent dans le presse-papiers, le *flux* indique le numéro de départ des séquences de flux.</span><span class="sxs-lookup"><span data-stu-id="f959d-142">If more than one video stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="f959d-143">Si vous utilisez cet indicateur et que vous souhaitez également coller l’audio, vous devez également utiliser l’indicateur « flux audio ».</span><span class="sxs-lookup"><span data-stu-id="f959d-143">If you use this flag and also want to paste audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="f959d-144">(Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont collés et conservent leurs numéros de flux d’origine.)</span><span class="sxs-lookup"><span data-stu-id="f959d-144">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="f959d-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f959d-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f959d-146">Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="f959d-146">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="f959d-147">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f959d-147">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f959d-148">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f959d-148">Return Value</span></span>

<span data-ttu-id="f959d-149">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="f959d-149">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f959d-150">Notes</span><span class="sxs-lookup"><span data-stu-id="f959d-150">Remarks</span></span>

<span data-ttu-id="f959d-151">Aucun signal n’est présent dans les données copiées à partir du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="f959d-151">No signals are present in the data copied from the clipboard.</span></span> <span data-ttu-id="f959d-152">La modification devient permanente uniquement lorsque les données sont enregistrées de manière explicite ; Toutefois, la lecture agit comme si les données avaient été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="f959d-152">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="f959d-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f959d-153">Requirements</span></span>



| <span data-ttu-id="f959d-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f959d-154">Requirement</span></span> | <span data-ttu-id="f959d-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="f959d-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f959d-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f959d-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f959d-157">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f959d-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f959d-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f959d-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f959d-159">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f959d-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f959d-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f959d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f959d-161">MCI</span><span class="sxs-lookup"><span data-stu-id="f959d-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f959d-162">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="f959d-162">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 


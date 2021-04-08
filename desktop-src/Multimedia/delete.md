---
title: commande Delete
description: La commande Delete supprime un segment de données d’un fichier. Les périphériques vidéo numériques et Waveform-Audio reconnaissent cette commande.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- commande Delete Windows multimédia
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844230"
---
# <a name="delete-command"></a><span data-ttu-id="1c70f-105">commande Delete</span><span class="sxs-lookup"><span data-stu-id="1c70f-105">delete command</span></span>

<span data-ttu-id="1c70f-106">La commande Delete supprime un segment de données d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="1c70f-106">The delete command deletes a data segment from a file.</span></span> <span data-ttu-id="1c70f-107">Les périphériques vidéo numériques et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="1c70f-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="1c70f-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="1c70f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="1c70f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c70f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c70f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1c70f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1c70f-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="1c70f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="1c70f-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="1c70f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="1c70f-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span><span class="sxs-lookup"><span data-stu-id="1c70f-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span></span>
</dt> <dd>

<span data-ttu-id="1c70f-114">Indicateur qui identifie un segment de données à supprimer.</span><span class="sxs-lookup"><span data-stu-id="1c70f-114">Flag that identifies a data segment to delete.</span></span> <span data-ttu-id="1c70f-115">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Delete** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="1c70f-115">The following table lists device types that recognize the **delete** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c70f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c70f-116">Value</span></span></th>
<th><span data-ttu-id="1c70f-117">Signification</span><span class="sxs-lookup"><span data-stu-id="1c70f-117">Meaning</span></span></th>
<th><span data-ttu-id="1c70f-118">Signification</span><span class="sxs-lookup"><span data-stu-id="1c70f-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c70f-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="1c70f-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="1c70f-120">au niveau du <em>rectangle</em></span><span class="sxs-lookup"><span data-stu-id="1c70f-120">at <em>rectangle</em></span></span></li>
<li><span data-ttu-id="1c70f-121"><em>flux</em> de flux audio</span><span class="sxs-lookup"><span data-stu-id="1c70f-121">audio stream <em>stream</em></span></span></li>
<li><span data-ttu-id="1c70f-122">à partir de la <em>position</em></span><span class="sxs-lookup"><span data-stu-id="1c70f-122">from <em>position</em></span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1c70f-123">pour <em>positionner</em></span><span class="sxs-lookup"><span data-stu-id="1c70f-123">to <em>position</em></span></span></li>
<li><span data-ttu-id="1c70f-124"><em>flux</em> de flux vidéo</span><span class="sxs-lookup"><span data-stu-id="1c70f-124">video stream <em>stream</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c70f-125">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="1c70f-125">waveaudio</span></span></td>
<td><span data-ttu-id="1c70f-126">à partir de la <em>position</em></span><span class="sxs-lookup"><span data-stu-id="1c70f-126">from <em>position</em></span></span></td>
<td><span data-ttu-id="1c70f-127">pour <em>positionner</em></span><span class="sxs-lookup"><span data-stu-id="1c70f-127">to <em>position</em></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1c70f-128">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre *lpszPosition* et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="1c70f-128">The following table lists the flags that can be specified in the *lpszPosition* parameter and their meanings.</span></span>



| <span data-ttu-id="1c70f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c70f-129">Value</span></span>                 | <span data-ttu-id="1c70f-130">Signification</span><span class="sxs-lookup"><span data-stu-id="1c70f-130">Meaning</span></span>                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c70f-131">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="1c70f-131">at *rectangle*</span></span>        | <span data-ttu-id="1c70f-132">Spécifie la partie de chaque frame supprimée.</span><span class="sxs-lookup"><span data-stu-id="1c70f-132">Specifies the portion of each frame deleted.</span></span> <span data-ttu-id="1c70f-133">En cas d’omission, la valeur par défaut est le frame entier.</span><span class="sxs-lookup"><span data-stu-id="1c70f-133">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="1c70f-134">Lorsque cet élément est spécifié, les cadres ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="1c70f-134">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="1c70f-135">Au lieu de cela, la zone à l’intérieur du rectangle devient noire.</span><span class="sxs-lookup"><span data-stu-id="1c70f-135">Instead the area inside the rectangle becomes black.</span></span>                                          |
| <span data-ttu-id="1c70f-136">*flux* de flux audio</span><span class="sxs-lookup"><span data-stu-id="1c70f-136">audio stream *stream*</span></span> | <span data-ttu-id="1c70f-137">Spécifie le flux audio dans l’espace de travail affecté par la commande.</span><span class="sxs-lookup"><span data-stu-id="1c70f-137">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="1c70f-138">Si vous utilisez cet indicateur et que vous souhaitez également supprimer la vidéo, vous devez également utiliser l’indicateur « flux vidéo ».</span><span class="sxs-lookup"><span data-stu-id="1c70f-138">If you use this flag and also want to delete video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="1c70f-139">(Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont supprimés.)</span><span class="sxs-lookup"><span data-stu-id="1c70f-139">(If neither flag is specified, all audio and video streams are deleted.)</span></span> |
| <span data-ttu-id="1c70f-140">à partir de la *position*</span><span class="sxs-lookup"><span data-stu-id="1c70f-140">from *position*</span></span>       | <span data-ttu-id="1c70f-141">Spécifie la position de début de la suppression.</span><span class="sxs-lookup"><span data-stu-id="1c70f-141">Specifies the position at which deletion begins.</span></span> <span data-ttu-id="1c70f-142">Si cet indicateur est omis, la suppression commence à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="1c70f-142">If this flag is omitted, the deletion begins at the current position.</span></span>                                                                                                                       |
| <span data-ttu-id="1c70f-143">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="1c70f-143">to *position*</span></span>         | <span data-ttu-id="1c70f-144">Spécifie la position à laquelle la suppression se termine.</span><span class="sxs-lookup"><span data-stu-id="1c70f-144">Specifies the position at which deletion ends.</span></span> <span data-ttu-id="1c70f-145">Si cet indicateur est omis, la suppression se poursuit jusqu’à la fin du contenu ou de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="1c70f-145">If this flag is omitted, the deletion continues to the end of the content or workspace.</span></span>                                                                                                       |
| <span data-ttu-id="1c70f-146">*flux* de flux vidéo</span><span class="sxs-lookup"><span data-stu-id="1c70f-146">video stream *stream*</span></span> | <span data-ttu-id="1c70f-147">Spécifie le flux vidéo dans l’espace de travail affecté par la commande.</span><span class="sxs-lookup"><span data-stu-id="1c70f-147">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="1c70f-148">Si vous utilisez cet indicateur et que vous souhaitez également supprimer l’audio, vous devez également utiliser l’indicateur « flux audio ».</span><span class="sxs-lookup"><span data-stu-id="1c70f-148">If you use this flag and also want to delete audio, you must also use "audio stream" flag.</span></span> <span data-ttu-id="1c70f-149">(Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont supprimés.)</span><span class="sxs-lookup"><span data-stu-id="1c70f-149">(If neither flag is specified, all audio and video streams are deleted.)</span></span>     |



 

</dd> <dt>

<span data-ttu-id="1c70f-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="1c70f-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1c70f-151">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="1c70f-151">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="1c70f-152">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="1c70f-152">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="1c70f-153">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1c70f-153">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c70f-154">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1c70f-154">Return Value</span></span>

<span data-ttu-id="1c70f-155">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="1c70f-155">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c70f-156">Notes</span><span class="sxs-lookup"><span data-stu-id="1c70f-156">Remarks</span></span>

<span data-ttu-id="1c70f-157">Avant d’émettre des commandes qui utilisent des valeurs de position, vous devez définir le format d’heure souhaité à l’aide de la commande [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="1c70f-157">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="1c70f-158">Exemples</span><span class="sxs-lookup"><span data-stu-id="1c70f-158">Examples</span></span>

<span data-ttu-id="1c70f-159">La commande suivante supprime les données Waveform-Audio de 1 milliseconde à 900 millisecondes (en supposant que le format d’heure est défini sur millisecondes).</span><span class="sxs-lookup"><span data-stu-id="1c70f-159">The following command deletes the waveform-audio data from 1 millisecond through 900 milliseconds (assuming the time format is set to milliseconds).</span></span>

``` syntax
delete mysound from 1 to 900
```

## <a name="requirements"></a><span data-ttu-id="1c70f-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c70f-160">Requirements</span></span>



| <span data-ttu-id="1c70f-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c70f-161">Requirement</span></span> | <span data-ttu-id="1c70f-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c70f-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1c70f-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c70f-163">Minimum supported client</span></span><br/> | <span data-ttu-id="1c70f-164">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c70f-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1c70f-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c70f-165">Minimum supported server</span></span><br/> | <span data-ttu-id="1c70f-166">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c70f-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1c70f-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c70f-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c70f-168">MCI</span><span class="sxs-lookup"><span data-stu-id="1c70f-168">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1c70f-169">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="1c70f-169">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="1c70f-170">set</span><span class="sxs-lookup"><span data-stu-id="1c70f-170">set</span></span>](set.md)
</dt> </dl>

 


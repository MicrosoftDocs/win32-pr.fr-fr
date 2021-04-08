---
title: CUE, commande
description: La commande de pile se prépare à la diffusion ou à l’enregistrement. Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- commande de pile Windows Multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844410"
---
# <a name="cue-command"></a><span data-ttu-id="b3f38-105">CUE, commande</span><span class="sxs-lookup"><span data-stu-id="b3f38-105">cue command</span></span>

<span data-ttu-id="b3f38-106">La commande de pile se prépare à la diffusion ou à l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3f38-106">The cue command prepares for playing or recording.</span></span> <span data-ttu-id="b3f38-107">Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="b3f38-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="b3f38-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="b3f38-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="b3f38-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3f38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3f38-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b3f38-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b3f38-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="b3f38-111">Identifier of an MCI device.</span></span> <span data-ttu-id="b3f38-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="b3f38-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="b3f38-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span><span class="sxs-lookup"><span data-stu-id="b3f38-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span></span>
</dt> <dd>

<span data-ttu-id="b3f38-114">Indicateur qui prépare un appareil pour la diffusion ou l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3f38-114">Flag that prepares a device for playing or recording.</span></span> <span data-ttu-id="b3f38-115">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **CUE** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="b3f38-115">The following table lists device types that recognize the **cue** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3f38-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3f38-116">Value</span></span></th>
<th><span data-ttu-id="b3f38-117">Signal</span><span class="sxs-lookup"><span data-stu-id="b3f38-117">Cue</span></span></th>
<th><span data-ttu-id="b3f38-118">Signal</span><span class="sxs-lookup"><span data-stu-id="b3f38-118">Cue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3f38-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="b3f38-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="b3f38-120">entrée</span><span class="sxs-lookup"><span data-stu-id="b3f38-120">input</span></span></li>
<li><span data-ttu-id="b3f38-121">NoShow</span><span class="sxs-lookup"><span data-stu-id="b3f38-121">noshow</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b3f38-122">sortie</span><span class="sxs-lookup"><span data-stu-id="b3f38-122">output</span></span></li>
<li><span data-ttu-id="b3f38-123">pour <em>positionner</em></span><span class="sxs-lookup"><span data-stu-id="b3f38-123">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3f38-124">vidéo</span><span class="sxs-lookup"><span data-stu-id="b3f38-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="b3f38-125">à partir de la <em>position</em></span><span class="sxs-lookup"><span data-stu-id="b3f38-125">from <em>position</em></span></span></li>
<li><span data-ttu-id="b3f38-126">entrée</span><span class="sxs-lookup"><span data-stu-id="b3f38-126">input</span></span></li>
<li><span data-ttu-id="b3f38-127">sortie</span><span class="sxs-lookup"><span data-stu-id="b3f38-127">output</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b3f38-128">preroll</span><span class="sxs-lookup"><span data-stu-id="b3f38-128">preroll</span></span></li>
<li><span data-ttu-id="b3f38-129">reverse</span><span class="sxs-lookup"><span data-stu-id="b3f38-129">reverse</span></span></li>
<li><span data-ttu-id="b3f38-130">pour <em>positionner</em></span><span class="sxs-lookup"><span data-stu-id="b3f38-130">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3f38-131">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="b3f38-131">waveaudio</span></span></td>
<td><span data-ttu-id="b3f38-132">entrée</span><span class="sxs-lookup"><span data-stu-id="b3f38-132">input</span></span></td>
<td><span data-ttu-id="b3f38-133">sortie</span><span class="sxs-lookup"><span data-stu-id="b3f38-133">output</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b3f38-134">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre *lpszInOutTo* et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="b3f38-134">The following table lists the flags that can be specified in the *lpszInOutTo* parameter and their meanings.</span></span>



| <span data-ttu-id="b3f38-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3f38-135">Value</span></span>           | <span data-ttu-id="b3f38-136">Signification</span><span class="sxs-lookup"><span data-stu-id="b3f38-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f38-137">à partir de la *position*</span><span class="sxs-lookup"><span data-stu-id="b3f38-137">from *position*</span></span> | <span data-ttu-id="b3f38-138">Indique où commencer.</span><span class="sxs-lookup"><span data-stu-id="b3f38-138">Indicates where to start.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b3f38-139">entrée</span><span class="sxs-lookup"><span data-stu-id="b3f38-139">input</span></span>           | <span data-ttu-id="b3f38-140">Prépare l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3f38-140">Prepares for recording.</span></span> <span data-ttu-id="b3f38-141">Pour les périphériques vidéo numériques, cet indicateur peut être omis si la source de présentation actuelle est déjà l’entrée externe.</span><span class="sxs-lookup"><span data-stu-id="b3f38-141">For digital-video devices, this flag can be omitted if the current presentation source is already the external input.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="b3f38-142">NoShow</span><span class="sxs-lookup"><span data-stu-id="b3f38-142">noshow</span></span>          | <span data-ttu-id="b3f38-143">Prépare la diffusion d’une image sans l’afficher.</span><span class="sxs-lookup"><span data-stu-id="b3f38-143">Prepares for playing a frame without displaying it.</span></span> <span data-ttu-id="b3f38-144">Lorsque cet indicateur est spécifié, l’affichage continue d’afficher l’image dans la mémoire tampon de trame, même si son frame correspondant n’est pas la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="b3f38-144">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="b3f38-145">Une commande de pile suivante sans cet indicateur et sans l’indicateur « to » affiche le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="b3f38-145">A subsequent cue command without this flag and without the "to" flag displays the current frame.</span></span> |
| <span data-ttu-id="b3f38-146">sortie</span><span class="sxs-lookup"><span data-stu-id="b3f38-146">output</span></span>          | <span data-ttu-id="b3f38-147">Prépare la durée de la diffusion.</span><span class="sxs-lookup"><span data-stu-id="b3f38-147">Prepares for playing.</span></span> <span data-ttu-id="b3f38-148">Si ni « Input » ni « output » n’est spécifié, le paramètre par défaut est « output ».</span><span class="sxs-lookup"><span data-stu-id="b3f38-148">If neither "input" nor "output" is specified, the default setting is "output".</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="b3f38-149">preroll</span><span class="sxs-lookup"><span data-stu-id="b3f38-149">preroll</span></span>         | <span data-ttu-id="b3f38-150">Déplace la distance du préroll à partir du *point d'* interrogation.</span><span class="sxs-lookup"><span data-stu-id="b3f38-150">Moves the preroll distance from the *in-point*.</span></span> <span data-ttu-id="b3f38-151">L’objet in-point est la position actuelle ou la position spécifiée par l’indicateur « from ».</span><span class="sxs-lookup"><span data-stu-id="b3f38-151">The in-point is the current position, or the position specified by the "from" flag.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="b3f38-152">reverse</span><span class="sxs-lookup"><span data-stu-id="b3f38-152">reverse</span></span>         | <span data-ttu-id="b3f38-153">Indique que la direction de lecture est en sens inverse (arrière).</span><span class="sxs-lookup"><span data-stu-id="b3f38-153">Indicates play direction is in reverse (backward).</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b3f38-154">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="b3f38-154">to *position*</span></span>   | <span data-ttu-id="b3f38-155">Déplace l’espace de travail à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b3f38-155">Moves the workspace to the specified position.</span></span> <span data-ttu-id="b3f38-156">Pour les périphériques VCR, cet indicateur indique l’endroit où s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="b3f38-156">For VCR devices, this flag indicates where to stop.</span></span>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="b3f38-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="b3f38-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b3f38-158">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="b3f38-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="b3f38-159">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="b3f38-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="b3f38-160">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b3f38-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3f38-161">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b3f38-161">Return Value</span></span>

<span data-ttu-id="b3f38-162">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="b3f38-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3f38-163">Notes</span><span class="sxs-lookup"><span data-stu-id="b3f38-163">Remarks</span></span>

<span data-ttu-id="b3f38-164">Bien qu’il ne soit pas nécessaire, l’émission de la commande de pile avant la création ou l’enregistrement sur certains appareils peut réduire le délai avant que l’appareil ne démarre l’action.</span><span class="sxs-lookup"><span data-stu-id="b3f38-164">Although it is not necessary, issuing the cue command before playing or recording on some devices might reduce the delay before the device starts the action.</span></span>

<span data-ttu-id="b3f38-165">Cette commande échoue si la diffusion ou l’enregistrement est en cours ou si l’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="b3f38-165">This command fails if playing or recording is in progress or if the device is paused.</span></span>

<span data-ttu-id="b3f38-166">Quand cueing pour la lecture (à l’aide de la « sortie » du signal), l’émission de la commande [Play](play.md) avec l’indicateur « from », « to » ou « reverse » annule la commande CUE.</span><span class="sxs-lookup"><span data-stu-id="b3f38-166">When cueing for playback (using cue "output"), issuing the [play](play.md) command with the "from", "to", or "reverse" flag cancels the cue command.</span></span>

<span data-ttu-id="b3f38-167">Quand cueing pour l’enregistrement (à l’aide de la balise « Input »), l’émission de la commande [Record](record.md) avec l’indicateur « from », « to » ou « Initialize » annule la commande CUE.</span><span class="sxs-lookup"><span data-stu-id="b3f38-167">When cueing for recording (using cue "input"), issuing the [record](record.md) command with the "from", "to", or "initialize" flag cancels the cue command.</span></span>

## <a name="examples"></a><span data-ttu-id="b3f38-168">Exemples</span><span class="sxs-lookup"><span data-stu-id="b3f38-168">Examples</span></span>

<span data-ttu-id="b3f38-169">La commande suivante prépare l’appareil « mySound » pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3f38-169">The following command prepares the "mysound" device for recording.</span></span>

``` syntax
cue mysound input
```

## <a name="requirements"></a><span data-ttu-id="b3f38-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3f38-170">Requirements</span></span>



| <span data-ttu-id="b3f38-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3f38-171">Requirement</span></span> | <span data-ttu-id="b3f38-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3f38-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b3f38-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3f38-173">Minimum supported client</span></span><br/> | <span data-ttu-id="b3f38-174">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3f38-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b3f38-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3f38-175">Minimum supported server</span></span><br/> | <span data-ttu-id="b3f38-176">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3f38-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b3f38-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3f38-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3f38-178">MCI</span><span class="sxs-lookup"><span data-stu-id="b3f38-178">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b3f38-179">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="b3f38-179">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="b3f38-180">répétition</span><span class="sxs-lookup"><span data-stu-id="b3f38-180">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="b3f38-181">enregistrement</span><span class="sxs-lookup"><span data-stu-id="b3f38-181">record</span></span>](record.md)
</dt> </dl>

 


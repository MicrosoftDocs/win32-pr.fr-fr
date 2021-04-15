---
title: commande Seek
description: La commande Seek passe à la position spécifiée et s’arrête. Les périphériques CD audio, Digital-Video, MIDI Sequencer, VCR, videodisc et Waveform-Audio reconnaissent cette commande.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- commande Seek Windows Multimedia
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383924"
---
# <a name="seek-command"></a><span data-ttu-id="0b890-105">commande Seek</span><span class="sxs-lookup"><span data-stu-id="0b890-105">seek command</span></span>

<span data-ttu-id="0b890-106">La commande Seek passe à la position spécifiée et s’arrête.</span><span class="sxs-lookup"><span data-stu-id="0b890-106">The seek command moves to the specified position and stops.</span></span> <span data-ttu-id="0b890-107">Les périphériques CD audio, Digital-Video, MIDI Sequencer, VCR, videodisc et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="0b890-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="0b890-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="0b890-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0b890-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b890-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b890-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0b890-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0b890-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="0b890-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0b890-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="0b890-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0b890-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span><span class="sxs-lookup"><span data-stu-id="0b890-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0b890-114">Indicateur de déplacement à une position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0b890-114">Flag for moving to a specified position.</span></span> <span data-ttu-id="0b890-115">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Seek** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="0b890-115">The following table lists device types that recognize the **seek** command and the flags used by each type.</span></span>



| <span data-ttu-id="0b890-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b890-116">Value</span></span>        | <span data-ttu-id="0b890-117">Signification</span><span class="sxs-lookup"><span data-stu-id="0b890-117">Meaning</span></span>                          | <span data-ttu-id="0b890-118">Signification</span><span class="sxs-lookup"><span data-stu-id="0b890-118">Meaning</span></span>                      |
|--------------|----------------------------------|------------------------------|
| <span data-ttu-id="0b890-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="0b890-119">cdaudio</span></span>      | <span data-ttu-id="0b890-120">fin jusqu’à la *position*</span><span class="sxs-lookup"><span data-stu-id="0b890-120">to end to *position*</span></span>             | <span data-ttu-id="0b890-121">pour démarrer</span><span class="sxs-lookup"><span data-stu-id="0b890-121">to start</span></span>                     |
| <span data-ttu-id="0b890-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="0b890-122">digitalvideo</span></span> | <span data-ttu-id="0b890-123">fin jusqu’à la *position*</span><span class="sxs-lookup"><span data-stu-id="0b890-123">to end to *position*</span></span>             | <span data-ttu-id="0b890-124">pour démarrer</span><span class="sxs-lookup"><span data-stu-id="0b890-124">to start</span></span>                     |
| <span data-ttu-id="0b890-125">sequencer</span><span class="sxs-lookup"><span data-stu-id="0b890-125">sequencer</span></span>    | <span data-ttu-id="0b890-126">fin jusqu’à la *position*</span><span class="sxs-lookup"><span data-stu-id="0b890-126">to end to *position*</span></span>             | <span data-ttu-id="0b890-127">pour démarrer</span><span class="sxs-lookup"><span data-stu-id="0b890-127">to start</span></span>                     |
| <span data-ttu-id="0b890-128">vidéo</span><span class="sxs-lookup"><span data-stu-id="0b890-128">vcr</span></span>          | <span data-ttu-id="0b890-129">à l' *instant*, marque *\_ num* inversé</span><span class="sxs-lookup"><span data-stu-id="0b890-129">at *time* mark *mark\_num* reverse</span></span> | <span data-ttu-id="0b890-130">fin jusqu’à la *position* de départ</span><span class="sxs-lookup"><span data-stu-id="0b890-130">to end to *position* to start</span></span> |
| <span data-ttu-id="0b890-131">videodisc</span><span class="sxs-lookup"><span data-stu-id="0b890-131">videodisc</span></span>    | <span data-ttu-id="0b890-132">inverser jusqu’à la fin</span><span class="sxs-lookup"><span data-stu-id="0b890-132">reverse to end</span></span>                   | <span data-ttu-id="0b890-133">pour *positionner* pour démarrer</span><span class="sxs-lookup"><span data-stu-id="0b890-133">to *position* to start</span></span>        |
| <span data-ttu-id="0b890-134">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="0b890-134">waveaudio</span></span>    | <span data-ttu-id="0b890-135">fin jusqu’à la *position*</span><span class="sxs-lookup"><span data-stu-id="0b890-135">to end to *position*</span></span>             | <span data-ttu-id="0b890-136">pour démarrer</span><span class="sxs-lookup"><span data-stu-id="0b890-136">to start</span></span>                     |



 

<span data-ttu-id="0b890-137">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszSeekFlags** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="0b890-137">The following table lists the flags that can be specified in the **lpszSeekFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="0b890-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b890-138">Value</span></span>            | <span data-ttu-id="0b890-139">Signification</span><span class="sxs-lookup"><span data-stu-id="0b890-139">Meaning</span></span>                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b890-140">à *temps*</span><span class="sxs-lookup"><span data-stu-id="0b890-140">at *time*</span></span>        | <span data-ttu-id="0b890-141">Indique quand l’appareil doit commencer à exécuter cette commande ou, si l’appareil a été reçu, lorsque la commande de signal démarre.</span><span class="sxs-lookup"><span data-stu-id="0b890-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="0b890-142">Pour plus d’informations, consultez la commande [CUE](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="0b890-142">For more information, see the [cue](cue.md) command.</span></span>                             |
| <span data-ttu-id="0b890-143">marque de marque *\_ num*</span><span class="sxs-lookup"><span data-stu-id="0b890-143">mark *mark\_num*</span></span> | <span data-ttu-id="0b890-144">Recherche la marque relative indiquée par *Mark \_ num*, qui doit être une valeur entière positive.</span><span class="sxs-lookup"><span data-stu-id="0b890-144">Seeks to the relative mark indicated by *mark\_num*, which must be a positive integer value.</span></span> <span data-ttu-id="0b890-145">Les marques sont des signaux écrits sur la bande VCR à l’aide de la commande [Mark](mark.md) et sont utilisés pour une recherche rapide.</span><span class="sxs-lookup"><span data-stu-id="0b890-145">Marks are signals written to the VCR tape using the [mark](mark.md) command and are used for high-speed searching.</span></span> |
| <span data-ttu-id="0b890-146">reverse</span><span class="sxs-lookup"><span data-stu-id="0b890-146">reverse</span></span>          | <span data-ttu-id="0b890-147">Indique que la direction de la recherche sur les magnétoscopes et CAV videodiscs est vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="0b890-147">Indicates that the seek direction on VCRs and CAV videodiscs is backward.</span></span> <span data-ttu-id="0b890-148">Cet indicateur n’est pas valide si l’indicateur « to » est spécifié.</span><span class="sxs-lookup"><span data-stu-id="0b890-148">This flag is invalid if the "to" flag is specified.</span></span> <span data-ttu-id="0b890-149">Pour les magnétoscopes, cet indicateur doit être utilisé avec l’indicateur « Mark ».</span><span class="sxs-lookup"><span data-stu-id="0b890-149">For VCRs, this flag must be used with the "mark" flag.</span></span>                             |
| <span data-ttu-id="0b890-150">pour terminer</span><span class="sxs-lookup"><span data-stu-id="0b890-150">to end</span></span>           | <span data-ttu-id="0b890-151">Recherche jusqu’à la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="0b890-151">Seeks to the end of the content.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="0b890-152">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="0b890-152">to *position*</span></span>    | <span data-ttu-id="0b890-153">Spécifie la position d’arrêt de la recherche.</span><span class="sxs-lookup"><span data-stu-id="0b890-153">Specifies the position to stop the seek.</span></span> <span data-ttu-id="0b890-154">Pour les appareils **cdaudio** , MCI retourne une erreur hors limites si la position spécifiée est supérieure à la longueur du disque.</span><span class="sxs-lookup"><span data-stu-id="0b890-154">For **cdaudio** devices, MCI returns an out-of-range error if the specified position is greater than the length of the disc.</span></span>                                            |
| <span data-ttu-id="0b890-155">pour démarrer</span><span class="sxs-lookup"><span data-stu-id="0b890-155">to start</span></span>         | <span data-ttu-id="0b890-156">Recherche le début du contenu.</span><span class="sxs-lookup"><span data-stu-id="0b890-156">Seeks to the start of the content.</span></span>                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="0b890-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0b890-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0b890-158">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="0b890-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="0b890-159">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="0b890-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="0b890-160">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0b890-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b890-161">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0b890-161">Return Value</span></span>

<span data-ttu-id="0b890-162">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="0b890-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b890-163">Notes</span><span class="sxs-lookup"><span data-stu-id="0b890-163">Remarks</span></span>

<span data-ttu-id="0b890-164">Avant d’émettre des commandes qui utilisent des valeurs de position, vous devez définir le format d’heure souhaité à l’aide de la commande [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="0b890-164">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

<span data-ttu-id="0b890-165">Les périphériques vidéo numériques prennent en charge deux modes de recherche, que vous pouvez modifier à l’aide de la commande [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="0b890-165">Digital-video devices support two seek modes, which you can change by using the [set](set.md) command.</span></span> <span data-ttu-id="0b890-166">Le mode « Seek exact on » provoque le déplacement de la commande Seek vers le frame spécifié.</span><span class="sxs-lookup"><span data-stu-id="0b890-166">The "seek exactly on" mode causes the seek command to move to the specified frame.</span></span> <span data-ttu-id="0b890-167">Le mode « Seek exact OFF » provoque le déplacement de la commande Seek vers l’image clé la plus proche avant le frame spécifié.</span><span class="sxs-lookup"><span data-stu-id="0b890-167">The "seek exactly off" mode causes the seek command to move to the closest key frame prior to the specified frame.</span></span>

<span data-ttu-id="0b890-168">Si un périphérique CD audio est lu lors de l’émission de la commande Seek, la lecture est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="0b890-168">If a CD audio device is playing when the seek command is issued, playback is stopped.</span></span> <span data-ttu-id="0b890-169">Lorsque la commande Seek est exécutée avec un appareil videodisc, l’appareil recherche à l’aide d’une avance rapide ou d’une inversion rapide avec la vidéo et l’audio.</span><span class="sxs-lookup"><span data-stu-id="0b890-169">When the seek command is issued with a videodisc device, the device searches using fast forward or fast reverse with video and audio off.</span></span>

<span data-ttu-id="0b890-170">Lorsque la commande Seek est émise avec un périphérique Wave-audio, le comportement dépend de la taille de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="0b890-170">When the seek command is issued with a waveform-audio device, the behavior depends on the sample size.</span></span> <span data-ttu-id="0b890-171">Si la taille de l’échantillon est supérieure ou égale à 16 bits, la fonction Seek se déplace au début de l’échantillon le plus proche lorsqu’une position spécifiée ne coïncide pas avec le début d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="0b890-171">If the sample size is 16 bits or greater, seek moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

## <a name="examples"></a><span data-ttu-id="0b890-172">Exemples</span><span class="sxs-lookup"><span data-stu-id="0b890-172">Examples</span></span>

<span data-ttu-id="0b890-173">La commande suivante recherche le début du fichier multimédia associé à l’appareil « mySound ».</span><span class="sxs-lookup"><span data-stu-id="0b890-173">The following command seeks to the start of the media file associated with the "mysound" device.</span></span>

``` syntax
seek mysound to start
```

## <a name="requirements"></a><span data-ttu-id="0b890-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b890-174">Requirements</span></span>



| <span data-ttu-id="0b890-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b890-175">Requirement</span></span> | <span data-ttu-id="0b890-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b890-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0b890-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b890-177">Minimum supported client</span></span><br/> | <span data-ttu-id="0b890-178">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b890-178">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0b890-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b890-179">Minimum supported server</span></span><br/> | <span data-ttu-id="0b890-180">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b890-180">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0b890-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b890-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b890-182">MCI</span><span class="sxs-lookup"><span data-stu-id="0b890-182">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0b890-183">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="0b890-183">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="0b890-184">signal</span><span class="sxs-lookup"><span data-stu-id="0b890-184">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="0b890-185">marque</span><span class="sxs-lookup"><span data-stu-id="0b890-185">mark</span></span>](mark.md)
</dt> <dt>

[<span data-ttu-id="0b890-186">set</span><span class="sxs-lookup"><span data-stu-id="0b890-186">set</span></span>](set.md)
</dt> </dl>

 


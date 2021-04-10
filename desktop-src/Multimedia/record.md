---
title: enregistrer, commande
description: La commande d’enregistrement démarre l’enregistrement des données. Les périphériques VCR et Waveform-Audio reconnaissent cette commande. Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne les implémentent pas.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- commande d’enregistrement Windows Multimedia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843121"
---
# <a name="record-command"></a><span data-ttu-id="37459-106">enregistrer, commande</span><span class="sxs-lookup"><span data-stu-id="37459-106">record command</span></span>

<span data-ttu-id="37459-107">La commande d’enregistrement démarre l’enregistrement des données.</span><span class="sxs-lookup"><span data-stu-id="37459-107">The record command starts recording data.</span></span> <span data-ttu-id="37459-108">Les périphériques VCR et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="37459-108">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="37459-109">Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne les implémentent pas.</span><span class="sxs-lookup"><span data-stu-id="37459-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="37459-110">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="37459-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="37459-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37459-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37459-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="37459-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="37459-113">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="37459-113">Identifier of an MCI device.</span></span> <span data-ttu-id="37459-114">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="37459-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="37459-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span><span class="sxs-lookup"><span data-stu-id="37459-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span></span>
</dt> <dd>

<span data-ttu-id="37459-116">Indicateur pour l’enregistrement des données.</span><span class="sxs-lookup"><span data-stu-id="37459-116">Flag for recording data.</span></span> <span data-ttu-id="37459-117">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande d' **enregistrement** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="37459-117">The following table lists device types that recognize the **record** command and the flags used by each type.</span></span>



| <span data-ttu-id="37459-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="37459-118">Value</span></span>        | <span data-ttu-id="37459-119">Signification</span><span class="sxs-lookup"><span data-stu-id="37459-119">Meaning</span></span>                                                | <span data-ttu-id="37459-120">Signification</span><span class="sxs-lookup"><span data-stu-id="37459-120">Meaning</span></span>                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="37459-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="37459-121">digitalvideo</span></span> | <span data-ttu-id="37459-122">*à partir du* *rectangle* flux audio Stream à partir de la *position* Hold</span><span class="sxs-lookup"><span data-stu-id="37459-122">at *rectangle* audio stream *stream* from *position* hold</span></span> | <span data-ttu-id="37459-123">Insérer l’écrasement du *flux* de flux vidéo de la *position*</span><span class="sxs-lookup"><span data-stu-id="37459-123">insert overwrite to *position* video stream *stream*</span></span> |
| <span data-ttu-id="37459-124">sequencer</span><span class="sxs-lookup"><span data-stu-id="37459-124">sequencer</span></span>    | <span data-ttu-id="37459-125">à partir de la *position* Insert</span><span class="sxs-lookup"><span data-stu-id="37459-125">from *position* insert</span></span>                                  | <span data-ttu-id="37459-126">remplacer la *position*</span><span class="sxs-lookup"><span data-stu-id="37459-126">overwrite to *position*</span></span>                             |
| <span data-ttu-id="37459-127">vidéo</span><span class="sxs-lookup"><span data-stu-id="37459-127">vcr</span></span>          | <span data-ttu-id="37459-128">à l' *heure* de l’initialisation de la *position*</span><span class="sxs-lookup"><span data-stu-id="37459-128">at *time* from *position* initialize</span></span>                     | <span data-ttu-id="37459-129">Insérer le remplacement à la *position*</span><span class="sxs-lookup"><span data-stu-id="37459-129">insert overwrite to *position*</span></span>                      |
| <span data-ttu-id="37459-130">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="37459-130">waveaudio</span></span>    | <span data-ttu-id="37459-131">à partir de la *position* Insert</span><span class="sxs-lookup"><span data-stu-id="37459-131">from *position* insert</span></span>                                  | <span data-ttu-id="37459-132">remplacer la *position*</span><span class="sxs-lookup"><span data-stu-id="37459-132">overwrite to *position*</span></span>                             |



 

<span data-ttu-id="37459-133">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszRecordFlags** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="37459-133">The following table lists the flags that can be specified in the **lpszRecordFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="37459-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="37459-134">Value</span></span>                 | <span data-ttu-id="37459-135">Signification</span><span class="sxs-lookup"><span data-stu-id="37459-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37459-136">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="37459-136">at *rectangle*</span></span>        | <span data-ttu-id="37459-137">Spécifie une zone rectangulaire de l’entrée externe utilisée comme source pour les pixels compressés et enregistrés.</span><span class="sxs-lookup"><span data-stu-id="37459-137">Specifies a rectangular region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="37459-138">S’il n’est pas spécifié, le rectangle est par défaut le rectangle spécifié pour [put](put.md) « Video ».</span><span class="sxs-lookup"><span data-stu-id="37459-138">If not specified, the rectangle defaults to the rectangle specified for [put](put.md) "video".</span></span> <span data-ttu-id="37459-139">Lorsqu’il est défini différemment du rectangle « Video », l’image affichée n’est pas ce qui est enregistré.</span><span class="sxs-lookup"><span data-stu-id="37459-139">When it is set differently from the "video" rectangle, the displayed image is not what is recorded.</span></span> |
| <span data-ttu-id="37459-140">à *temps*</span><span class="sxs-lookup"><span data-stu-id="37459-140">at *time*</span></span>             | <span data-ttu-id="37459-141">Indique quand l’appareil doit commencer à exécuter cette commande ou, si l’appareil a été reçu, lorsque la commande de signal démarre.</span><span class="sxs-lookup"><span data-stu-id="37459-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="37459-142">Pour plus d’informations, consultez la commande [CUE](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="37459-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                             |
| <span data-ttu-id="37459-143">*flux* de flux audio</span><span class="sxs-lookup"><span data-stu-id="37459-143">audio stream *stream*</span></span> | <span data-ttu-id="37459-144">Spécifie le flux audio utilisé pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="37459-144">Specifies the audio stream used for recording.</span></span> <span data-ttu-id="37459-145">Si cet indicateur n’est pas spécifié et que le format de fichier ne définit pas de valeur par défaut, il est enregistré dans le flux qui est physiquement en premier.</span><span class="sxs-lookup"><span data-stu-id="37459-145">If this flag is not specified and the file format does not define a default, it is recorded into the stream that is physically first.</span></span>                                                                                                                             |
| <span data-ttu-id="37459-146">à partir de la *position*</span><span class="sxs-lookup"><span data-stu-id="37459-146">from *position*</span></span>       | <span data-ttu-id="37459-147">Spécifie une position de départ pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="37459-147">Specifies a starting position for the recording.</span></span> <span data-ttu-id="37459-148">Si l’indicateur « from » n’est pas spécifié, l’appareil commence à enregistrer à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="37459-148">If the "from" flag is not specified, the device starts recording at the current position.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="37459-149">inaltérable</span><span class="sxs-lookup"><span data-stu-id="37459-149">hold</span></span>                  | <span data-ttu-id="37459-150">Fige l’image lorsque l’enregistrement est terminé au lieu d’en visualiser la vidéo en direct.</span><span class="sxs-lookup"><span data-stu-id="37459-150">Freezes the image when recording has finished instead of showing live video.</span></span> <span data-ttu-id="37459-151">Lorsque l’enregistrement s’arrête, une commande de « fichier » d' [analyse](monitor.md) automatique est exécutée.</span><span class="sxs-lookup"><span data-stu-id="37459-151">When recording stops, an automatic [monitor](monitor.md) "file" command is performed.</span></span> <span data-ttu-id="37459-152">Pour revenir à la vidéo en direct, émettez la commande « entrée » du **moniteur** .</span><span class="sxs-lookup"><span data-stu-id="37459-152">To return to live video, issue the **monitor** "input" command.</span></span>                                                                              |
| <span data-ttu-id="37459-153">initialize</span><span class="sxs-lookup"><span data-stu-id="37459-153">initialize</span></span>            | <span data-ttu-id="37459-154">Initialisez la bande (support), qui implique l’enregistrement du code temporel (si possible) pour la vidéo et l’audio vides.</span><span class="sxs-lookup"><span data-stu-id="37459-154">Initialize the tape (media), which involves recording timecode (if possible) for blank video and audio.</span></span> <span data-ttu-id="37459-155">Cette commande peut prendre plusieurs heures si la bande entière doit être initialisée.</span><span class="sxs-lookup"><span data-stu-id="37459-155">This command might take several hours if the entire tape must be initialized.</span></span>                                                                                                                            |
| <span data-ttu-id="37459-156">insert</span><span class="sxs-lookup"><span data-stu-id="37459-156">insert</span></span>                | <span data-ttu-id="37459-157">Spécifie que les nouvelles données sont ajoutées au fichier à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="37459-157">Specifies that new data is added to the file at the current position.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="37459-158">overwrite</span><span class="sxs-lookup"><span data-stu-id="37459-158">overwrite</span></span>             | <span data-ttu-id="37459-159">Spécifie que les nouvelles données remplacent les données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="37459-159">Specifies that new data will replace data in the file.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="37459-160">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="37459-160">to *position*</span></span>         | <span data-ttu-id="37459-161">Spécifie une position de fin pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="37459-161">Specifies an ending position for the recording.</span></span> <span data-ttu-id="37459-162">Si l’indicateur « to » n’est pas spécifié, l’appareil enregistre jusqu’à ce qu’il reçoive une commande [Stop](stop.md) ou [Pause](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="37459-162">If the "to" flag is not specified, the device records until it receives a [stop](stop.md) or [pause](pause.md) command.</span></span>                                                                                                                                        |
| <span data-ttu-id="37459-163">*flux* de flux vidéo</span><span class="sxs-lookup"><span data-stu-id="37459-163">video stream *stream*</span></span> | <span data-ttu-id="37459-164">Spécifie le flux vidéo utilisé pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="37459-164">Specifies the video stream used for recording.</span></span> <span data-ttu-id="37459-165">Si ce paramètre n’est pas spécifié et que le format de fichier ne définit pas de valeur par défaut, il est enregistré dans le flux qui est physiquement en premier.</span><span class="sxs-lookup"><span data-stu-id="37459-165">If this is not specified and the file format does not define a default, then it is recorded into the stream that is physically first.</span></span>                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="37459-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="37459-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="37459-167">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="37459-167">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="37459-168">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="37459-168">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="37459-169">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="37459-169">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37459-170">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="37459-170">Return Value</span></span>

<span data-ttu-id="37459-171">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="37459-171">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="37459-172">Notes</span><span class="sxs-lookup"><span data-stu-id="37459-172">Remarks</span></span>

<span data-ttu-id="37459-173">L’enregistrement s’arrête lorsqu’une commande [Stop](stop.md) ou [Pause](pause.md) est émise.</span><span class="sxs-lookup"><span data-stu-id="37459-173">The recording stops when a [stop](stop.md) or [pause](pause.md) command is issued.</span></span> <span data-ttu-id="37459-174">Pour le pilote MCIWAVE, toutes les données enregistrées après l’ouverture d’un fichier sont ignorées si le fichier est fermé sans l’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="37459-174">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="37459-175">Avant d’émettre des commandes qui utilisent des valeurs de position, vous devez définir le format d’heure souhaité à l’aide de la commande [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="37459-175">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="37459-176">Les pistes à enregistrer sont spécifiées par l' [settimecode](settimecode.md) « enregistrement », définissez les commandes « assembler l’enregistrement », [setvideo](setvideo.md) « enregistrement » et « enregistrement » de [SetAudio](setaudio.md) .</span><span class="sxs-lookup"><span data-stu-id="37459-176">The tracks to be recorded are specified by the [settimecode](settimecode.md) "record", set "assemble record", [setvideo](setvideo.md) "record", and [setaudio](setaudio.md) "record" commands.</span></span>

## <a name="examples"></a><span data-ttu-id="37459-177">Exemples</span><span class="sxs-lookup"><span data-stu-id="37459-177">Examples</span></span>

<span data-ttu-id="37459-178">La commande suivante démarre l’enregistrement à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="37459-178">The following command starts recording at the current position.</span></span>

``` syntax
record mysound
```

## <a name="requirements"></a><span data-ttu-id="37459-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37459-179">Requirements</span></span>



| <span data-ttu-id="37459-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37459-180">Requirement</span></span> | <span data-ttu-id="37459-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="37459-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="37459-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37459-182">Minimum supported client</span></span><br/> | <span data-ttu-id="37459-183">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37459-183">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="37459-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37459-184">Minimum supported server</span></span><br/> | <span data-ttu-id="37459-185">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37459-185">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="37459-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37459-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37459-187">MCI</span><span class="sxs-lookup"><span data-stu-id="37459-187">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="37459-188">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="37459-188">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="37459-189">signal</span><span class="sxs-lookup"><span data-stu-id="37459-189">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="37459-190">socle</span><span class="sxs-lookup"><span data-stu-id="37459-190">monitor</span></span>](monitor.md)
</dt> <dt>

[<span data-ttu-id="37459-191">pause</span><span class="sxs-lookup"><span data-stu-id="37459-191">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="37459-192">posé</span><span class="sxs-lookup"><span data-stu-id="37459-192">put</span></span>](put.md)
</dt> <dt>

[<span data-ttu-id="37459-193">set</span><span class="sxs-lookup"><span data-stu-id="37459-193">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="37459-194">setaudio</span><span class="sxs-lookup"><span data-stu-id="37459-194">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="37459-195">settimecode</span><span class="sxs-lookup"><span data-stu-id="37459-195">settimecode</span></span>](settimecode.md)
</dt> <dt>

[<span data-ttu-id="37459-196">setvideo</span><span class="sxs-lookup"><span data-stu-id="37459-196">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="37459-197">stop</span><span class="sxs-lookup"><span data-stu-id="37459-197">stop</span></span>](stop.md)
</dt> </dl>

 


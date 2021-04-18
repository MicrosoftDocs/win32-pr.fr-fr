---
title: Save, commande
description: La commande Save enregistre un fichier MCI. Les périphériques vidéo-superposition et Waveform-Audio reconnaissent cette commande. Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne le prennent pas en charge.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- commande Save Windows Multimedia
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540769"
---
# <a name="save-command"></a><span data-ttu-id="c5bbc-106">Save, commande</span><span class="sxs-lookup"><span data-stu-id="c5bbc-106">save command</span></span>

<span data-ttu-id="c5bbc-107">La commande Save enregistre un fichier MCI.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-107">The save command saves an MCI file.</span></span> <span data-ttu-id="c5bbc-108">Les périphériques vidéo-superposition et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-108">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="c5bbc-109">Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne le prennent pas en charge.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not support it.</span></span>

<span data-ttu-id="c5bbc-110">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c5bbc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5bbc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5bbc-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c5bbc-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c5bbc-113">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-113">Identifier of an MCI device.</span></span> <span data-ttu-id="c5bbc-114">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c5bbc-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span><span class="sxs-lookup"><span data-stu-id="c5bbc-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span></span>
</dt> <dd>

<span data-ttu-id="c5bbc-116">Indicateur spécifiant le nom du fichier en cours d’enregistrement et, éventuellement, les indicateurs supplémentaires qui modifient l’opération d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-116">Flag specifying the name of the file being saved and, optionally, additional flags modifying the save operation.</span></span> <span data-ttu-id="c5bbc-117">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Save** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-117">The following table lists device types that recognize the **save** command and the flags used by each type.</span></span>



| <span data-ttu-id="c5bbc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5bbc-118">Value</span></span>        | <span data-ttu-id="c5bbc-119">Signification</span><span class="sxs-lookup"><span data-stu-id="c5bbc-119">Meaning</span></span>              | <span data-ttu-id="c5bbc-120">Signification</span><span class="sxs-lookup"><span data-stu-id="c5bbc-120">Meaning</span></span>               |
|--------------|----------------------|-----------------------|
| <span data-ttu-id="c5bbc-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="c5bbc-121">digitalvideo</span></span> | <span data-ttu-id="c5bbc-122">abandonner au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="c5bbc-122">abort at *rectangle*</span></span> | <span data-ttu-id="c5bbc-123">*nom de fichier* keepreserve</span><span class="sxs-lookup"><span data-stu-id="c5bbc-123">*filename* keepreserve</span></span> |
| <span data-ttu-id="c5bbc-124">superposition</span><span class="sxs-lookup"><span data-stu-id="c5bbc-124">overlay</span></span>      | <span data-ttu-id="c5bbc-125">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="c5bbc-125">at *rectangle*</span></span>       | <span data-ttu-id="c5bbc-126">*extension*</span><span class="sxs-lookup"><span data-stu-id="c5bbc-126">*filename*</span></span>            |
| <span data-ttu-id="c5bbc-127">sequencer</span><span class="sxs-lookup"><span data-stu-id="c5bbc-127">sequencer</span></span>    | <span data-ttu-id="c5bbc-128">*extension*</span><span class="sxs-lookup"><span data-stu-id="c5bbc-128">*filename*</span></span>           |                       |
| <span data-ttu-id="c5bbc-129">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="c5bbc-129">waveaudio</span></span>    | <span data-ttu-id="c5bbc-130">*extension*</span><span class="sxs-lookup"><span data-stu-id="c5bbc-130">*filename*</span></span>           |                       |



 

<span data-ttu-id="c5bbc-131">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszFilename** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-131">The following table lists the flags that can be specified in the **lpszFilename** parameter and their meanings.</span></span>



| <span data-ttu-id="c5bbc-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5bbc-132">Value</span></span>          | <span data-ttu-id="c5bbc-133">Signification</span><span class="sxs-lookup"><span data-stu-id="c5bbc-133">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bbc-134">abort</span><span class="sxs-lookup"><span data-stu-id="c5bbc-134">abort</span></span>          | <span data-ttu-id="c5bbc-135">Arrête une opération d' **enregistrement** en cours.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-135">Stops a **save** operation in progress.</span></span> <span data-ttu-id="c5bbc-136">S’il est utilisé, il doit s’agir du seul élément présent.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-136">If used, this must be the only item present.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c5bbc-137">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="c5bbc-137">at *rectangle*</span></span> | <span data-ttu-id="c5bbc-138">Spécifie un rectangle par rapport à l’origine de la mémoire tampon du frame.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-138">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="c5bbc-139">Le *rectangle* est spécifié en tant que *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-139">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="c5bbc-140">Les coordonnées *x1 Y1* spécifient l’angle supérieur gauche et les coordonnées *x2 Y2* spécifient la largeur et la hauteur. Pour les périphériques vidéo numériques, la commande de [capture](capture.md) est utilisée pour capturer le contenu de la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-140">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.For digital-video devices, the [capture](capture.md) command is used to capture the contents of the frame buffer.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="c5bbc-141">*extension*</span><span class="sxs-lookup"><span data-stu-id="c5bbc-141">*filename*</span></span>     | <span data-ttu-id="c5bbc-142">Spécifie le nom de fichier à assigner au fichier de données.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-142">Specifies the filename to assign to the data file.</span></span> <span data-ttu-id="c5bbc-143">Si aucun chemin d’accès n’est spécifié, le fichier est placé sur le disque et dans le répertoire spécifié précédemment dans la commande de [réserve](reserve.md) explicite ou implicite.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-143">If a path is not specified, the file will be placed on the disk and in the directory previously specified on the explicit or implicit [reserve](reserve.md) command.</span></span> <span data-ttu-id="c5bbc-144">Si la **réserve** n’a pas été émise, le lecteur et le répertoire par défaut sont ceux associés à la tâche de l’application.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-144">If **reserve** has not been issued, the default drive and directory are those associated with the application's task.</span></span> <span data-ttu-id="c5bbc-145">Si un chemin d’accès est spécifié, l’appareil peut exiger qu’il se trouve sur le lecteur de disque spécifié par la **réserve** explicite ou implicite.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-145">If a path is specified, the device might require it to be on the disk drive specified by the explicit or implicit **reserve**.</span></span> <span data-ttu-id="c5bbc-146">Cet indicateur est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-146">This flag is required.</span></span> |
| <span data-ttu-id="c5bbc-147">keepreserve</span><span class="sxs-lookup"><span data-stu-id="c5bbc-147">keepreserve</span></span>    | <span data-ttu-id="c5bbc-148">Spécifie que l’espace disque inutilisé à partir de la commande de **réserve** d’origine n’est pas libéré.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-148">Specifies that unused disk space left over from the original **reserve** command is not deallocated.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="c5bbc-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c5bbc-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c5bbc-150">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-150">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c5bbc-151">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="c5bbc-151">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="c5bbc-152">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c5bbc-152">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5bbc-153">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c5bbc-153">Return Value</span></span>

<span data-ttu-id="c5bbc-154">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-154">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5bbc-155">Notes</span><span class="sxs-lookup"><span data-stu-id="c5bbc-155">Remarks</span></span>

<span data-ttu-id="c5bbc-156">La variable *filename* est requise si l’appareil a été ouvert à l’aide de l’identificateur de périphérique « New ».</span><span class="sxs-lookup"><span data-stu-id="c5bbc-156">The *filename* variable is required if the device was opened using the "new" device identifier.</span></span>

## <a name="examples"></a><span data-ttu-id="c5bbc-157">Exemples</span><span class="sxs-lookup"><span data-stu-id="c5bbc-157">Examples</span></span>

<span data-ttu-id="c5bbc-158">La commande suivante enregistre l’intégralité de la mémoire tampon vidéo dans un fichier nommé VCAPFILE. TGA.</span><span class="sxs-lookup"><span data-stu-id="c5bbc-158">The following command saves the entire video buffer to a file named VCAPFILE.TGA.</span></span>

``` syntax
save vboard c:\vcap\vcapfile.tga
```

## <a name="requirements"></a><span data-ttu-id="c5bbc-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5bbc-159">Requirements</span></span>



| <span data-ttu-id="c5bbc-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5bbc-160">Requirement</span></span> | <span data-ttu-id="c5bbc-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5bbc-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c5bbc-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5bbc-162">Minimum supported client</span></span><br/> | <span data-ttu-id="c5bbc-163">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5bbc-163">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c5bbc-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5bbc-164">Minimum supported server</span></span><br/> | <span data-ttu-id="c5bbc-165">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5bbc-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c5bbc-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5bbc-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5bbc-167">MCI</span><span class="sxs-lookup"><span data-stu-id="c5bbc-167">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c5bbc-168">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="c5bbc-168">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c5bbc-169">attire</span><span class="sxs-lookup"><span data-stu-id="c5bbc-169">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="c5bbc-170">reserve</span><span class="sxs-lookup"><span data-stu-id="c5bbc-170">reserve</span></span>](reserve.md)
</dt> </dl>

 


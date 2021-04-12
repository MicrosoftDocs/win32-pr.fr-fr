---
title: info (commande)
description: La commande info récupère une description du matériel à partir d’un appareil. Tous les périphériques MCI reconnaissent cette commande.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- commande info Windows Multimedia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d401efca6a59d1ed3cbf433d7c33311678705d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385140"
---
# <a name="info-command"></a><span data-ttu-id="d283e-105">info (commande)</span><span class="sxs-lookup"><span data-stu-id="d283e-105">info command</span></span>

<span data-ttu-id="d283e-106">La commande info récupère une description du matériel à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="d283e-106">The info command retrieves a hardware description from a device.</span></span> <span data-ttu-id="d283e-107">Tous les périphériques MCI reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="d283e-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="d283e-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="d283e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d283e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d283e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d283e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d283e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d283e-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="d283e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d283e-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="d283e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d283e-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span><span class="sxs-lookup"><span data-stu-id="d283e-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span></span>
</dt> <dd>

<span data-ttu-id="d283e-114">Indicateur qui identifie le type d’informations requis.</span><span class="sxs-lookup"><span data-stu-id="d283e-114">Flag that identifies the type of information required.</span></span> <span data-ttu-id="d283e-115">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **info** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="d283e-115">The following table lists device types that recognize the **info** command and the flags used by each type.</span></span>



| <span data-ttu-id="d283e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d283e-116">Value</span></span>        | <span data-ttu-id="d283e-117">Signification</span><span class="sxs-lookup"><span data-stu-id="d283e-117">Meaning</span></span>                                                             | <span data-ttu-id="d283e-118">Signification</span><span class="sxs-lookup"><span data-stu-id="d283e-118">Meaning</span></span>                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="d283e-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="d283e-119">cdaudio</span></span>      | <span data-ttu-id="d283e-120">info identityinfo UPC</span><span class="sxs-lookup"><span data-stu-id="d283e-120">info identityinfo upc</span></span>                                               | <span data-ttu-id="d283e-121">product</span><span class="sxs-lookup"><span data-stu-id="d283e-121">product</span></span>                                             |
| <span data-ttu-id="d283e-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="d283e-122">digitalvideo</span></span> | <span data-ttu-id="d283e-123">qualité audio algorithmaudio qualityfileproductstill algorithmstill</span><span class="sxs-lookup"><span data-stu-id="d283e-123">audio algorithmaudio qualityfileproductstill algorithmstill quality</span></span> | <span data-ttu-id="d283e-124">usageversionvideo algorithmvideo qualitywindow texte</span><span class="sxs-lookup"><span data-stu-id="d283e-124">usageversionvideo algorithmvideo qualitywindow text</span></span> |
| <span data-ttu-id="d283e-125">superposition</span><span class="sxs-lookup"><span data-stu-id="d283e-125">overlay</span></span>      | <span data-ttu-id="d283e-126">fileproduct</span><span class="sxs-lookup"><span data-stu-id="d283e-126">fileproduct</span></span>                                                         | <span data-ttu-id="d283e-127">texte de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="d283e-127">window text</span></span>                                         |
| <span data-ttu-id="d283e-128">sequencer</span><span class="sxs-lookup"><span data-stu-id="d283e-128">sequencer</span></span>    | <span data-ttu-id="d283e-129">copyrightfile</span><span class="sxs-lookup"><span data-stu-id="d283e-129">copyrightfile</span></span>                                                       | <span data-ttu-id="d283e-130">nameproduct</span><span class="sxs-lookup"><span data-stu-id="d283e-130">nameproduct</span></span>                                         |
| <span data-ttu-id="d283e-131">vidéo</span><span class="sxs-lookup"><span data-stu-id="d283e-131">vcr</span></span>          | <span data-ttu-id="d283e-132">product</span><span class="sxs-lookup"><span data-stu-id="d283e-132">product</span></span>                                                             | <span data-ttu-id="d283e-133">version</span><span class="sxs-lookup"><span data-stu-id="d283e-133">version</span></span>                                             |
| <span data-ttu-id="d283e-134">videodisk</span><span class="sxs-lookup"><span data-stu-id="d283e-134">videodisk</span></span>    | <span data-ttu-id="d283e-135">product</span><span class="sxs-lookup"><span data-stu-id="d283e-135">product</span></span>                                                             |                                                     |
| <span data-ttu-id="d283e-136">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="d283e-136">waveaudio</span></span>    | <span data-ttu-id="d283e-137">fileinput</span><span class="sxs-lookup"><span data-stu-id="d283e-137">fileinput</span></span>                                                           | <span data-ttu-id="d283e-138">outputproduct</span><span class="sxs-lookup"><span data-stu-id="d283e-138">outputproduct</span></span>                                       |



 

<span data-ttu-id="d283e-139">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszInfoType** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="d283e-139">The following table lists the flags that can be specified in the **lpszInfoType** parameter and their meanings.</span></span>



| <span data-ttu-id="d283e-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="d283e-140">Value</span></span>           | <span data-ttu-id="d283e-141">Signification</span><span class="sxs-lookup"><span data-stu-id="d283e-141">Meaning</span></span>                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d283e-142">algorithme audio</span><span class="sxs-lookup"><span data-stu-id="d283e-142">audio algorithm</span></span> | <span data-ttu-id="d283e-143">Retourne le nom de l’algorithme de compression audio actuel.</span><span class="sxs-lookup"><span data-stu-id="d283e-143">Returns the name of the current audio compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="d283e-144">qualité audio</span><span class="sxs-lookup"><span data-stu-id="d283e-144">audio quality</span></span>   | <span data-ttu-id="d283e-145">Retourne le nom du descripteur de qualité audio actuel.</span><span class="sxs-lookup"><span data-stu-id="d283e-145">Returns the name for the current audio quality descriptor.</span></span> <span data-ttu-id="d283e-146">Cela peut retourner « Unknown » si l’application a défini des paramètres sur des valeurs spécifiques qui ne correspondent pas aux qualités définies.</span><span class="sxs-lookup"><span data-stu-id="d283e-146">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="d283e-147">copyright</span><span class="sxs-lookup"><span data-stu-id="d283e-147">copyright</span></span>       | <span data-ttu-id="d283e-148">Récupère l’avis de copyright du fichier MIDI à partir de l’événement de métadonnées de copyright.</span><span class="sxs-lookup"><span data-stu-id="d283e-148">Retrieves the MIDI file copyright notice from the copyright meta event.</span></span>                                                                                                                            |
| <span data-ttu-id="d283e-149">fichier</span><span class="sxs-lookup"><span data-stu-id="d283e-149">file</span></span>            | <span data-ttu-id="d283e-150">Récupère le nom du fichier utilisé par l’appareil composé.</span><span class="sxs-lookup"><span data-stu-id="d283e-150">Retrieves the name of the file used by the compound device.</span></span> <span data-ttu-id="d283e-151">Si l’appareil est ouvert sans fichier et que la commande [Load](load.md) n’a pas été utilisée, une chaîne NULL est retournée.</span><span class="sxs-lookup"><span data-stu-id="d283e-151">If the device is opened without a file and the [load](load.md) command has not been used, a null string is returned.</span></span>                  |
| <span data-ttu-id="d283e-152">identité des informations</span><span class="sxs-lookup"><span data-stu-id="d283e-152">info identity</span></span>   | <span data-ttu-id="d283e-153">Produit un identificateur unique pour le CD audio actuellement chargé dans le lecteur interrogé.</span><span class="sxs-lookup"><span data-stu-id="d283e-153">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span>                                                                                                        |
| <span data-ttu-id="d283e-154">info UPC</span><span class="sxs-lookup"><span data-stu-id="d283e-154">info upc</span></span>        | <span data-ttu-id="d283e-155">Produit le code UPC (Universal Product Code) encodé sur un CD audio.</span><span class="sxs-lookup"><span data-stu-id="d283e-155">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="d283e-156">Le UPC est une chaîne de chiffres.</span><span class="sxs-lookup"><span data-stu-id="d283e-156">The UPC is a string of digits.</span></span> <span data-ttu-id="d283e-157">Elle n’est peut-être pas disponible pour tous les CD.</span><span class="sxs-lookup"><span data-stu-id="d283e-157">It might not be available for all CDs.</span></span>                                                    |
| <span data-ttu-id="d283e-158">entrée</span><span class="sxs-lookup"><span data-stu-id="d283e-158">input</span></span>           | <span data-ttu-id="d283e-159">Récupère la description de l’appareil d’entrée actuel.</span><span class="sxs-lookup"><span data-stu-id="d283e-159">Retrieves the description of the current input device.</span></span> <span data-ttu-id="d283e-160">Retourne "none" si aucun périphérique d’entrée n’est défini.</span><span class="sxs-lookup"><span data-stu-id="d283e-160">Returns "none" if an input device is not set.</span></span>                                                                                               |
| <span data-ttu-id="d283e-161">name</span><span class="sxs-lookup"><span data-stu-id="d283e-161">name</span></span>            | <span data-ttu-id="d283e-162">Récupère le nom de la séquence à partir de l’événement Meta nom de la séquence/suivi.</span><span class="sxs-lookup"><span data-stu-id="d283e-162">Retrieves the sequence name from the sequence/track name meta event.</span></span>                                                                                                                               |
| <span data-ttu-id="d283e-163">sortie</span><span class="sxs-lookup"><span data-stu-id="d283e-163">output</span></span>          | <span data-ttu-id="d283e-164">Récupère la description du périphérique de sortie actuel.</span><span class="sxs-lookup"><span data-stu-id="d283e-164">Retrieves the description of the current output device.</span></span> <span data-ttu-id="d283e-165">Retourne "none" si aucun périphérique de sortie n’est défini.</span><span class="sxs-lookup"><span data-stu-id="d283e-165">Returns "none" if an output device is not set.</span></span>                                                                                             |
| <span data-ttu-id="d283e-166">product</span><span class="sxs-lookup"><span data-stu-id="d283e-166">product</span></span>         | <span data-ttu-id="d283e-167">Récupère une description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d283e-167">Retrieves a description of the device.</span></span> <span data-ttu-id="d283e-168">Ces informations incluent souvent le nom et le modèle du produit.</span><span class="sxs-lookup"><span data-stu-id="d283e-168">This information often includes the product name and model.</span></span> <span data-ttu-id="d283e-169">La longueur de la chaîne ne doit pas dépasser 31 caractères.</span><span class="sxs-lookup"><span data-stu-id="d283e-169">The string length will be 31 characters or fewer.</span></span>                                               |
| <span data-ttu-id="d283e-170">algorithme toujours</span><span class="sxs-lookup"><span data-stu-id="d283e-170">still algorithm</span></span> | <span data-ttu-id="d283e-171">Retourne le nom de l’algorithme de compression d’image continue actuel.</span><span class="sxs-lookup"><span data-stu-id="d283e-171">Returns the name of the current still image compression algorithm.</span></span>                                                                                                                                 |
| <span data-ttu-id="d283e-172">qualité toujours</span><span class="sxs-lookup"><span data-stu-id="d283e-172">still quality</span></span>   | <span data-ttu-id="d283e-173">Retourne le nom du descripteur de qualité d’image continue actuel.</span><span class="sxs-lookup"><span data-stu-id="d283e-173">Returns the name for the current still image quality descriptor.</span></span> <span data-ttu-id="d283e-174">Cela peut retourner « Unknown » si l’application a défini des paramètres sur des valeurs spécifiques qui ne correspondent pas aux qualités définies.</span><span class="sxs-lookup"><span data-stu-id="d283e-174">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span> |
| <span data-ttu-id="d283e-175">usage</span><span class="sxs-lookup"><span data-stu-id="d283e-175">usage</span></span>           | <span data-ttu-id="d283e-176">Retourne une chaîne qui décrit les restrictions d’utilisation qui peuvent être imposées par le propriétaire des données audio ou visuelles dans l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="d283e-176">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audio data in the workspace.</span></span>                                                                    |
| <span data-ttu-id="d283e-177">version</span><span class="sxs-lookup"><span data-stu-id="d283e-177">version</span></span>         | <span data-ttu-id="d283e-178">Retourne le niveau de version du pilote de périphérique et du matériel.</span><span class="sxs-lookup"><span data-stu-id="d283e-178">Returns the release level of the device driver and hardware.</span></span>                                                                                                                                       |
| <span data-ttu-id="d283e-179">algorithme vidéo</span><span class="sxs-lookup"><span data-stu-id="d283e-179">video algorithm</span></span> | <span data-ttu-id="d283e-180">Retourne le nom de l’algorithme de compression vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="d283e-180">Returns the name of the current video compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="d283e-181">qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="d283e-181">video quality</span></span>   | <span data-ttu-id="d283e-182">Retourne le nom du descripteur de qualité vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="d283e-182">Returns the name for the current video quality descriptor.</span></span> <span data-ttu-id="d283e-183">Cela peut retourner « Unknown » si l’application a défini des paramètres sur des valeurs spécifiques qui ne correspondent pas aux qualités définies.</span><span class="sxs-lookup"><span data-stu-id="d283e-183">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="d283e-184">texte de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="d283e-184">window text</span></span>     | <span data-ttu-id="d283e-185">Récupère la légende de la fenêtre utilisée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d283e-185">Retrieves the caption of the window used by the device.</span></span>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="d283e-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d283e-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d283e-187">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="d283e-187">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="d283e-188">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="d283e-188">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="d283e-189">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d283e-189">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d283e-190">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d283e-190">Return Value</span></span>

<span data-ttu-id="d283e-191">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="d283e-191">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="d283e-192">Exemples</span><span class="sxs-lookup"><span data-stu-id="d283e-192">Examples</span></span>

<span data-ttu-id="d283e-193">La commande suivante récupère une description du matériel associé à l’appareil « mySound ».</span><span class="sxs-lookup"><span data-stu-id="d283e-193">The following command retrieves a description of the hardware associated with the "mysound" device.</span></span>

``` syntax
info mysound product
```

## <a name="requirements"></a><span data-ttu-id="d283e-194">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d283e-194">Requirements</span></span>



| <span data-ttu-id="d283e-195">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d283e-195">Requirement</span></span> | <span data-ttu-id="d283e-196">Valeur</span><span class="sxs-lookup"><span data-stu-id="d283e-196">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d283e-197">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d283e-197">Minimum supported client</span></span><br/> | <span data-ttu-id="d283e-198">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d283e-198">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d283e-199">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d283e-199">Minimum supported server</span></span><br/> | <span data-ttu-id="d283e-200">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d283e-200">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d283e-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d283e-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d283e-202">MCI</span><span class="sxs-lookup"><span data-stu-id="d283e-202">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d283e-203">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="d283e-203">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="d283e-204">load</span><span class="sxs-lookup"><span data-stu-id="d283e-204">load</span></span>](load.md)
</dt> </dl>

 


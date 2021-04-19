---
title: commande Play
description: La commande Play démarre la lecture d’un appareil. Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- commande Play Windows Multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509096"
---
# <a name="play-command"></a><span data-ttu-id="0e56e-105">commande Play</span><span class="sxs-lookup"><span data-stu-id="0e56e-105">play command</span></span>

<span data-ttu-id="0e56e-106">La commande Play démarre la lecture d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="0e56e-106">The play command starts playing a device.</span></span> <span data-ttu-id="0e56e-107">Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="0e56e-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="0e56e-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="0e56e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0e56e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e56e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e56e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0e56e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0e56e-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="0e56e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0e56e-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="0e56e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0e56e-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span><span class="sxs-lookup"><span data-stu-id="0e56e-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0e56e-114">Indicateur de la façon dont un appareil est lu.</span><span class="sxs-lookup"><span data-stu-id="0e56e-114">Flag for playing a device.</span></span> <span data-ttu-id="0e56e-115">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Play** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="0e56e-115">The following table lists device types that recognize the **play** command and the flags used by each type.</span></span>



| <span data-ttu-id="0e56e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e56e-116">Value</span></span>        | <span data-ttu-id="0e56e-117">Signification</span><span class="sxs-lookup"><span data-stu-id="0e56e-117">Meaning</span></span>                          | <span data-ttu-id="0e56e-118">Signification</span><span class="sxs-lookup"><span data-stu-id="0e56e-118">Meaning</span></span>                           |
|--------------|----------------------------------|-----------------------------------|
| <span data-ttu-id="0e56e-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="0e56e-119">cdaudio</span></span>      | <span data-ttu-id="0e56e-120">à partir de la *position*</span><span class="sxs-lookup"><span data-stu-id="0e56e-120">from *position*</span></span>                  | <span data-ttu-id="0e56e-121">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="0e56e-121">to *position*</span></span>                     |
| <span data-ttu-id="0e56e-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="0e56e-122">digitalvideo</span></span> | <span data-ttu-id="0e56e-123">à partir de la *position* plein écran</span><span class="sxs-lookup"><span data-stu-id="0e56e-123">from *position* fullscreen repeat</span></span> | <span data-ttu-id="0e56e-124">inverser la fenêtre *position*</span><span class="sxs-lookup"><span data-stu-id="0e56e-124">reverse to *position* window</span></span>       |
| <span data-ttu-id="0e56e-125">sequencer</span><span class="sxs-lookup"><span data-stu-id="0e56e-125">sequencer</span></span>    | <span data-ttu-id="0e56e-126">à partir de la *position*</span><span class="sxs-lookup"><span data-stu-id="0e56e-126">from *position*</span></span>                  | <span data-ttu-id="0e56e-127">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="0e56e-127">to *position*</span></span>                     |
| <span data-ttu-id="0e56e-128">vidéo</span><span class="sxs-lookup"><span data-stu-id="0e56e-128">vcr</span></span>          | <span data-ttu-id="0e56e-129">à l' *heure* de la *position* inverse</span><span class="sxs-lookup"><span data-stu-id="0e56e-129">at *time* from *position* reverse</span></span>  | <span data-ttu-id="0e56e-130">analyser jusqu’au *poste*</span><span class="sxs-lookup"><span data-stu-id="0e56e-130">scan to *position*</span></span>                |
| <span data-ttu-id="0e56e-131">videodisc</span><span class="sxs-lookup"><span data-stu-id="0e56e-131">videodisc</span></span>    | <span data-ttu-id="0e56e-132">analyse inversée rapide à partir de la *position*</span><span class="sxs-lookup"><span data-stu-id="0e56e-132">fast from *position* reverse scan</span></span> | <span data-ttu-id="0e56e-133">*entier* vitesse lente à *positionner*</span><span class="sxs-lookup"><span data-stu-id="0e56e-133">slow speed *integer* to *position*</span></span> |
| <span data-ttu-id="0e56e-134">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="0e56e-134">waveaudio</span></span>    | <span data-ttu-id="0e56e-135">à partir de la *position*</span><span class="sxs-lookup"><span data-stu-id="0e56e-135">from *position*</span></span>                  | <span data-ttu-id="0e56e-136">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="0e56e-136">to *position*</span></span>                     |



 

<span data-ttu-id="0e56e-137">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszPlayFlags** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="0e56e-137">The following table lists the flags that can be specified in the **lpszPlayFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="0e56e-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e56e-138">Value</span></span>           | <span data-ttu-id="0e56e-139">Signification</span><span class="sxs-lookup"><span data-stu-id="0e56e-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e56e-140">à *temps*</span><span class="sxs-lookup"><span data-stu-id="0e56e-140">at *time*</span></span>       | <span data-ttu-id="0e56e-141">Indique quand l’appareil doit commencer à exécuter cette commande ou, si l’appareil a été reçu, lorsque la commande de signal démarre.</span><span class="sxs-lookup"><span data-stu-id="0e56e-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="0e56e-142">Pour plus d’informations, consultez la commande [CUE](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="0e56e-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="0e56e-143">fast</span><span class="sxs-lookup"><span data-stu-id="0e56e-143">fast</span></span>            | <span data-ttu-id="0e56e-144">Indique que la lecture de l’appareil doit être plus rapide que la normale.</span><span class="sxs-lookup"><span data-stu-id="0e56e-144">Indicates that the device should play faster than normal.</span></span> <span data-ttu-id="0e56e-145">Pour déterminer la vitesse exacte sur un lecteur videodisc, utilisez l’indicateur « Speed » de la commande [Status](status.md) .</span><span class="sxs-lookup"><span data-stu-id="0e56e-145">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="0e56e-146">Pour spécifier la vitesse plus précisément, utilisez l’indicateur « Speed » de cette commande.</span><span class="sxs-lookup"><span data-stu-id="0e56e-146">To specify the speed more precisely, use the "speed" flag of this command.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="0e56e-147">à partir de la *position*</span><span class="sxs-lookup"><span data-stu-id="0e56e-147">from *position*</span></span> | <span data-ttu-id="0e56e-148">Spécifie une position de départ pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="0e56e-148">Specifies a starting position for the playback.</span></span> <span data-ttu-id="0e56e-149">Si l’indicateur « from » n’est pas spécifié, la lecture commence à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="0e56e-149">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="0e56e-150">Pour les appareils **cdaudio** , si la position « de » est supérieure à la position de fin du disque, ou si la position « de » est supérieure à la position « à », le pilote retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="0e56e-150">For **cdaudio** devices, if the "from" position is greater than the end position of the disc, or if the "from" position is greater than the "to" position, the driver returns an error.</span></span> <span data-ttu-id="0e56e-151">Pour les appareils **videodisc** , les positions par défaut se trouvent dans des frames pour les disques CAV et en heures, minutes et secondes pour les disques CLV.</span><span class="sxs-lookup"><span data-stu-id="0e56e-151">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span> |
| <span data-ttu-id="0e56e-152">large</span><span class="sxs-lookup"><span data-stu-id="0e56e-152">fullscreen</span></span>      | <span data-ttu-id="0e56e-153">Spécifie qu’un affichage plein écran doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="0e56e-153">Specifies that a full-screen display should be used.</span></span> <span data-ttu-id="0e56e-154">Utilisez cet indicateur uniquement lors de la diffusion de fichiers compressés.</span><span class="sxs-lookup"><span data-stu-id="0e56e-154">Use this flag only when playing compressed files.</span></span> <span data-ttu-id="0e56e-155">(Les fichiers non compressés ne s’affichent pas en mode plein écran.)</span><span class="sxs-lookup"><span data-stu-id="0e56e-155">(Uncompressed files won't play full-screen.)</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0e56e-156">répéter</span><span class="sxs-lookup"><span data-stu-id="0e56e-156">repeat</span></span>          | <span data-ttu-id="0e56e-157">Spécifie que la lecture doit redémarrer lorsque la fin du contenu est atteinte.</span><span class="sxs-lookup"><span data-stu-id="0e56e-157">Specifies that playback should restart when the end of the content is reached.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0e56e-158">reverse</span><span class="sxs-lookup"><span data-stu-id="0e56e-158">reverse</span></span>         | <span data-ttu-id="0e56e-159">Spécifie que le sens de lecture est vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="0e56e-159">Specifies that the play direction is backward.</span></span> <span data-ttu-id="0e56e-160">Vous ne pouvez pas spécifier un emplacement de fin avec l’indicateur « inversée ».</span><span class="sxs-lookup"><span data-stu-id="0e56e-160">You cannot specify an ending location with the "reverse" flag.</span></span> <span data-ttu-id="0e56e-161">Pour videodiscs, « Scan » s’applique uniquement au format CAV.</span><span class="sxs-lookup"><span data-stu-id="0e56e-161">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="0e56e-162">vérifier</span><span class="sxs-lookup"><span data-stu-id="0e56e-162">scan</span></span>            | <span data-ttu-id="0e56e-163">S’exécute aussi rapidement que possible sans désactiver la vidéo (même si l’audio est peut-être désactivé).</span><span class="sxs-lookup"><span data-stu-id="0e56e-163">Plays as fast as possible without disabling video (although audio might be disabled).</span></span> <span data-ttu-id="0e56e-164">Pour videodiscs, « Scan » s’applique uniquement au format CAV.</span><span class="sxs-lookup"><span data-stu-id="0e56e-164">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0e56e-165">slow</span><span class="sxs-lookup"><span data-stu-id="0e56e-165">slow</span></span>            | <span data-ttu-id="0e56e-166">La lecture est lente.</span><span class="sxs-lookup"><span data-stu-id="0e56e-166">Plays slowly.</span></span> <span data-ttu-id="0e56e-167">Pour déterminer la vitesse exacte sur un lecteur videodisc, utilisez l’indicateur « Speed » de la commande [Status](status.md) .</span><span class="sxs-lookup"><span data-stu-id="0e56e-167">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="0e56e-168">Pour spécifier la vitesse plus précisément, utilisez l’indicateur « Speed » de cette commande.</span><span class="sxs-lookup"><span data-stu-id="0e56e-168">To specify the speed more precisely, use the "speed" flag of this command.</span></span> <span data-ttu-id="0e56e-169">Pour videodiscs, « Slow » s’applique uniquement au format CAV.</span><span class="sxs-lookup"><span data-stu-id="0e56e-169">For videodiscs, "slow" applies only to CAV format.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="0e56e-170">*entier* de vitesse</span><span class="sxs-lookup"><span data-stu-id="0e56e-170">speed *integer*</span></span> | <span data-ttu-id="0e56e-171">Lit un videodisc à la vitesse spécifiée, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="0e56e-171">Plays a videodisc at the specified speed, in frames per second.</span></span> <span data-ttu-id="0e56e-172">Cet indicateur s’applique uniquement aux disques CAV.</span><span class="sxs-lookup"><span data-stu-id="0e56e-172">This flag applies only to CAV discs.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="0e56e-173">pour *positionner*</span><span class="sxs-lookup"><span data-stu-id="0e56e-173">to *position*</span></span>   | <span data-ttu-id="0e56e-174">Spécifie une position de fin pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="0e56e-174">Specifies an ending position for the playback.</span></span> <span data-ttu-id="0e56e-175">Si l’indicateur « to » n’est pas spécifié, la lecture s’arrête à la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="0e56e-175">If the "to" flag is not specified, playback stops at the end of the content.</span></span> <span data-ttu-id="0e56e-176">Pour les appareils **cdaudio** , si la position « to » est supérieure à la position de fin du disque, le pilote retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="0e56e-176">For **cdaudio** devices, if the "to" position is greater than the end position of the disc, the driver returns an error.</span></span> <span data-ttu-id="0e56e-177">Pour les appareils **videodisc** , les positions par défaut se trouvent dans des frames pour les disques CAV et en heures, minutes et secondes pour les disques CLV.</span><span class="sxs-lookup"><span data-stu-id="0e56e-177">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span>                                                                  |
| <span data-ttu-id="0e56e-178">window</span><span class="sxs-lookup"><span data-stu-id="0e56e-178">window</span></span>          | <span data-ttu-id="0e56e-179">Spécifie que la diffusion doit utiliser la fenêtre associée à l’instance d’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e56e-179">Specifies that playing should use the window associated with the device instance.</span></span> <span data-ttu-id="0e56e-180">Il s'agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e56e-180">This is the default setting.</span></span>                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="0e56e-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0e56e-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0e56e-182">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="0e56e-182">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="0e56e-183">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="0e56e-183">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="0e56e-184">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0e56e-184">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e56e-185">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0e56e-185">Return Value</span></span>

<span data-ttu-id="0e56e-186">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="0e56e-186">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e56e-187">Notes</span><span class="sxs-lookup"><span data-stu-id="0e56e-187">Remarks</span></span>

<span data-ttu-id="0e56e-188">Avant d’émettre des commandes qui utilisent des valeurs de position, vous devez définir le format d’heure souhaité à l’aide de la commande [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="0e56e-188">Before issuing commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="0e56e-189">Cette commande commence à la vitesse actuelle, telle qu’elle est définie avec la commande « Speed » définie.</span><span class="sxs-lookup"><span data-stu-id="0e56e-189">This command begins playing at the current speed, as set with the set "speed" command.</span></span> <span data-ttu-id="0e56e-190">La direction est inversée si l’indicateur « Reverse » est spécifié, ou si l’indicateur « to » est spécifié en tant que valeur inférieure à l’indicateur « from ».</span><span class="sxs-lookup"><span data-stu-id="0e56e-190">The direction is reverse if the "reverse" flag is specified, or if the "to" flag is specified as a value less than the "from" flag.</span></span> <span data-ttu-id="0e56e-191">Si l’indicateur « from » n’est pas spécifié, la lecture commence à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="0e56e-191">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="0e56e-192">Les indicateurs « to » et « reverse » ne peuvent pas être utilisés ensemble.</span><span class="sxs-lookup"><span data-stu-id="0e56e-192">The "to" and "reverse" flags cannot be used together.</span></span>

## <a name="examples"></a><span data-ttu-id="0e56e-193">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e56e-193">Examples</span></span>

<span data-ttu-id="0e56e-194">La commande suivante lit l’appareil « mySound » de la position 1000 à la position 2000, en envoyant un message de notification à la fin de la lecture.</span><span class="sxs-lookup"><span data-stu-id="0e56e-194">The following command plays the "mysound" device from position 1000 through position 2000, sending a notification message when the playback completes.</span></span>

``` syntax
play mysound from 1000 to 2000 notify
```

## <a name="requirements"></a><span data-ttu-id="0e56e-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e56e-195">Requirements</span></span>



| <span data-ttu-id="0e56e-196">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e56e-196">Requirement</span></span> | <span data-ttu-id="0e56e-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e56e-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0e56e-198">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e56e-198">Minimum supported client</span></span><br/> | <span data-ttu-id="0e56e-199">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e56e-199">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0e56e-200">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e56e-200">Minimum supported server</span></span><br/> | <span data-ttu-id="0e56e-201">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e56e-201">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0e56e-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e56e-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e56e-203">MCI</span><span class="sxs-lookup"><span data-stu-id="0e56e-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0e56e-204">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="0e56e-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="0e56e-205">signal</span><span class="sxs-lookup"><span data-stu-id="0e56e-205">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="0e56e-206">set</span><span class="sxs-lookup"><span data-stu-id="0e56e-206">set</span></span>](set.md)
</dt> </dl>

 


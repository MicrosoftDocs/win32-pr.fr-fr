---
title: figer, commande
description: La commande Freeze fige l’entrée vidéo ou la sortie vidéo sur un magnétoscope ou désactive l’acquisition vidéo dans la mémoire tampon de trame. Les appareils vidéo numérique, vidéo-superposition et VCR reconnaissent cette commande.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- commande figer Windows Multimedia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032332"
---
# <a name="freeze-command"></a><span data-ttu-id="8acf5-105">figer, commande</span><span class="sxs-lookup"><span data-stu-id="8acf5-105">freeze command</span></span>

<span data-ttu-id="8acf5-106">La commande Freeze fige l’entrée vidéo ou la sortie vidéo sur un magnétoscope ou désactive l’acquisition vidéo dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="8acf5-106">The freeze command freezes video input or video output on a VCR or disables video acquisition to the frame buffer.</span></span> <span data-ttu-id="8acf5-107">Les appareils vidéo numérique, vidéo-superposition et VCR reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="8acf5-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="8acf5-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="8acf5-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="8acf5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8acf5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8acf5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8acf5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8acf5-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="8acf5-111">Identifier of an MCI device.</span></span> <span data-ttu-id="8acf5-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="8acf5-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="8acf5-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span><span class="sxs-lookup"><span data-stu-id="8acf5-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8acf5-114">Indicateur qui identifie les éléments à figer.</span><span class="sxs-lookup"><span data-stu-id="8acf5-114">Flag that identifies what to freeze.</span></span> <span data-ttu-id="8acf5-115">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Freeze** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="8acf5-115">The following table lists device types that recognize the **freeze** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8acf5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8acf5-116">Value</span></span></th>
<th><span data-ttu-id="8acf5-117">Signification</span><span class="sxs-lookup"><span data-stu-id="8acf5-117">Meaning</span></span></th>
<th><span data-ttu-id="8acf5-118">Signification</span><span class="sxs-lookup"><span data-stu-id="8acf5-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8acf5-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="8acf5-119">digitalvideo</span></span></td>
<td><span data-ttu-id="8acf5-120">au niveau du <em>rectangle</em></span><span class="sxs-lookup"><span data-stu-id="8acf5-120">at <em>rectangle</em></span></span></td>
<td><span data-ttu-id="8acf5-121">extérieurs</span><span class="sxs-lookup"><span data-stu-id="8acf5-121">outside</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8acf5-122">superposition</span><span class="sxs-lookup"><span data-stu-id="8acf5-122">overlay</span></span></td>
<td><span data-ttu-id="8acf5-123">au niveau du <em>rectangle</em></span><span class="sxs-lookup"><span data-stu-id="8acf5-123">at <em>rectangle</em></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8acf5-124">vidéo</span><span class="sxs-lookup"><span data-stu-id="8acf5-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="8acf5-125">field</span><span class="sxs-lookup"><span data-stu-id="8acf5-125">field</span></span></li>
<li><span data-ttu-id="8acf5-126">frame</span><span class="sxs-lookup"><span data-stu-id="8acf5-126">frame</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8acf5-127">entrée</span><span class="sxs-lookup"><span data-stu-id="8acf5-127">input</span></span></li>
<li><span data-ttu-id="8acf5-128">sortie</span><span class="sxs-lookup"><span data-stu-id="8acf5-128">output</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8acf5-129">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre *lpszFreezeFlags* et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="8acf5-129">The following table lists the flags that can be specified in the *lpszFreezeFlags* parameter and their meanings.</span></span>



| <span data-ttu-id="8acf5-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="8acf5-130">Value</span></span>          | <span data-ttu-id="8acf5-131">Signification</span><span class="sxs-lookup"><span data-stu-id="8acf5-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acf5-132">au niveau du *rectangle*</span><span class="sxs-lookup"><span data-stu-id="8acf5-132">at *rectangle*</span></span> | <span data-ttu-id="8acf5-133">Spécifie la région qui sera figée.</span><span class="sxs-lookup"><span data-stu-id="8acf5-133">Specifies the region that will be frozen.</span></span> <span data-ttu-id="8acf5-134">Pour les périphériques de superposition vidéo, l’acquisition de vidéos est désactivée pour cette région.</span><span class="sxs-lookup"><span data-stu-id="8acf5-134">For video-overlay devices, this region will have video acquisition disabled.</span></span> <span data-ttu-id="8acf5-135">Pour les périphériques vidéo numériques, le bit du masque de verrouillage est activé sur les pixels du rectangle (sauf si l’indicateur « extérieur » est spécifié).</span><span class="sxs-lookup"><span data-stu-id="8acf5-135">For digital-video devices, the pixels within the rectangle will have their lock mask bit turned on (unless the "outside" flag is specified).</span></span> <span data-ttu-id="8acf5-136">Le rectangle est relatif à l’origine de la mémoire tampon vidéo et est spécifié comme *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="8acf5-136">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="8acf5-137">Les coordonnées *x1 Y1* spécifient l’angle supérieur gauche du rectangle, tandis que les coordonnées *x2 Y2* spécifient la largeur et la hauteur.</span><span class="sxs-lookup"><span data-stu-id="8acf5-137">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="8acf5-138">field</span><span class="sxs-lookup"><span data-stu-id="8acf5-138">field</span></span>          | <span data-ttu-id="8acf5-139">Fige le premier champ.</span><span class="sxs-lookup"><span data-stu-id="8acf5-139">Freezes the first field.</span></span> <span data-ttu-id="8acf5-140">Le champ est supposé par défaut (si ni le cadre ni le champ n’est spécifié).</span><span class="sxs-lookup"><span data-stu-id="8acf5-140">Field is assumed by default (if neither frame nor field is specified).</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8acf5-141">frame</span><span class="sxs-lookup"><span data-stu-id="8acf5-141">frame</span></span>          | <span data-ttu-id="8acf5-142">Fige le frame entier, en affichant les deux champs.</span><span class="sxs-lookup"><span data-stu-id="8acf5-142">Freezes the entire frame, displaying both fields.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8acf5-143">entrée</span><span class="sxs-lookup"><span data-stu-id="8acf5-143">input</span></span>          | <span data-ttu-id="8acf5-144">Fige le frame actuel de l’image d’entrée, qu’elle soit en pause ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8acf5-144">Freezes the current frame of the input image, whether it is paused or running.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8acf5-145">sortie</span><span class="sxs-lookup"><span data-stu-id="8acf5-145">output</span></span>         | <span data-ttu-id="8acf5-146">Fige le frame actuel de la sortie à partir du magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="8acf5-146">Freezes the current frame of the output from the VCR.</span></span> <span data-ttu-id="8acf5-147">Si le magnétoscope est en cours d’exécution lorsque le blocage est émis, le frame actuel est figé et le magnétoscope est suspendu.</span><span class="sxs-lookup"><span data-stu-id="8acf5-147">If the VCR is playing when freeze is issued, the current frame is frozen and the VCR is paused.</span></span> <span data-ttu-id="8acf5-148">Si le magnétoscope est suspendu lorsque cette commande est émise, le frame actuel est figé.</span><span class="sxs-lookup"><span data-stu-id="8acf5-148">If the VCR is paused when this command is issued, the current frame is frozen.</span></span> <span data-ttu-id="8acf5-149">L’image figée reste sur le périphérique de sortie jusqu’à ce qu’une commande de [décongélation](unfreeze.md) soit émise.</span><span class="sxs-lookup"><span data-stu-id="8acf5-149">The frozen image remains on the output device until an [unfreeze](unfreeze.md) command is issued.</span></span> <span data-ttu-id="8acf5-150">Si ni « Input » ni « output » n’est spécifié, « output » est supposé.</span><span class="sxs-lookup"><span data-stu-id="8acf5-150">If neither "input" nor "output" is specified, "output" is assumed.</span></span>                                                                                    |
| <span data-ttu-id="8acf5-151">extérieurs</span><span class="sxs-lookup"><span data-stu-id="8acf5-151">outside</span></span>        | <span data-ttu-id="8acf5-152">Indique que la zone en dehors de la région spécifiée à l’aide de l’indicateur « at » est figée.</span><span class="sxs-lookup"><span data-stu-id="8acf5-152">Indicates that the area outside the region specified using the "at" flag is frozen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="8acf5-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="8acf5-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8acf5-154">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="8acf5-154">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="8acf5-155">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="8acf5-155">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="8acf5-156">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8acf5-156">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8acf5-157">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8acf5-157">Return Value</span></span>

<span data-ttu-id="8acf5-158">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="8acf5-158">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8acf5-159">Notes</span><span class="sxs-lookup"><span data-stu-id="8acf5-159">Remarks</span></span>

<span data-ttu-id="8acf5-160">Utilisée avec les périphériques VCR, cette commande est destinée aux cartes de saisie de trame.</span><span class="sxs-lookup"><span data-stu-id="8acf5-160">When used with VCR devices, this command is intended for frame-grabbing cards.</span></span>

<span data-ttu-id="8acf5-161">Pour spécifier des régions d’acquisition irrégulière avec l’indicateur « at », utilisez une série de [commandes Freeze et dégeler.](unfreeze.md)</span><span class="sxs-lookup"><span data-stu-id="8acf5-161">To specify irregular acquisition regions with the "at" flag, use a series of freeze and [unfreeze](unfreeze.md) commands.</span></span> <span data-ttu-id="8acf5-162">Certains périphériques de superposition vidéo limitent la complexité de la région d’acquisition.</span><span class="sxs-lookup"><span data-stu-id="8acf5-162">Some video-overlay devices limit the complexity of the acquisition region.</span></span>

<span data-ttu-id="8acf5-163">Cette commande est prise en charge uniquement si un appel à la commande [Capability](capability.md) avec l’indicateur « peut se figer » retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="8acf5-163">This command is supported only if a call to the [capability](capability.md) command with the "can freeze" flag returns **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="8acf5-164">Exemples</span><span class="sxs-lookup"><span data-stu-id="8acf5-164">Examples</span></span>

<span data-ttu-id="8acf5-165">La commande suivante désactive l’acquisition vidéo dans un carré de 100 pixels dans le coin supérieur gauche de la mémoire tampon vidéo.</span><span class="sxs-lookup"><span data-stu-id="8acf5-165">The following command disables video acquisition in a 100-pixel square at the upper left corner of the video buffer.</span></span>

``` syntax
freeze vboard at 0 0 100 100
```

## <a name="requirements"></a><span data-ttu-id="8acf5-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8acf5-166">Requirements</span></span>



| <span data-ttu-id="8acf5-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8acf5-167">Requirement</span></span> | <span data-ttu-id="8acf5-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="8acf5-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8acf5-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8acf5-169">Minimum supported client</span></span><br/> | <span data-ttu-id="8acf5-170">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8acf5-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8acf5-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8acf5-171">Minimum supported server</span></span><br/> | <span data-ttu-id="8acf5-172">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8acf5-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8acf5-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8acf5-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8acf5-174">MCI</span><span class="sxs-lookup"><span data-stu-id="8acf5-174">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8acf5-175">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="8acf5-175">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="8acf5-176">capability</span><span class="sxs-lookup"><span data-stu-id="8acf5-176">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="8acf5-177">libérer</span><span class="sxs-lookup"><span data-stu-id="8acf5-177">unfreeze</span></span>](unfreeze.md)
</dt> </dl>

 


---
title: fonctionnalité, commande
description: La commande Capability demande des informations sur une capacité particulière d’un appareil. Tous les périphériques MCI reconnaissent cette commande.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- commande de fonctionnalité multimédia Windows
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464635"
---
# <a name="capability-command"></a><span data-ttu-id="2c42e-105">fonctionnalité, commande</span><span class="sxs-lookup"><span data-stu-id="2c42e-105">capability command</span></span>

<span data-ttu-id="2c42e-106">La commande Capability demande des informations sur une capacité particulière d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="2c42e-106">The capability command requests information about a particular capability of a device.</span></span> <span data-ttu-id="2c42e-107">Tous les périphériques MCI reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="2c42e-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="2c42e-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="2c42e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="2c42e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c42e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c42e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2c42e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2c42e-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="2c42e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="2c42e-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="2c42e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="2c42e-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="2c42e-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="2c42e-114">Indicateur qui identifie une fonctionnalité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2c42e-114">Flag that identifies a device capability.</span></span> <span data-ttu-id="2c42e-115">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande de **fonctionnalité** et les indicateurs utilisés par chaque type :</span><span class="sxs-lookup"><span data-stu-id="2c42e-115">The following table lists device types that recognize the **capability** command and the flags used by each type:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c42e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c42e-116">Value</span></span></th>
<th><span data-ttu-id="2c42e-117">Type</span><span class="sxs-lookup"><span data-stu-id="2c42e-117">Type</span></span></th>
<th><span data-ttu-id="2c42e-118">Type</span><span class="sxs-lookup"><span data-stu-id="2c42e-118">Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c42e-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="2c42e-119">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="2c42e-120">peut éjecter</span><span class="sxs-lookup"><span data-stu-id="2c42e-120">can eject</span></span></li>
<li><span data-ttu-id="2c42e-121">peut jouer</span><span class="sxs-lookup"><span data-stu-id="2c42e-121">can play</span></span></li>
<li><span data-ttu-id="2c42e-122">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-122">can record</span></span></li>
<li><span data-ttu-id="2c42e-123">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-123">can save</span></span></li>
<li><span data-ttu-id="2c42e-124">appareil composé</span><span class="sxs-lookup"><span data-stu-id="2c42e-124">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2c42e-125">type de périphérique</span><span class="sxs-lookup"><span data-stu-id="2c42e-125">device type</span></span></li>
<li><span data-ttu-id="2c42e-126">a de l’audio</span><span class="sxs-lookup"><span data-stu-id="2c42e-126">has audio</span></span></li>
<li><span data-ttu-id="2c42e-127">a une vidéo</span><span class="sxs-lookup"><span data-stu-id="2c42e-127">has video</span></span></li>
<li><span data-ttu-id="2c42e-128">utilise des fichiers</span><span class="sxs-lookup"><span data-stu-id="2c42e-128">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-129">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="2c42e-129">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="2c42e-130">peut éjecter</span><span class="sxs-lookup"><span data-stu-id="2c42e-130">can eject</span></span></li>
<li><span data-ttu-id="2c42e-131">peut geler</span><span class="sxs-lookup"><span data-stu-id="2c42e-131">can freeze</span></span></li>
<li><span data-ttu-id="2c42e-132">verrouillage possible</span><span class="sxs-lookup"><span data-stu-id="2c42e-132">can lock</span></span></li>
<li><span data-ttu-id="2c42e-133">peut jouer</span><span class="sxs-lookup"><span data-stu-id="2c42e-133">can play</span></span></li>
<li><span data-ttu-id="2c42e-134">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-134">can record</span></span></li>
<li><span data-ttu-id="2c42e-135">peut inverser</span><span class="sxs-lookup"><span data-stu-id="2c42e-135">can reverse</span></span></li>
<li><span data-ttu-id="2c42e-136">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-136">can save</span></span></li>
<li><span data-ttu-id="2c42e-137">peut étirer</span><span class="sxs-lookup"><span data-stu-id="2c42e-137">can stretch</span></span></li>
<li><span data-ttu-id="2c42e-138">peut étirer l’entrée</span><span class="sxs-lookup"><span data-stu-id="2c42e-138">can stretch input</span></span></li>
<li><span data-ttu-id="2c42e-139">test possible</span><span class="sxs-lookup"><span data-stu-id="2c42e-139">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2c42e-140">appareil composé</span><span class="sxs-lookup"><span data-stu-id="2c42e-140">compound device</span></span></li>
<li><span data-ttu-id="2c42e-141">type de périphérique</span><span class="sxs-lookup"><span data-stu-id="2c42e-141">device type</span></span></li>
<li><span data-ttu-id="2c42e-142">a de l’audio</span><span class="sxs-lookup"><span data-stu-id="2c42e-142">has audio</span></span></li>
<li><span data-ttu-id="2c42e-143">a toujours</span><span class="sxs-lookup"><span data-stu-id="2c42e-143">has still</span></span></li>
<li><span data-ttu-id="2c42e-144">a une vidéo</span><span class="sxs-lookup"><span data-stu-id="2c42e-144">has video</span></span></li>
<li><span data-ttu-id="2c42e-145">taux de lecture maximal</span><span class="sxs-lookup"><span data-stu-id="2c42e-145">maximum play rate</span></span></li>
<li><span data-ttu-id="2c42e-146">Vitesse de lecture minimale</span><span class="sxs-lookup"><span data-stu-id="2c42e-146">minimum play rate</span></span></li>
<li><span data-ttu-id="2c42e-147">utilise des fichiers</span><span class="sxs-lookup"><span data-stu-id="2c42e-147">uses files</span></span></li>
<li><span data-ttu-id="2c42e-148">utilise des palettes</span><span class="sxs-lookup"><span data-stu-id="2c42e-148">uses palettes</span></span></li>
<li><span data-ttu-id="2c42e-149">windows</span><span class="sxs-lookup"><span data-stu-id="2c42e-149">windows</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-150">superposition</span><span class="sxs-lookup"><span data-stu-id="2c42e-150">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="2c42e-151">peut éjecter</span><span class="sxs-lookup"><span data-stu-id="2c42e-151">can eject</span></span></li>
<li><span data-ttu-id="2c42e-152">peut geler</span><span class="sxs-lookup"><span data-stu-id="2c42e-152">can freeze</span></span></li>
<li><span data-ttu-id="2c42e-153">peut jouer</span><span class="sxs-lookup"><span data-stu-id="2c42e-153">can play</span></span></li>
<li><span data-ttu-id="2c42e-154">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-154">can record</span></span></li>
<li><span data-ttu-id="2c42e-155">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-155">can save</span></span></li>
<li><span data-ttu-id="2c42e-156">peut étirer</span><span class="sxs-lookup"><span data-stu-id="2c42e-156">can stretch</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2c42e-157">appareil composé</span><span class="sxs-lookup"><span data-stu-id="2c42e-157">compound device</span></span></li>
<li><span data-ttu-id="2c42e-158">type de périphérique</span><span class="sxs-lookup"><span data-stu-id="2c42e-158">device type</span></span></li>
<li><span data-ttu-id="2c42e-159">a de l’audio</span><span class="sxs-lookup"><span data-stu-id="2c42e-159">has audio</span></span></li>
<li><span data-ttu-id="2c42e-160">a une vidéo</span><span class="sxs-lookup"><span data-stu-id="2c42e-160">has video</span></span></li>
<li><span data-ttu-id="2c42e-161">utilise des fichiers</span><span class="sxs-lookup"><span data-stu-id="2c42e-161">uses files</span></span></li>
<li><span data-ttu-id="2c42e-162">windows</span><span class="sxs-lookup"><span data-stu-id="2c42e-162">windows</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-163">sequencer</span><span class="sxs-lookup"><span data-stu-id="2c42e-163">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="2c42e-164">peut éjecter</span><span class="sxs-lookup"><span data-stu-id="2c42e-164">can eject</span></span></li>
<li><span data-ttu-id="2c42e-165">peut jouer</span><span class="sxs-lookup"><span data-stu-id="2c42e-165">can play</span></span></li>
<li><span data-ttu-id="2c42e-166">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-166">can record</span></span></li>
<li><span data-ttu-id="2c42e-167">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-167">can save</span></span></li>
<li><span data-ttu-id="2c42e-168">appareil composé</span><span class="sxs-lookup"><span data-stu-id="2c42e-168">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2c42e-169">type de périphérique</span><span class="sxs-lookup"><span data-stu-id="2c42e-169">device type</span></span></li>
<li><span data-ttu-id="2c42e-170">a de l’audio</span><span class="sxs-lookup"><span data-stu-id="2c42e-170">has audio</span></span></li>
<li><span data-ttu-id="2c42e-171">a une vidéo</span><span class="sxs-lookup"><span data-stu-id="2c42e-171">has video</span></span></li>
<li><span data-ttu-id="2c42e-172">utilise des fichiers</span><span class="sxs-lookup"><span data-stu-id="2c42e-172">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-173">vidéo</span><span class="sxs-lookup"><span data-stu-id="2c42e-173">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="2c42e-174">peut détecter une longueur</span><span class="sxs-lookup"><span data-stu-id="2c42e-174">can detect length</span></span></li>
<li><span data-ttu-id="2c42e-175">peut éjecter</span><span class="sxs-lookup"><span data-stu-id="2c42e-175">can eject</span></span></li>
<li><span data-ttu-id="2c42e-176">peut geler</span><span class="sxs-lookup"><span data-stu-id="2c42e-176">can freeze</span></span></li>
<li><span data-ttu-id="2c42e-177">peut surveiller les sources</span><span class="sxs-lookup"><span data-stu-id="2c42e-177">can monitor sources</span></span></li>
<li><span data-ttu-id="2c42e-178">peut jouer</span><span class="sxs-lookup"><span data-stu-id="2c42e-178">can play</span></span></li>
<li><span data-ttu-id="2c42e-179">peut être préroll</span><span class="sxs-lookup"><span data-stu-id="2c42e-179">can preroll</span></span></li>
<li><span data-ttu-id="2c42e-180">peut afficher un aperçu</span><span class="sxs-lookup"><span data-stu-id="2c42e-180">can preview</span></span></li>
<li><span data-ttu-id="2c42e-181">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-181">can record</span></span></li>
<li><span data-ttu-id="2c42e-182">peut inverser</span><span class="sxs-lookup"><span data-stu-id="2c42e-182">can reverse</span></span></li>
<li><span data-ttu-id="2c42e-183">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-183">can save</span></span></li>
<li><span data-ttu-id="2c42e-184">test possible</span><span class="sxs-lookup"><span data-stu-id="2c42e-184">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2c42e-185">taux d’incrément d’horloge</span><span class="sxs-lookup"><span data-stu-id="2c42e-185">clock increment rate</span></span></li>
<li><span data-ttu-id="2c42e-186">appareil composé</span><span class="sxs-lookup"><span data-stu-id="2c42e-186">compound device</span></span></li>
<li><span data-ttu-id="2c42e-187">type de périphérique</span><span class="sxs-lookup"><span data-stu-id="2c42e-187">device type</span></span></li>
<li><span data-ttu-id="2c42e-188">a de l’audio</span><span class="sxs-lookup"><span data-stu-id="2c42e-188">has audio</span></span></li>
<li><span data-ttu-id="2c42e-189">a une horloge</span><span class="sxs-lookup"><span data-stu-id="2c42e-189">has clock</span></span></li>
<li><span data-ttu-id="2c42e-190">a un code temporel</span><span class="sxs-lookup"><span data-stu-id="2c42e-190">has timecode</span></span></li>
<li><span data-ttu-id="2c42e-191">a une vidéo</span><span class="sxs-lookup"><span data-stu-id="2c42e-191">has video</span></span></li>
<li><span data-ttu-id="2c42e-192">nombre de marques</span><span class="sxs-lookup"><span data-stu-id="2c42e-192">number of marks</span></span></li>
<li><span data-ttu-id="2c42e-193">précision de la recherche</span><span class="sxs-lookup"><span data-stu-id="2c42e-193">seek accuracy</span></span></li>
<li><span data-ttu-id="2c42e-194">utilise des fichiers</span><span class="sxs-lookup"><span data-stu-id="2c42e-194">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-195">videodisc</span><span class="sxs-lookup"><span data-stu-id="2c42e-195">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="2c42e-196">peut éjecter</span><span class="sxs-lookup"><span data-stu-id="2c42e-196">can eject</span></span></li>
<li><span data-ttu-id="2c42e-197">peut jouer</span><span class="sxs-lookup"><span data-stu-id="2c42e-197">can play</span></span></li>
<li><span data-ttu-id="2c42e-198">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-198">can record</span></span></li>
<li><span data-ttu-id="2c42e-199">peut inverser</span><span class="sxs-lookup"><span data-stu-id="2c42e-199">can reverse</span></span></li>
<li><span data-ttu-id="2c42e-200">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-200">can save</span></span></li>
<li><span data-ttu-id="2c42e-201">CAV</span><span class="sxs-lookup"><span data-stu-id="2c42e-201">CAV</span></span></li>
<li><span data-ttu-id="2c42e-202">CLV</span><span class="sxs-lookup"><span data-stu-id="2c42e-202">CLV</span></span></li>
<li><span data-ttu-id="2c42e-203">appareil composé</span><span class="sxs-lookup"><span data-stu-id="2c42e-203">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2c42e-204">type de périphérique</span><span class="sxs-lookup"><span data-stu-id="2c42e-204">device type</span></span></li>
<li><span data-ttu-id="2c42e-205">Vitesse de lecture rapide</span><span class="sxs-lookup"><span data-stu-id="2c42e-205">fast play rate</span></span></li>
<li><span data-ttu-id="2c42e-206">a de l’audio</span><span class="sxs-lookup"><span data-stu-id="2c42e-206">has audio</span></span></li>
<li><span data-ttu-id="2c42e-207">a une vidéo</span><span class="sxs-lookup"><span data-stu-id="2c42e-207">has video</span></span></li>
<li><span data-ttu-id="2c42e-208">taux de lecture normal</span><span class="sxs-lookup"><span data-stu-id="2c42e-208">normal play rate</span></span></li>
<li><span data-ttu-id="2c42e-209">taux de lecture lent</span><span class="sxs-lookup"><span data-stu-id="2c42e-209">slow play rate</span></span></li>
<li><span data-ttu-id="2c42e-210">utilise des fichiers</span><span class="sxs-lookup"><span data-stu-id="2c42e-210">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-211">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="2c42e-211">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="2c42e-212">peut éjecter</span><span class="sxs-lookup"><span data-stu-id="2c42e-212">can eject</span></span></li>
<li><span data-ttu-id="2c42e-213">peut jouer</span><span class="sxs-lookup"><span data-stu-id="2c42e-213">can play</span></span></li>
<li><span data-ttu-id="2c42e-214">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-214">can record</span></span></li>
<li><span data-ttu-id="2c42e-215">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-215">can save</span></span></li>
<li><span data-ttu-id="2c42e-216">appareil composé</span><span class="sxs-lookup"><span data-stu-id="2c42e-216">compound device</span></span></li>
<li><span data-ttu-id="2c42e-217">type de périphérique</span><span class="sxs-lookup"><span data-stu-id="2c42e-217">device type</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2c42e-218">a de l’audio</span><span class="sxs-lookup"><span data-stu-id="2c42e-218">has audio</span></span></li>
<li><span data-ttu-id="2c42e-219">a une vidéo</span><span class="sxs-lookup"><span data-stu-id="2c42e-219">has video</span></span></li>
<li><span data-ttu-id="2c42e-220">inputs</span><span class="sxs-lookup"><span data-stu-id="2c42e-220">inputs</span></span></li>
<li><span data-ttu-id="2c42e-221">outputs</span><span class="sxs-lookup"><span data-stu-id="2c42e-221">outputs</span></span></li>
<li><span data-ttu-id="2c42e-222">utilise des fichiers</span><span class="sxs-lookup"><span data-stu-id="2c42e-222">uses files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2c42e-223">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre *lpszRequest* et leurs significations :</span><span class="sxs-lookup"><span data-stu-id="2c42e-223">The following table lists the flags that can be specified in the *lpszRequest* parameter and their meanings:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c42e-224">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="2c42e-224">Flags</span></span></th>
<th><span data-ttu-id="2c42e-225">Signification</span><span class="sxs-lookup"><span data-stu-id="2c42e-225">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c42e-226">peut détecter une longueur</span><span class="sxs-lookup"><span data-stu-id="2c42e-226">can detect length</span></span></td>
<td><span data-ttu-id="2c42e-227">Retourne la <strong>valeur true</strong> si l’appareil peut détecter la longueur du média.</span><span class="sxs-lookup"><span data-stu-id="2c42e-227">Returns <strong>TRUE</strong> if the device can detect the length of the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-228">peut éjecter</span><span class="sxs-lookup"><span data-stu-id="2c42e-228">can eject</span></span></td>
<td><span data-ttu-id="2c42e-229">Retourne la <strong>valeur true</strong> si l’appareil peut éjecter le média.</span><span class="sxs-lookup"><span data-stu-id="2c42e-229">Returns <strong>TRUE</strong> if the device can eject the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-230">peut geler</span><span class="sxs-lookup"><span data-stu-id="2c42e-230">can freeze</span></span></td>
<td><span data-ttu-id="2c42e-231">Retourne la <strong>valeur true</strong> si l’appareil peut geler des données dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="2c42e-231">Returns <strong>TRUE</strong> if the device can freeze data in the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-232">verrouillage possible</span><span class="sxs-lookup"><span data-stu-id="2c42e-232">can lock</span></span></td>
<td><span data-ttu-id="2c42e-233">Retourne la <strong>valeur true</strong> si l’appareil peut verrouiller les données.</span><span class="sxs-lookup"><span data-stu-id="2c42e-233">Returns <strong>TRUE</strong> if the device can lock data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-234">peut surveiller les sources</span><span class="sxs-lookup"><span data-stu-id="2c42e-234">can monitor sources</span></span></td>
<td><span data-ttu-id="2c42e-235">Retourne la <strong>valeur true</strong> si l’appareil peut passer une entrée (source) à la sortie analysée, indépendamment de la sélection d’entrée actuelle.</span><span class="sxs-lookup"><span data-stu-id="2c42e-235">Returns <strong>TRUE</strong> if the device can pass an input (source) to the monitored output, independent of the current input selection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-236">peut jouer</span><span class="sxs-lookup"><span data-stu-id="2c42e-236">can play</span></span></td>
<td><span data-ttu-id="2c42e-237">Retourne la <strong>valeur true</strong> si l’appareil peut jouer.</span><span class="sxs-lookup"><span data-stu-id="2c42e-237">Returns <strong>TRUE</strong> if the device can play.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-238">peut être préroll</span><span class="sxs-lookup"><span data-stu-id="2c42e-238">can preroll</span></span></td>
<td><span data-ttu-id="2c42e-239">Retourne la <strong>valeur true</strong> si l’appareil prend en charge l' &quot; &quot; indicateur de préroll avec la commande <a href="cue.md">CUE</a> .</span><span class="sxs-lookup"><span data-stu-id="2c42e-239">Returns <strong>TRUE</strong> if the device supports the &quot;preroll&quot; flag with the <a href="cue.md">cue</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-240">peut afficher un aperçu</span><span class="sxs-lookup"><span data-stu-id="2c42e-240">can preview</span></span></td>
<td><span data-ttu-id="2c42e-241">Retourne la <strong>valeur true</strong> si l’appareil prend en charge les aperçus.</span><span class="sxs-lookup"><span data-stu-id="2c42e-241">Returns <strong>TRUE</strong> if the device supports previews.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-242">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-242">can record</span></span></td>
<td><span data-ttu-id="2c42e-243">Retourne la <strong>valeur true</strong> si l’appareil prend en charge l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2c42e-243">Returns <strong>TRUE</strong> if the device supports recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-244">peut inverser</span><span class="sxs-lookup"><span data-stu-id="2c42e-244">can reverse</span></span></td>
<td><span data-ttu-id="2c42e-245">Retourne la <strong>valeur true</strong> si l’appareil peut jouer en sens inverse.</span><span class="sxs-lookup"><span data-stu-id="2c42e-245">Returns <strong>TRUE</strong> if the device can play in reverse.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-246">peut enregistrer</span><span class="sxs-lookup"><span data-stu-id="2c42e-246">can save</span></span></td>
<td><span data-ttu-id="2c42e-247">Retourne la <strong>valeur true</strong> si l’appareil peut enregistrer des données.</span><span class="sxs-lookup"><span data-stu-id="2c42e-247">Returns <strong>TRUE</strong> if the device can save data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-248">peut étirer</span><span class="sxs-lookup"><span data-stu-id="2c42e-248">can stretch</span></span></td>
<td><span data-ttu-id="2c42e-249">Retourne la <strong>valeur true</strong> si l’appareil peut étirer des frames pour remplir un rectangle d’affichage donné.</span><span class="sxs-lookup"><span data-stu-id="2c42e-249">Returns <strong>TRUE</strong> if the device can stretch frames to fill a given display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-250">peut étirer l’entrée</span><span class="sxs-lookup"><span data-stu-id="2c42e-250">can stretch input</span></span></td>
<td><span data-ttu-id="2c42e-251">Retourne la <strong>valeur true</strong> si l’appareil peut redimensionner une image dans le processus de sa numérisation dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="2c42e-251">Returns <strong>TRUE</strong> if the device can resize an image in the process of digitizing it into the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-252">test possible</span><span class="sxs-lookup"><span data-stu-id="2c42e-252">can test</span></span></td>
<td><span data-ttu-id="2c42e-253">Retourne la <strong>valeur true</strong> si l’appareil reconnaît le mot clé test.</span><span class="sxs-lookup"><span data-stu-id="2c42e-253">Returns <strong>TRUE</strong> if the device recognizes the test keyword.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-254">cav</span><span class="sxs-lookup"><span data-stu-id="2c42e-254">cav</span></span></td>
<td><span data-ttu-id="2c42e-255">Lorsqu’il est combiné à d’autres éléments, cet indicateur spécifie que les informations de retour s’appliquent au format CAV videodiscs.</span><span class="sxs-lookup"><span data-stu-id="2c42e-255">When combined with other items, this flag specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="2c42e-256">Il s’agit de la valeur par défaut si aucun videodisc n’est inséré.</span><span class="sxs-lookup"><span data-stu-id="2c42e-256">This is the default if no videodisc is inserted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-257">taux d’incrément d’horloge</span><span class="sxs-lookup"><span data-stu-id="2c42e-257">clock increment rate</span></span></td>
<td><span data-ttu-id="2c42e-258">Retourne le nombre de sous-cloisonnements pris en charge par l’horloge externe par seconde.</span><span class="sxs-lookup"><span data-stu-id="2c42e-258">Returns the number of subdivisions the external clock supports per second.</span></span> <span data-ttu-id="2c42e-259">Si l’horloge externe est une horloge en millisecondes, la valeur de retour est 1000.</span><span class="sxs-lookup"><span data-stu-id="2c42e-259">If the external clock is a millisecond clock, the return value is 1000.</span></span> <span data-ttu-id="2c42e-260">Si la valeur de retour est 0, aucune horloge n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2c42e-260">If the return value is 0, no clock is supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-261">clv</span><span class="sxs-lookup"><span data-stu-id="2c42e-261">clv</span></span></td>
<td><span data-ttu-id="2c42e-262">Lorsqu’il est combiné à d’autres éléments, cet indicateur spécifie que les informations de retour s’appliquent au format CLV videodiscs.</span><span class="sxs-lookup"><span data-stu-id="2c42e-262">When combined with other items, this flag specifies that the return information applies to CLV format videodiscs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-263">appareil composé</span><span class="sxs-lookup"><span data-stu-id="2c42e-263">compound device</span></span></td>
<td><span data-ttu-id="2c42e-264">Retourne la <strong>valeur true</strong> si l’appareil prend en charge un nom d’élément (fileName).</span><span class="sxs-lookup"><span data-stu-id="2c42e-264">Returns <strong>TRUE</strong> if the device supports an element name (filename).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-265">type de périphérique</span><span class="sxs-lookup"><span data-stu-id="2c42e-265">device type</span></span></td>
<td><span data-ttu-id="2c42e-266">Retourne un nom de type d’appareil, qui peut être l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2c42e-266">Returns a device type name, which can be one of the following:</span></span>
<ul>
<li><span data-ttu-id="2c42e-267">cdaudio</span><span class="sxs-lookup"><span data-stu-id="2c42e-267">cdaudio</span></span></li>
<li><span data-ttu-id="2c42e-268">anciens</span><span class="sxs-lookup"><span data-stu-id="2c42e-268">dat</span></span></li>
<li><span data-ttu-id="2c42e-269">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="2c42e-269">digitalvideo</span></span></li>
<li><span data-ttu-id="2c42e-270">autre</span><span class="sxs-lookup"><span data-stu-id="2c42e-270">other</span></span></li>
<li><span data-ttu-id="2c42e-271">superposition</span><span class="sxs-lookup"><span data-stu-id="2c42e-271">overlay</span></span></li>
<li><span data-ttu-id="2c42e-272">scanneur</span><span class="sxs-lookup"><span data-stu-id="2c42e-272">scanner</span></span></li>
<li><span data-ttu-id="2c42e-273">sequencer</span><span class="sxs-lookup"><span data-stu-id="2c42e-273">sequencer</span></span></li>
<li><span data-ttu-id="2c42e-274">vidéo</span><span class="sxs-lookup"><span data-stu-id="2c42e-274">vcr</span></span></li>
<li><span data-ttu-id="2c42e-275">videodisc</span><span class="sxs-lookup"><span data-stu-id="2c42e-275">videodisc</span></span></li>
<li><span data-ttu-id="2c42e-276">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="2c42e-276">waveaudio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-277">Vitesse de lecture rapide</span><span class="sxs-lookup"><span data-stu-id="2c42e-277">fast play rate</span></span></td>
<td><span data-ttu-id="2c42e-278">Retourne le taux de lecture rapide en images par seconde, ou zéro si l’appareil ne peut pas être lu rapidement.</span><span class="sxs-lookup"><span data-stu-id="2c42e-278">Returns the fast play rate in frames per second, or zero if the device cannot play fast.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-279">a de l’audio</span><span class="sxs-lookup"><span data-stu-id="2c42e-279">has audio</span></span></td>
<td><span data-ttu-id="2c42e-280">Retourne la <strong>valeur true</strong> si l’appareil prend en charge la lecture audio.</span><span class="sxs-lookup"><span data-stu-id="2c42e-280">Returns <strong>TRUE</strong> if the device supports audio playback.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-281">a une horloge</span><span class="sxs-lookup"><span data-stu-id="2c42e-281">has clock</span></span></td>
<td><span data-ttu-id="2c42e-282">Retourne la <strong>valeur true</strong> si l’appareil a une horloge.</span><span class="sxs-lookup"><span data-stu-id="2c42e-282">Returns <strong>TRUE</strong> if the device has a clock.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-283">a toujours</span><span class="sxs-lookup"><span data-stu-id="2c42e-283">has still</span></span></td>
<td><span data-ttu-id="2c42e-284">Retourne la <strong>valeur true</strong> si l’appareil traite les fichiers avec une seule image plus efficacement que les fichiers vidéo animés.</span><span class="sxs-lookup"><span data-stu-id="2c42e-284">Returns <strong>TRUE</strong> if the device treats files with a single image more efficiently than motion video files.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-285">a un code temporel</span><span class="sxs-lookup"><span data-stu-id="2c42e-285">has timecode</span></span></td>
<td><span data-ttu-id="2c42e-286">Retourne la <strong>valeur true</strong> si l’appareil est en capacité de prendre en charge le code temporel, ou s’il est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2c42e-286">Returns <strong>TRUE</strong> if the device is capable of supporting timecode, or if it is unknown.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-287">a une vidéo</span><span class="sxs-lookup"><span data-stu-id="2c42e-287">has video</span></span></td>
<td><span data-ttu-id="2c42e-288">Retourne la <strong>valeur true</strong> si l’appareil prend en charge la vidéo.</span><span class="sxs-lookup"><span data-stu-id="2c42e-288">Returns <strong>TRUE</strong> if the device supports video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-289">inputs</span><span class="sxs-lookup"><span data-stu-id="2c42e-289">inputs</span></span></td>
<td><span data-ttu-id="2c42e-290">Retourne le nombre total de périphériques d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2c42e-290">Returns the total number of input devices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-291">taux de lecture maximal</span><span class="sxs-lookup"><span data-stu-id="2c42e-291">maximum play rate</span></span></td>
<td><span data-ttu-id="2c42e-292">Retourne la vitesse de lecture maximale, en images par seconde, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2c42e-292">Returns the maximum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-293">Vitesse de lecture minimale</span><span class="sxs-lookup"><span data-stu-id="2c42e-293">minimum play rate</span></span></td>
<td><span data-ttu-id="2c42e-294">Retourne la vitesse de lecture minimale, en images par seconde, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2c42e-294">Returns the minimum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-295">taux de lecture normal</span><span class="sxs-lookup"><span data-stu-id="2c42e-295">normal play rate</span></span></td>
<td><span data-ttu-id="2c42e-296">Retourne la vitesse de lecture normale, en images par seconde, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2c42e-296">Returns the normal play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-297">nombre de marques</span><span class="sxs-lookup"><span data-stu-id="2c42e-297">number of marks</span></span></td>
<td><span data-ttu-id="2c42e-298">Retourne le nombre maximal de marques qui peuvent être utilisées ; la valeur zéro indique que les marques ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2c42e-298">Returns the maximum number of marks that can be used; zero indicates that marks are unsupported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-299">outputs</span><span class="sxs-lookup"><span data-stu-id="2c42e-299">outputs</span></span></td>
<td><span data-ttu-id="2c42e-300">Retourne le nombre total de périphériques de sortie.</span><span class="sxs-lookup"><span data-stu-id="2c42e-300">Returns the total number of output devices.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-301">précision de la recherche</span><span class="sxs-lookup"><span data-stu-id="2c42e-301">seek accuracy</span></span></td>
<td><span data-ttu-id="2c42e-302">Retourne la précision attendue d’une recherche dans les frames ; 0 indique que l’appareil est correct, 1 indique que l’appareil s’attend à se trouver dans une trame de la position de recherche indiquée, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="2c42e-302">Returns the expected accuracy of a search in frames; 0 indicates that the device is frame accurate, 1 indicates that the device expects to be within one frame of the indicated seek position, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-303">taux de lecture lent</span><span class="sxs-lookup"><span data-stu-id="2c42e-303">slow play rate</span></span></td>
<td><span data-ttu-id="2c42e-304">Retourne le taux de lecture lent en images par seconde, ou zéro si l’appareil ne peut pas fonctionner lentement.</span><span class="sxs-lookup"><span data-stu-id="2c42e-304">Returns the slow play rate in frames per second, or zero if the device cannot play slowly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-305">utilise des fichiers</span><span class="sxs-lookup"><span data-stu-id="2c42e-305">uses files</span></span></td>
<td><span data-ttu-id="2c42e-306">Retourne la <strong>valeur true</strong> si le stockage de données utilisé par un périphérique composé est un fichier.</span><span class="sxs-lookup"><span data-stu-id="2c42e-306">Returns <strong>TRUE</strong> if the data storage used by a compound device is a file.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c42e-307">utilise des palettes</span><span class="sxs-lookup"><span data-stu-id="2c42e-307">uses palettes</span></span></td>
<td><span data-ttu-id="2c42e-308">Retourne la <strong>valeur true</strong> si l’appareil utilise des palettes.</span><span class="sxs-lookup"><span data-stu-id="2c42e-308">Returns <strong>TRUE</strong> if the device uses palettes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c42e-309">windows</span><span class="sxs-lookup"><span data-stu-id="2c42e-309">windows</span></span></td>
<td><span data-ttu-id="2c42e-310">Retourne le nombre de fenêtres d’affichage simultanées que l’appareil peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="2c42e-310">Returns the number of simultaneous display windows the device can support.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="2c42e-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="2c42e-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2c42e-312">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="2c42e-312">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="2c42e-313">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="2c42e-313">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="2c42e-314">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2c42e-314">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c42e-315">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2c42e-315">Return Value</span></span>

<span data-ttu-id="2c42e-316">Retourne des informations dans le paramètre *lpszReturnString* de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2c42e-316">Returns information in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="2c42e-317">Les informations dépendent du type de demande.</span><span class="sxs-lookup"><span data-stu-id="2c42e-317">The information is dependent on the request type.</span></span>

## <a name="examples"></a><span data-ttu-id="2c42e-318">Exemples</span><span class="sxs-lookup"><span data-stu-id="2c42e-318">Examples</span></span>

<span data-ttu-id="2c42e-319">La commande suivante retourne le type de périphérique de l’appareil « mySound ».</span><span class="sxs-lookup"><span data-stu-id="2c42e-319">The following command returns the device type of the "mysound" device.</span></span>

``` syntax
capability mysound device type
```

## <a name="requirements"></a><span data-ttu-id="2c42e-320">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c42e-320">Requirements</span></span>



| <span data-ttu-id="2c42e-321">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c42e-321">Requirement</span></span> | <span data-ttu-id="2c42e-322">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c42e-322">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2c42e-323">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c42e-323">Minimum supported client</span></span><br/> | <span data-ttu-id="2c42e-324">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c42e-324">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2c42e-325">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c42e-325">Minimum supported server</span></span><br/> | <span data-ttu-id="2c42e-326">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c42e-326">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2c42e-327">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c42e-327">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c42e-328">MCI</span><span class="sxs-lookup"><span data-stu-id="2c42e-328">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2c42e-329">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="2c42e-329">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="2c42e-330">signal</span><span class="sxs-lookup"><span data-stu-id="2c42e-330">cue</span></span>](cue.md)
</dt> </dl>

 


---
title: commande Set
description: La commande Set établit les paramètres de contrôle de l’appareil. Les périphériques CD audio, numérique-vidéo, MIDI Sequencer, VCR, videodisc, vidéo-overlay et Waveform-Audio reconnaissent cette commande.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- commande Set Windows Multimedia
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/12/2021
ms.locfileid: "106531234"
---
# <a name="set-command"></a><span data-ttu-id="6eae8-105">commande Set</span><span class="sxs-lookup"><span data-stu-id="6eae8-105">set command</span></span>

> [!NOTE]
> <span data-ttu-id="6eae8-106">Communication sans biais Microsoft prend en charge un environnement diversifié et un environnement d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="6eae8-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="6eae8-107">Dans ce document, il existe des références au mot « esclave ».</span><span class="sxs-lookup"><span data-stu-id="6eae8-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="6eae8-108">Le [Guide de style de Microsoft pour les Communications Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconnaît cela comme un mot d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="6eae8-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="6eae8-109">Ce libellé est utilisé, car il s’agit actuellement de la formulation utilisée dans les commandes.</span><span class="sxs-lookup"><span data-stu-id="6eae8-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="6eae8-110">Pour des fins de cohérence, ce document contient ce mot.</span><span class="sxs-lookup"><span data-stu-id="6eae8-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="6eae8-111">Lorsque ce mot est modifié dans les commandes, nous allons corriger ce document pour qu’il soit aligné.</span><span class="sxs-lookup"><span data-stu-id="6eae8-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>


<span data-ttu-id="6eae8-112">La commande Set établit les paramètres de contrôle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6eae8-112">The set command establishes control settings for the device.</span></span> <span data-ttu-id="6eae8-113">Les périphériques CD audio, numérique-vidéo, MIDI Sequencer, VCR, videodisc, vidéo-overlay et Waveform-Audio reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="6eae8-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="6eae8-114">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="6eae8-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="6eae8-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6eae8-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eae8-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6eae8-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6eae8-117">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="6eae8-117">Identifier of an MCI device.</span></span> <span data-ttu-id="6eae8-118">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6eae8-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6eae8-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span><span class="sxs-lookup"><span data-stu-id="6eae8-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span></span>
</dt> <dd>

<span data-ttu-id="6eae8-120">Indicateur pour l’établissement des paramètres de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6eae8-120">Flag for establishing control settings.</span></span> <span data-ttu-id="6eae8-121">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Set** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="6eae8-121">The following table lists device types that recognize the **set** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6eae8-122">Type d’appareil</span><span class="sxs-lookup"><span data-stu-id="6eae8-122">Device Type</span></span></th>
<th><span data-ttu-id="6eae8-123">Indicateurs de commande</span><span class="sxs-lookup"><span data-stu-id="6eae8-123">Command Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6eae8-124">cdaudio</span><span class="sxs-lookup"><span data-stu-id="6eae8-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="6eae8-125">tout audio désactivé</span><span class="sxs-lookup"><span data-stu-id="6eae8-125">audio all off</span></span></li>
<li><span data-ttu-id="6eae8-126">tout son sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-126">audio all on</span></span></li>
<li><span data-ttu-id="6eae8-127">audio quitté</span><span class="sxs-lookup"><span data-stu-id="6eae8-127">audio left off</span></span></li>
<li><span data-ttu-id="6eae8-128">audio restant activé</span><span class="sxs-lookup"><span data-stu-id="6eae8-128">audio left on</span></span></li>
<li><span data-ttu-id="6eae8-129">audio immédiatement éteint</span><span class="sxs-lookup"><span data-stu-id="6eae8-129">audio right off</span></span></li>
<li><span data-ttu-id="6eae8-130">contenu audio</span><span class="sxs-lookup"><span data-stu-id="6eae8-130">audio right on</span></span></li>
<li><span data-ttu-id="6eae8-131">porte fermée</span><span class="sxs-lookup"><span data-stu-id="6eae8-131">door closed</span></span></li>
<li><span data-ttu-id="6eae8-132">porte ouverte</span><span class="sxs-lookup"><span data-stu-id="6eae8-132">door open</span></span></li>
<li><span data-ttu-id="6eae8-133">format d’heure en millisecondes</span><span class="sxs-lookup"><span data-stu-id="6eae8-133">time format milliseconds</span></span></li>
<li><span data-ttu-id="6eae8-134">format d’heure MSF</span><span class="sxs-lookup"><span data-stu-id="6eae8-134">time format msf</span></span></li>
<li><span data-ttu-id="6eae8-135">format d’heure TMSF</span><span class="sxs-lookup"><span data-stu-id="6eae8-135">time format tmsf</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-136">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="6eae8-136">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="6eae8-137">tout audio désactivé</span><span class="sxs-lookup"><span data-stu-id="6eae8-137">audio all off</span></span></li>
<li><span data-ttu-id="6eae8-138">tout son sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-138">audio all on</span></span></li>
<li><span data-ttu-id="6eae8-139">audio quitté</span><span class="sxs-lookup"><span data-stu-id="6eae8-139">audio left off</span></span></li>
<li><span data-ttu-id="6eae8-140">audio restant activé</span><span class="sxs-lookup"><span data-stu-id="6eae8-140">audio left on</span></span></li>
<li><span data-ttu-id="6eae8-141">audio immédiatement éteint</span><span class="sxs-lookup"><span data-stu-id="6eae8-141">audio right off</span></span></li>
<li><span data-ttu-id="6eae8-142">contenu audio</span><span class="sxs-lookup"><span data-stu-id="6eae8-142">audio right on</span></span></li>
<li><span data-ttu-id="6eae8-143">porte fermée</span><span class="sxs-lookup"><span data-stu-id="6eae8-143">door closed</span></span></li>
<li><span data-ttu-id="6eae8-144">porte ouverte</span><span class="sxs-lookup"><span data-stu-id="6eae8-144">door open</span></span></li>
<li><span data-ttu-id="6eae8-145"><em>format</em> de format de fichier</span><span class="sxs-lookup"><span data-stu-id="6eae8-145">file format <em>format</em></span></span></li>
<li><span data-ttu-id="6eae8-146">recherche exacte</span><span class="sxs-lookup"><span data-stu-id="6eae8-146">seek exactly on</span></span></li>
<li><span data-ttu-id="6eae8-147">recherche exacte</span><span class="sxs-lookup"><span data-stu-id="6eae8-147">seek exactly off</span></span></li>
<li><span data-ttu-id="6eae8-148"><em>facteur</em> de vitesse</span><span class="sxs-lookup"><span data-stu-id="6eae8-148">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="6eae8-149"><em>format</em> de format de fichier toujours</span><span class="sxs-lookup"><span data-stu-id="6eae8-149">still file format <em>format</em></span></span></li>
<li><span data-ttu-id="6eae8-150">frames de format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-150">time format frames</span></span></li>
<li><span data-ttu-id="6eae8-151">format d’heure en millisecondes</span><span class="sxs-lookup"><span data-stu-id="6eae8-151">time format milliseconds</span></span></li>
<li><span data-ttu-id="6eae8-152">vidéo désactivée</span><span class="sxs-lookup"><span data-stu-id="6eae8-152">video off</span></span></li>
<li><span data-ttu-id="6eae8-153">vidéo sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-153">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-154">superposition</span><span class="sxs-lookup"><span data-stu-id="6eae8-154">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="6eae8-155">tout audio désactivé</span><span class="sxs-lookup"><span data-stu-id="6eae8-155">audio all off</span></span></li>
<li><span data-ttu-id="6eae8-156">tout son sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-156">audio all on</span></span></li>
<li><span data-ttu-id="6eae8-157">audio quitté</span><span class="sxs-lookup"><span data-stu-id="6eae8-157">audio left off</span></span></li>
<li><span data-ttu-id="6eae8-158">audio restant activé</span><span class="sxs-lookup"><span data-stu-id="6eae8-158">audio left on</span></span></li>
<li><span data-ttu-id="6eae8-159">audio immédiatement éteint</span><span class="sxs-lookup"><span data-stu-id="6eae8-159">audio right off</span></span></li>
<li><span data-ttu-id="6eae8-160">contenu audio</span><span class="sxs-lookup"><span data-stu-id="6eae8-160">audio right on</span></span></li>
<li><span data-ttu-id="6eae8-161">porte fermée</span><span class="sxs-lookup"><span data-stu-id="6eae8-161">door closed</span></span></li>
<li><span data-ttu-id="6eae8-162">porte ouverte</span><span class="sxs-lookup"><span data-stu-id="6eae8-162">door open</span></span></li>
<li><span data-ttu-id="6eae8-163">vidéo désactivée</span><span class="sxs-lookup"><span data-stu-id="6eae8-163">video off</span></span></li>
<li><span data-ttu-id="6eae8-164">vidéo sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-164">video on</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-165">sequencer</span><span class="sxs-lookup"><span data-stu-id="6eae8-165">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="6eae8-166">tout audio désactivé</span><span class="sxs-lookup"><span data-stu-id="6eae8-166">audio all off</span></span></li>
<li><span data-ttu-id="6eae8-167">tout son sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-167">audio all on</span></span></li>
<li><span data-ttu-id="6eae8-168">audio quitté</span><span class="sxs-lookup"><span data-stu-id="6eae8-168">audio left off</span></span></li>
<li><span data-ttu-id="6eae8-169">audio restant activé</span><span class="sxs-lookup"><span data-stu-id="6eae8-169">audio left on</span></span></li>
<li><span data-ttu-id="6eae8-170">audio immédiatement éteint</span><span class="sxs-lookup"><span data-stu-id="6eae8-170">audio right off</span></span></li>
<li><span data-ttu-id="6eae8-171">contenu audio</span><span class="sxs-lookup"><span data-stu-id="6eae8-171">audio right on</span></span></li>
<li><span data-ttu-id="6eae8-172">porte fermée</span><span class="sxs-lookup"><span data-stu-id="6eae8-172">door closed</span></span></li>
<li><span data-ttu-id="6eae8-173">porte ouverte</span><span class="sxs-lookup"><span data-stu-id="6eae8-173">door open</span></span></li>
<li><span data-ttu-id="6eae8-174">MIDI maître</span><span class="sxs-lookup"><span data-stu-id="6eae8-174">master MIDI</span></span></li>
<li><span data-ttu-id="6eae8-175">maître aucun</span><span class="sxs-lookup"><span data-stu-id="6eae8-175">master none</span></span></li>
<li><span data-ttu-id="6eae8-176">SMPTE maître</span><span class="sxs-lookup"><span data-stu-id="6eae8-176">master SMPTE</span></span></li>
<li><span data-ttu-id="6eae8-177"><em>heure</em> du décalage</span><span class="sxs-lookup"><span data-stu-id="6eae8-177">offset <em>time</em></span></span></li>
<li><span data-ttu-id="6eae8-178">mappeur de port</span><span class="sxs-lookup"><span data-stu-id="6eae8-178">port mapper</span></span></li>
<li><span data-ttu-id="6eae8-179">port aucun</span><span class="sxs-lookup"><span data-stu-id="6eae8-179">port none</span></span></li>
<li><span data-ttu-id="6eae8-180"><em>port_number</em> de port</span><span class="sxs-lookup"><span data-stu-id="6eae8-180">port <em>port_number</em></span></span></li>
<li><span data-ttu-id="6eae8-181">fichier esclave</span><span class="sxs-lookup"><span data-stu-id="6eae8-181">slave file</span></span></li>
<li><span data-ttu-id="6eae8-182">MIDI esclave</span><span class="sxs-lookup"><span data-stu-id="6eae8-182">slave MIDI</span></span></li>
<li><span data-ttu-id="6eae8-183">esclave aucun</span><span class="sxs-lookup"><span data-stu-id="6eae8-183">slave none</span></span></li>
<li><span data-ttu-id="6eae8-184">SMPTE esclave</span><span class="sxs-lookup"><span data-stu-id="6eae8-184">slave SMPTE</span></span></li>
<li><span data-ttu-id="6eae8-185">tempo <em>tempo_value</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-185">tempo <em>tempo_value</em></span></span></li>
<li><span data-ttu-id="6eae8-186">format d’heure en millisecondes</span><span class="sxs-lookup"><span data-stu-id="6eae8-186">time format milliseconds</span></span></li>
<li><span data-ttu-id="6eae8-187">format d’heure SMPTE <em>fps</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-187">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="6eae8-188">suppression du format d’heure SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="6eae8-188">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="6eae8-189">pointeur de chanson au format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-189">time format song pointer</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-190"><strong>vidéo</strong></span><span class="sxs-lookup"><span data-stu-id="6eae8-190"><strong>vcr</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="6eae8-191">enregistrement d’assemblage activé</span><span class="sxs-lookup"><span data-stu-id="6eae8-191">assemble record on</span></span></li>
<li><span data-ttu-id="6eae8-192">réassembler l’enregistrement désactivé</span><span class="sxs-lookup"><span data-stu-id="6eae8-192">assemble record off</span></span></li>
<li><span data-ttu-id="6eae8-193">tout audio désactivé</span><span class="sxs-lookup"><span data-stu-id="6eae8-193">audio all off</span></span></li>
<li><span data-ttu-id="6eae8-194">tout son sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-194">audio all on</span></span></li>
<li><span data-ttu-id="6eae8-195">audio quitté</span><span class="sxs-lookup"><span data-stu-id="6eae8-195">audio left off</span></span></li>
<li><span data-ttu-id="6eae8-196">audio restant activé</span><span class="sxs-lookup"><span data-stu-id="6eae8-196">audio left on</span></span></li>
<li><span data-ttu-id="6eae8-197">audio immédiatement éteint</span><span class="sxs-lookup"><span data-stu-id="6eae8-197">audio right off</span></span></li>
<li><span data-ttu-id="6eae8-198">contenu audio</span><span class="sxs-lookup"><span data-stu-id="6eae8-198">audio right on</span></span></li>
<li><span data-ttu-id="6eae8-199"><em>heure</em> de l’horloge</span><span class="sxs-lookup"><span data-stu-id="6eae8-199">clock <em>time</em></span></span></li>
<li><span data-ttu-id="6eae8-200">format du compteur</span><span class="sxs-lookup"><span data-stu-id="6eae8-200">counter format</span></span></li>
<li><span data-ttu-id="6eae8-201"><em>valeur</em> de compteur</span><span class="sxs-lookup"><span data-stu-id="6eae8-201">counter <em>value</em></span></span></li>
<li><span data-ttu-id="6eae8-202">porte fermée</span><span class="sxs-lookup"><span data-stu-id="6eae8-202">door closed</span></span></li>
<li><span data-ttu-id="6eae8-203">porte ouverte</span><span class="sxs-lookup"><span data-stu-id="6eae8-203">door open</span></span></li>
<li><span data-ttu-id="6eae8-204">compteur d’index</span><span class="sxs-lookup"><span data-stu-id="6eae8-204">index counter</span></span></li>
<li><span data-ttu-id="6eae8-205">Date d’index</span><span class="sxs-lookup"><span data-stu-id="6eae8-205">index date</span></span></li>
<li><span data-ttu-id="6eae8-206">heure de l’index</span><span class="sxs-lookup"><span data-stu-id="6eae8-206">index time</span></span></li>
<li><span data-ttu-id="6eae8-207">heure de l’index</span><span class="sxs-lookup"><span data-stu-id="6eae8-207">index time</span></span></li>
<li><span data-ttu-id="6eae8-208"><em>durée</em> de CodeLength</span><span class="sxs-lookup"><span data-stu-id="6eae8-208">codelength <em>duration</em></span></span></li>
<li><span data-ttu-id="6eae8-209"><em>délai d’attente</em> de pause</span><span class="sxs-lookup"><span data-stu-id="6eae8-209">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="6eae8-210">durée de Postroll-</span><span class="sxs-lookup"><span data-stu-id="6eae8-210">postroll duration -</span></span></li>
<li><span data-ttu-id="6eae8-211"><em>duration</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-211"><em>duration</em></span></span></li>
<li><span data-ttu-id="6eae8-212">Sous tension</span><span class="sxs-lookup"><span data-stu-id="6eae8-212">power on</span></span></li>
<li><span data-ttu-id="6eae8-213">mettre hors tension</span><span class="sxs-lookup"><span data-stu-id="6eae8-213">power off</span></span></li>
<li><span data-ttu-id="6eae8-214"><em>durée</em> du préroll</span><span class="sxs-lookup"><span data-stu-id="6eae8-214">preroll duration <em>duration</em></span></span></li>
<li><span data-ttu-id="6eae8-215">format d’enregistrement SP</span><span class="sxs-lookup"><span data-stu-id="6eae8-215">record format SP</span></span></li>
<li><span data-ttu-id="6eae8-216">format d’enregistrement LP</span><span class="sxs-lookup"><span data-stu-id="6eae8-216">record format LP</span></span></li>
<li><span data-ttu-id="6eae8-217">format d’enregistrement EP</span><span class="sxs-lookup"><span data-stu-id="6eae8-217">record format EP</span></span></li>
<li><span data-ttu-id="6eae8-218"><em>facteur</em> de vitesse</span><span class="sxs-lookup"><span data-stu-id="6eae8-218">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="6eae8-219">frames de format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-219">time format frames</span></span></li>
<li><span data-ttu-id="6eae8-220">format d’heure HMS</span><span class="sxs-lookup"><span data-stu-id="6eae8-220">time format hms</span></span></li>
<li><span data-ttu-id="6eae8-221">format d’heure en millisecondes</span><span class="sxs-lookup"><span data-stu-id="6eae8-221">time format milliseconds</span></span></li>
<li><span data-ttu-id="6eae8-222">format d’heure MSF</span><span class="sxs-lookup"><span data-stu-id="6eae8-222">time format msf</span></span></li>
<li><span data-ttu-id="6eae8-223">format d’heure SMPTE <em>fps</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-223">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="6eae8-224">suppression du format d’heure SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="6eae8-224">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="6eae8-225">format d’heure TMSF</span><span class="sxs-lookup"><span data-stu-id="6eae8-225">time format tmsf</span></span></li>
<li><span data-ttu-id="6eae8-226">compteur du mode temps</span><span class="sxs-lookup"><span data-stu-id="6eae8-226">time mode counter</span></span></li>
<li><span data-ttu-id="6eae8-227">détection du mode de temps</span><span class="sxs-lookup"><span data-stu-id="6eae8-227">time mode detect</span></span></li>
<li><span data-ttu-id="6eae8-228">code temporel du mode Time</span><span class="sxs-lookup"><span data-stu-id="6eae8-228">time mode timecode</span></span></li>
<li><span data-ttu-id="6eae8-229">suivi plus</span><span class="sxs-lookup"><span data-stu-id="6eae8-229">tracking plus</span></span></li>
<li><span data-ttu-id="6eae8-230">suivi moins</span><span class="sxs-lookup"><span data-stu-id="6eae8-230">tracking minus</span></span></li>
<li><span data-ttu-id="6eae8-231">réinitialisation du suivi</span><span class="sxs-lookup"><span data-stu-id="6eae8-231">tracking reset</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-232">videodisc</span><span class="sxs-lookup"><span data-stu-id="6eae8-232">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="6eae8-233">tout audio désactivé</span><span class="sxs-lookup"><span data-stu-id="6eae8-233">audio all off</span></span></li>
<li><span data-ttu-id="6eae8-234">tout son sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-234">audio all on</span></span></li>
<li><span data-ttu-id="6eae8-235">audio quitté</span><span class="sxs-lookup"><span data-stu-id="6eae8-235">audio left off</span></span></li>
<li><span data-ttu-id="6eae8-236">audio restant activé</span><span class="sxs-lookup"><span data-stu-id="6eae8-236">audio left on</span></span></li>
<li><span data-ttu-id="6eae8-237">audio immédiatement éteint</span><span class="sxs-lookup"><span data-stu-id="6eae8-237">audio right off</span></span></li>
<li><span data-ttu-id="6eae8-238">contenu audio</span><span class="sxs-lookup"><span data-stu-id="6eae8-238">audio right on</span></span></li>
<li><span data-ttu-id="6eae8-239">porte fermée</span><span class="sxs-lookup"><span data-stu-id="6eae8-239">door closed</span></span></li>
<li><span data-ttu-id="6eae8-240">porte ouverte</span><span class="sxs-lookup"><span data-stu-id="6eae8-240">door open</span></span></li>
<li><span data-ttu-id="6eae8-241">frames de format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-241">time format frames</span></span></li>
<li><span data-ttu-id="6eae8-242">format d’heure HMS</span><span class="sxs-lookup"><span data-stu-id="6eae8-242">time format hms</span></span></li>
<li><span data-ttu-id="6eae8-243">format d’heure en millisecondes</span><span class="sxs-lookup"><span data-stu-id="6eae8-243">time format milliseconds</span></span></li>
<li><span data-ttu-id="6eae8-244">suivi du format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-244">time format track</span></span></li>
<li><span data-ttu-id="6eae8-245">vidéo désactivée</span><span class="sxs-lookup"><span data-stu-id="6eae8-245">video off</span></span></li>
<li><span data-ttu-id="6eae8-246">vidéo sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-246">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-247">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="6eae8-247">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="6eae8-248"><em>entier</em> d’alignement</span><span class="sxs-lookup"><span data-stu-id="6eae8-248">alignment <em>integer</em></span></span></li>
<li><span data-ttu-id="6eae8-249">toute entrée</span><span class="sxs-lookup"><span data-stu-id="6eae8-249">any input</span></span></li>
<li><span data-ttu-id="6eae8-250">toute sortie</span><span class="sxs-lookup"><span data-stu-id="6eae8-250">any output</span></span></li>
<li><span data-ttu-id="6eae8-251">tout audio désactivé</span><span class="sxs-lookup"><span data-stu-id="6eae8-251">audio all off</span></span></li>
<li><span data-ttu-id="6eae8-252">tout son sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-252">audio all on</span></span></li>
<li><span data-ttu-id="6eae8-253">audio quitté</span><span class="sxs-lookup"><span data-stu-id="6eae8-253">audio left off</span></span></li>
<li><span data-ttu-id="6eae8-254">audio restant activé</span><span class="sxs-lookup"><span data-stu-id="6eae8-254">audio left on</span></span></li>
<li><span data-ttu-id="6eae8-255">audio immédiatement éteint</span><span class="sxs-lookup"><span data-stu-id="6eae8-255">audio right off</span></span></li>
<li><span data-ttu-id="6eae8-256">contenu audio</span><span class="sxs-lookup"><span data-stu-id="6eae8-256">audio right on</span></span></li>
<li><span data-ttu-id="6eae8-257">BitsPerSample <em>BIT_COUNT</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-257">bitspersample <em>bit_count</em></span></span></li>
<li><span data-ttu-id="6eae8-258">bytespersec <em>byte_rate</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-258">bytespersec <em>byte_rate</em></span></span></li>
<li><span data-ttu-id="6eae8-259">canaux <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-259">channels <em>channel_count</em></span></span></li>
<li><span data-ttu-id="6eae8-260">porte fermée</span><span class="sxs-lookup"><span data-stu-id="6eae8-260">door closed</span></span></li>
<li><span data-ttu-id="6eae8-261">porte ouverte</span><span class="sxs-lookup"><span data-stu-id="6eae8-261">door open</span></span></li>
<li><span data-ttu-id="6eae8-262">format de balise PCM</span><span class="sxs-lookup"><span data-stu-id="6eae8-262">format tag pcm</span></span></li>
<li><span data-ttu-id="6eae8-263"><em>balise</em> de format tag</span><span class="sxs-lookup"><span data-stu-id="6eae8-263">format tag <em>tag</em></span></span></li>
<li><span data-ttu-id="6eae8-264"><em>entier</em> d’entrée</span><span class="sxs-lookup"><span data-stu-id="6eae8-264">input <em>integer</em></span></span></li>
<li><span data-ttu-id="6eae8-265"><em>entier</em> de sortie</span><span class="sxs-lookup"><span data-stu-id="6eae8-265">output <em>integer</em></span></span></li>
<li><span data-ttu-id="6eae8-266"><em>entier</em> SamplesPerSec</span><span class="sxs-lookup"><span data-stu-id="6eae8-266">samplespersec <em>integer</em></span></span></li>
<li><span data-ttu-id="6eae8-267">octets de format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-267">time format bytes</span></span></li>
<li><span data-ttu-id="6eae8-268">format d’heure en millisecondes</span><span class="sxs-lookup"><span data-stu-id="6eae8-268">time format milliseconds</span></span></li>
<li><span data-ttu-id="6eae8-269">exemples de format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-269">time format samples</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6eae8-270">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszSetting** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="6eae8-270">The following table lists the flags that can be specified in the **lpszSetting** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6eae8-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="6eae8-271">Value</span></span></th>
<th><span data-ttu-id="6eae8-272">Signification</span><span class="sxs-lookup"><span data-stu-id="6eae8-272">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6eae8-273"><em>entier</em> d’alignement</span><span class="sxs-lookup"><span data-stu-id="6eae8-273">alignment <em>integer</em></span></span></td>
<td><span data-ttu-id="6eae8-274">Définit l’alignement des blocs de données par rapport au début des données transmises au périphérique Wave-audio.</span><span class="sxs-lookup"><span data-stu-id="6eae8-274">Sets the alignment of data blocks relative to the start of data passed to the waveform-audio device.</span></span> <span data-ttu-id="6eae8-275">Le fichier est enregistré dans ce format.</span><span class="sxs-lookup"><span data-stu-id="6eae8-275">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-276">toute entrée</span><span class="sxs-lookup"><span data-stu-id="6eae8-276">any input</span></span></td>
<td><span data-ttu-id="6eae8-277">Utilise toute entrée qui prend en charge le format actuel lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eae8-277">Use any input that supports the current format when recording.</span></span> <span data-ttu-id="6eae8-278">Il s'agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="6eae8-278">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-279">toute sortie</span><span class="sxs-lookup"><span data-stu-id="6eae8-279">any output</span></span></td>
<td><span data-ttu-id="6eae8-280">Utilise une sortie qui prend en charge le format actuel lors de la diffusion.</span><span class="sxs-lookup"><span data-stu-id="6eae8-280">Use any output that supports the current format when playing.</span></span> <span data-ttu-id="6eae8-281">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="6eae8-281">This is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-282">enregistrement d’assemblage activé</span><span class="sxs-lookup"><span data-stu-id="6eae8-282">assemble record on</span></span> <br/> <span data-ttu-id="6eae8-283">réassembler l’enregistrement désactivé</span><span class="sxs-lookup"><span data-stu-id="6eae8-283">assemble record off</span></span> <br/></td>
<td><span data-ttu-id="6eae8-284">En mode assembler, toutes les pistes sont enregistrées comme défini par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6eae8-284">In assemble mode, all tracks are recorded as defined by the device.</span></span> <span data-ttu-id="6eae8-285">La plupart des magnétoscopes sont en mode assemblage par défaut.</span><span class="sxs-lookup"><span data-stu-id="6eae8-285">Most VCRs are in assemble mode by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-286">tout audio désactivé</span><span class="sxs-lookup"><span data-stu-id="6eae8-286">audio all off</span></span> <br/> <span data-ttu-id="6eae8-287">tout son sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-287">audio all on</span></span> <br/></td>
<td><span data-ttu-id="6eae8-288">Désactive ou active la sortie audio.</span><span class="sxs-lookup"><span data-stu-id="6eae8-288">Disables or enables audio output.</span></span> <span data-ttu-id="6eae8-289">Les périphériques de superposition vidéo, MCISEQ Sequencer et MCIWAVE périphérique audio-audio ne prennent pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eae8-289">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-290">audio quitté</span><span class="sxs-lookup"><span data-stu-id="6eae8-290">audio left off</span></span> <br/> <span data-ttu-id="6eae8-291">audio restant activé</span><span class="sxs-lookup"><span data-stu-id="6eae8-291">audio left on</span></span> <br/> <span data-ttu-id="6eae8-292">audio immédiatement éteint</span><span class="sxs-lookup"><span data-stu-id="6eae8-292">audio right off</span></span> <br/> <span data-ttu-id="6eae8-293">contenu audio</span><span class="sxs-lookup"><span data-stu-id="6eae8-293">audio right on</span></span> <br/></td>
<td><span data-ttu-id="6eae8-294">Désactive ou active la sortie vers le canal audio gauche ou droit.</span><span class="sxs-lookup"><span data-stu-id="6eae8-294">Disables or enables output to either the left or the right audio channel.</span></span> <span data-ttu-id="6eae8-295">Les périphériques de superposition vidéo, MCISEQ Sequencer et MCIWAVE périphérique audio-audio ne prennent pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eae8-295">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-296">BitsPerSample <em>BIT_COUNT</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-296">bitspersample <em>bit_count</em></span></span></td>
<td><span data-ttu-id="6eae8-297">Définit le nombre de bits par échantillon PCM (Pulse Code Modulation) lu ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="6eae8-297">Sets the number of bits per PCM (Pulse Code Modulation) sample played or recorded.</span></span> <span data-ttu-id="6eae8-298">Le fichier est enregistré dans ce format.</span><span class="sxs-lookup"><span data-stu-id="6eae8-298">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-299">bytespersec <em>byte_rate</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-299">bytespersec <em>byte_rate</em></span></span></td>
<td><span data-ttu-id="6eae8-300">Définit le nombre moyen d’octets par seconde lus ou enregistrés.</span><span class="sxs-lookup"><span data-stu-id="6eae8-300">Sets the average number of bytes per second played or recorded.</span></span> <span data-ttu-id="6eae8-301">Le fichier est enregistré dans ce format.</span><span class="sxs-lookup"><span data-stu-id="6eae8-301">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-302">canaux <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-302">channels <em>channel_count</em></span></span></td>
<td><span data-ttu-id="6eae8-303">Définit les canaux pour la diffusion et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eae8-303">Sets the channels for playing and recording.</span></span> <span data-ttu-id="6eae8-304">Le fichier est enregistré dans ce format.</span><span class="sxs-lookup"><span data-stu-id="6eae8-304">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-305"><em>heure</em> de l’horloge</span><span class="sxs-lookup"><span data-stu-id="6eae8-305">clock <em>time</em></span></span></td>
<td><span data-ttu-id="6eae8-306">Définit l’heure de l’horloge externe <em>.</em></span><span class="sxs-lookup"><span data-stu-id="6eae8-306">Sets time on the external clock to <em>time.</em></span></span> <span data-ttu-id="6eae8-307">Le format est spécifié en tant qu’entier long non signé.</span><span class="sxs-lookup"><span data-stu-id="6eae8-307">The format is specified as a long unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-308">format du compteur</span><span class="sxs-lookup"><span data-stu-id="6eae8-308">counter format</span></span></td>
<td><span data-ttu-id="6eae8-309">Définissez le format d’heure du compteur, tel qu’il est retourné par le compteur d' <a href="status.md">État</a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="6eae8-309">Set the time format for the counter, as returned by <a href="status.md">status</a> &quot;counter&quot;.</span></span> <span data-ttu-id="6eae8-310">Pour plus d’informations sur les types applicables, consultez la commande <strong>Set</strong> &quot; Time format &quot; .</span><span class="sxs-lookup"><span data-stu-id="6eae8-310">For information about applicable types, see the <strong>set</strong> &quot;time format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-311"><em>valeur</em> de compteur</span><span class="sxs-lookup"><span data-stu-id="6eae8-311">counter <em>value</em></span></span></td>
<td><span data-ttu-id="6eae8-312">Définit le compteur VCR à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6eae8-312">Sets the VCR counter to the specified value.</span></span> <span data-ttu-id="6eae8-313">La valeur doit être spécifiée dans le format de compteur actuel.</span><span class="sxs-lookup"><span data-stu-id="6eae8-313">The value must be specified in the current counter format.</span></span> <span data-ttu-id="6eae8-314">Pour plus d’informations, consultez la commande <strong>Set</strong> &quot; Counter format &quot; .</span><span class="sxs-lookup"><span data-stu-id="6eae8-314">For more information, see the <strong>set</strong> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-315">porte fermée</span><span class="sxs-lookup"><span data-stu-id="6eae8-315">door closed</span></span></td>
<td><span data-ttu-id="6eae8-316">Retire la barre d’État et ferme la porte, si possible.</span><span class="sxs-lookup"><span data-stu-id="6eae8-316">Retracts the tray and closes the door, if possible.</span></span> <span data-ttu-id="6eae8-317">Pour les magnétoscopes, charge automatiquement la bande.</span><span class="sxs-lookup"><span data-stu-id="6eae8-317">For VCRs, loads the tape automatically.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-318">porte ouverte</span><span class="sxs-lookup"><span data-stu-id="6eae8-318">door open</span></span></td>
<td><span data-ttu-id="6eae8-319">Ouvre la porte et éjecte le plateau ou la bande, si possible.</span><span class="sxs-lookup"><span data-stu-id="6eae8-319">Opens the door and ejects the tray or tape, if possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-320"><em>format</em> de format de fichier</span><span class="sxs-lookup"><span data-stu-id="6eae8-320">file format <em>format</em></span></span></td>
<td><span data-ttu-id="6eae8-321">Spécifie un format de fichier utilisé pour les commandes d' <a href="save.md">enregistrement</a> ou de <a href="capture.md">capture</a> .</span><span class="sxs-lookup"><span data-stu-id="6eae8-321">Specifies a file format that is used for <a href="save.md">save</a> or <a href="capture.md">capture</a> commands.</span></span> <span data-ttu-id="6eae8-322">En cas d’omission, il peut s’agit d’un format défini par défaut pour le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="6eae8-322">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="6eae8-323">Si le format de fichier spécifié est en conflit avec l’algorithme et la qualité actuellement sélectionnés, ils sont remplacés par les valeurs par défaut pour le format de fichier.</span><span class="sxs-lookup"><span data-stu-id="6eae8-323">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="6eae8-324">Les formats de fichier suivants sont définis :</span><span class="sxs-lookup"><span data-stu-id="6eae8-324">The following file formats are defined:</span></span>
<ul>
<li><span data-ttu-id="6eae8-325">AVI : spécifie le format AVI.</span><span class="sxs-lookup"><span data-stu-id="6eae8-325">avi: Specifies AVI format.</span></span></li>
<li><span data-ttu-id="6eae8-326">avss : spécifie le format AVSS.</span><span class="sxs-lookup"><span data-stu-id="6eae8-326">avss: Specifies AVSS format.</span></span></li>
<li><span data-ttu-id="6eae8-327">DIB : spécifie le format DIB.</span><span class="sxs-lookup"><span data-stu-id="6eae8-327">dib: Specifies DIB format.</span></span></li>
<li><span data-ttu-id="6eae8-328">JFIF : spécifie le format JFIF.</span><span class="sxs-lookup"><span data-stu-id="6eae8-328">jfif: Specifies JFIF format.</span></span></li>
<li><span data-ttu-id="6eae8-329">JPEG : spécifie le format JPEG.</span><span class="sxs-lookup"><span data-stu-id="6eae8-329">jpeg: Specifies JPEG format.</span></span></li>
<li><span data-ttu-id="6eae8-330">MPEG : spécifie le format MPEG.</span><span class="sxs-lookup"><span data-stu-id="6eae8-330">mpeg: Specifies MPEG format.</span></span></li>
<li><span data-ttu-id="6eae8-331">RDIB : spécifie le format DIB RLE.</span><span class="sxs-lookup"><span data-stu-id="6eae8-331">rdib: Specifies RLE DIB format.</span></span></li>
<li><span data-ttu-id="6eae8-332">rjpeg : spécifie le format RJPEG.</span><span class="sxs-lookup"><span data-stu-id="6eae8-332">rjpeg: Specifies RJPEG format.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-333">format de balise PCM</span><span class="sxs-lookup"><span data-stu-id="6eae8-333">format tag pcm</span></span></td>
<td><span data-ttu-id="6eae8-334">Définit le type de format PCM pour la diffusion et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eae8-334">Sets the format type to PCM for playing and recording.</span></span> <span data-ttu-id="6eae8-335">Le fichier est enregistré dans ce format.</span><span class="sxs-lookup"><span data-stu-id="6eae8-335">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-336"><em>balise</em> de format tag</span><span class="sxs-lookup"><span data-stu-id="6eae8-336">format tag <em>tag</em></span></span></td>
<td><span data-ttu-id="6eae8-337">Définit le type de format pour la diffusion et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eae8-337">Sets the format type for playing and recording.</span></span> <span data-ttu-id="6eae8-338">Le fichier est enregistré dans ce format.</span><span class="sxs-lookup"><span data-stu-id="6eae8-338">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-339">code temporel de l’index</span><span class="sxs-lookup"><span data-stu-id="6eae8-339">index timecode</span></span> <br/> <span data-ttu-id="6eae8-340">compteur d’index</span><span class="sxs-lookup"><span data-stu-id="6eae8-340">index counter</span></span> <br/> <span data-ttu-id="6eae8-341">Date d’index</span><span class="sxs-lookup"><span data-stu-id="6eae8-341">index date</span></span> <br/> <span data-ttu-id="6eae8-342">heure de l’index</span><span class="sxs-lookup"><span data-stu-id="6eae8-342">index time</span></span> <br/></td>
<td><span data-ttu-id="6eae8-343">Définit l’écran d’affichage actuel sur le magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="6eae8-343">Sets the current display screen on the VCR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-344"><em>entier</em> d’entrée</span><span class="sxs-lookup"><span data-stu-id="6eae8-344">input <em>integer</em></span></span></td>
<td><span data-ttu-id="6eae8-345">Définit le canal audio utilisé comme entrée.</span><span class="sxs-lookup"><span data-stu-id="6eae8-345">Sets the audio channel used as the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-346"><em>durée</em> de la durée</span><span class="sxs-lookup"><span data-stu-id="6eae8-346">length <em>duration</em></span></span></td>
<td><span data-ttu-id="6eae8-347">Définit la longueur spécifiée par l’utilisateur de la bande dans le magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="6eae8-347">Sets the user-specified length of the tape in the VCR.</span></span> <span data-ttu-id="6eae8-348">Cette longueur est retournée par la commande de longueur d' <a href="status.md">État</a> &quot; &quot; et est fournie à des fins de compatibilité avec les applications qui nécessitent cette commande pour retourner une longueur valide.</span><span class="sxs-lookup"><span data-stu-id="6eae8-348">This length is returned by the <a href="status.md">status</a> &quot;length&quot; command and is provided for compatibility with applications that require this command to return a valid length.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-349">midi maître</span><span class="sxs-lookup"><span data-stu-id="6eae8-349">master midi</span></span></td>
<td><span data-ttu-id="6eae8-350">Définit le séquenceur MIDI comme source de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6eae8-350">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="6eae8-351">Les données de synchronisation sont envoyées au format MIDI.</span><span class="sxs-lookup"><span data-stu-id="6eae8-351">Synchronization data is sent in MIDI format.</span></span> <span data-ttu-id="6eae8-352">MCISEQ Sequencer ne prend pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eae8-352">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-353">maître aucun</span><span class="sxs-lookup"><span data-stu-id="6eae8-353">master none</span></span></td>
<td><span data-ttu-id="6eae8-354">Empêche le séquenceur MIDI d’envoyer des données de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6eae8-354">Inhibits the MIDI sequencer from sending synchronization data.</span></span> <span data-ttu-id="6eae8-355">MCISEQ Sequencer ne prend pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eae8-355">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-356">SMPTE maître</span><span class="sxs-lookup"><span data-stu-id="6eae8-356">master smpte</span></span></td>
<td><span data-ttu-id="6eae8-357">Définit le séquenceur MIDI comme source de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6eae8-357">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="6eae8-358">Les données de synchronisation sont envoyées au format SMPTE (société de motion image and Television Engineers).</span><span class="sxs-lookup"><span data-stu-id="6eae8-358">Synchronization data is sent in SMPTE (Society of Motion Picture and Television Engineers) format.</span></span> <span data-ttu-id="6eae8-359">MCISEQ Sequencer ne prend pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eae8-359">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-360"><em>heure</em> du décalage</span><span class="sxs-lookup"><span data-stu-id="6eae8-360">offset <em>time</em></span></span></td>
<td><span data-ttu-id="6eae8-361">Définit le <em>temps</em>de décalage SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eae8-361">Sets the SMPTE offset <em>time</em>.</span></span> <span data-ttu-id="6eae8-362">Le décalage est l’heure de début d’une séquence basée sur SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eae8-362">The offset is the beginning time of a SMPTE based sequence.</span></span> <span data-ttu-id="6eae8-363">L' <em>heure</em> est exprimée sous la forme <em>hh</em>: <em>mm</em>: <em>SS</em>: <em>FF</em>, où <em>hh</em> est hours, <em>mm</em> correspond à minutes, <em>SS</em> à secondes et <em>FF</em> à la trame.</span><span class="sxs-lookup"><span data-stu-id="6eae8-363">The <em>time</em> is expressed as <em>hh</em>: <em>mm</em>: <em>ss</em>: <em>ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-364"><em>entier</em> de sortie</span><span class="sxs-lookup"><span data-stu-id="6eae8-364">output <em>integer</em></span></span></td>
<td><span data-ttu-id="6eae8-365">Définit le canal audio utilisé comme sortie.</span><span class="sxs-lookup"><span data-stu-id="6eae8-365">Sets the audio channel used as the output.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-366"><em>délai d’attente</em> de pause</span><span class="sxs-lookup"><span data-stu-id="6eae8-366">pause <em>timeout</em></span></span></td>
<td><span data-ttu-id="6eae8-367">Définit la durée maximale, en millisecondes, d’une commande de <a href="pause.md">Pause</a> .</span><span class="sxs-lookup"><span data-stu-id="6eae8-367">Sets the maximum duration, in milliseconds, of a <a href="pause.md">pause</a> command.</span></span> <span data-ttu-id="6eae8-368">Une valeur de <em>délai d’attente</em> de zéro indique qu’aucun délai d’attente n’A lieu.</span><span class="sxs-lookup"><span data-stu-id="6eae8-368">A <em>timeout</em> value of zero indicates that no time-out will occur.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-369"><em>durée</em> de la durée de Postroll</span><span class="sxs-lookup"><span data-stu-id="6eae8-369">postroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="6eae8-370">Définit la longueur, dans le format d’heure actuel, nécessaire pour freiner le transport du magnétoscope lors de l’émission d’une commande d' <a href="stop.md">arrêt</a> ou de <strong>Pause</strong> .</span><span class="sxs-lookup"><span data-stu-id="6eae8-370">Sets the length, in the current time format, needed to brake the VCR transport when a <a href="stop.md">stop</a> or <strong>pause</strong> command is issued.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-371">mappeur de port</span><span class="sxs-lookup"><span data-stu-id="6eae8-371">port mapper</span></span></td>
<td><span data-ttu-id="6eae8-372">Définit le Mappeur MIDI comme port recevant les messages MIDI.</span><span class="sxs-lookup"><span data-stu-id="6eae8-372">Sets the MIDI mapper as the port receiving the MIDI messages.</span></span> <span data-ttu-id="6eae8-373">Cette commande échoue si le Mappeur MIDI ou un port dont il a besoin est utilisé par une autre application.</span><span class="sxs-lookup"><span data-stu-id="6eae8-373">This command fails if the MIDI mapper or a port it needs is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-374">port aucun</span><span class="sxs-lookup"><span data-stu-id="6eae8-374">port none</span></span></td>
<td><span data-ttu-id="6eae8-375">Désactive l’envoi des messages MIDI.</span><span class="sxs-lookup"><span data-stu-id="6eae8-375">Disables the sending of MIDI messages.</span></span> <span data-ttu-id="6eae8-376">Cette commande ferme également un port MIDI.</span><span class="sxs-lookup"><span data-stu-id="6eae8-376">This command also closes a MIDI port.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-377"><em>port_number</em> de port</span><span class="sxs-lookup"><span data-stu-id="6eae8-377">port <em>port_number</em></span></span></td>
<td><span data-ttu-id="6eae8-378">Définit le port MIDI recevant les messages MIDI.</span><span class="sxs-lookup"><span data-stu-id="6eae8-378">Sets the MIDI port receiving the MIDI messages.</span></span> <span data-ttu-id="6eae8-379">Cette commande échoue si le port que vous essayez d’ouvrir est utilisé par une autre application.</span><span class="sxs-lookup"><span data-stu-id="6eae8-379">This command fails if the port you are trying to open is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-380">Sous tension</span><span class="sxs-lookup"><span data-stu-id="6eae8-380">power on</span></span> <br/> <span data-ttu-id="6eae8-381">mettre hors tension</span><span class="sxs-lookup"><span data-stu-id="6eae8-381">power off</span></span> <br/></td>
<td><span data-ttu-id="6eae8-382">Active ou désactive la mise sous tension de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6eae8-382">Sets the device power to on or off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-383"><em>durée</em> du préroll</span><span class="sxs-lookup"><span data-stu-id="6eae8-383">preroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="6eae8-384">Définit la longueur, dans le format d’heure actuel, nécessaire pour stabiliser la sortie du magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="6eae8-384">Sets the length, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-385">format d’enregistrement SP</span><span class="sxs-lookup"><span data-stu-id="6eae8-385">record format SP</span></span> <br/> <span data-ttu-id="6eae8-386">format d’enregistrement LP</span><span class="sxs-lookup"><span data-stu-id="6eae8-386">record format LP</span></span> <br/> <span data-ttu-id="6eae8-387">format d’enregistrement EP</span><span class="sxs-lookup"><span data-stu-id="6eae8-387">record format EP</span></span> <br/></td>
<td><span data-ttu-id="6eae8-388">Définit le mode d’enregistrement du magnétoscope sur SP pour la lecture standard, EP pour extension de lecture ou LP pour une lecture longue.</span><span class="sxs-lookup"><span data-stu-id="6eae8-388">Sets the recording mode for the VCR to SP for standard play, EP for extended play, or LP for long play.</span></span> <span data-ttu-id="6eae8-389">Ces valeurs ne sont pas destinées à être spécifiques à la SHV.</span><span class="sxs-lookup"><span data-stu-id="6eae8-389">These values are not intended to be VHS specific.</span></span> <span data-ttu-id="6eae8-390">Elles sont mappées à trois modes appropriés avec d’autres formats de bande.</span><span class="sxs-lookup"><span data-stu-id="6eae8-390">They map to any three appropriate modes with other tape formats.</span></span> <span data-ttu-id="6eae8-391">Par exemple, SP est mappé à l’enregistrement le plus rapide et de qualité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="6eae8-391">For example, SP maps to the fastest, highest quality recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-392"><em>entier</em> SamplesPerSec</span><span class="sxs-lookup"><span data-stu-id="6eae8-392">samplespersec <em>integer</em></span></span></td>
<td><span data-ttu-id="6eae8-393">Définit le taux d’échantillonnage pour la diffusion et l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6eae8-393">Sets the sample rate for playing and recording.</span></span> <span data-ttu-id="6eae8-394">Le fichier est enregistré dans ce format.</span><span class="sxs-lookup"><span data-stu-id="6eae8-394">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-395">recherche exacte</span><span class="sxs-lookup"><span data-stu-id="6eae8-395">seek exactly on</span></span><br/> <span data-ttu-id="6eae8-396">recherche exacte</span><span class="sxs-lookup"><span data-stu-id="6eae8-396">seek exactly off</span></span> <br/></td>
<td><span data-ttu-id="6eae8-397">Sélectionne l’un des deux modes de recherche.</span><span class="sxs-lookup"><span data-stu-id="6eae8-397">Selects one of two seek modes.</span></span> <span data-ttu-id="6eae8-398">Lorsque &quot; Seek est activé &quot; , Seek passe toujours à la trame spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6eae8-398">With &quot;seek exactly on&quot;, seek will always move to the frame specified.</span></span> <span data-ttu-id="6eae8-399">Lorsque &quot; Seek &quot; est défini sur OFF, Seek se déplace vers l’image clé la plus proche avant le frame spécifié.</span><span class="sxs-lookup"><span data-stu-id="6eae8-399">With &quot;seek exactly off&quot;, seek will move to the closest key frame prior to the frame specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-400">fichier esclave</span><span class="sxs-lookup"><span data-stu-id="6eae8-400">slave file</span></span></td>
<td><span data-ttu-id="6eae8-401">Définit le séquenceur MIDI pour utiliser les données de fichier en tant que source de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6eae8-401">Sets the MIDI sequencer to use file data as the synchronization source.</span></span> <span data-ttu-id="6eae8-402">Il s'agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="6eae8-402">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-403">midi esclave</span><span class="sxs-lookup"><span data-stu-id="6eae8-403">slave midi</span></span></td>
<td><span data-ttu-id="6eae8-404">Définit le séquenceur MIDI pour qu’il utilise les données MIDI entrantes pour la source de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6eae8-404">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="6eae8-405">Sequencer reconnaît les données de synchronisation avec le format MIDI.</span><span class="sxs-lookup"><span data-stu-id="6eae8-405">The sequencer recognizes synchronization data with the MIDI format.</span></span> <span data-ttu-id="6eae8-406">MCISEQ Sequencer ne prend pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eae8-406">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-407">esclave aucun</span><span class="sxs-lookup"><span data-stu-id="6eae8-407">slave none</span></span></td>
<td><span data-ttu-id="6eae8-408">Définit le séquenceur MIDI pour ignorer la synchronisation</span><span class="sxs-lookup"><span data-stu-id="6eae8-408">Sets the MIDI sequencer to ignore synchronization</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-409">SMPTE esclave</span><span class="sxs-lookup"><span data-stu-id="6eae8-409">slave smpte</span></span></td>
<td><span data-ttu-id="6eae8-410">Définit le séquenceur MIDI pour qu’il utilise les données MIDI entrantes pour la source de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6eae8-410">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="6eae8-411">Sequencer reconnaît les données de synchronisation avec le format SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eae8-411">The sequencer recognizes synchronization data with the SMPTE format.</span></span> <span data-ttu-id="6eae8-412">MCISEQ Sequencer ne prend pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eae8-412">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-413">facteur de vitesse</span><span class="sxs-lookup"><span data-stu-id="6eae8-413">speed factor</span></span></td>
<td><span data-ttu-id="6eae8-414">Définit la vitesse relative de lecture vidéo et audio à partir de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="6eae8-414">Sets the relative speed of video and audio playback from the workspace.</span></span> <span data-ttu-id="6eae8-415">Factor est le rapport entre la fréquence d’images nominale et la fréquence d’images souhaitée, où la fréquence d’images nominale est désignée comme 1000.</span><span class="sxs-lookup"><span data-stu-id="6eae8-415">Factor is the ratio between the nominal frame rate and the desired frame rate, where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="6eae8-416">(Un taux de 500 est une vitesse semi-normale, 2000 une vitesse normale, et ainsi de suite.) Si vous définissez la vitesse sur zéro, la vidéo est lue le plus rapidement possible sans supprimer les images ni les données audio.</span><span class="sxs-lookup"><span data-stu-id="6eae8-416">(A rate of 500 is half normal speed, 2000 is twice normal speed, and so on.) Setting the speed to zero plays the video as fast as possible without dropping frames and without audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-417"><em>format</em> de format de fichier toujours</span><span class="sxs-lookup"><span data-stu-id="6eae8-417">still file format <em>format</em></span></span></td>
<td><span data-ttu-id="6eae8-418">Spécifie le format de fichier utilisé pour les commandes de capture.</span><span class="sxs-lookup"><span data-stu-id="6eae8-418">Specifies the file format used for capture commands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-419">tempo tempo_value</span><span class="sxs-lookup"><span data-stu-id="6eae8-419">tempo tempo_value</span></span></td>
<td><span data-ttu-id="6eae8-420">Définit le tempo de la séquence en fonction du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="6eae8-420">Sets the tempo of the sequence according to the current time format.</span></span> <span data-ttu-id="6eae8-421">Dans le cas d’un fichier basé sur PPQN, le tempo_value est interprété comme un temps par minute.</span><span class="sxs-lookup"><span data-stu-id="6eae8-421">For a PPQN-based file, the tempo_value is interpreted as beats per minute.</span></span> <span data-ttu-id="6eae8-422">Dans le cas d’un fichier basé sur la SMPTE, le tempo_value est interprété comme un nombre d’images par seconde.</span><span class="sxs-lookup"><span data-stu-id="6eae8-422">For a SMPTE-based file, the tempo_value is interpreted as frames per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-423">octets de format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-423">time format bytes</span></span></td>
<td><span data-ttu-id="6eae8-424">Dans un format de fichier PCM, définit le format d’heure sur octets.</span><span class="sxs-lookup"><span data-stu-id="6eae8-424">In a PCM file format, sets the time format to bytes.</span></span> <span data-ttu-id="6eae8-425">Toutes les informations de position sont spécifiées sous la forme d’octets après cette commande.</span><span class="sxs-lookup"><span data-stu-id="6eae8-425">All position information is specified as bytes following this command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-426">frames de format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-426">time format frames</span></span></td>
<td><span data-ttu-id="6eae8-427">Définit le format d’heure sur les frames.</span><span class="sxs-lookup"><span data-stu-id="6eae8-427">Sets the time format to frames.</span></span> <span data-ttu-id="6eae8-428">Toutes les commandes qui utilisent des valeurs de position supposent des frames.</span><span class="sxs-lookup"><span data-stu-id="6eae8-428">All commands that use position values will assume frames.</span></span> <span data-ttu-id="6eae8-429">Lorsque l’appareil est ouvert, frames est le mode par défaut.</span><span class="sxs-lookup"><span data-stu-id="6eae8-429">When the device is opened, frames is the default mode.</span></span> <span data-ttu-id="6eae8-430">Pris en charge par videodiscs à l’aide du format CAV.</span><span class="sxs-lookup"><span data-stu-id="6eae8-430">Supported by videodiscs using CAV format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-431">format d’heure HMS</span><span class="sxs-lookup"><span data-stu-id="6eae8-431">time format hms</span></span></td>
<td><span data-ttu-id="6eae8-432">Définit le format d’heure sur les heures, les minutes et les secondes.</span><span class="sxs-lookup"><span data-stu-id="6eae8-432">Sets the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="6eae8-433">Toutes les commandes qui utilisent des valeurs de position supposent HMS.</span><span class="sxs-lookup"><span data-stu-id="6eae8-433">All commands that use position values will assume HMS.</span></span> <span data-ttu-id="6eae8-434">HMS est le format par défaut pour CLV videodiscs.</span><span class="sxs-lookup"><span data-stu-id="6eae8-434">HMS is the default format for CLV videodiscs.</span></span> <span data-ttu-id="6eae8-435">Spécifiez une valeur HMS hh : mm : SS, où HH correspond à heures, mm à minutes et SS à secondes.</span><span class="sxs-lookup"><span data-stu-id="6eae8-435">Specify an HMS value as hh:mm:ss, where hh is hours, mm is minutes, and ss is seconds.</span></span> <span data-ttu-id="6eae8-436">Vous pouvez omettre un champ si celui-ci et tous les champs suivants sont nuls.</span><span class="sxs-lookup"><span data-stu-id="6eae8-436">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="6eae8-437">Par exemple, 3, 3:0 et 3:0:0 sont tous des moyens valides pour exprimer 3 heures.</span><span class="sxs-lookup"><span data-stu-id="6eae8-437">For example, 3, 3:0, and 3:0:0 are all valid ways to express 3 hours.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-438">format d’heure en millisecondes</span><span class="sxs-lookup"><span data-stu-id="6eae8-438">time format milliseconds</span></span></td>
<td><span data-ttu-id="6eae8-439">Définit le format d’heure sur millisecondes.</span><span class="sxs-lookup"><span data-stu-id="6eae8-439">Sets the time format to milliseconds.</span></span> <span data-ttu-id="6eae8-440">Toutes les commandes qui utilisent des valeurs de position prennent la valeur en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="6eae8-440">All commands that use position values will assume milliseconds.</span></span> <span data-ttu-id="6eae8-441">Vous pouvez abréger les millisecondes comme &quot; MS &quot; .</span><span class="sxs-lookup"><span data-stu-id="6eae8-441">You can abbreviate milliseconds as &quot;ms&quot;.</span></span> <span data-ttu-id="6eae8-442">Pour les appareils Sequencer, le fichier de séquence définit le format par défaut sur PPQN ou SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eae8-442">For sequencer devices, the sequence file sets the default format to PPQN or SMPTE.</span></span> <span data-ttu-id="6eae8-443">Les périphériques de superposition vidéo ne prennent pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eae8-443">Video-overlay devices do not support this flag.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-444">format d’heure MSF</span><span class="sxs-lookup"><span data-stu-id="6eae8-444">time format msf</span></span></td>
<td><span data-ttu-id="6eae8-445">Définit le format d’heure sur les minutes, les secondes et les frames.</span><span class="sxs-lookup"><span data-stu-id="6eae8-445">Sets the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="6eae8-446">Toutes les commandes qui utilisent des valeurs de position supposent MSF (le format par défaut pour les CD audio).</span><span class="sxs-lookup"><span data-stu-id="6eae8-446">All commands that use position values will assume MSF (the default format for CD audio).</span></span> <span data-ttu-id="6eae8-447">Spécifiez une valeur MSF au format mm : SS : FF, où mm correspond à minutes, SS à secondes et FF à frames.</span><span class="sxs-lookup"><span data-stu-id="6eae8-447">Specify an MSF value as mm:ss:ff, where mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="6eae8-448">Vous pouvez omettre un champ si celui-ci et tous les champs suivants sont nuls.</span><span class="sxs-lookup"><span data-stu-id="6eae8-448">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="6eae8-449">Par exemple, 3, 3:0 et 3:0:0 sont des méthodes valides pour exprimer 3 minutes.</span><span class="sxs-lookup"><span data-stu-id="6eae8-449">For example, 3, 3:0, and 3:0:0 are valid ways to express 3 minutes.</span></span><br/> <span data-ttu-id="6eae8-450">Les champs MSF ont les valeurs maximales suivantes :</span><span class="sxs-lookup"><span data-stu-id="6eae8-450">The MSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="6eae8-451">Minutes 99</span><span class="sxs-lookup"><span data-stu-id="6eae8-451">Minutes 99</span></span></li>
<li><span data-ttu-id="6eae8-452">Secondes 59</span><span class="sxs-lookup"><span data-stu-id="6eae8-452">Seconds 59</span></span></li>
<li><span data-ttu-id="6eae8-453">Frames 74</span><span class="sxs-lookup"><span data-stu-id="6eae8-453">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-454">exemples de format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-454">time format samples</span></span></td>
<td><span data-ttu-id="6eae8-455">Définit le format d’heure sur Samples.</span><span class="sxs-lookup"><span data-stu-id="6eae8-455">Sets the time format to samples.</span></span> <span data-ttu-id="6eae8-456">Toutes les informations de position sont spécifiées en tant qu’exemples après cette commande.</span><span class="sxs-lookup"><span data-stu-id="6eae8-456">All position information is specified as samples following this command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-457">format d’heure SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="6eae8-457">time format smpte 24</span></span><br/> <span data-ttu-id="6eae8-458">format d’heure SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="6eae8-458">time format smpte 25</span></span><br/> <span data-ttu-id="6eae8-459">format d’heure SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="6eae8-459">time format smpte 30</span></span><br/></td>
<td><span data-ttu-id="6eae8-460">Définit le format d’heure sur une fréquence d’images SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eae8-460">Sets the time format to an SMPTE frame rate.</span></span> <span data-ttu-id="6eae8-461">Pour les magnétoscopes, définit le format d’heure hh : mm : SS : FF, où les valeurs autorisées sont comprises entre 00:00:00:00 et 23:59:59 : XX, tandis que la valeur XX est inférieure aux images par seconde, comme spécifié par le nombre 24, 25 ou 30 comme spécifié dans l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="6eae8-461">For VCRs, sets the time format to hh:mm:ss:ff, where the legal values are 00:00:00:00 through 23:59:59:xx, and xx is one less than the frames per second as specified by the number 24, 25, or 30 as specified in the flag.</span></span> <span data-ttu-id="6eae8-462">En entrée, deux-points ( :) sont requis pour séparer les composants.</span><span class="sxs-lookup"><span data-stu-id="6eae8-462">On input, colons (:) are required to separate the components.</span></span> <span data-ttu-id="6eae8-463">Les unités les moins significatives peuvent être omises si elles sont égales à 00 ; par exemple, 02:00 est le même que 02:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="6eae8-463">The least significant units can be omitted if they are 00; for example, 02:00 is the same as 02:00:00:00.</span></span> <span data-ttu-id="6eae8-464">Toutes les commandes qui utilisent des valeurs de position prennent le format SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eae8-464">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="6eae8-465">Le fichier de séquence définit le format par défaut sur PPQN ou SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eae8-465">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-466">suppression du format d’heure SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="6eae8-466">time format smpte 30 drop</span></span></td>
<td><span data-ttu-id="6eae8-467">Définit le format d’heure sur la fréquence d’images de dépôt SMPTE 30.</span><span class="sxs-lookup"><span data-stu-id="6eae8-467">Sets the time format to SMPTE 30 drop frame rate.</span></span> <span data-ttu-id="6eae8-468">Pour les magnétoscopes, identique à SMPTE 30, sauf que certaines positions du code temporel sont supprimées du format de façon à ce que les positions du code temporel enregistrées pour chaque image (à la fréquence d’images NTSC de 29,97 fps) correspondent au temps réel (à 30 i/s).</span><span class="sxs-lookup"><span data-stu-id="6eae8-468">For VCRs, same as SMPTE 30, except that certain timecode positions are dropped from the format to have the recorded timecode positions for each frame (at the NTSC frame rate of 29.97 fps) correspond to real time (at 30 fps).</span></span> <span data-ttu-id="6eae8-469">Les positions de code temporel supprimées sont les suivantes : deux fois par minute, pour les neuf premières minutes de contenu enregistré.</span><span class="sxs-lookup"><span data-stu-id="6eae8-469">Timecode positions that are dropped are as follows: two every minute, on the minute, for the first nine of every ten minutes of recorded content.</span></span> <span data-ttu-id="6eae8-470">Par exemple, à 01:04:59:29, la position suivante du code temporel est 01:05:00:02, et non 01:05:00:00.</span><span class="sxs-lookup"><span data-stu-id="6eae8-470">For example, at 01:04:59:29, the next timecode position would be 01:05:00:02, not 01:05:00:00.</span></span> <span data-ttu-id="6eae8-471">Toutes les commandes qui utilisent des valeurs de position prennent le format SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eae8-471">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="6eae8-472">Le fichier de séquence définit le format par défaut sur PPQN ou SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6eae8-472">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-473">pointeur de chanson au format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-473">time format song pointer</span></span></td>
<td><span data-ttu-id="6eae8-474">Définit le format d’heure sur le pointeur de la chanson (seizième Remarques).</span><span class="sxs-lookup"><span data-stu-id="6eae8-474">Sets the time format to song pointer (sixteenth notes).</span></span> <span data-ttu-id="6eae8-475">Toutes les commandes qui utilisent des valeurs de position supposent l’utilisation d’unités de pointeur de chanson.</span><span class="sxs-lookup"><span data-stu-id="6eae8-475">All commands that use position values will assume song pointer units.</span></span> <span data-ttu-id="6eae8-476">Cet indicateur n’est valide que pour une séquence de type de division PPQN.</span><span class="sxs-lookup"><span data-stu-id="6eae8-476">This flag is valid only for a sequence of division type PPQN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-477">format d’heure TMSF</span><span class="sxs-lookup"><span data-stu-id="6eae8-477">time format tmsf</span></span></td>
<td><span data-ttu-id="6eae8-478">Définit le format d’heure sur les suivis, les minutes, les secondes et les frames.</span><span class="sxs-lookup"><span data-stu-id="6eae8-478">Sets the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="6eae8-479">Toutes les commandes qui utilisent des valeurs de position supposent TMSF.</span><span class="sxs-lookup"><span data-stu-id="6eae8-479">All commands that use position values will assume TMSF.</span></span> <span data-ttu-id="6eae8-480">Spécifiez une valeur TMSF comme TT : mm : SS : FF, où TT est Tracks, mm est minutes, SS est secondes et FF est le frame.</span><span class="sxs-lookup"><span data-stu-id="6eae8-480">Specify a TMSF value as tt:mm:ss:ff, where tt is tracks, mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="6eae8-481">Vous pouvez omettre un champ si celui-ci et tous les champs suivants sont nuls.</span><span class="sxs-lookup"><span data-stu-id="6eae8-481">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="6eae8-482">Par exemple, 3, 3:0, 3:0:0 et 3:0:0:0 sont tous des moyens valides pour exprimer Track 3.</span><span class="sxs-lookup"><span data-stu-id="6eae8-482">For example, 3, 3:0, 3:0:0, and 3:0:0:0 are all valid ways to express track 3.</span></span> <br/> <span data-ttu-id="6eae8-483">Les valeurs maximales des champs TMSF sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6eae8-483">The TMSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="6eae8-484">Suit 99</span><span class="sxs-lookup"><span data-stu-id="6eae8-484">Tracks 99</span></span></li>
<li><span data-ttu-id="6eae8-485">Minutes 90</span><span class="sxs-lookup"><span data-stu-id="6eae8-485">Minutes 90</span></span></li>
<li><span data-ttu-id="6eae8-486">Secondes 59</span><span class="sxs-lookup"><span data-stu-id="6eae8-486">Seconds 59</span></span></li>
<li><span data-ttu-id="6eae8-487">Frames 74</span><span class="sxs-lookup"><span data-stu-id="6eae8-487">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-488">suivi du format d’heure</span><span class="sxs-lookup"><span data-stu-id="6eae8-488">time format track</span></span></td>
<td><span data-ttu-id="6eae8-489">Définit le format de position des pistes.</span><span class="sxs-lookup"><span data-stu-id="6eae8-489">Sets the position format to tracks.</span></span> <span data-ttu-id="6eae8-490">Toutes les commandes qui utilisent des valeurs de position supposent des pistes.</span><span class="sxs-lookup"><span data-stu-id="6eae8-490">All commands that use position values will assume tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-491">compteur du mode temps</span><span class="sxs-lookup"><span data-stu-id="6eae8-491">time mode counter</span></span></td>
<td><span data-ttu-id="6eae8-492">Définit le mode de positionnement-informations pour utiliser les compteurs VCR.</span><span class="sxs-lookup"><span data-stu-id="6eae8-492">Sets the position-information mode to use the VCR counters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-493">détection du mode de temps</span><span class="sxs-lookup"><span data-stu-id="6eae8-493">time mode detect</span></span></td>
<td><span data-ttu-id="6eae8-494">Définit le mode d’informations de position en fonction de la détection des informations de code temporel sur la bande.</span><span class="sxs-lookup"><span data-stu-id="6eae8-494">Sets the position information mode based on detection of timecode information on the tape.</span></span> <span data-ttu-id="6eae8-495">Si des informations de code temporel sont détectées, le type d’heure est défini sur &quot; timecode &quot; ; sinon, le type d’heure est défini sur &quot; Counter &quot; .</span><span class="sxs-lookup"><span data-stu-id="6eae8-495">If timecode information is detected, the time type is set to &quot;timecode&quot;; otherwise, the time type is set to &quot;counter&quot;.</span></span> <span data-ttu-id="6eae8-496">&quot;&quot;La détection est un mode spécial.</span><span class="sxs-lookup"><span data-stu-id="6eae8-496">&quot;Detect&quot; is a special mode.</span></span> <span data-ttu-id="6eae8-497">Chaque fois que le pilote est ouvert, une nouvelle bande est insérée, ou la &quot; commande de mode &quot; de temps est émise, le pilote vérifie le mode d’heure actuel disponible sur la bande et définit le &quot; type &quot; de temps sur &quot; code temporel &quot; ou &quot; compteur &quot; .</span><span class="sxs-lookup"><span data-stu-id="6eae8-497">Whenever the driver is opened, a new tape is inserted, or the &quot;time mode&quot; command is issued, the driver checks the current time mode available on the tape and sets &quot;time type&quot; to either &quot;timecode&quot; or &quot;counter&quot;.</span></span> <span data-ttu-id="6eae8-498">Une fois le &quot; type &quot; de temps défini, le pilote ne le modifie pas tant que l’une des conditions ci-dessus n’a pas été reproduite.</span><span class="sxs-lookup"><span data-stu-id="6eae8-498">Once &quot;time type&quot; is set, the driver doesn't change it until one of the above conditions occurs again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-499">code temporel du mode Time</span><span class="sxs-lookup"><span data-stu-id="6eae8-499">time mode timecode</span></span></td>
<td><span data-ttu-id="6eae8-500">Définit le mode d’informations de position pour utiliser &quot; &quot; les informations de code temporel sur la bande.</span><span class="sxs-lookup"><span data-stu-id="6eae8-500">Sets the position information mode to use &quot;timecode&quot; information on the tape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-501">suivi plus</span><span class="sxs-lookup"><span data-stu-id="6eae8-501">tracking plus</span></span> <br/> <span data-ttu-id="6eae8-502">suivi moins</span><span class="sxs-lookup"><span data-stu-id="6eae8-502">tracking minus</span></span> <br/> <span data-ttu-id="6eae8-503">réinitialisation du suivi</span><span class="sxs-lookup"><span data-stu-id="6eae8-503">tracking reset</span></span> <br/></td>
<td><span data-ttu-id="6eae8-504">Ajuste la vitesse du transport des cassettes vidéo en incréments précis.</span><span class="sxs-lookup"><span data-stu-id="6eae8-504">Adjusts the speed of the videotape transport in fine increments.</span></span> <span data-ttu-id="6eae8-505">Utilisez les &quot; indicateurs de suivi &quot; lorsqu’une image bruyante est obtenue à partir d’un magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="6eae8-505">Use the &quot;tracking&quot; flags when a noisy picture is obtained from a VCR.</span></span> <span data-ttu-id="6eae8-506">&quot;Le suivi plus &quot; augmente la vitesse de transport.</span><span class="sxs-lookup"><span data-stu-id="6eae8-506">&quot;Tracking plus&quot; increases the transport speed.</span></span> <span data-ttu-id="6eae8-507">&quot;Le suivi moins &quot; diminue la vitesse de transport.</span><span class="sxs-lookup"><span data-stu-id="6eae8-507">&quot;Tracking minus&quot; decreases the transport speed.</span></span> <span data-ttu-id="6eae8-508">&quot;Le suivi &quot; de la réinitialisation retourne l’ajustement de suivi à zéro.</span><span class="sxs-lookup"><span data-stu-id="6eae8-508">&quot;Tracking reset&quot; returns the tracking adjustment to zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eae8-509">vidéo désactivée</span><span class="sxs-lookup"><span data-stu-id="6eae8-509">video off</span></span></td>
<td><span data-ttu-id="6eae8-510">Désactive la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="6eae8-510">Disables video output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eae8-511">vidéo sur</span><span class="sxs-lookup"><span data-stu-id="6eae8-511">video on</span></span></td>
<td><span data-ttu-id="6eae8-512">Active la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="6eae8-512">Enables video output.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="6eae8-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6eae8-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6eae8-514">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="6eae8-514">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="6eae8-515">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="6eae8-515">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="6eae8-516">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6eae8-516">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eae8-517">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6eae8-517">Return Value</span></span>

<span data-ttu-id="6eae8-518">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="6eae8-518">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eae8-519">Notes</span><span class="sxs-lookup"><span data-stu-id="6eae8-519">Remarks</span></span>

<span data-ttu-id="6eae8-520">Plusieurs propriétés des données Waveform-Audio sont définies lors de la création du fichier de stockage des données.</span><span class="sxs-lookup"><span data-stu-id="6eae8-520">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="6eae8-521">Ces propriétés décrivent comment les données sont structurées dans le fichier et ne peuvent pas être modifiées une fois l’enregistrement commencé.</span><span class="sxs-lookup"><span data-stu-id="6eae8-521">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="6eae8-522">La liste suivante identifie ces propriétés :</span><span class="sxs-lookup"><span data-stu-id="6eae8-522">The following list identifies these properties:</span></span>

-   <span data-ttu-id="6eae8-523">alignement</span><span class="sxs-lookup"><span data-stu-id="6eae8-523">alignment</span></span>
-   <span data-ttu-id="6eae8-524">bitspersample</span><span class="sxs-lookup"><span data-stu-id="6eae8-524">bitspersample</span></span>
-   <span data-ttu-id="6eae8-525">bytespersec</span><span class="sxs-lookup"><span data-stu-id="6eae8-525">bytespersec</span></span>
-   <span data-ttu-id="6eae8-526">channels</span><span class="sxs-lookup"><span data-stu-id="6eae8-526">channels</span></span>
-   <span data-ttu-id="6eae8-527">balise de format</span><span class="sxs-lookup"><span data-stu-id="6eae8-527">format tag</span></span>
-   <span data-ttu-id="6eae8-528">samplespersec</span><span class="sxs-lookup"><span data-stu-id="6eae8-528">samplespersec</span></span>

## <a name="examples"></a><span data-ttu-id="6eae8-529">Exemples</span><span class="sxs-lookup"><span data-stu-id="6eae8-529">Examples</span></span>

<span data-ttu-id="6eae8-530">La commande suivante définit le format d’heure sur millisecondes et définit le format Waveform-Audio sur 8 bits, mono, 11 kHz.</span><span class="sxs-lookup"><span data-stu-id="6eae8-530">The following command sets the time format to milliseconds and sets the waveform-audio format to 8 bit, mono, 11 kHz.</span></span>

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a><span data-ttu-id="6eae8-531">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6eae8-531">Requirements</span></span>



| <span data-ttu-id="6eae8-532">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6eae8-532">Requirement</span></span> | <span data-ttu-id="6eae8-533">Valeur</span><span class="sxs-lookup"><span data-stu-id="6eae8-533">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6eae8-534">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eae8-534">Minimum supported client</span></span><br/> | <span data-ttu-id="6eae8-535">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eae8-535">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6eae8-536">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eae8-536">Minimum supported server</span></span><br/> | <span data-ttu-id="6eae8-537">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eae8-537">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6eae8-538">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6eae8-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eae8-539">MCI</span><span class="sxs-lookup"><span data-stu-id="6eae8-539">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6eae8-540">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="6eae8-540">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="6eae8-541">attire</span><span class="sxs-lookup"><span data-stu-id="6eae8-541">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="6eae8-542">pause</span><span class="sxs-lookup"><span data-stu-id="6eae8-542">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="6eae8-543">enregistrer</span><span class="sxs-lookup"><span data-stu-id="6eae8-543">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="6eae8-544">stop</span><span class="sxs-lookup"><span data-stu-id="6eae8-544">stop</span></span>](stop.md)
</dt> </dl>

 


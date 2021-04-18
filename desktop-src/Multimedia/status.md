---
title: commande Status
description: La commande status demande des informations d’État à partir d’un appareil. Tous les appareils reconnaissent cette commande.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- commande Status Windows Multimedia
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/12/2021
ms.locfileid: "106522857"
---
# <a name="status-command"></a><span data-ttu-id="387c1-105">commande Status</span><span class="sxs-lookup"><span data-stu-id="387c1-105">status command</span></span>

> [!NOTE]
> <span data-ttu-id="387c1-106">Communication sans biais Microsoft prend en charge un environnement diversifié et un environnement d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="387c1-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="387c1-107">Dans ce document, il existe des références au mot « esclave ».</span><span class="sxs-lookup"><span data-stu-id="387c1-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="387c1-108">Le [Guide de style de Microsoft pour les Communications Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconnaît cela comme un mot d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="387c1-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="387c1-109">Ce libellé est utilisé, car il s’agit actuellement de la formulation utilisée dans les commandes.</span><span class="sxs-lookup"><span data-stu-id="387c1-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="387c1-110">Pour des fins de cohérence, ce document contient ce mot.</span><span class="sxs-lookup"><span data-stu-id="387c1-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="387c1-111">Lorsque ce mot est modifié dans les commandes, nous allons corriger ce document pour qu’il soit aligné.</span><span class="sxs-lookup"><span data-stu-id="387c1-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="387c1-112">La commande status demande des informations d’État à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="387c1-112">The status command requests status information from a device.</span></span> <span data-ttu-id="387c1-113">Tous les appareils reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="387c1-113">All devices recognize this command.</span></span>

<span data-ttu-id="387c1-114">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="387c1-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="387c1-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="387c1-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="387c1-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="387c1-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="387c1-117">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="387c1-117">Identifier of an MCI device.</span></span> <span data-ttu-id="387c1-118">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="387c1-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="387c1-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="387c1-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="387c1-120">Indicateur de demande d’informations d’État.</span><span class="sxs-lookup"><span data-stu-id="387c1-120">Flag for requesting status information.</span></span> <span data-ttu-id="387c1-121">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Status** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="387c1-121">The following table lists device types that recognize the **status** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="387c1-122">Type d’appareil</span><span class="sxs-lookup"><span data-stu-id="387c1-122">Device Type</span></span></th>
<th><span data-ttu-id="387c1-123">Indicateurs de demande</span><span class="sxs-lookup"><span data-stu-id="387c1-123">Request Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="387c1-124">cdaudio</span><span class="sxs-lookup"><span data-stu-id="387c1-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="387c1-125"><em>numéro</em> de suivi de type cdaudio</span><span class="sxs-lookup"><span data-stu-id="387c1-125">cdaudio type track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-126">piste actuelle</span><span class="sxs-lookup"><span data-stu-id="387c1-126">current track</span></span></li>
<li><span data-ttu-id="387c1-127">length</span><span class="sxs-lookup"><span data-stu-id="387c1-127">length</span></span></li>
<li><span data-ttu-id="387c1-128"><em>nombre</em> de pistes de longueur</span><span class="sxs-lookup"><span data-stu-id="387c1-128">length track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-129">support présent</span><span class="sxs-lookup"><span data-stu-id="387c1-129">media present</span></span></li>
<li><span data-ttu-id="387c1-130">mode</span><span class="sxs-lookup"><span data-stu-id="387c1-130">mode</span></span></li>
<li><span data-ttu-id="387c1-131">nombre de pistes</span><span class="sxs-lookup"><span data-stu-id="387c1-131">number of tracks</span></span></li>
<li><span data-ttu-id="387c1-132">position</span><span class="sxs-lookup"><span data-stu-id="387c1-132">position</span></span></li>
<li><span data-ttu-id="387c1-133"><em>numéro</em> de piste de position</span><span class="sxs-lookup"><span data-stu-id="387c1-133">position track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-134">ready</span><span class="sxs-lookup"><span data-stu-id="387c1-134">ready</span></span></li>
<li><span data-ttu-id="387c1-135">position de départ</span><span class="sxs-lookup"><span data-stu-id="387c1-135">start position</span></span></li>
<li><span data-ttu-id="387c1-136">format horaire</span><span class="sxs-lookup"><span data-stu-id="387c1-136">time format</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-137">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="387c1-137">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="387c1-138">audio</span><span class="sxs-lookup"><span data-stu-id="387c1-138">audio</span></span></li>
<li><span data-ttu-id="387c1-139">alignement audio</span><span class="sxs-lookup"><span data-stu-id="387c1-139">audio alignment</span></span></li>
<li><span data-ttu-id="387c1-140">BitsPerSample audio</span><span class="sxs-lookup"><span data-stu-id="387c1-140">audio bitspersample</span></span></li>
<li><span data-ttu-id="387c1-141">sauts audio</span><span class="sxs-lookup"><span data-stu-id="387c1-141">audio breaks</span></span></li>
<li><span data-ttu-id="387c1-142">bytespersec audio</span><span class="sxs-lookup"><span data-stu-id="387c1-142">audio bytespersec</span></span></li>
<li><span data-ttu-id="387c1-143">entrée audio</span><span class="sxs-lookup"><span data-stu-id="387c1-143">audio input</span></span></li>
<li><span data-ttu-id="387c1-144">enregistrement audio</span><span class="sxs-lookup"><span data-stu-id="387c1-144">audio record</span></span></li>
<li><span data-ttu-id="387c1-145">source audio</span><span class="sxs-lookup"><span data-stu-id="387c1-145">audio source</span></span></li>
<li><span data-ttu-id="387c1-146">SamplesPerSec audio</span><span class="sxs-lookup"><span data-stu-id="387c1-146">audio samplespersec</span></span></li>
<li><span data-ttu-id="387c1-147">flux audio</span><span class="sxs-lookup"><span data-stu-id="387c1-147">audio stream</span></span></li>
<li><span data-ttu-id="387c1-148">graves</span><span class="sxs-lookup"><span data-stu-id="387c1-148">bass</span></span></li>
<li><span data-ttu-id="387c1-149">bitsperpel</span><span class="sxs-lookup"><span data-stu-id="387c1-149">bitsperpel</span></span></li>
<li><span data-ttu-id="387c1-150">luminosité</span><span class="sxs-lookup"><span data-stu-id="387c1-150">brightness</span></span></li>
<li><span data-ttu-id="387c1-151">color</span><span class="sxs-lookup"><span data-stu-id="387c1-151">color</span></span></li>
<li><span data-ttu-id="387c1-152">élevé</span><span class="sxs-lookup"><span data-stu-id="387c1-152">contrast</span></span></li>
<li><span data-ttu-id="387c1-153">piste actuelle</span><span class="sxs-lookup"><span data-stu-id="387c1-153">current track</span></span></li>
<li><span data-ttu-id="387c1-154"><em>lecteur</em> d’espace disque</span><span class="sxs-lookup"><span data-stu-id="387c1-154">disk space <em>drive</em></span></span></li>
<li><span data-ttu-id="387c1-155">saisie semi-automatique des fichiers</span><span class="sxs-lookup"><span data-stu-id="387c1-155">file completion</span></span></li>
<li><span data-ttu-id="387c1-156">format de fichier</span><span class="sxs-lookup"><span data-stu-id="387c1-156">file format</span></span></li>
<li><span data-ttu-id="387c1-157">mode de fichier</span><span class="sxs-lookup"><span data-stu-id="387c1-157">file mode</span></span></li>
<li><span data-ttu-id="387c1-158">forward</span><span class="sxs-lookup"><span data-stu-id="387c1-158">forward</span></span></li>
<li><span data-ttu-id="387c1-159">frames ignorés</span><span class="sxs-lookup"><span data-stu-id="387c1-159">frames skipped</span></span></li>
<li><span data-ttu-id="387c1-160">gamma</span><span class="sxs-lookup"><span data-stu-id="387c1-160">gamma</span></span></li>
<li><span data-ttu-id="387c1-161">entrée</span><span class="sxs-lookup"><span data-stu-id="387c1-161">input</span></span></li>
<li><span data-ttu-id="387c1-162">volume de gauche</span><span class="sxs-lookup"><span data-stu-id="387c1-162">left volume</span></span></li>
<li><span data-ttu-id="387c1-163">length</span><span class="sxs-lookup"><span data-stu-id="387c1-163">length</span></span></li>
<li><span data-ttu-id="387c1-164"><em>nombre</em> de pistes de longueur</span><span class="sxs-lookup"><span data-stu-id="387c1-164">length track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-165">support présent</span><span class="sxs-lookup"><span data-stu-id="387c1-165">media present</span></span></li>
<li><span data-ttu-id="387c1-166">mode</span><span class="sxs-lookup"><span data-stu-id="387c1-166">mode</span></span></li>
<li><span data-ttu-id="387c1-167">monitor</span><span class="sxs-lookup"><span data-stu-id="387c1-167">monitor</span></span></li>
<li><span data-ttu-id="387c1-168">méthode Monitor</span><span class="sxs-lookup"><span data-stu-id="387c1-168">monitor method</span></span></li>
<li><span data-ttu-id="387c1-169">minime</span><span class="sxs-lookup"><span data-stu-id="387c1-169">nominal</span></span></li>
<li><span data-ttu-id="387c1-170">fréquence d’images nominales</span><span class="sxs-lookup"><span data-stu-id="387c1-170">nominal frame rate</span></span></li>
<li><span data-ttu-id="387c1-171">fréquence des images d’enregistrement nominales</span><span class="sxs-lookup"><span data-stu-id="387c1-171">nominal record frame rate</span></span></li>
<li><span data-ttu-id="387c1-172">nombre de pistes</span><span class="sxs-lookup"><span data-stu-id="387c1-172">number of tracks</span></span></li>
<li><span data-ttu-id="387c1-173">sortie</span><span class="sxs-lookup"><span data-stu-id="387c1-173">output</span></span></li>
<li><span data-ttu-id="387c1-174">handle de palette</span><span class="sxs-lookup"><span data-stu-id="387c1-174">palette handle</span></span></li>
<li><span data-ttu-id="387c1-175">mode pause</span><span class="sxs-lookup"><span data-stu-id="387c1-175">pause mode</span></span></li>
<li><span data-ttu-id="387c1-176">Vitesse de lecture</span><span class="sxs-lookup"><span data-stu-id="387c1-176">play speed</span></span></li>
<li><span data-ttu-id="387c1-177">position</span><span class="sxs-lookup"><span data-stu-id="387c1-177">position</span></span></li>
<li><span data-ttu-id="387c1-178"><em>numéro</em> de piste de position</span><span class="sxs-lookup"><span data-stu-id="387c1-178">position track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-179">ready</span><span class="sxs-lookup"><span data-stu-id="387c1-179">ready</span></span></li>
<li><span data-ttu-id="387c1-180">fréquence des trames d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="387c1-180">record frame rate</span></span></li>
<li><span data-ttu-id="387c1-181"><em>Frame</em> de référence</span><span class="sxs-lookup"><span data-stu-id="387c1-181">reference <em>frame</em></span></span></li>
<li><span data-ttu-id="387c1-182">taille réservée</span><span class="sxs-lookup"><span data-stu-id="387c1-182">reserved size</span></span></li>
<li><span data-ttu-id="387c1-183">volume approprié</span><span class="sxs-lookup"><span data-stu-id="387c1-183">right volume</span></span></li>
<li><span data-ttu-id="387c1-184">Rechercher exactement</span><span class="sxs-lookup"><span data-stu-id="387c1-184">seek exactly</span></span></li>
<li><span data-ttu-id="387c1-185">netteté</span><span class="sxs-lookup"><span data-stu-id="387c1-185">sharpness</span></span></li>
<li><span data-ttu-id="387c1-186">intégrant</span><span class="sxs-lookup"><span data-stu-id="387c1-186">smpte</span></span></li>
<li><span data-ttu-id="387c1-187">speed</span><span class="sxs-lookup"><span data-stu-id="387c1-187">speed</span></span></li>
<li><span data-ttu-id="387c1-188">position de départ</span><span class="sxs-lookup"><span data-stu-id="387c1-188">start position</span></span></li>
<li><span data-ttu-id="387c1-189">format de fichier toujours</span><span class="sxs-lookup"><span data-stu-id="387c1-189">still file format</span></span></li>
<li><span data-ttu-id="387c1-190">format horaire</span><span class="sxs-lookup"><span data-stu-id="387c1-190">time format</span></span></li>
<li><span data-ttu-id="387c1-191">teinté</span><span class="sxs-lookup"><span data-stu-id="387c1-191">tint</span></span></li>
<li><span data-ttu-id="387c1-192">les aigus</span><span class="sxs-lookup"><span data-stu-id="387c1-192">treble</span></span></li>
<li><span data-ttu-id="387c1-193">non enregistrées</span><span class="sxs-lookup"><span data-stu-id="387c1-193">unsaved</span></span></li>
<li><span data-ttu-id="387c1-194">video</span><span class="sxs-lookup"><span data-stu-id="387c1-194">video</span></span></li>
<li><span data-ttu-id="387c1-195">index de clé vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-195">video key index</span></span></li>
<li><span data-ttu-id="387c1-196">couleur de la touche vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-196">video key color</span></span></li>
<li><span data-ttu-id="387c1-197">enregistrement vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-197">video record</span></span></li>
<li><span data-ttu-id="387c1-198">source vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-198">video source</span></span></li>
<li><span data-ttu-id="387c1-199">Numéro de la source vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-199">video source number</span></span></li>
<li><span data-ttu-id="387c1-200">flux vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-200">video stream</span></span></li>
<li><span data-ttu-id="387c1-201">volume</span><span class="sxs-lookup"><span data-stu-id="387c1-201">volume</span></span></li>
<li><span data-ttu-id="387c1-202">handle de fenêtre</span><span class="sxs-lookup"><span data-stu-id="387c1-202">window handle</span></span></li>
<li><span data-ttu-id="387c1-203">fenêtre visible</span><span class="sxs-lookup"><span data-stu-id="387c1-203">window visible</span></span></li>
<li><span data-ttu-id="387c1-204">fenêtre réduite</span><span class="sxs-lookup"><span data-stu-id="387c1-204">window minimized</span></span></li>
<li><span data-ttu-id="387c1-205">fenêtre agrandie</span><span class="sxs-lookup"><span data-stu-id="387c1-205">window maximized</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-206">superposition</span><span class="sxs-lookup"><span data-stu-id="387c1-206">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="387c1-207">support présent</span><span class="sxs-lookup"><span data-stu-id="387c1-207">media present</span></span></li>
<li><span data-ttu-id="387c1-208">mode</span><span class="sxs-lookup"><span data-stu-id="387c1-208">mode</span></span></li>
<li><span data-ttu-id="387c1-209">nombre de pistes</span><span class="sxs-lookup"><span data-stu-id="387c1-209">number of tracks</span></span></li>
<li><span data-ttu-id="387c1-210">ready</span><span class="sxs-lookup"><span data-stu-id="387c1-210">ready</span></span></li>
<li><span data-ttu-id="387c1-211">étirement</span><span class="sxs-lookup"><span data-stu-id="387c1-211">stretch</span></span></li>
<li><span data-ttu-id="387c1-212">handle de fenêtre</span><span class="sxs-lookup"><span data-stu-id="387c1-212">window handle</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-213">sequencer</span><span class="sxs-lookup"><span data-stu-id="387c1-213">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="387c1-214">piste actuelle</span><span class="sxs-lookup"><span data-stu-id="387c1-214">current track</span></span></li>
<li><span data-ttu-id="387c1-215">type de division</span><span class="sxs-lookup"><span data-stu-id="387c1-215">division type</span></span></li>
<li><span data-ttu-id="387c1-216">length</span><span class="sxs-lookup"><span data-stu-id="387c1-216">length</span></span></li>
<li><span data-ttu-id="387c1-217">longueur du <em>numéro</em> de suivi de la longueur</span><span class="sxs-lookup"><span data-stu-id="387c1-217">length track <em>number</em> master</span></span></li>
<li><span data-ttu-id="387c1-218">support présent</span><span class="sxs-lookup"><span data-stu-id="387c1-218">media present</span></span></li>
<li><span data-ttu-id="387c1-219">mode</span><span class="sxs-lookup"><span data-stu-id="387c1-219">mode</span></span></li>
<li><span data-ttu-id="387c1-220">nombre de pistes</span><span class="sxs-lookup"><span data-stu-id="387c1-220">number of tracks</span></span></li>
<li><span data-ttu-id="387c1-221">offset</span><span class="sxs-lookup"><span data-stu-id="387c1-221">offset</span></span></li>
<li><span data-ttu-id="387c1-222">port</span><span class="sxs-lookup"><span data-stu-id="387c1-222">port</span></span></li>
<li><span data-ttu-id="387c1-223">position</span><span class="sxs-lookup"><span data-stu-id="387c1-223">position</span></span></li>
<li><span data-ttu-id="387c1-224"><em>numéro</em> de piste de position</span><span class="sxs-lookup"><span data-stu-id="387c1-224">position track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-225">ready</span><span class="sxs-lookup"><span data-stu-id="387c1-225">ready</span></span></li>
<li><span data-ttu-id="387c1-226">subordonné</span><span class="sxs-lookup"><span data-stu-id="387c1-226">slave</span></span></li>
<li><span data-ttu-id="387c1-227">position de départ</span><span class="sxs-lookup"><span data-stu-id="387c1-227">start position</span></span></li>
<li><span data-ttu-id="387c1-228">tempo</span><span class="sxs-lookup"><span data-stu-id="387c1-228">tempo</span></span></li>
<li><span data-ttu-id="387c1-229">format horaire</span><span class="sxs-lookup"><span data-stu-id="387c1-229">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-230">vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-230">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="387c1-231">enregistrement d’assemblage</span><span class="sxs-lookup"><span data-stu-id="387c1-231">assemble record</span></span></li>
<li><span data-ttu-id="387c1-232">moniteur audio</span><span class="sxs-lookup"><span data-stu-id="387c1-232">audio monitor</span></span></li>
<li><span data-ttu-id="387c1-233">Numéro de moniteur audio</span><span class="sxs-lookup"><span data-stu-id="387c1-233">audio monitor number</span></span></li>
<li><span data-ttu-id="387c1-234">enregistrement audio</span><span class="sxs-lookup"><span data-stu-id="387c1-234">audio record</span></span></li>
<li><span data-ttu-id="387c1-235"><em>numéro</em> de piste d’enregistrement audio</span><span class="sxs-lookup"><span data-stu-id="387c1-235">audio record track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-236">source audio</span><span class="sxs-lookup"><span data-stu-id="387c1-236">audio source</span></span></li>
<li><span data-ttu-id="387c1-237">Numéro de la source audio</span><span class="sxs-lookup"><span data-stu-id="387c1-237">audio source number</span></span></li>
<li><span data-ttu-id="387c1-238">channel</span><span class="sxs-lookup"><span data-stu-id="387c1-238">channel</span></span></li>
<li><span data-ttu-id="387c1-239"><em>numéro</em> de récepteur de canal</span><span class="sxs-lookup"><span data-stu-id="387c1-239">channel tuner <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-240">horloge</span><span class="sxs-lookup"><span data-stu-id="387c1-240">clock</span></span></li>
<li><span data-ttu-id="387c1-241">ID de l’horloge</span><span class="sxs-lookup"><span data-stu-id="387c1-241">clock id</span></span></li>
<li><span data-ttu-id="387c1-242">counter</span><span class="sxs-lookup"><span data-stu-id="387c1-242">counter</span></span></li>
<li><span data-ttu-id="387c1-243">format du compteur</span><span class="sxs-lookup"><span data-stu-id="387c1-243">counter format</span></span></li>
<li><span data-ttu-id="387c1-244">résolution de compteur</span><span class="sxs-lookup"><span data-stu-id="387c1-244">counter resolution</span></span></li>
<li><span data-ttu-id="387c1-245">piste actuelle</span><span class="sxs-lookup"><span data-stu-id="387c1-245">current track</span></span></li>
<li><span data-ttu-id="387c1-246">fréquence d’images</span><span class="sxs-lookup"><span data-stu-id="387c1-246">frame rate</span></span></li>
<li><span data-ttu-id="387c1-247">index</span><span class="sxs-lookup"><span data-stu-id="387c1-247">index</span></span></li>
<li><span data-ttu-id="387c1-248">index sur</span><span class="sxs-lookup"><span data-stu-id="387c1-248">index on</span></span></li>
<li><span data-ttu-id="387c1-249">length</span><span class="sxs-lookup"><span data-stu-id="387c1-249">length</span></span></li>
<li><span data-ttu-id="387c1-250"><em>nombre</em> de pistes de longueur</span><span class="sxs-lookup"><span data-stu-id="387c1-250">length track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-251">support présent</span><span class="sxs-lookup"><span data-stu-id="387c1-251">media present</span></span></li>
<li><span data-ttu-id="387c1-252">type de média</span><span class="sxs-lookup"><span data-stu-id="387c1-252">media type</span></span></li>
<li><span data-ttu-id="387c1-253">mode</span><span class="sxs-lookup"><span data-stu-id="387c1-253">mode</span></span></li>
<li><span data-ttu-id="387c1-254">nombre de pistes audio</span><span class="sxs-lookup"><span data-stu-id="387c1-254">number of audio tracks</span></span></li>
<li><span data-ttu-id="387c1-255">nombre de pistes</span><span class="sxs-lookup"><span data-stu-id="387c1-255">number of tracks</span></span></li>
<li><span data-ttu-id="387c1-256">nombre de pistes vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-256">number of video tracks</span></span></li>
<li><span data-ttu-id="387c1-257"><em>délai d’attente</em> de pause</span><span class="sxs-lookup"><span data-stu-id="387c1-257">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="387c1-258">format de lecture</span><span class="sxs-lookup"><span data-stu-id="387c1-258">play format</span></span></li>
<li><span data-ttu-id="387c1-259">position</span><span class="sxs-lookup"><span data-stu-id="387c1-259">position</span></span></li>
<li><span data-ttu-id="387c1-260">début de la position</span><span class="sxs-lookup"><span data-stu-id="387c1-260">position start</span></span></li>
<li><span data-ttu-id="387c1-261"><em>numéro</em> de piste de position</span><span class="sxs-lookup"><span data-stu-id="387c1-261">position track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-262"><em>durée</em> de Postroll</span><span class="sxs-lookup"><span data-stu-id="387c1-262">postroll <em>duration</em></span></span></li>
<li><span data-ttu-id="387c1-263">Sous tension</span><span class="sxs-lookup"><span data-stu-id="387c1-263">power on</span></span></li>
<li><span data-ttu-id="387c1-264"><em>durée</em> du préroll</span><span class="sxs-lookup"><span data-stu-id="387c1-264">preroll <em>duration</em></span></span></li>
<li><span data-ttu-id="387c1-265">ready</span><span class="sxs-lookup"><span data-stu-id="387c1-265">ready</span></span></li>
<li><span data-ttu-id="387c1-266">format d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="387c1-266">record format</span></span></li>
<li><span data-ttu-id="387c1-267">speed</span><span class="sxs-lookup"><span data-stu-id="387c1-267">speed</span></span></li>
<li><span data-ttu-id="387c1-268">format horaire</span><span class="sxs-lookup"><span data-stu-id="387c1-268">time format</span></span></li>
<li><span data-ttu-id="387c1-269">mode heure</span><span class="sxs-lookup"><span data-stu-id="387c1-269">time mode</span></span></li>
<li><span data-ttu-id="387c1-270">type de temps</span><span class="sxs-lookup"><span data-stu-id="387c1-270">time type</span></span></li>
<li><span data-ttu-id="387c1-271">code temporel présent</span><span class="sxs-lookup"><span data-stu-id="387c1-271">timecode present</span></span></li>
<li><span data-ttu-id="387c1-272">enregistrement du code temporel</span><span class="sxs-lookup"><span data-stu-id="387c1-272">timecode record</span></span></li>
<li><span data-ttu-id="387c1-273">type de code temporel</span><span class="sxs-lookup"><span data-stu-id="387c1-273">timecode type</span></span></li>
<li><span data-ttu-id="387c1-274">Numéro de tuner</span><span class="sxs-lookup"><span data-stu-id="387c1-274">tuner number</span></span></li>
<li><span data-ttu-id="387c1-275">moniteur vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-275">video monitor</span></span></li>
<li><span data-ttu-id="387c1-276">Numéro du moniteur vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-276">video monitor number</span></span></li>
<li><span data-ttu-id="387c1-277">enregistrement vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-277">video record</span></span></li>
<li><span data-ttu-id="387c1-278"><em>numéro</em> de piste de l’enregistrement vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-278">video record track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-279">source vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-279">video source</span></span></li>
<li><span data-ttu-id="387c1-280">Numéro de la source vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-280">video source number</span></span></li>
<li><span data-ttu-id="387c1-281">protégé en écriture</span><span class="sxs-lookup"><span data-stu-id="387c1-281">write protected</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-282">videodisc</span><span class="sxs-lookup"><span data-stu-id="387c1-282">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="387c1-283">piste actuelle</span><span class="sxs-lookup"><span data-stu-id="387c1-283">current track</span></span></li>
<li><span data-ttu-id="387c1-284">taille du disque</span><span class="sxs-lookup"><span data-stu-id="387c1-284">disc size</span></span></li>
<li><span data-ttu-id="387c1-285">forward</span><span class="sxs-lookup"><span data-stu-id="387c1-285">forward</span></span></li>
<li><span data-ttu-id="387c1-286">length</span><span class="sxs-lookup"><span data-stu-id="387c1-286">length</span></span></li>
<li><span data-ttu-id="387c1-287"><em>nombre</em> de pistes de longueur</span><span class="sxs-lookup"><span data-stu-id="387c1-287">length track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-288">support présent</span><span class="sxs-lookup"><span data-stu-id="387c1-288">media present</span></span></li>
<li><span data-ttu-id="387c1-289">type de média</span><span class="sxs-lookup"><span data-stu-id="387c1-289">media type</span></span></li>
<li><span data-ttu-id="387c1-290">mode</span><span class="sxs-lookup"><span data-stu-id="387c1-290">mode</span></span></li>
<li><span data-ttu-id="387c1-291">nombre de pistes</span><span class="sxs-lookup"><span data-stu-id="387c1-291">number of tracks</span></span></li>
<li><span data-ttu-id="387c1-292">position</span><span class="sxs-lookup"><span data-stu-id="387c1-292">position</span></span></li>
<li><span data-ttu-id="387c1-293"><em>numéro</em> de piste de position</span><span class="sxs-lookup"><span data-stu-id="387c1-293">position track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-294">ready</span><span class="sxs-lookup"><span data-stu-id="387c1-294">ready</span></span></li>
<li><span data-ttu-id="387c1-295">initi</span><span class="sxs-lookup"><span data-stu-id="387c1-295">side</span></span></li>
<li><span data-ttu-id="387c1-296">speed</span><span class="sxs-lookup"><span data-stu-id="387c1-296">speed</span></span></li>
<li><span data-ttu-id="387c1-297">position de départ</span><span class="sxs-lookup"><span data-stu-id="387c1-297">start position</span></span></li>
<li><span data-ttu-id="387c1-298">format horaire</span><span class="sxs-lookup"><span data-stu-id="387c1-298">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-299">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="387c1-299">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="387c1-300">alignement</span><span class="sxs-lookup"><span data-stu-id="387c1-300">alignment</span></span></li>
<li><span data-ttu-id="387c1-301">bitspersample</span><span class="sxs-lookup"><span data-stu-id="387c1-301">bitspersample</span></span></li>
<li><span data-ttu-id="387c1-302">bytespersec</span><span class="sxs-lookup"><span data-stu-id="387c1-302">bytespersec</span></span></li>
<li><span data-ttu-id="387c1-303">channels</span><span class="sxs-lookup"><span data-stu-id="387c1-303">channels</span></span></li>
<li><span data-ttu-id="387c1-304">piste actuelle</span><span class="sxs-lookup"><span data-stu-id="387c1-304">current track</span></span></li>
<li><span data-ttu-id="387c1-305">balise de format</span><span class="sxs-lookup"><span data-stu-id="387c1-305">format tag</span></span></li>
<li><span data-ttu-id="387c1-306">entrée</span><span class="sxs-lookup"><span data-stu-id="387c1-306">input</span></span></li>
<li><span data-ttu-id="387c1-307">length</span><span class="sxs-lookup"><span data-stu-id="387c1-307">length</span></span></li>
<li><span data-ttu-id="387c1-308"><em>nombre</em> de pistes de longueur</span><span class="sxs-lookup"><span data-stu-id="387c1-308">length track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-309">niveau</span><span class="sxs-lookup"><span data-stu-id="387c1-309">level</span></span></li>
<li><span data-ttu-id="387c1-310">support présent</span><span class="sxs-lookup"><span data-stu-id="387c1-310">media present</span></span></li>
<li><span data-ttu-id="387c1-311">mode</span><span class="sxs-lookup"><span data-stu-id="387c1-311">mode</span></span></li>
<li><span data-ttu-id="387c1-312">nombre de pistes</span><span class="sxs-lookup"><span data-stu-id="387c1-312">number of tracks</span></span></li>
<li><span data-ttu-id="387c1-313">sortie</span><span class="sxs-lookup"><span data-stu-id="387c1-313">output</span></span></li>
<li><span data-ttu-id="387c1-314">position</span><span class="sxs-lookup"><span data-stu-id="387c1-314">position</span></span></li>
<li><span data-ttu-id="387c1-315"><em>numéro</em> de piste de position</span><span class="sxs-lookup"><span data-stu-id="387c1-315">position track <em>number</em></span></span></li>
<li><span data-ttu-id="387c1-316">ready</span><span class="sxs-lookup"><span data-stu-id="387c1-316">ready</span></span></li>
<li><span data-ttu-id="387c1-317">samplespersec</span><span class="sxs-lookup"><span data-stu-id="387c1-317">samplespersec</span></span></li>
<li><span data-ttu-id="387c1-318">position de départ</span><span class="sxs-lookup"><span data-stu-id="387c1-318">start position</span></span></li>
<li><span data-ttu-id="387c1-319">format horaire</span><span class="sxs-lookup"><span data-stu-id="387c1-319">time format</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="387c1-320">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszRequest** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="387c1-320">The following table lists the flags that can be specified in the **lpszRequest** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="387c1-321">Valeur</span><span class="sxs-lookup"><span data-stu-id="387c1-321">Value</span></span></th>
<th><span data-ttu-id="387c1-322">Signification</span><span class="sxs-lookup"><span data-stu-id="387c1-322">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="387c1-323">alignement</span><span class="sxs-lookup"><span data-stu-id="387c1-323">alignment</span></span></td>
<td><span data-ttu-id="387c1-324">Retourne l’alignement de bloc des données, en octets.</span><span class="sxs-lookup"><span data-stu-id="387c1-324">Returns the block alignment of data, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-325">enregistrement d’assemblage</span><span class="sxs-lookup"><span data-stu-id="387c1-325">assemble record</span></span></td>
<td><span data-ttu-id="387c1-326">Retourne la <strong>valeur true</strong> si l’appareil est configuré pour l’enregistrement en mode d’assemblage.</span><span class="sxs-lookup"><span data-stu-id="387c1-326">Returns <strong>TRUE</strong> if the device is set to assemble mode recording.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-327">audio</span><span class="sxs-lookup"><span data-stu-id="387c1-327">audio</span></span></td>
<td><span data-ttu-id="387c1-328">Retourne &quot; on &quot; ou &quot; OFF &quot; selon la commande <a href="setaudio.md">SetAudio</a> &quot; on &quot; ou OFF la plus &quot; récente &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-328">Returns &quot;on&quot; or &quot;off&quot; depending on the most recent <a href="setaudio.md">setaudio</a> &quot;on&quot; or &quot;off&quot; command.</span></span> <span data-ttu-id="387c1-329">Elle retourne la valeur &quot; &quot; si un ou les deux enceintes sont activées, et &quot; désactivent dans le &quot; cas contraire.</span><span class="sxs-lookup"><span data-stu-id="387c1-329">It returns &quot;on&quot; if either or both speakers are enabled, and &quot;off&quot; otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-330">alignement audio</span><span class="sxs-lookup"><span data-stu-id="387c1-330">audio alignment</span></span></td>
<td><span data-ttu-id="387c1-331">Retourne l’alignement des blocs de données par rapport au début des données Waveform-Audio en entrée.</span><span class="sxs-lookup"><span data-stu-id="387c1-331">Returns the alignment of data blocks relative to the start of input waveform-audio data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-332">BitsPerSample audio</span><span class="sxs-lookup"><span data-stu-id="387c1-332">audio bitspersample</span></span></td>
<td><span data-ttu-id="387c1-333">Retourne le nombre de bits par échantillon que l’appareil utilise pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="387c1-333">Returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="387c1-334">Cet indicateur s’applique uniquement aux appareils prenant en charge l' &quot; &quot; algorithme PCM.</span><span class="sxs-lookup"><span data-stu-id="387c1-334">This flag applies only to devices supporting the &quot;pcm&quot; algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-335">sauts audio</span><span class="sxs-lookup"><span data-stu-id="387c1-335">audio breaks</span></span></td>
<td><span data-ttu-id="387c1-336">Retourne le nombre de fois que la partie audio de la dernière séquence AVI a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="387c1-336">Returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="387c1-337">Le système compte un saut audio chaque fois qu’il tente d’écrire des données audio sur le pilote de périphérique et découvre que le pilote a déjà lu toutes les données disponibles.</span><span class="sxs-lookup"><span data-stu-id="387c1-337">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="387c1-338">Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="387c1-338">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="387c1-339">Il est destiné uniquement à l’évaluation des performances ; la valeur de retour est difficile à interpréter.</span><span class="sxs-lookup"><span data-stu-id="387c1-339">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-340">bytespersec audio</span><span class="sxs-lookup"><span data-stu-id="387c1-340">audio bytespersec</span></span></td>
<td><span data-ttu-id="387c1-341">Retourne le nombre moyen d’octets par seconde utilisés pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="387c1-341">Returns the average number of bytes per second used for recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-342">entrée audio</span><span class="sxs-lookup"><span data-stu-id="387c1-342">audio input</span></span></td>
<td><span data-ttu-id="387c1-343">Retourne le niveau audio instantané approximatif du signal audio d’entrée analogique.</span><span class="sxs-lookup"><span data-stu-id="387c1-343">Returns the approximate instantaneous audio level of the analog input audio signal.</span></span> <span data-ttu-id="387c1-344">Une valeur supérieure à 1000 implique une déformation de découpage.</span><span class="sxs-lookup"><span data-stu-id="387c1-344">A value greater than 1000 implies clipping distortion.</span></span> <span data-ttu-id="387c1-345">Certains appareils peuvent retourner cette valeur uniquement lors de l’enregistrement audio.</span><span class="sxs-lookup"><span data-stu-id="387c1-345">Some devices can return this value only while recording audio.</span></span> <span data-ttu-id="387c1-346">La valeur n’a pas de commande <a href="set.md">Set</a> ou <a href="setaudio.md">SetAudio</a> associée.</span><span class="sxs-lookup"><span data-stu-id="387c1-346">The value has no associated <a href="set.md">set</a> or <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-347">moniteur audio</span><span class="sxs-lookup"><span data-stu-id="387c1-347">audio monitor</span></span></td>
<td><span data-ttu-id="387c1-348">Retourne &quot; &quot; la sortie ou l’un des types d’entrée source valides.</span><span class="sxs-lookup"><span data-stu-id="387c1-348">Returns &quot;output&quot;, or one of the valid source-input types.</span></span> <span data-ttu-id="387c1-349">Pour plus d’informations, consultez la commande <strong>SetAudio</strong> &quot; Monitor &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-349">For more information, see the <strong>setaudio</strong> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-350">Numéro de moniteur audio</span><span class="sxs-lookup"><span data-stu-id="387c1-350">audio monitor number</span></span></td>
<td><span data-ttu-id="387c1-351">Retourne le numéro vidéo surveillée du type spécifié par le moniteur d' <strong>État</strong> &quot; audio &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-351">Returns the monitored-video number of the type specified by <strong>status</strong> &quot;audio monitor&quot;.</span></span> <span data-ttu-id="387c1-352">Pour plus d’informations, consultez la commande <a href="setaudio.md">SetAudio</a> .</span><span class="sxs-lookup"><span data-stu-id="387c1-352">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-353">enregistrement audio</span><span class="sxs-lookup"><span data-stu-id="387c1-353">audio record</span></span></td>
<td><span data-ttu-id="387c1-354">Retourne &quot; on &quot; ou &quot; OFF &quot; , en reflétant l’état défini par l’enregistrement <strong>SetAudio</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-354">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by <strong>setaudio</strong> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-355"><em>numéro</em> de piste d’enregistrement audio</span><span class="sxs-lookup"><span data-stu-id="387c1-355">audio record track <em>number</em></span></span></td>
<td><span data-ttu-id="387c1-356">Renvoie la <strong>valeur true</strong> si le magnétoscope est configuré pour enregistrer l’audio.</span><span class="sxs-lookup"><span data-stu-id="387c1-356">Returns <strong>TRUE</strong> if the VCR is set to record audio.</span></span> <span data-ttu-id="387c1-357">Si aucun numéro de piste n’est indiqué, la valeur par défaut de 1 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="387c1-357">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-358">SamplesPerSec audio</span><span class="sxs-lookup"><span data-stu-id="387c1-358">audio samplespersec</span></span></td>
<td><span data-ttu-id="387c1-359">Retourne le nombre d’échantillons par seconde enregistrés.</span><span class="sxs-lookup"><span data-stu-id="387c1-359">Returns the number of samples per second recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-360">source audio</span><span class="sxs-lookup"><span data-stu-id="387c1-360">audio source</span></span></td>
<td><span data-ttu-id="387c1-361">Retourne la source de digitaliseur audio actuelle : &quot; gauche &quot; , &quot; droite &quot; , &quot; moyenne &quot; ou &quot; stéréo &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-361">Returns the current audio digitizer source: &quot;left&quot;, &quot;right&quot;, &quot;average&quot;, or &quot;stereo&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-362">Numéro de la source audio</span><span class="sxs-lookup"><span data-stu-id="387c1-362">audio source number</span></span></td>
<td><span data-ttu-id="387c1-363">Retourne le numéro de source audio du type retourné par la <strong></strong> &quot; source audio d’état &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-363">Returns the audio-source number of the type returned by <strong>status</strong> &quot;audio source&quot;.</span></span> <span data-ttu-id="387c1-364">Pour plus d’informations, consultez la commande <a href="setaudio.md">SetAudio</a> .</span><span class="sxs-lookup"><span data-stu-id="387c1-364">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-365">flux audio</span><span class="sxs-lookup"><span data-stu-id="387c1-365">audio stream</span></span></td>
<td><span data-ttu-id="387c1-366">Retourne le numéro du flux audio actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-366">Returns the current audio-stream number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-367">graves</span><span class="sxs-lookup"><span data-stu-id="387c1-367">bass</span></span></td>
<td><span data-ttu-id="387c1-368">Retourne le niveau audio-Bass actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-368">Returns the current audio-bass level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-369">bitsperpel</span><span class="sxs-lookup"><span data-stu-id="387c1-369">bitsperpel</span></span></td>
<td><span data-ttu-id="387c1-370">Retourne le nombre de bits par pixel pour l’enregistrement des données capturées ou enregistrées.</span><span class="sxs-lookup"><span data-stu-id="387c1-370">Returns the number of bits per pixel for saving captured or recorded data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-371">bitspersample</span><span class="sxs-lookup"><span data-stu-id="387c1-371">bitspersample</span></span></td>
<td><span data-ttu-id="387c1-372">Retourne les bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="387c1-372">Returns the bits per sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-373">luminosité</span><span class="sxs-lookup"><span data-stu-id="387c1-373">brightness</span></span></td>
<td><span data-ttu-id="387c1-374">Retourne le niveau de luminosité vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-374">Returns the current video-brightness level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-375">bytespersec</span><span class="sxs-lookup"><span data-stu-id="387c1-375">bytespersec</span></span></td>
<td><span data-ttu-id="387c1-376">Retourne le nombre moyen d’octets par seconde lus ou enregistrés.</span><span class="sxs-lookup"><span data-stu-id="387c1-376">Returns the average number of bytes per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-377"><em>numéro</em> de suivi de type cdaudio</span><span class="sxs-lookup"><span data-stu-id="387c1-377">cdaudio type track <em>number</em></span></span></td>
<td><span data-ttu-id="387c1-378">Retourne le type du numéro de piste spécifié.</span><span class="sxs-lookup"><span data-stu-id="387c1-378">Returns the type of the specified track number.</span></span> <span data-ttu-id="387c1-379">Il peut s’agir &quot; de l’audio ou d’un &quot; &quot; autre.&quot;</span><span class="sxs-lookup"><span data-stu-id="387c1-379">This can be &quot;audio&quot; or &quot;other.&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-380">channel</span><span class="sxs-lookup"><span data-stu-id="387c1-380">channel</span></span></td>
<td><span data-ttu-id="387c1-381">Retourne la valeur entière du canal défini sur le tuner.</span><span class="sxs-lookup"><span data-stu-id="387c1-381">Returns the integer value of the channel set on the tuner.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-382"><em>numéro</em> de récepteur de canal</span><span class="sxs-lookup"><span data-stu-id="387c1-382">channel tuner <em>number</em></span></span></td>
<td><span data-ttu-id="387c1-383">Si &quot; le &quot; <em>numéro</em> de tuner est donné, le canal actuellement sélectionné sur le <em>numéro</em> de tuner logique est retourné.</span><span class="sxs-lookup"><span data-stu-id="387c1-383">If &quot;tuner&quot; <em>number</em> is given, then the currently selected channel on the logical tuner <em>number</em> will be returned.</span></span> <span data-ttu-id="387c1-384">Notez qu’il peut y avoir plusieurs tuners logiques.</span><span class="sxs-lookup"><span data-stu-id="387c1-384">Note that there can be several logical tuners.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-385">channels</span><span class="sxs-lookup"><span data-stu-id="387c1-385">channels</span></span></td>
<td><span data-ttu-id="387c1-386">Retourne le nombre de canaux définis (1 pour mono, 2 pour stéréo).</span><span class="sxs-lookup"><span data-stu-id="387c1-386">Returns the number of channels set (1 for mono, 2 for stereo).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-387">horloge</span><span class="sxs-lookup"><span data-stu-id="387c1-387">clock</span></span></td>
<td><span data-ttu-id="387c1-388">Retourne l’heure externe.</span><span class="sxs-lookup"><span data-stu-id="387c1-388">Returns the external time.</span></span> <span data-ttu-id="387c1-389">L’heure doit être un entier long non signé exprimant des incréments totaux.</span><span class="sxs-lookup"><span data-stu-id="387c1-389">The time must be an unsigned long integer expressing total increments.</span></span> <span data-ttu-id="387c1-390">Pour plus d’informations, consultez la commande vitesse d’incrément de l’horloge de <a href="capability.md">capacité</a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-390">For more information, see the <a href="capability.md">capability</a> &quot;clock increment rate&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-391">ID de l’horloge</span><span class="sxs-lookup"><span data-stu-id="387c1-391">clock id</span></span></td>
<td><span data-ttu-id="387c1-392">Retourne un entier unique identifiant l’horloge.</span><span class="sxs-lookup"><span data-stu-id="387c1-392">Returns a unique integer identifying the clock.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-393">color</span><span class="sxs-lookup"><span data-stu-id="387c1-393">color</span></span></td>
<td><span data-ttu-id="387c1-394">Retourne le niveau de couleur actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-394">Returns the current color level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-395">élevé</span><span class="sxs-lookup"><span data-stu-id="387c1-395">contrast</span></span></td>
<td><span data-ttu-id="387c1-396">Retourne le niveau de contraste actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-396">Returns the current contrast level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-397">counter</span><span class="sxs-lookup"><span data-stu-id="387c1-397">counter</span></span></td>
<td><span data-ttu-id="387c1-398">Retourne la position du compteur dans le format de compteur actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-398">Returns the counter position, in the current counter format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-399">format du compteur</span><span class="sxs-lookup"><span data-stu-id="387c1-399">counter format</span></span></td>
<td><span data-ttu-id="387c1-400">Retourne le format de compteur actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-400">Returns the current counter format.</span></span> <span data-ttu-id="387c1-401">Pour plus d’informations, consultez la commande <a href="set.md">Set</a> &quot; Counter format &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-401">For more information, see the <a href="set.md">set</a> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-402">résolution de compteur</span><span class="sxs-lookup"><span data-stu-id="387c1-402">counter resolution</span></span></td>
<td><span data-ttu-id="387c1-403">Retourne des &quot; images &quot; ou des &quot; secondes &quot; , indiquant la résolution du compteur.</span><span class="sxs-lookup"><span data-stu-id="387c1-403">Returns &quot;frames&quot; or &quot;seconds&quot;, indicating the counter's resolution.</span></span> <span data-ttu-id="387c1-404">Ce n’est pas la même chose que la précision.</span><span class="sxs-lookup"><span data-stu-id="387c1-404">This is not the same as accuracy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-405">piste actuelle</span><span class="sxs-lookup"><span data-stu-id="387c1-405">current track</span></span></td>
<td><span data-ttu-id="387c1-406">Retourne la piste actuelle. MCISEQ Sequencer retourne 1.</span><span class="sxs-lookup"><span data-stu-id="387c1-406">Returns the current track. The MCISEQ sequencer returns 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-407">taille du disque</span><span class="sxs-lookup"><span data-stu-id="387c1-407">disc size</span></span></td>
<td><span data-ttu-id="387c1-408">Retourne 8 ou 12, indiquant la taille du disque chargé, en pouces.</span><span class="sxs-lookup"><span data-stu-id="387c1-408">Returns either 8 or 12, indicating the size of the loaded disc in inches.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-409"><em>lecteur</em> d’espace disque</span><span class="sxs-lookup"><span data-stu-id="387c1-409">disk space <em>drive</em></span></span></td>
<td><span data-ttu-id="387c1-410">Retourne l’espace disque approximatif, dans le format d’heure actuel, qui peut être obtenu par une commande <a href="reserve.md">Reserve</a> pour le lecteur de disque spécifié <em>.</em></span><span class="sxs-lookup"><span data-stu-id="387c1-410">Returns the approximate disk space, in the current time format, that can be obtained by a <a href="reserve.md">reserve</a> command for the specified disk <em>drive.</em></span></span> <span data-ttu-id="387c1-411">Le <em>lecteur</em> est généralement spécifié sous la forme d’une lettre unique ou d’une lettre suivie d’un signe deux-points ( :).</span><span class="sxs-lookup"><span data-stu-id="387c1-411">The <em>drive</em> is usually specified as a single letter or a single letter followed by a colon (:).</span></span> <span data-ttu-id="387c1-412">Certains appareils peuvent toutefois utiliser un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="387c1-412">Some devices, however, might use a path.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-413">type de division</span><span class="sxs-lookup"><span data-stu-id="387c1-413">division type</span></span></td>
<td><span data-ttu-id="387c1-414">Retourne l’un des types de divisions de fichier suivants :</span><span class="sxs-lookup"><span data-stu-id="387c1-414">Returns one of the following file division types:</span></span>
<ul>
<li><span data-ttu-id="387c1-415">PPQN</span><span class="sxs-lookup"><span data-stu-id="387c1-415">PPQN</span></span></li>
<li><span data-ttu-id="387c1-416">Cadre SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="387c1-416">SMPTE 24 frame</span></span></li>
<li><span data-ttu-id="387c1-417">Cadre SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="387c1-417">SMPTE 25 frame</span></span></li>
<li><span data-ttu-id="387c1-418">Trame de dépôt SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="387c1-418">SMPTE 30 drop frame</span></span></li>
<li><span data-ttu-id="387c1-419">Trame de 30 SMPTE</span><span class="sxs-lookup"><span data-stu-id="387c1-419">SMPTE 30 frame</span></span></li>
</ul>
<br/> <span data-ttu-id="387c1-420">Utilisez ces informations pour déterminer le format du fichier MIDI et la signification des informations relatives au tempo et à la position.</span><span class="sxs-lookup"><span data-stu-id="387c1-420">Use this information to determine the format of the MIDI file and the meaning of tempo and position information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-421">saisie semi-automatique des fichiers</span><span class="sxs-lookup"><span data-stu-id="387c1-421">file completion</span></span></td>
<td><span data-ttu-id="387c1-422">Retourne le pourcentage estimé pendant lequel l’opération de <a href="load.md">chargement</a>, d' <a href="save.md">enregistrement</a>, de <a href="capture.md">capture</a>, de <a href="cut.md">couper</a>, de <a href="copy.md">copier</a>, de <a href="delete.md">suppression</a>, de <a href="paste.md">Collage</a>ou d' <a href="undo.md">annulation</a> a progressé.</span><span class="sxs-lookup"><span data-stu-id="387c1-422">Returns the estimated percentage a <a href="load.md">load</a>, <a href="save.md">save</a>, <a href="capture.md">capture</a>, <a href="cut.md">cut</a>, <a href="copy.md">copy</a>, <a href="delete.md">delete</a>, <a href="paste.md">paste</a>, or <a href="undo.md">undo</a> operation has progressed.</span></span> <span data-ttu-id="387c1-423">(Les applications peuvent l’utiliser pour fournir un indicateur visuel de la progression.)</span><span class="sxs-lookup"><span data-stu-id="387c1-423">(Applications can use this to provide a visual indicator of progress.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-424">format de fichier</span><span class="sxs-lookup"><span data-stu-id="387c1-424">file format</span></span></td>
<td><span data-ttu-id="387c1-425">Retourne le format de fichier actuel pour les <strong>commandes d'</strong> <a href="record.md">enregistrement</a> ou d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="387c1-425">Returns the current file format for <a href="record.md">record</a> or <strong>save</strong> commands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-426">mode de fichier</span><span class="sxs-lookup"><span data-stu-id="387c1-426">file mode</span></span></td>
<td><span data-ttu-id="387c1-427">Retourne le &quot; chargement &quot; , &quot; l’enregistrement &quot; , la &quot; modification ou l' &quot; &quot; inactivité &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-427">Returns &quot;loading&quot;, &quot;saving&quot;, &quot;editing&quot;, or &quot;idle&quot;.</span></span> <span data-ttu-id="387c1-428">Pendant une opération de <a href="load.md"><strong>chargement</strong></a> , elle retourne le &quot; chargement &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-428">During a <a href="load.md"><strong>load</strong></a> operation, it returns &quot;loading&quot;.</span></span> <span data-ttu-id="387c1-429">Lors des opérations d' <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>enregistrement</strong></a> et de <a href="capture.md"><strong>capture</strong></a> , &quot; l’enregistrement est retourné &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-429">During <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>save</strong></a> and <a href="capture.md"><strong>capture</strong></a> operations, it returns &quot;saving&quot;.</span></span> <span data-ttu-id="387c1-430">Pendant les opérations <a href="cut.md"><strong>couper</strong></a>, <a href="copy.md"><strong>copier</strong></a>, <a href="delete.md"><strong>supprimer</strong></a>, <a href="paste.md"><strong>coller</strong></a>ou <a href="undo.md"><strong>Annuler</strong></a> , retourne la &quot; modification &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-430">During <a href="cut.md"><strong>cut</strong></a>, <a href="copy.md"><strong>copy</strong></a>, <a href="delete.md"><strong>delete</strong></a>, <a href="paste.md"><strong>paste</strong></a>, or <a href="undo.md"><strong>undo</strong></a> operations, it returns &quot;editing&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-431">balise de format</span><span class="sxs-lookup"><span data-stu-id="387c1-431">format tag</span></span></td>
<td><span data-ttu-id="387c1-432">Retourne la balise de format.</span><span class="sxs-lookup"><span data-stu-id="387c1-432">Returns the format tag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-433">forward</span><span class="sxs-lookup"><span data-stu-id="387c1-433">forward</span></span></td>
<td><span data-ttu-id="387c1-434">Retourne la <strong>valeur true</strong> si le sens de lecture est vers l’avant ou si l’appareil n’est pas en train de jouer.</span><span class="sxs-lookup"><span data-stu-id="387c1-434">Returns <strong>TRUE</strong> if the play direction is forward or if the device is not playing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-435">fréquence d’images</span><span class="sxs-lookup"><span data-stu-id="387c1-435">frame rate</span></span></td>
<td><span data-ttu-id="387c1-436">Retourne le nombre d’images par seconde que l’appareil doit utiliser par défaut.</span><span class="sxs-lookup"><span data-stu-id="387c1-436">Returns the number of frames per second that the device will use by default.</span></span> <span data-ttu-id="387c1-437">Les appareils NTSC renvoient 30, PAL 25, etc.</span><span class="sxs-lookup"><span data-stu-id="387c1-437">NTSC devices return 30, PAL 25, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-438">frames ignorés</span><span class="sxs-lookup"><span data-stu-id="387c1-438">frames skipped</span></span></td>
<td><span data-ttu-id="387c1-439">Retourne le nombre de frames qui n’ont pas été dessinés lors de la lecture de la dernière séquence AVI.</span><span class="sxs-lookup"><span data-stu-id="387c1-439">Returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="387c1-440">Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="387c1-440">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="387c1-441">Il est destiné uniquement à l’évaluation des performances ; la valeur de retour est difficile à interpréter.</span><span class="sxs-lookup"><span data-stu-id="387c1-441">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-442">gamma</span><span class="sxs-lookup"><span data-stu-id="387c1-442">gamma</span></span></td>
<td><span data-ttu-id="387c1-443">Retourne la valeur définie avec <a href="setvideo.md"><strong>setvideo</strong></a> &quot; gamma à &quot; <em>value</em>.</span><span class="sxs-lookup"><span data-stu-id="387c1-443">Returns the value set with <a href="setvideo.md"><strong>setvideo</strong></a> &quot;gamma to&quot; <em>value</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-444">index</span><span class="sxs-lookup"><span data-stu-id="387c1-444">index</span></span></td>
<td><span data-ttu-id="387c1-445">Retourne l’affichage actuel de l’index.</span><span class="sxs-lookup"><span data-stu-id="387c1-445">Returns the current index display.</span></span> <span data-ttu-id="387c1-446">Pour plus d’informations, consultez la commande <a href="set.md"><strong>Set</strong></a> &quot; index &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-446">For more information, see the <a href="set.md"><strong>set</strong></a> &quot;index&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-447">index sur</span><span class="sxs-lookup"><span data-stu-id="387c1-447">index on</span></span></td>
<td><span data-ttu-id="387c1-448">Retourne la <strong>valeur true</strong> si l’index est activé.</span><span class="sxs-lookup"><span data-stu-id="387c1-448">Returns <strong>TRUE</strong> if the index is on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-449">entrée</span><span class="sxs-lookup"><span data-stu-id="387c1-449">input</span></span></td>
<td><span data-ttu-id="387c1-450">Retourne le jeu de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="387c1-450">Returns the input set.</span></span> <span data-ttu-id="387c1-451">Si aucune valeur n’est définie, l’erreur retournée indique que n’importe quel appareil peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="387c1-451">If one is not set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="387c1-452">Pour les périphériques vidéo numériques, modifie les &quot; basses &quot; , les &quot; aigus &quot; , le &quot; volume, la &quot; &quot; luminosité, la &quot; &quot; couleur, le &quot; &quot; contraste, la &quot; &quot; gamma, la &quot; &quot; netteté &quot; ou &quot; &quot; l’indicateur de teinte afin qu’elle s’applique uniquement à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="387c1-452">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the input.</span></span> <span data-ttu-id="387c1-453">Il s’agit de la valeur par défaut lors de l’analyse de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="387c1-453">This is the default when monitoring the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-454">volume de gauche</span><span class="sxs-lookup"><span data-stu-id="387c1-454">left volume</span></span></td>
<td><span data-ttu-id="387c1-455">Retourne le volume défini pour le canal audio de gauche.</span><span class="sxs-lookup"><span data-stu-id="387c1-455">Returns the volume set for the left audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-456">length</span><span class="sxs-lookup"><span data-stu-id="387c1-456">length</span></span></td>
<td><span data-ttu-id="387c1-457">Retourne la longueur totale du média, au format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-457">Returns the total length of the media, in the current time format.</span></span> <span data-ttu-id="387c1-458">Pour les fichiers PPQN, la longueur est retournée dans les unités du pointeur de la chanson.</span><span class="sxs-lookup"><span data-stu-id="387c1-458">For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="387c1-459">Pour les fichiers SMPTE, il est retourné sous la forme <em>hh : mm : SS : FF</em>, où <em>hh</em> correspond aux heures, <em>mm</em> à minutes, <em>SS</em> à secondes et <em>FF</em> à des trames.</span><span class="sxs-lookup"><span data-stu-id="387c1-459">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="387c1-460">Pour les périphériques VCR, la longueur est de 2 heures (sauf si la longueur a été explicitement modifiée à l’aide de la commande <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>Set</strong></a> ).</span><span class="sxs-lookup"><span data-stu-id="387c1-460">For VCR devices, the length is 2 hours (unless the length has been explicitly changed using the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> command).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-461"><em>nombre</em> de pistes de longueur</span><span class="sxs-lookup"><span data-stu-id="387c1-461">length track <em>number</em></span></span></td>
<td><span data-ttu-id="387c1-462">Retourne la longueur de la piste, en temps ou en images, spécifiée par <em>nombre</em>. Pour les fichiers PPQN, la longueur est retournée dans les unités du pointeur de la chanson.</span><span class="sxs-lookup"><span data-stu-id="387c1-462">Returns the length of the track, in time or frames, specified by <em>number</em>.For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="387c1-463">Pour les fichiers SMPTE, il est retourné sous la forme <em>hh : mm : SS : FF</em>, où <em>hh</em> correspond aux heures, <em>mm</em> à minutes, <em>SS</em> à secondes et <em>FF</em> à des trames.</span><span class="sxs-lookup"><span data-stu-id="387c1-463">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-464">niveau</span><span class="sxs-lookup"><span data-stu-id="387c1-464">level</span></span></td>
<td><span data-ttu-id="387c1-465">Retourne l’exemple de valeur audio PCM actuelle.</span><span class="sxs-lookup"><span data-stu-id="387c1-465">Returns the current PCM audio sample value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-466">master</span><span class="sxs-lookup"><span data-stu-id="387c1-466">master</span></span></td>
<td><span data-ttu-id="387c1-467">Retourne &quot; midi &quot; , &quot; None &quot; ou &quot; SMPTE &quot; selon le type de jeu de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="387c1-467">Returns &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-468">support présent</span><span class="sxs-lookup"><span data-stu-id="387c1-468">media present</span></span></td>
<td><span data-ttu-id="387c1-469">Retourne la <strong>valeur true</strong> si le média est inséré dans l’appareil ou <strong>false</strong> dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="387c1-469">Returns <strong>TRUE</strong> if the media is inserted in the device or <strong>FALSE</strong> otherwise.</span></span> <span data-ttu-id="387c1-470">Les périphériques Sequencer, Video-Overlay, Digital-Video et Waveform-Audio renvoient la <strong>valeur true</strong>.</span><span class="sxs-lookup"><span data-stu-id="387c1-470">Sequencer, video-overlay, digital-video, and waveform-audio devices return <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-471">type de média</span><span class="sxs-lookup"><span data-stu-id="387c1-471">media type</span></span></td>
<td><span data-ttu-id="387c1-472">Retourne le type du média.</span><span class="sxs-lookup"><span data-stu-id="387c1-472">Returns the type of the media.</span></span> <span data-ttu-id="387c1-473">Pour les MAGNÉTOSCOPEs, il s’agit de &quot; 8mm &quot; , &quot; VHS &quot; , &quot; SVHS &quot; , &quot; beta &quot; , &quot; Hi8 &quot; , &quot; edbeta &quot; ou &quot; autre &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-473">For VCRS, this is &quot;8mm&quot;, &quot;vhs&quot;, &quot;svhs&quot;, &quot;beta&quot;, &quot;Hi8&quot;, &quot;edbeta&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="387c1-474">Pour videodiscs, il s’agit de &quot; CAV &quot; , &quot; CLV &quot; ou &quot; other &quot; , selon le type de videodisc.</span><span class="sxs-lookup"><span data-stu-id="387c1-474">For videodiscs, this is &quot;CAV&quot;, &quot;CLV&quot;, or &quot;other&quot;, depending on the type of videodisc.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-475">mode</span><span class="sxs-lookup"><span data-stu-id="387c1-475">mode</span></span></td>
<td><span data-ttu-id="387c1-476">Retourne le mode actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="387c1-476">Returns the current mode of the device.</span></span> <span data-ttu-id="387c1-477">Tous les appareils peuvent retourner les &quot; valeurs non prêt &quot; , &quot; suspendu &quot; , &quot; lecture &quot; et &quot; arrêté &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-477">All devices can return the &quot;not ready&quot;, &quot;paused&quot;, &quot;playing&quot;, and &quot;stopped&quot; values.</span></span> <span data-ttu-id="387c1-478">Certains appareils peuvent renvoyer les valeurs supplémentaires ouvertes, imposées &quot; &quot; &quot; &quot; , &quot; d’enregistrement &quot; et de &quot; recherche &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-478">Some devices can return the additional &quot;open&quot;, &quot;parked&quot;, &quot;recording&quot;, and &quot;seeking&quot; values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-479">monitor</span><span class="sxs-lookup"><span data-stu-id="387c1-479">monitor</span></span></td>
<td><span data-ttu-id="387c1-480">Retourne le &quot; fichier &quot; ou l' &quot; entrée &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-480">Returns &quot;file&quot; or &quot;input&quot;.</span></span> <span data-ttu-id="387c1-481">La valeur retournée indique la source de présentation actuelle.</span><span class="sxs-lookup"><span data-stu-id="387c1-481">The returned value indicates the current presentation source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-482">méthode Monitor</span><span class="sxs-lookup"><span data-stu-id="387c1-482">monitor method</span></span></td>
<td><span data-ttu-id="387c1-483">Retourne &quot; pre &quot; , &quot; poster &quot; ou &quot; direct &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-483">Returns &quot;pre&quot;, &quot;post&quot;, or &quot;direct&quot;.</span></span> <span data-ttu-id="387c1-484">La valeur retournée indique la méthode utilisée pour la surveillance d’entrée.</span><span class="sxs-lookup"><span data-stu-id="387c1-484">The returned value indicates the method used for input monitoring.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-485">minime</span><span class="sxs-lookup"><span data-stu-id="387c1-485">nominal</span></span></td>
<td><span data-ttu-id="387c1-486">L’élément modifie les &quot; &quot; indicateurs de basses, de &quot; luminosité &quot; , de &quot; couleur &quot; , de &quot; contraste, de &quot; &quot; gamma, de netteté, de &quot; teinte, de &quot; &quot; &quot; &quot; &quot; aigu et de &quot; &quot; volume &quot; pour retourner la valeur nominale au lieu du paramètre actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-486">The item modifies the &quot;bass&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, &quot;tint&quot;, &quot;treble,&quot; and &quot;volume&quot; flags to return the nominal value instead of the current setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-487">fréquence d’images nominales</span><span class="sxs-lookup"><span data-stu-id="387c1-487">nominal frame rate</span></span></td>
<td><span data-ttu-id="387c1-488">Retourne la fréquence d’images nominales associée au fichier.</span><span class="sxs-lookup"><span data-stu-id="387c1-488">Returns the nominal frame rate associated with the file.</span></span> <span data-ttu-id="387c1-489">Les unités sont en images par seconde, multiplié par 1000.</span><span class="sxs-lookup"><span data-stu-id="387c1-489">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-490">fréquence des images d’enregistrement nominales</span><span class="sxs-lookup"><span data-stu-id="387c1-490">nominal record frame rate</span></span></td>
<td><span data-ttu-id="387c1-491">Retourne la fréquence d’images nominales associée au signal vidéo d’entrée.</span><span class="sxs-lookup"><span data-stu-id="387c1-491">Returns the nominal frame rate associated with the input video signal.</span></span> <span data-ttu-id="387c1-492">Les unités sont en images par seconde, multiplié par 1000.</span><span class="sxs-lookup"><span data-stu-id="387c1-492">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-493">nombre de pistes audio</span><span class="sxs-lookup"><span data-stu-id="387c1-493">number of audio tracks</span></span></td>
<td><span data-ttu-id="387c1-494">Retourne le nombre de pistes audio sur le support.</span><span class="sxs-lookup"><span data-stu-id="387c1-494">Returns the number of audio tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-495">nombre de pistes</span><span class="sxs-lookup"><span data-stu-id="387c1-495">number of tracks</span></span></td>
<td><span data-ttu-id="387c1-496">Retourne le nombre de pistes sur le média.</span><span class="sxs-lookup"><span data-stu-id="387c1-496">Returns the number of tracks on the media.</span></span> <span data-ttu-id="387c1-497">Les appareils MCISEQ et MCIWAVE retournent 1, comme le font la plupart des périphériques VCR.</span><span class="sxs-lookup"><span data-stu-id="387c1-497">The MCISEQ and MCIWAVE devices return 1, as do most VCR devices.</span></span> <span data-ttu-id="387c1-498">L’appareil MCIPIONR ne prend pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="387c1-498">The MCIPIONR device does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-499">nombre de pistes vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-499">number of video tracks</span></span></td>
<td><span data-ttu-id="387c1-500">Retourne le nombre de pistes vidéo sur le support.</span><span class="sxs-lookup"><span data-stu-id="387c1-500">Returns the number of video tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-501">offset</span><span class="sxs-lookup"><span data-stu-id="387c1-501">offset</span></span></td>
<td><span data-ttu-id="387c1-502">Retourne le décalage d’un fichier basé sur une SMPTE.</span><span class="sxs-lookup"><span data-stu-id="387c1-502">Returns the offset of a SMPTE-based file.</span></span> <span data-ttu-id="387c1-503">Le décalage est l’heure de début d’une séquence basée sur SMPTE.</span><span class="sxs-lookup"><span data-stu-id="387c1-503">The offset is the start time of a SMPTE-based sequence.</span></span> <span data-ttu-id="387c1-504">L’heure est retournée sous la forme <em>hh : mm : SS : FF</em>, où <em>hh</em> est hours, <em>mm</em> correspond à minutes, <em>SS</em> à secondes et <em>FF</em> à la trame.</span><span class="sxs-lookup"><span data-stu-id="387c1-504">The time is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-505">sortie</span><span class="sxs-lookup"><span data-stu-id="387c1-505">output</span></span></td>
<td><span data-ttu-id="387c1-506">Retourne la sortie actuellement définie.</span><span class="sxs-lookup"><span data-stu-id="387c1-506">Returns the currently set output.</span></span> <span data-ttu-id="387c1-507">Si aucune sortie n’est définie, l’erreur retournée indique que tous les appareils peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="387c1-507">If no output is set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="387c1-508">Pour les périphériques vidéo numériques, modifie les &quot; basses &quot; , les &quot; aigus &quot; , le &quot; volume, la &quot; &quot; luminosité, la &quot; &quot; couleur, le &quot; &quot; contraste, la &quot; &quot; gamma, la &quot; &quot; netteté &quot; ou &quot; &quot; l’indicateur de teinte afin qu’elle s’applique uniquement à la sortie.</span><span class="sxs-lookup"><span data-stu-id="387c1-508">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the output.</span></span> <span data-ttu-id="387c1-509">Il s’agit de la valeur par défaut lors de l’analyse d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="387c1-509">This is the default when monitoring a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-510">mode pause</span><span class="sxs-lookup"><span data-stu-id="387c1-510">pause mode</span></span></td>
<td><span data-ttu-id="387c1-511">Retourne l' &quot; enregistrement &quot; si l’appareil est mis en pause pendant l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="387c1-511">Returns &quot;recording&quot; if the device is paused while recording.</span></span> <span data-ttu-id="387c1-512">Elle retourne &quot; &quot; la valeur si l’appareil est en pause pendant la durée de la diffusion.</span><span class="sxs-lookup"><span data-stu-id="387c1-512">It returns &quot;playing&quot; if the device is paused while playing.</span></span> <span data-ttu-id="387c1-513">Elle retourne l' &quot; action d’erreur non applicable en mode actuel &quot; si l’appareil n’est pas suspendu.</span><span class="sxs-lookup"><span data-stu-id="387c1-513">It returns the error &quot;Action not applicable in current mode&quot; if the device is not paused.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-514">délai d’attente de pause</span><span class="sxs-lookup"><span data-stu-id="387c1-514">pause timeout</span></span></td>
<td><span data-ttu-id="387c1-515">Retourne la durée maximale, en millisecondes, d’une commande d' <a href="pause.md"><strong>interruption</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="387c1-515">Returns the maximum duration, in milliseconds, of a <a href="pause.md"><strong>pause</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-516">format de lecture</span><span class="sxs-lookup"><span data-stu-id="387c1-516">play format</span></span></td>
<td><span data-ttu-id="387c1-517">Retourne un code qui indique le format de lecture des cassettes vidéo, s’il est détectable : &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; ou &quot; autre &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-517">Returns a code indicating the format that the videotape will be played back in, if detectable: &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="387c1-518">Pour plus d’informations, consultez l' &quot; indicateur de format d’enregistrement &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-518">For more information, see the &quot;record format&quot; flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-519">Vitesse de lecture</span><span class="sxs-lookup"><span data-stu-id="387c1-519">play speed</span></span></td>
<td><span data-ttu-id="387c1-520">Retourne une valeur représentant la différence entre la durée de l’exécution réelle de la dernière séquence AVI et la durée d’exécution de la cible.</span><span class="sxs-lookup"><span data-stu-id="387c1-520">Returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="387c1-521">La valeur 1000 indique que l’heure cible et l’heure réelle étaient les mêmes.</span><span class="sxs-lookup"><span data-stu-id="387c1-521">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="387c1-522">Une valeur de 2000, par exemple, indique que la séquence AVI prenait deux fois plus de temps que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="387c1-522">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="387c1-523">Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="387c1-523">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="387c1-524">Il est destiné uniquement à l’évaluation des performances ; la valeur de retour est difficile à interpréter.</span><span class="sxs-lookup"><span data-stu-id="387c1-524">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-525">port</span><span class="sxs-lookup"><span data-stu-id="387c1-525">port</span></span></td>
<td><span data-ttu-id="387c1-526">Retourne le numéro de port MIDI affecté à la séquence.</span><span class="sxs-lookup"><span data-stu-id="387c1-526">Returns the MIDI port number assigned to the sequence.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-527">position</span><span class="sxs-lookup"><span data-stu-id="387c1-527">position</span></span></td>
<td><span data-ttu-id="387c1-528">Retourne la position actuelle. Pour les fichiers PPQN, la position est retournée dans les unités du pointeur de la chanson.</span><span class="sxs-lookup"><span data-stu-id="387c1-528">Returns the current position.For PPQN files, the position is returned in song pointer units.</span></span> <span data-ttu-id="387c1-529">Pour les fichiers SMPTE, il est retourné sous la forme <em>hh : mm : SS : FF</em>, où <em>hh</em> correspond aux heures, <em>mm</em> à minutes, SS à secondes et <em>FF</em> à des trames.</span><span class="sxs-lookup"><span data-stu-id="387c1-529">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, ss is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-530">début de la position</span><span class="sxs-lookup"><span data-stu-id="387c1-530">position start</span></span></td>
<td><span data-ttu-id="387c1-531">Retourne la position du début du média utilisable.</span><span class="sxs-lookup"><span data-stu-id="387c1-531">Returns the position of the start of the usable media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-532"><em>numéro</em> de piste de position</span><span class="sxs-lookup"><span data-stu-id="387c1-532">position track <em>number</em></span></span></td>
<td><span data-ttu-id="387c1-533">Retourne la position du début de la piste spécifiée par <em>nombre</em>.</span><span class="sxs-lookup"><span data-stu-id="387c1-533">Returns the position of the start of the track specified by <em>number</em>.</span></span> <span data-ttu-id="387c1-534">Pour les fichiers PPQN, le format d’heure est retourné dans les unités du pointeur de la chanson.</span><span class="sxs-lookup"><span data-stu-id="387c1-534">For PPQN files, the time format is returned in song pointer units.</span></span> <span data-ttu-id="387c1-535">Pour les fichiers SMPTE, il est retourné sous la forme <em>hh : mm : SS : FF</em>, où <em>hh</em> correspond aux heures, <em>mm</em> à minutes, <em>SS</em> à secondes et <em>FF</em> à des trames.</span><span class="sxs-lookup"><span data-stu-id="387c1-535">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="387c1-536">MCISEQ Sequencer retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="387c1-536">The MCISEQ sequencer returns zero.</span></span> <span data-ttu-id="387c1-537">L’appareil MCIPIONR ne prend pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="387c1-537">The MCIPIONR device does not support this flag.</span></span> <span data-ttu-id="387c1-538">L’appareil MCIWAVE retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="387c1-538">The MCIWAVE device returns zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-539">durée de Postroll</span><span class="sxs-lookup"><span data-stu-id="387c1-539">postroll duration</span></span></td>
<td><span data-ttu-id="387c1-540">Retourne la longueur des cassettes vidéo au format de l’heure actuelle, nécessaire pour freiner le transport du magnétoscope lors de l’émission d’une commande <a href="stop.md"><strong>Stop</strong></a> ou <a href="pause.md"><strong>Pause</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="387c1-540">Returns the length of videotape, in the current time format, needed to brake the VCR transport when a <a href="stop.md"><strong>stop</strong></a> or <a href="pause.md"><strong>pause</strong></a> command is issued.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-541">Sous tension</span><span class="sxs-lookup"><span data-stu-id="387c1-541">power on</span></span></td>
<td><span data-ttu-id="387c1-542">Retourne la <strong>valeur true</strong> si la mise sous tension du magnétoscope est activée.</span><span class="sxs-lookup"><span data-stu-id="387c1-542">Returns <strong>TRUE</strong> if the VCR's power is on.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-543">durée du préroll</span><span class="sxs-lookup"><span data-stu-id="387c1-543">preroll duration</span></span></td>
<td><span data-ttu-id="387c1-544">Retourne la longueur des cassettes vidéo, au format de l’heure actuelle, nécessaire pour stabiliser la sortie du magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="387c1-544">Returns the length of videotape, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-545">ready</span><span class="sxs-lookup"><span data-stu-id="387c1-545">ready</span></span></td>
<td><span data-ttu-id="387c1-546">Retourne la <strong>valeur true</strong> si l’appareil est prêt à accepter une autre commande.</span><span class="sxs-lookup"><span data-stu-id="387c1-546">Returns <strong>TRUE</strong> if the device is ready to accept another command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-547">format d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="387c1-547">record format</span></span></td>
<td><span data-ttu-id="387c1-548">Retourne un code qui indique le format dans lequel les cassettes vidéo seront enregistrées.</span><span class="sxs-lookup"><span data-stu-id="387c1-548">Returns a code indicating the format that the videotape will be recorded in.</span></span> <span data-ttu-id="387c1-549">Les types de retour actuels sont &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; ou &quot; autre &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-549">The current return types are &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="387c1-550">Ces formats ne sont pas spécifiques à la SHV et peuvent être appliqués à n’importe quel magnétoscope ayant plusieurs formats d’enregistrement sélectionnables.</span><span class="sxs-lookup"><span data-stu-id="387c1-550">These formats are not VHS specific and can be applied to any VCR that has multiple selectable recording formats.</span></span> <span data-ttu-id="387c1-551">Le &quot; type de processeur &quot; de stockage est le format d’enregistrement de qualité le plus rapide et le plus élevé. il est utilisé par défaut sur les magnétoscopes à format unique.</span><span class="sxs-lookup"><span data-stu-id="387c1-551">The &quot;sp&quot; type is the fastest, highest quality recording format and is used as default on single format VCRs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-552">fréquence des trames d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="387c1-552">record frame rate</span></span></td>
<td><span data-ttu-id="387c1-553">Retourne la fréquence d’images, en images par seconde, multiplié par 1000, utilisée pour la compression.</span><span class="sxs-lookup"><span data-stu-id="387c1-553">Returns the frame rate, in frames per second multiplied by 1000, used for compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-554"><em>Frame</em> de référence</span><span class="sxs-lookup"><span data-stu-id="387c1-554">reference <em>frame</em></span></span></td>
<td><span data-ttu-id="387c1-555">Retourne le numéro de frame de l’image de l’image clé la plus proche qui précède le <em>cadre</em>spécifié.</span><span class="sxs-lookup"><span data-stu-id="387c1-555">Returns the frame number for the nearest key frame image that precedes the specified <em>frame</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-556">taille réservée</span><span class="sxs-lookup"><span data-stu-id="387c1-556">reserved size</span></span></td>
<td><span data-ttu-id="387c1-557">Retourne la taille, dans le format d’heure actuel, de l’espace de travail réservé.</span><span class="sxs-lookup"><span data-stu-id="387c1-557">Returns the size, in the current time format, of the reserved workspace.</span></span> <span data-ttu-id="387c1-558">La taille correspond au temps approximatif nécessaire pour lire les données compressées à partir d’un espace de travail complet.</span><span class="sxs-lookup"><span data-stu-id="387c1-558">The size corresponds to the approximate time it would take to play the compressed data from a full workspace.</span></span> <span data-ttu-id="387c1-559">Elle retourne zéro s’il n’y a pas d’espace disque réservé.</span><span class="sxs-lookup"><span data-stu-id="387c1-559">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="387c1-560">Cet indicateur retourne la taille approximative car l’espace disque précis pour les données compressées ne peut pas, en général, être prédit tant que les données n’ont pas été compressées.</span><span class="sxs-lookup"><span data-stu-id="387c1-560">This flag returns the approximate size because the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-561">volume approprié</span><span class="sxs-lookup"><span data-stu-id="387c1-561">right volume</span></span></td>
<td><span data-ttu-id="387c1-562">Retourne le volume défini pour le canal audio de droite.</span><span class="sxs-lookup"><span data-stu-id="387c1-562">Returns the volume set for the right audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-563">samplespersec</span><span class="sxs-lookup"><span data-stu-id="387c1-563">samplespersec</span></span></td>
<td><span data-ttu-id="387c1-564">Retourne le nombre d’échantillons par seconde lus ou enregistrés.</span><span class="sxs-lookup"><span data-stu-id="387c1-564">Returns the number of samples per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-565">Rechercher exactement</span><span class="sxs-lookup"><span data-stu-id="387c1-565">seek exactly</span></span></td>
<td><span data-ttu-id="387c1-566">Retourne &quot; on &quot; ou &quot; OFF &quot; , indiquant si l' &quot; indicateur Seek exact &quot; est défini.</span><span class="sxs-lookup"><span data-stu-id="387c1-566">Returns &quot;on&quot; or &quot;off&quot;, indicating whether or not the &quot;seek exactly&quot; flag is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-567">netteté</span><span class="sxs-lookup"><span data-stu-id="387c1-567">sharpness</span></span></td>
<td><span data-ttu-id="387c1-568">Retourne le niveau de netteté actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="387c1-568">Returns the current sharpness level of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-569">initi</span><span class="sxs-lookup"><span data-stu-id="387c1-569">side</span></span></td>
<td><span data-ttu-id="387c1-570">Retourne 1 ou 2 pour indiquer le côté du videodisc à charger.</span><span class="sxs-lookup"><span data-stu-id="387c1-570">Returns 1 or 2 to indicate which side of the videodisc is loaded.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-571">subordonné</span><span class="sxs-lookup"><span data-stu-id="387c1-571">slave</span></span></td>
<td><span data-ttu-id="387c1-572">Retourne &quot; fichier &quot; , &quot; midi &quot; , &quot; aucun &quot; ou &quot; SMPTE &quot; selon le type de jeu de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="387c1-572">Returns &quot;file&quot; , &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-573">intégrant</span><span class="sxs-lookup"><span data-stu-id="387c1-573">smpte</span></span></td>
<td><span data-ttu-id="387c1-574">Retourne le code temporel SMPTE associé à la position actuelle dans l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="387c1-574">Returns the SMPTE timecode associated with the current position in the workspace.</span></span> <span data-ttu-id="387c1-575">Il s’agit d’une chaîne au format <em>JJ : JJ : JJ : JJ</em>, où chaque <em>d</em> désigne un chiffre compris entre 0 et 9.</span><span class="sxs-lookup"><span data-stu-id="387c1-575">This is a string with the form <em>dd:dd:dd:dd</em>, where each <em>d</em> denotes a digit from 0 to 9.</span></span> <span data-ttu-id="387c1-576">Si les données de l’espace de travail n’incluent pas de données de code temporel, cet indicateur retourne 00:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="387c1-576">If the workspace data does not include timecode data, then this flag returns 00:00:00:00.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-577">speed</span><span class="sxs-lookup"><span data-stu-id="387c1-577">speed</span></span></td>
<td><span data-ttu-id="387c1-578">Retourne la vitesse actuelle de l’appareil en images par seconde (ou dans le même format que celui utilisé par la commande <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>Set</strong></a> &quot; Speed &quot; ).</span><span class="sxs-lookup"><span data-stu-id="387c1-578">Returns the current speed of the device in frames per second (or in the same format used by the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot;speed&quot; command).</span></span> <span data-ttu-id="387c1-579">MCIPIONR videodisc Player ne prend pas en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="387c1-579">The MCIPIONR videodisc player does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-580">position de départ</span><span class="sxs-lookup"><span data-stu-id="387c1-580">start position</span></span></td>
<td><span data-ttu-id="387c1-581">Retourne la position de départ du média.</span><span class="sxs-lookup"><span data-stu-id="387c1-581">Returns the starting position of the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-582">format de fichier toujours</span><span class="sxs-lookup"><span data-stu-id="387c1-582">still file format</span></span></td>
<td><span data-ttu-id="387c1-583">Retourne le format de fichier actuel pour la commande de <a href="capture.md"><strong>capture</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="387c1-583">Returns the current file format for the <a href="capture.md"><strong>capture</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-584">étirement</span><span class="sxs-lookup"><span data-stu-id="387c1-584">stretch</span></span></td>
<td><span data-ttu-id="387c1-585">Retourne la <strong>valeur true</strong> si l’étirement est activé.</span><span class="sxs-lookup"><span data-stu-id="387c1-585">Returns <strong>TRUE</strong> if stretching is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-586">tempo</span><span class="sxs-lookup"><span data-stu-id="387c1-586">tempo</span></span></td>
<td><span data-ttu-id="387c1-587">Retourne le tempo actuel d’une séquence MIDI dans le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-587">Returns the current tempo of a MIDI sequence in the current time format.</span></span> <span data-ttu-id="387c1-588">Pour les fichiers avec le format PPQN, le tempo est en temps par minute.</span><span class="sxs-lookup"><span data-stu-id="387c1-588">For files with PPQN format, the tempo is in beats per minute.</span></span> <span data-ttu-id="387c1-589">Pour les fichiers avec le format SMPTE, le tempo est en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="387c1-589">For files with SMPTE format, the tempo is in frames per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-590">format horaire</span><span class="sxs-lookup"><span data-stu-id="387c1-590">time format</span></span></td>
<td><span data-ttu-id="387c1-591">Retourne le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-591">Returns the current time format.</span></span> <span data-ttu-id="387c1-592">Pour plus d’informations, consultez les formats d’heure dans la commande <a href="set.md"><strong>Set</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="387c1-592">For more information, see the time formats in the <a href="set.md"><strong>set</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-593">mode heure</span><span class="sxs-lookup"><span data-stu-id="387c1-593">time mode</span></span></td>
<td><span data-ttu-id="387c1-594">Retourne le mode de l’heure de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="387c1-594">Returns the current position time mode.</span></span> <span data-ttu-id="387c1-595">Il peut s’agir de la &quot; détection &quot; , du &quot; code temporel &quot; ou du &quot; compteur &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-595">It can be &quot;detect&quot;, &quot;timecode&quot;, or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-596">type de temps</span><span class="sxs-lookup"><span data-stu-id="387c1-596">time type</span></span></td>
<td><span data-ttu-id="387c1-597">Retourne l’heure de la position actuelle en cours d’utilisation : &quot; code temporel &quot; ou &quot; compteur &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-597">Returns the current position time in use: &quot;timecode&quot; or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-598">code temporel présent</span><span class="sxs-lookup"><span data-stu-id="387c1-598">timecode present</span></span></td>
<td><span data-ttu-id="387c1-599">Retourne la <strong>valeur true</strong> si le code temporel a été enregistré à la position actuelle sur la bande.</span><span class="sxs-lookup"><span data-stu-id="387c1-599">Returns <strong>TRUE</strong> if timecode has been recorded at the current position on the tape.</span></span> <span data-ttu-id="387c1-600">Le code temporel doit avancer à partir de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="387c1-600">The timecode must advance from the current position.</span></span> <span data-ttu-id="387c1-601">Il peut être nécessaire de lire un magnétoscope pour vérifier cette condition.</span><span class="sxs-lookup"><span data-stu-id="387c1-601">A VCR might need to be played to check this condition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-602">enregistrement du code temporel</span><span class="sxs-lookup"><span data-stu-id="387c1-602">timecode record</span></span></td>
<td><span data-ttu-id="387c1-603">Renvoie la <strong>valeur true</strong> si le magnétoscope est défini pour enregistrer le code temporel.</span><span class="sxs-lookup"><span data-stu-id="387c1-603">Returns <strong>TRUE</strong> if the VCR is set to record timecode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-604">type de code temporel</span><span class="sxs-lookup"><span data-stu-id="387c1-604">timecode type</span></span></td>
<td><span data-ttu-id="387c1-605">Retourne &quot; SMPTE &quot; , la &quot; suppression SMPTE &quot; , &quot; other &quot; ou &quot; None &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-605">Returns &quot;smpte&quot;, &quot;smpte drop&quot;, &quot;other&quot;, or &quot;none&quot;.</span></span> <span data-ttu-id="387c1-606">Notez que les images par seconde peuvent être obtenues à partir de la &quot; commande fréquence des trames d’État et que la &quot; précision de l’appareil peut être retournée par la commande de précision de la <a href="capability.md"><strong>fonction</strong></a> &quot; Seek &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-606">Note the frames per second can be obtained from the status &quot;frame rate&quot; command, and the accuracy of the device can be returned by the <a href="capability.md"><strong>capability</strong></a> &quot;seek accuracy&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-607">teinté</span><span class="sxs-lookup"><span data-stu-id="387c1-607">tint</span></span></td>
<td><span data-ttu-id="387c1-608">Retourne le niveau de teinte vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-608">Returns the current video-tint level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-609">les aigus</span><span class="sxs-lookup"><span data-stu-id="387c1-609">treble</span></span></td>
<td><span data-ttu-id="387c1-610">Retourne le niveau des aigus audio actuels.</span><span class="sxs-lookup"><span data-stu-id="387c1-610">Returns the current audio-treble level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-611">Numéro de tuner</span><span class="sxs-lookup"><span data-stu-id="387c1-611">tuner number</span></span></td>
<td><span data-ttu-id="387c1-612">Retourne le numéro de tuner logique actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-612">Returns the current logical-tuner number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-613">non enregistrées</span><span class="sxs-lookup"><span data-stu-id="387c1-613">unsaved</span></span></td>
<td><span data-ttu-id="387c1-614">Retourne la <strong>valeur true</strong> s’il y a des données enregistrées dans l’espace de travail qui peuvent être perdues à la suite d’une commande de <a href="close.md"><strong>fermeture</strong></a>, de <a href="load.md"><strong>chargement</strong></a>, d' <a href="record.md"><strong>enregistrement</strong></a>, de <a href="reserve.md"><strong>réserve</strong></a>, de <a href="cut.md"><strong>coupure</strong></a>, de <a href="delete.md"><strong>suppression</strong></a>ou de <a href="paste.md"><strong>Collage</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="387c1-614">Returns <strong>TRUE</strong> if there is recorded data in the workspace that might be lost as a result of a <a href="close.md"><strong>close</strong></a>, <a href="load.md"><strong>load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>reserve</strong></a>, <a href="cut.md"><strong>cut</strong></a>, <a href="delete.md"><strong>delete</strong></a>, or <a href="paste.md"><strong>paste</strong></a> command.</span></span> <span data-ttu-id="387c1-615">Sinon, retourne <strong>false</strong> .</span><span class="sxs-lookup"><span data-stu-id="387c1-615">Returns <strong>FALSE</strong> otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-616">video</span><span class="sxs-lookup"><span data-stu-id="387c1-616">video</span></span></td>
<td><span data-ttu-id="387c1-617">Retourne &quot; on &quot; ou &quot; OFF &quot; , en reflétant l’état défini par la commande <a href="setvideo.md"><strong>setvideo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="387c1-617">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-618">couleur de la touche vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-618">video key color</span></span></td>
<td><span data-ttu-id="387c1-619">Retourne la valeur de la couleur de la clé.</span><span class="sxs-lookup"><span data-stu-id="387c1-619">Returns the value for the key color.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-620">index de clé vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-620">video key index</span></span></td>
<td><span data-ttu-id="387c1-621">Retourne la valeur de l’index de clé.</span><span class="sxs-lookup"><span data-stu-id="387c1-621">Returns the value for the key index.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-622">moniteur vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-622">video monitor</span></span></td>
<td><span data-ttu-id="387c1-623">Retourne &quot; &quot; la sortie ou l’un des types d’entrée source valides.</span><span class="sxs-lookup"><span data-stu-id="387c1-623">Returns &quot;output&quot; or one of the valid source-input types.</span></span> <span data-ttu-id="387c1-624">Pour plus d’informations, consultez la commande <a href="setvideo.md"><strong>setvideo</strong></a> &quot; Monitor &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-624">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-625">Numéro du moniteur vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-625">video monitor number</span></span></td>
<td><span data-ttu-id="387c1-626">Retourne le numéro vidéo surveillée du type retourné par le &quot; moniteur vidéo d’état &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-626">Returns the monitored-video number of the type returned by status &quot;video monitor&quot;.</span></span> <span data-ttu-id="387c1-627">Pour plus d’informations, consultez la commande <a href="setvideo.md">setvideo</a> .</span><span class="sxs-lookup"><span data-stu-id="387c1-627">For more information, see the <a href="setvideo.md">setvideo</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-628">enregistrement vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-628">video record</span></span></td>
<td><span data-ttu-id="387c1-629">Retourne &quot; on &quot; ou &quot; OFF &quot; , en reflétant l’état actuel défini par l’enregistrement <a href="setvideo.md"><strong>setvideo</strong></a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="387c1-629">Returns &quot;on&quot; or &quot;off&quot;, reflecting the current state set by <a href="setvideo.md"><strong>setvideo</strong></a> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-630"><em>numéro</em> de piste de l’enregistrement vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-630">video record track <em>number</em></span></span></td>
<td><span data-ttu-id="387c1-631">Retourne la <strong>valeur true</strong> si le magnétoscope est configuré pour enregistrer la vidéo.</span><span class="sxs-lookup"><span data-stu-id="387c1-631">Return <strong>TRUE</strong> if the VCR is set to record video.</span></span> <span data-ttu-id="387c1-632">Si aucun numéro de piste n’est indiqué, la valeur par défaut de 1 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="387c1-632">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-633">source vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-633">video source</span></span></td>
<td><span data-ttu-id="387c1-634">Retourne le type de source vidéo.</span><span class="sxs-lookup"><span data-stu-id="387c1-634">Returns the video-source type.</span></span> <span data-ttu-id="387c1-635">Pour plus d’informations, consultez la commande <a href="setvideo.md"><strong>setvideo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="387c1-635">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-636">Numéro de la source vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-636">video source number</span></span></td>
<td><span data-ttu-id="387c1-637">Retourne un nombre correspondant à la source vidéo du type en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="387c1-637">Returns a number corresponding to the video source of the type in use.</span></span> <span data-ttu-id="387c1-638">Par exemple, elle retourne 2 si la deuxième entrée de la source vidéo NTSC est utilisée.</span><span class="sxs-lookup"><span data-stu-id="387c1-638">For example, it returns 2 if the second NTSC video source input is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-639">flux vidéo</span><span class="sxs-lookup"><span data-stu-id="387c1-639">video stream</span></span></td>
<td><span data-ttu-id="387c1-640">Retourne le numéro de flux vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="387c1-640">Returns the current video-stream number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-641">volume</span><span class="sxs-lookup"><span data-stu-id="387c1-641">volume</span></span></td>
<td><span data-ttu-id="387c1-642">Retourne le volume moyen du haut-parleur gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="387c1-642">Returns the average volume to the left and right speaker.</span></span> <span data-ttu-id="387c1-643">Cela renvoie une erreur si l’appareil n’a pas été lu ou si le volume n’a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="387c1-643">This returns an error if the device has not been played or volume has not been set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-644">handle de fenêtre</span><span class="sxs-lookup"><span data-stu-id="387c1-644">window handle</span></span></td>
<td><span data-ttu-id="387c1-645">Retourne la valeur décimale ASCII du handle de fenêtre dans le mot de poids faible de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="387c1-645">Returns the ASCII decimal value for the window handle in the low-order word of the return value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-646">fenêtre agrandie</span><span class="sxs-lookup"><span data-stu-id="387c1-646">window maximized</span></span></td>
<td><span data-ttu-id="387c1-647">Retourne la <strong>valeur true</strong> si la fenêtre est agrandie.</span><span class="sxs-lookup"><span data-stu-id="387c1-647">Returns <strong>TRUE</strong> if the window is maximized.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-648">fenêtre réduite</span><span class="sxs-lookup"><span data-stu-id="387c1-648">window minimized</span></span></td>
<td><span data-ttu-id="387c1-649">Retourne la <strong>valeur true</strong> si la fenêtre est réduite.</span><span class="sxs-lookup"><span data-stu-id="387c1-649">Returns <strong>TRUE</strong> if the window is minimized.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="387c1-650">fenêtre visible</span><span class="sxs-lookup"><span data-stu-id="387c1-650">window visible</span></span></td>
<td><span data-ttu-id="387c1-651">Retourne la <strong>valeur true</strong> si la fenêtre n’est pas masquée.</span><span class="sxs-lookup"><span data-stu-id="387c1-651">Returns <strong>TRUE</strong> if the window is not hidden.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="387c1-652">protégé en écriture</span><span class="sxs-lookup"><span data-stu-id="387c1-652">write protected</span></span></td>
<td><span data-ttu-id="387c1-653">Retourne la <strong>valeur true</strong> si l’appareil détecte qu’il ne peut pas enregistrer (autrement dit, si la protection en écriture est activée).</span><span class="sxs-lookup"><span data-stu-id="387c1-653">Returns <strong>TRUE</strong> if the device detects that it cannot record (that is, if the write protect is on).</span></span> <span data-ttu-id="387c1-654">S’il peut enregistrer ou s’il ne parvient pas à déterminer s’il peut enregistrer (sans réellement écrire), le pilote retourne la <strong>valeur false</strong>.</span><span class="sxs-lookup"><span data-stu-id="387c1-654">If it can record, or if it is unable to determine whether or not it can record (without actually writing), the driver returns <strong>FALSE</strong>.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="387c1-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="387c1-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="387c1-656">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="387c1-656">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="387c1-657">Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="387c1-657">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="387c1-658">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="387c1-658">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="387c1-659">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="387c1-659">Return Value</span></span>

<span data-ttu-id="387c1-660">Retourne des informations dans le paramètre *lpszReturnString* de [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="387c1-660">Returns information in the *lpszReturnString* parameter of [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span></span> <span data-ttu-id="387c1-661">Les informations dépendent du type de demande.</span><span class="sxs-lookup"><span data-stu-id="387c1-661">The information is dependent on the request type.</span></span>

## <a name="remarks"></a><span data-ttu-id="387c1-662">Notes</span><span class="sxs-lookup"><span data-stu-id="387c1-662">Remarks</span></span>

<span data-ttu-id="387c1-663">Avant d’émettre des commandes qui utilisent des valeurs de position, vous devez définir le format d’heure souhaité à l’aide de la commande [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="387c1-663">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="387c1-664">Exemples</span><span class="sxs-lookup"><span data-stu-id="387c1-664">Examples</span></span>

<span data-ttu-id="387c1-665">La commande suivante retourne le mode actuel de l’appareil « mySound ».</span><span class="sxs-lookup"><span data-stu-id="387c1-665">The following command returns the current mode of the "mysound" device.</span></span>

``` syntax
status mysound mode
```

## <a name="requirements"></a><span data-ttu-id="387c1-666">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="387c1-666">Requirements</span></span>



| <span data-ttu-id="387c1-667">Condition requise</span><span class="sxs-lookup"><span data-stu-id="387c1-667">Requirement</span></span> | <span data-ttu-id="387c1-668">Valeur</span><span class="sxs-lookup"><span data-stu-id="387c1-668">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="387c1-669">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="387c1-669">Minimum supported client</span></span><br/> | <span data-ttu-id="387c1-670">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="387c1-670">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="387c1-671">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="387c1-671">Minimum supported server</span></span><br/> | <span data-ttu-id="387c1-672">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="387c1-672">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="387c1-673">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="387c1-673">See also</span></span>

<dl> <dt>

[<span data-ttu-id="387c1-674">MCI</span><span class="sxs-lookup"><span data-stu-id="387c1-674">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="387c1-675">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="387c1-675">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="387c1-676">capability</span><span class="sxs-lookup"><span data-stu-id="387c1-676">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="387c1-677">attire</span><span class="sxs-lookup"><span data-stu-id="387c1-677">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="387c1-678">close</span><span class="sxs-lookup"><span data-stu-id="387c1-678">close</span></span>](close.md)
</dt> <dt>

[<span data-ttu-id="387c1-679">réduis</span><span class="sxs-lookup"><span data-stu-id="387c1-679">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="387c1-680">delete</span><span class="sxs-lookup"><span data-stu-id="387c1-680">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="387c1-681">load</span><span class="sxs-lookup"><span data-stu-id="387c1-681">load</span></span>](load.md)
</dt> <dt>

[<span data-ttu-id="387c1-682">pause</span><span class="sxs-lookup"><span data-stu-id="387c1-682">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="387c1-683">coller</span><span class="sxs-lookup"><span data-stu-id="387c1-683">paste</span></span>](paste.md)
</dt> <dt>

[<span data-ttu-id="387c1-684">enregistrement</span><span class="sxs-lookup"><span data-stu-id="387c1-684">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="387c1-685">reserve</span><span class="sxs-lookup"><span data-stu-id="387c1-685">reserve</span></span>](reserve.md)
</dt> <dt>

[<span data-ttu-id="387c1-686">enregistrer</span><span class="sxs-lookup"><span data-stu-id="387c1-686">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="387c1-687">set</span><span class="sxs-lookup"><span data-stu-id="387c1-687">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="387c1-688">setaudio</span><span class="sxs-lookup"><span data-stu-id="387c1-688">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="387c1-689">setvideo</span><span class="sxs-lookup"><span data-stu-id="387c1-689">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="387c1-690">stop</span><span class="sxs-lookup"><span data-stu-id="387c1-690">stop</span></span>](stop.md)
</dt> <dt>

[<span data-ttu-id="387c1-691">annuler</span><span class="sxs-lookup"><span data-stu-id="387c1-691">undo</span></span>](undo.md)
</dt> </dl>

 


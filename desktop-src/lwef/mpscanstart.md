---
title: MpScanStart, fonction (MpClient. h)
description: Démarre une opération d’analyse.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpScanStart
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942395"
---
# <a name="mpscanstart-function"></a><span data-ttu-id="2fb67-104">MpScanStart fonction)</span><span class="sxs-lookup"><span data-stu-id="2fb67-104">MpScanStart function</span></span>

<span data-ttu-id="2fb67-105">Démarre une opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2fb67-105">Starts a scanning operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb67-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fb67-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a><span data-ttu-id="2fb67-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fb67-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fb67-108">*hMpHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fb67-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb67-109">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="2fb67-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="2fb67-110">Handle de l’interface du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="2fb67-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="2fb67-111">Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb67-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2fb67-112">*ScanType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fb67-112">*ScanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb67-113">Type : **[ **MPSCAN \_**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="2fb67-113">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

<span data-ttu-id="2fb67-114">Spécifie le type d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2fb67-114">Specifies the type of scan.</span></span> <span data-ttu-id="2fb67-115">Ce paramètre doit être l’un des membres du [**\_ type MPSCAN**](mpscan-type.md) enueration.</span><span class="sxs-lookup"><span data-stu-id="2fb67-115">This parameter must be one of the members of the [**MPSCAN\_TYPE**](mpscan-type.md) enueration.</span></span>

</dd> <dt>

<span data-ttu-id="2fb67-116">*dwScanOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fb67-116">*dwScanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb67-117">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2fb67-117">Type: **DWORD**</span></span>

<span data-ttu-id="2fb67-118">Spécifie différentes options pour l’opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2fb67-118">Specifies various options for scanning operation.</span></span>



| <span data-ttu-id="2fb67-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fb67-119">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="2fb67-120">Signification</span><span class="sxs-lookup"><span data-stu-id="2fb67-120">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <span data-ttu-id="2fb67-121"><dt>**\_option MPSCAN \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-121"><dt>**MPSCAN\_OPTION\_NONE**</dt></span></span> </dl>                               | <span data-ttu-id="2fb67-122">Aucune option spécifique n’est demandée.</span><span class="sxs-lookup"><span data-stu-id="2fb67-122">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <span data-ttu-id="2fb67-123"><dt>**\_option MPSCAN \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-123"><dt>**MPSCAN\_OPTION\_ASYNC**</dt></span></span> </dl>                            | <span data-ttu-id="2fb67-124">L’opération d’analyse doit être asynchrone, où **MpScanStart** retourne immédiatement après l’initialisation réussie de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2fb67-124">The scan operation is to be asynchronous, where **MpScanStart** returns immediately after the successful initiation of scanning.</span></span> <span data-ttu-id="2fb67-125">(Par défaut, l’opération d’analyse est synchrone, ce qui signifie que **MpScanStart** ne retournera qu’une fois l’analyse terminée.)</span><span class="sxs-lookup"><span data-stu-id="2fb67-125">(By default the scan operation is synchronous, meaning **MpScanStart** will return only after the scan is finished.)</span></span><br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <span data-ttu-id="2fb67-126"><dt>**progression de l' \_ option MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-126"><dt>**MPSCAN\_OPTION\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="2fb67-127">L’appelant souhaite recevoir des informations sur la progression de l’analyse via un rappel.</span><span class="sxs-lookup"><span data-stu-id="2fb67-127">The caller is interested in receiving scan progress information via a callback.</span></span><br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <span data-ttu-id="2fb67-128"><dt>**\_option MPSCAN \_ LOWPRIORITY**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-128"><dt>**MPSCAN\_OPTION\_LOWPRIORITY**</dt></span></span> </dl>          | <span data-ttu-id="2fb67-129">Effectuez l’analyse avec une priorité basse.</span><span class="sxs-lookup"><span data-stu-id="2fb67-129">Perform the scan with low priority.</span></span> <span data-ttu-id="2fb67-130">(Par défaut, l’opération d’analyse est effectuée avec une priorité normale.)</span><span class="sxs-lookup"><span data-stu-id="2fb67-130">(By default the scan operation is performed with normal priority.)</span></span><br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <span data-ttu-id="2fb67-131"><dt>**\_option MPSCAN \_ PACKEDEXES**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-131"><dt>**MPSCAN\_OPTION\_PACKEDEXES**</dt></span></span> </dl>             | <span data-ttu-id="2fb67-132">Analyser les exécutables empaquetés pour détecter les menaces potentielles.</span><span class="sxs-lookup"><span data-stu-id="2fb67-132">Scan packed executables for possible threats.</span></span><br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <span data-ttu-id="2fb67-133"><dt>**\_Archives des options MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-133"><dt>**MPSCAN\_OPTION\_ARCHIVES**</dt></span></span> </dl>                   | <span data-ttu-id="2fb67-134">Analyser le contenu de l’Archive pour identifier les menaces potentielles.</span><span class="sxs-lookup"><span data-stu-id="2fb67-134">Scan archive contents for possible threats.</span></span> <span data-ttu-id="2fb67-135">Les archives sont des fichiers avec des extensions telles que. zip,. cab ou. tar.</span><span class="sxs-lookup"><span data-stu-id="2fb67-135">Archives are files with extensions such as .zip, .cab, or .tar.</span></span><br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <span data-ttu-id="2fb67-136"><dt>**\_heuristique des options MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-136"><dt>**MPSCAN\_OPTION\_HEURISTICS**</dt></span></span> </dl>             | <span data-ttu-id="2fb67-137">Activez l’analyse heuristique.</span><span class="sxs-lookup"><span data-stu-id="2fb67-137">Enable heuristics-based scanning.</span></span> <span data-ttu-id="2fb67-138">Cela permet de rechercher les menaces dont le type de détection est défini sur heuristiques.</span><span class="sxs-lookup"><span data-stu-id="2fb67-138">This will scan for threats with detection type set to heuristics.</span></span><br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <span data-ttu-id="2fb67-139"><dt>**\_option MPSCAN \_ REPORTFRIENDLY**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-139"><dt>**MPSCAN\_OPTION\_REPORTFRIENDLY**</dt></span></span> </dl> | <span data-ttu-id="2fb67-140">Signaler les éléments conviviaux dans une analyse des ressources.</span><span class="sxs-lookup"><span data-stu-id="2fb67-140">Report friendly items in a resource scan.</span></span> <span data-ttu-id="2fb67-141">Cela est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="2fb67-141">This is intended for internal use only.</span></span><br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <span data-ttu-id="2fb67-142"><dt>**\_option MPSCAN \_ REPORTUNKNOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-142"><dt>**MPSCAN\_OPTION\_REPORTUNKNOWN**</dt></span></span> </dl>    | <span data-ttu-id="2fb67-143">Signaler les éléments inconnus dans une analyse des ressources.</span><span class="sxs-lookup"><span data-stu-id="2fb67-143">Report unknown items in a resource scan.</span></span> <span data-ttu-id="2fb67-144">Cela est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="2fb67-144">This is intended for internal use only.</span></span><br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <span data-ttu-id="2fb67-145"><dt>**\_option MPSCAN \_ noconsolide**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-145"><dt>**MPSCAN\_OPTION\_NOCONSOLIDATE**</dt></span></span> </dl>    | <span data-ttu-id="2fb67-146">Ne Consolidez pas les résultats de l’analyse avec la vue globale des menaces.</span><span class="sxs-lookup"><span data-stu-id="2fb67-146">Do not consolidate scan results with global threat view.</span></span> <span data-ttu-id="2fb67-147">Cela est utile pour un client (tel qu’un client de messagerie) qui souhaite contrôler le nettoyage de l’expérience utilisateur par lui-même plutôt que d’autoriser l’expérience utilisateur de nettoyage anti-programme malveillant par défaut.</span><span class="sxs-lookup"><span data-stu-id="2fb67-147">This is useful for a client (such as an email client) which wants to control cleaning UX by itself rather than allowing default anti-malware cleaning UX.</span></span> <span data-ttu-id="2fb67-148">Cela est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="2fb67-148">This is intended for internal use only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2fb67-149">*pScanResources* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2fb67-149">*pScanResources* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb67-150">Type : **\_ ressources PMPSCAN**</span><span class="sxs-lookup"><span data-stu-id="2fb67-150">Type: **PMPSCAN\_RESOURCES**</span></span>

<span data-ttu-id="2fb67-151">Pointeur vers les informations sur les ressources d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2fb67-151">A pointer to the scan resource information.</span></span> <span data-ttu-id="2fb67-152">Ce paramètre doit avoir la **valeur null** pour une analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="2fb67-152">This parameter must be **NULL** for a quick scan.</span></span> <span data-ttu-id="2fb67-153">Il s’agit d’un paramètre facultatif pour une analyse complète.</span><span class="sxs-lookup"><span data-stu-id="2fb67-153">This is an optional parameter for a full scan.</span></span> <span data-ttu-id="2fb67-154">Pour une analyse de ressource, ce paramètre doit être spécifié avec au moins une structure d’informations sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="2fb67-154">For a resource scan this parameter must be specified with at least one resource information structure.</span></span> <span data-ttu-id="2fb67-155">Pour analyser des ressources spécifiques, l’appelant doit disposer de l’autorisation de **\_ lecture générique** pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="2fb67-155">To scan specific resources the caller must have **GENERIC\_READ** permission for the resource.</span></span> <span data-ttu-id="2fb67-156">Consultez [**\_ ressources MPSCAN**](mpscan-resources.md).</span><span class="sxs-lookup"><span data-stu-id="2fb67-156">See [**MPSCAN\_RESOURCES**](mpscan-resources.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fb67-157">*pCallbackInfo* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2fb67-157">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb67-158">Type : **PMPCALLBACK \_ info**</span><span class="sxs-lookup"><span data-stu-id="2fb67-158">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="2fb67-159">Pointeur vers les informations de rappel utilisées pour alimenter le client avec les modifications de l’état d’analyse (par exemple, Start et Complete) et les informations de progression.</span><span class="sxs-lookup"><span data-stu-id="2fb67-159">A pointer to the callback information used to feed the client with scan state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="2fb67-160">Les [**\_ données MPCALLBACK**](mpcallback-data.md) retournées dans la fonction de rappel signalent l’état d’analyse réel et les informations relatives à la progression.</span><span class="sxs-lookup"><span data-stu-id="2fb67-160">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual scan state and progress-related information.</span></span> <span data-ttu-id="2fb67-161">La liste suivante répertorie les rappels possibles :</span><span class="sxs-lookup"><span data-stu-id="2fb67-161">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="2fb67-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fb67-162">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="2fb67-163">Signification</span><span class="sxs-lookup"><span data-stu-id="2fb67-163">Meaning</span></span>                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <span data-ttu-id="2fb67-164"><dt>**début de l' \_ analyse MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-164"><dt>**MPNOTIFY\_SCAN\_START**</dt></span></span> </dl>                            | <span data-ttu-id="2fb67-165">L’opération d’analyse a démarré.</span><span class="sxs-lookup"><span data-stu-id="2fb67-165">Scan operation started.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <span data-ttu-id="2fb67-166"><dt>**\_analyse MPNOTIFY \_ terminée**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-166"><dt>**MPNOTIFY\_SCAN\_COMPLETE**</dt></span></span> </dl>                   | <span data-ttu-id="2fb67-167">L’opération d’analyse est terminée.</span><span class="sxs-lookup"><span data-stu-id="2fb67-167">Scan operation completed.</span></span> <span data-ttu-id="2fb67-168">Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb67-168">Additional information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <span data-ttu-id="2fb67-169"><dt>**\_analyse MPNOTIFY \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-169"><dt>**MPNOTIFY\_SCAN\_PAUSED**</dt></span></span> </dl>                         | <span data-ttu-id="2fb67-170">L’opération d’analyse est suspendue.</span><span class="sxs-lookup"><span data-stu-id="2fb67-170">Scan operation is paused.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <span data-ttu-id="2fb67-171"><dt>**\_analyse MPNOTIFY \_ reprise**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-171"><dt>**MPNOTIFY\_SCAN\_RESUMED**</dt></span></span> </dl>                      | <span data-ttu-id="2fb67-172">L’opération d’analyse a repris de la suspension.</span><span class="sxs-lookup"><span data-stu-id="2fb67-172">Scan operation resumed from pause.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <span data-ttu-id="2fb67-173"><dt>**annulation de l' \_ analyse MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-173"><dt>**MPNOTIFY\_SCAN\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="2fb67-174">L’opération d’analyse a été annulée.</span><span class="sxs-lookup"><span data-stu-id="2fb67-174">Scan operation was cancelled.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <span data-ttu-id="2fb67-175"><dt>**progression de l' \_ analyse MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-175"><dt>**MPNOTIFY\_SCAN\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="2fb67-176">Analyser les informations de progression.</span><span class="sxs-lookup"><span data-stu-id="2fb67-176">Scan progress information.</span></span> <span data-ttu-id="2fb67-177">Des informations supplémentaires (telles que les statistiques sur les ressources) sont disponibles via la structure de [**\_ données MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb67-177">Additional information (such as resource statistics) is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <span data-ttu-id="2fb67-178"><dt>**\_erreur d’analyse MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-178"><dt>**MPNOTIFY\_SCAN\_ERROR**</dt></span></span> </dl>                            | <span data-ttu-id="2fb67-179">Analyser les informations d’erreur pour une ressource spécifique.</span><span class="sxs-lookup"><span data-stu-id="2fb67-179">Scan error information for a specific resource.</span></span> <span data-ttu-id="2fb67-180">Les informations de ressource spécifiques sont disponibles via la structure de [**\_ données MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb67-180">The specific resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <span data-ttu-id="2fb67-181"><dt>**\_analyse MPNOTIFY \_ infectée**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-181"><dt>**MPNOTIFY\_SCAN\_INFECTED**</dt></span></span> </dl>                   | <span data-ttu-id="2fb67-182">L’analyse a trouvé une ressource infectée.</span><span class="sxs-lookup"><span data-stu-id="2fb67-182">Scan found an infected resource.</span></span> <span data-ttu-id="2fb67-183">Notez que, dans la plupart des cas, cela entraînera une menace signalée à la fin de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2fb67-183">Note that in most of the cases this will result in some threat reported at the end of the scan.</span></span> <span data-ttu-id="2fb67-184">Parfois, il ne peut pas se matérialiser comme une menace en raison d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="2fb67-184">Sometimes it may not materialize as a threat because of exclusions.</span></span> <span data-ttu-id="2fb67-185">Des informations supplémentaires sur les ressources infectées sont disponibles via la structure de [**\_ données MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb67-185">Additional infected resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <span data-ttu-id="2fb67-186"><dt>**MPNOTIFY \_ Scan \_ MEMORYSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-186"><dt>**MPNOTIFY\_SCAN\_MEMORYSTART**</dt></span></span> </dl>          | <span data-ttu-id="2fb67-187">La partie analyse rapide de la totalité de l’analyse a démarré.</span><span class="sxs-lookup"><span data-stu-id="2fb67-187">Quick scan portion of the full scan has started.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <span data-ttu-id="2fb67-188"><dt>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-188"><dt>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="2fb67-189">La partie analyse rapide de l’analyse complète est terminée.</span><span class="sxs-lookup"><span data-stu-id="2fb67-189">Quick scan portion of the full scan has completed.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="2fb67-190"><dt>**\_échec interne \_ MPNOTIFY**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-190"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>          | <span data-ttu-id="2fb67-191">L’opération d’analyse a rencontré un échec générique.</span><span class="sxs-lookup"><span data-stu-id="2fb67-191">Scan operation has encountered a generic failure.</span></span> <span data-ttu-id="2fb67-192">Le *HRESULT* dans [**les \_ données MPCALLBACK**](mpcallback-data.md) contient le code d’erreur spécifique.</span><span class="sxs-lookup"><span data-stu-id="2fb67-192">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="2fb67-193">*phScanHandle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2fb67-193">*phScanHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb67-194">Type : **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="2fb67-194">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="2fb67-195">Handle d’analyse retourné qui identifie l’analyse actuellement lancée.</span><span class="sxs-lookup"><span data-stu-id="2fb67-195">Returned scan handle which identifies the currently initiated scan.</span></span> <span data-ttu-id="2fb67-196">Ce handle peut être utilisé dans les appels de fonction suivants, par exemple pour récupérer un résultat d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2fb67-196">This handle can be used in subsequent function calls, such as to retrieve a scan result.</span></span> <span data-ttu-id="2fb67-197">Le descripteur doit être fermé avec la fonction [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb67-197">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fb67-198">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fb67-198">Return value</span></span>

<span data-ttu-id="2fb67-199">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2fb67-199">Type: **HRESULT**</span></span>

<span data-ttu-id="2fb67-200">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2fb67-200">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="2fb67-201">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="2fb67-201">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="2fb67-202">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2fb67-202">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fb67-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fb67-203">Requirements</span></span>



| <span data-ttu-id="2fb67-204">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fb67-204">Requirement</span></span> | <span data-ttu-id="2fb67-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fb67-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb67-206">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fb67-206">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb67-207">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fb67-207">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2fb67-208">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fb67-208">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb67-209">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fb67-209">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2fb67-210">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fb67-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fb67-211"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-211"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fb67-212">DLL</span><span class="sxs-lookup"><span data-stu-id="2fb67-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fb67-213"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fb67-213"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fb67-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fb67-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb67-215">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="2fb67-215">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="2fb67-216">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="2fb67-216">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="2fb67-217">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="2fb67-217">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="2fb67-218">**\_données MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="2fb67-218">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="2fb67-219">**\_données MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="2fb67-219">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="2fb67-220">**\_ressources MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="2fb67-220">**MPSCAN\_RESOURCES**</span></span>](mpscan-resources.md)
</dt> <dt>

[<span data-ttu-id="2fb67-221">**\_type MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="2fb67-221">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> </dl>

 

 






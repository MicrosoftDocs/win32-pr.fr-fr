---
title: Valeurs retournées
description: Les constantes ci-dessous représentent des valeurs de retour que l’optimisation de remise (DO) génère et des valeurs de retour HTTP qui EFFECTUEnt des captures.
ms.assetid: 68AC4581-C748-49AB-A588-15816E534756
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e58d66587061cc44fc441249407b73653153322
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031599"
---
# <a name="do-return-values"></a><span data-ttu-id="e0be9-103">Valeurs retournées</span><span class="sxs-lookup"><span data-stu-id="e0be9-103">DO Return Values</span></span>

<span data-ttu-id="e0be9-104">Les constantes ci-dessous représentent des valeurs de retour que l’optimisation de remise (DO) génère et des valeurs de retour HTTP qui EFFECTUEnt des captures.</span><span class="sxs-lookup"><span data-stu-id="e0be9-104">The below constants represent return values that Delivery Optimization (DO) generates and HTTP return values that DO captures.</span></span> <span data-ttu-id="e0be9-105">Toutes les autres valeurs de retour que vous pouvez recevoir sont COM, RPC ou les valeurs de retour Windows converties (utilisez la macro [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) pour convertir les valeurs de retour Windows en valeurs HRESULT).</span><span class="sxs-lookup"><span data-stu-id="e0be9-105">All other return values that you can receive are COM, RPC, or converted Windows return values (DO uses the [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<dl> <dt>

<span data-ttu-id="e0be9-106"><span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001)</span><span class="sxs-lookup"><span data-stu-id="e0be9-106"><span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-107">L’optimisation de la distribution n’a pas pu fournir le service.</span><span class="sxs-lookup"><span data-stu-id="e0be9-107">Delivery Optimization was unable to provide the service.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-108"><span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002)</span><span class="sxs-lookup"><span data-stu-id="e0be9-108"><span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-109">Le téléchargement d’un fichier n’a vu aucune progression au cours de la période définie.</span><span class="sxs-lookup"><span data-stu-id="e0be9-109">Download of a file saw no progress within the defined period.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-110"><span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003)</span><span class="sxs-lookup"><span data-stu-id="e0be9-110"><span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-111">La tâche est introuvable, il attend la présence d’un travail.</span><span class="sxs-lookup"><span data-stu-id="e0be9-111">Job was not found, expecting a job to be present.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-112"><span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004)</span><span class="sxs-lookup"><span data-stu-id="e0be9-112"><span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-113">Il n’y avait aucun fichier dans le travail, en attendant au moins un fichier.</span><span class="sxs-lookup"><span data-stu-id="e0be9-113">There was no file in the job, expecting at least one file.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-114"><span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d)</span><span class="sxs-lookup"><span data-stu-id="e0be9-114"><span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-115">Aucun chemin d’accès au fichier local n’est spécifié pour ce téléchargement.</span><span class="sxs-lookup"><span data-stu-id="e0be9-115">There is no local file path specified for this download.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-116"><span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010)</span><span class="sxs-lookup"><span data-stu-id="e0be9-116"><span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-117">Aucun fichier n’est disponible, car aucune URL n’a généré une erreur.</span><span class="sxs-lookup"><span data-stu-id="e0be9-117">No file is available because no URL generated an error.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-118"><span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011)</span><span class="sxs-lookup"><span data-stu-id="e0be9-118"><span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-119">SetProperty () ou GetProperty () appelé avec un ID de propriété inconnu.</span><span class="sxs-lookup"><span data-stu-id="e0be9-119">SetProperty() or GetProperty() called with an unknown property ID.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-120"><span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012)</span><span class="sxs-lookup"><span data-stu-id="e0be9-120"><span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-121">Impossible d’appeler SetProperty () sur une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e0be9-121">Unable to call SetProperty() on a read-only property.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-122"><span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013)</span><span class="sxs-lookup"><span data-stu-id="e0be9-122"><span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-123">L’opération demandée n’est pas autorisée dans l’état actuel du travail.</span><span class="sxs-lookup"><span data-stu-id="e0be9-123">The requested action is not allowed in the current job state.</span></span> <span data-ttu-id="e0be9-124">Le travail a peut-être été annulé ou a terminé son transfert.</span><span class="sxs-lookup"><span data-stu-id="e0be9-124">The job might have been canceled or completed transferring.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-125"><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014)</span><span class="sxs-lookup"><span data-stu-id="e0be9-125"><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-126">Aucune erreur ne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e0be9-126">No errors have occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-127"><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002)</span><span class="sxs-lookup"><span data-stu-id="e0be9-127"><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-128">Le travail de téléchargement n’est pas autorisé en raison des paramètres utilisateur/administrateur.</span><span class="sxs-lookup"><span data-stu-id="e0be9-128">Download job not allowed due to user/admin settings.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-129"><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801)</span><span class="sxs-lookup"><span data-stu-id="e0be9-129"><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-130">Suspendez le travail en raison de restrictions de stratégie de coût.</span><span class="sxs-lookup"><span data-stu-id="e0be9-130">DO paused the job due to cost policy restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-131"><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803)</span><span class="sxs-lookup"><span data-stu-id="e0be9-131"><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-132">Suspendez le travail en raison de la détection des restrictions de réseau cellulaire et de stratégie.</span><span class="sxs-lookup"><span data-stu-id="e0be9-132">DO paused the job due to detection of cellular network and policy restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-133"><span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804)</span><span class="sxs-lookup"><span data-stu-id="e0be9-133"><span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-134">La tâche a été suspendue en raison de la détection du changement d’état d’alimentation en mode non AC.</span><span class="sxs-lookup"><span data-stu-id="e0be9-134">DO paused the job due to detection of power state change into non-AC mode.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-135"><span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805)</span><span class="sxs-lookup"><span data-stu-id="e0be9-135"><span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-136">Interrompez le travail en raison d’une perte de connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="e0be9-136">DO paused the job due to loss of network connectivity.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-137"><span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807)</span><span class="sxs-lookup"><span data-stu-id="e0be9-137"><span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-138">La tâche terminée a été suspendue en raison de la détection du réseau VPN.</span><span class="sxs-lookup"><span data-stu-id="e0be9-138">DO paused the completed job due to detection of VPN network.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-139"><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808)</span><span class="sxs-lookup"><span data-stu-id="e0be9-139"><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-140">La tâche terminée a été suspendue en raison de la détection de l’utilisation de la mémoire critique sur le système.</span><span class="sxs-lookup"><span data-stu-id="e0be9-140">DO paused the completed job due to detection of critical memory usage on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-141"><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001)</span><span class="sxs-lookup"><span data-stu-id="e0be9-141"><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-142">Le serveur HTTP a retourné une réponse dont la taille des données n’est pas égale à ce qui a été demandé.</span><span class="sxs-lookup"><span data-stu-id="e0be9-142">HTTP server returned a response with data size not equal to what was requested.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-143"><span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010)</span><span class="sxs-lookup"><span data-stu-id="e0be9-143"><span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-144">La plage d’octets spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e0be9-144">The specified byte range is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-145"><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011)</span><span class="sxs-lookup"><span data-stu-id="e0be9-145"><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-146">Le serveur ne prend pas en charge le protocole HTTP requis.</span><span class="sxs-lookup"><span data-stu-id="e0be9-146">The server does not support the necessary HTTP protocol.</span></span> <span data-ttu-id="e0be9-147">L’optimisation de la remise (DO) requiert que le serveur prenne en charge l’en-tête de protocole Range.</span><span class="sxs-lookup"><span data-stu-id="e0be9-147">Delivery Optimization (DO) requires that the server support the Range protocol header.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-148"><span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012)</span><span class="sxs-lookup"><span data-stu-id="e0be9-148"><span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-149">La liste de plages d’octets contient des plages qui se chevauchent, ce qui n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e0be9-149">The list of byte ranges contains some overlapping ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e0be9-150"><span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802)</span><span class="sxs-lookup"><span data-stu-id="e0be9-150"><span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802)</span></span>
</dt> <dd>

<span data-ttu-id="e0be9-151">Erreur irrécupérable rencontrée dans le noyau.</span><span class="sxs-lookup"><span data-stu-id="e0be9-151">Fatal error encountered in core.</span></span>

</dd> </dl>

 

 
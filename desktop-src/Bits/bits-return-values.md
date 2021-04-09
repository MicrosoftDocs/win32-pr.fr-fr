---
title: Valeurs de retour BITS
description: Le fichier Bitsmsg. h contient les constantes de valeur de retour suivantes.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- BITS d’erreur
- BITS d’erreur, codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941237"
---
# <a name="bits-return-values"></a><span data-ttu-id="26dd1-105">Valeurs de retour BITS</span><span class="sxs-lookup"><span data-stu-id="26dd1-105">BITS Return Values</span></span>

<span data-ttu-id="26dd1-106">Le fichier Bitsmsg. h contient les constantes de valeur de retour suivantes.</span><span class="sxs-lookup"><span data-stu-id="26dd1-106">The Bitsmsg.h file contains the following return value constants.</span></span> <span data-ttu-id="26dd1-107">Les constantes représentent des valeurs de retour que BITS génère et des valeurs de retour HTTP que BITS capture.</span><span class="sxs-lookup"><span data-stu-id="26dd1-107">The constants represent return values that BITS generates and HTTP return values that BITS captures.</span></span> <span data-ttu-id="26dd1-108">Toutes les autres valeurs de retour que vous pouvez recevoir sont COM, RPC ou les valeurs de retour Windows converties (BITS utilise le [HRESULT de la macro \_ \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) pour convertir les valeurs de retour Windows en valeurs HRESULT).</span><span class="sxs-lookup"><span data-stu-id="26dd1-108">All other return values that you can receive are COM, RPC, or converted Windows return values (BITS uses the [HRESULT\_FROM\_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<span data-ttu-id="26dd1-109">Notez que le fichier Bitsmsg. h contient des valeurs de retour supplémentaires non listées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="26dd1-109">Note that the Bitsmsg.h file contains additional return values not listed below.</span></span>

<dl> <dt>

<span data-ttu-id="26dd1-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>\_ \_ Fin partielle BG S \_ (0x00200017)</span><span class="sxs-lookup"><span data-stu-id="26dd1-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG\_S\_PARTIAL\_COMPLETE (0x00200017)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-111">Un sous-ensemble des fichiers du travail a été transféré correctement avant l’appel de la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="26dd1-111">A subset of the job's files transferred successfully before the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method was called.</span></span> <span data-ttu-id="26dd1-112">Ceux qui n’ont pas été terminés ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="26dd1-112">Those that were not complete were deleted.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S \_ ne peut pas \_ \_ Supprimer les \_ fichiers (0x0020001A)</span><span class="sxs-lookup"><span data-stu-id="26dd1-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG\_S\_UNABLE\_TO\_DELETE\_FILES (0x0020001A)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-114">Impossible de supprimer tous les fichiers temporaires associés au travail.</span><span class="sxs-lookup"><span data-stu-id="26dd1-114">Unable to delete all temporary files associated with the job.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ S \_ remplacé \_ par la \_ stratégie (0x00200055)</span><span class="sxs-lookup"><span data-stu-id="26dd1-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG\_S\_OVERRIDDEN\_BY\_POLICY (0x00200055)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-116">La préférence de configuration a été enregistrée avec succès, mais la préférence n’est pas utilisée, car un paramètre de stratégie de groupe configuré remplace la préférence.</span><span class="sxs-lookup"><span data-stu-id="26dd1-116">The configuration preference has been saved successfully, but the preference will not be used because a configured Group Policy setting overrides the preference.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ \_ introuvable (0x80200001)</span><span class="sxs-lookup"><span data-stu-id="26dd1-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG\_E\_NOT\_FOUND (0x80200001)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-118">La tâche demandée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="26dd1-118">The requested job was not found.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>\_État BG E \_ non valide \_ (0x80200002)</span><span class="sxs-lookup"><span data-stu-id="26dd1-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG\_E\_INVALID\_STATE (0x80200002)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-120">L’opération demandée n’est pas autorisée dans l’état actuel du travail.</span><span class="sxs-lookup"><span data-stu-id="26dd1-120">The requested action is not allowed in the current job state.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ vide (0x80200003)</span><span class="sxs-lookup"><span data-stu-id="26dd1-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG\_E\_EMPTY (0x80200003)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-122">Le travail doit contenir un ou plusieurs fichiers avant de pouvoir reprendre le travail.</span><span class="sxs-lookup"><span data-stu-id="26dd1-122">The job must contain one or more files before you can resume the job.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>\_Fichier BG \_ E \_ non \_ disponible (0x80200004)</span><span class="sxs-lookup"><span data-stu-id="26dd1-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>BG\_E\_FILE\_NOT\_AVAILABLE (0x80200004)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-124">Les informations de fichier ne sont pas disponibles, car l’erreur n’est pas associée à un fichier local ou distant.</span><span class="sxs-lookup"><span data-stu-id="26dd1-124">File information is not available because the error is not associated with a local or remote file.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>\_Protocole BG \_ E \_ non \_ disponible (0x80200005)</span><span class="sxs-lookup"><span data-stu-id="26dd1-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>BG\_E\_PROTOCOL\_NOT\_AVAILABLE (0x80200005)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-126">Les informations de protocole ne sont pas disponibles, car l’erreur n’est pas associée au protocole de transfert spécifié.</span><span class="sxs-lookup"><span data-stu-id="26dd1-126">Protocol information is not available because the error is not associated with the specified transfer protocol.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>\_Destination BG \_ E \_ verrouillée (0x8020000D)</span><span class="sxs-lookup"><span data-stu-id="26dd1-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG\_E\_DESTINATION\_LOCKED (0x8020000D)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-128">Le volume du système de fichiers de destination, spécifié dans le nom de fichier local, est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="26dd1-128">The destination file system volume, specified in the local file name, is locked.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>\_Volume E \_ BG \_ modifié (0x8020000E)</span><span class="sxs-lookup"><span data-stu-id="26dd1-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG\_E\_VOLUME\_CHANGED (0x8020000E)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-130">Le volume de destination, spécifié dans le nom de fichier local, a changé.</span><span class="sxs-lookup"><span data-stu-id="26dd1-130">The destination volume, specified in the local file name, has changed.</span></span> <span data-ttu-id="26dd1-131">Par exemple, la disquette d’origine a été remplacée par une autre disquette.</span><span class="sxs-lookup"><span data-stu-id="26dd1-131">For example, the original floppy disk has been replaced with a different floppy disk.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>\_Informations d’erreur BG E \_ \_ \_ non disponibles (0x8020000F)</span><span class="sxs-lookup"><span data-stu-id="26dd1-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>BG\_E\_ERROR\_INFORMATION\_UNAVAILABLE (0x8020000F)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-133">Les informations d’erreur sont disponibles uniquement lorsque l’état du travail est \_ erreur d’état de la tâche BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="26dd1-133">Error information is only available when the state of the job is BG\_JOB\_STATE\_ERROR.</span></span> <span data-ttu-id="26dd1-134">Les informations sur l’erreur ne sont pas disponibles une fois que le service BITS a commencé à transférer les données du travail ou que le client se ferme.</span><span class="sxs-lookup"><span data-stu-id="26dd1-134">The error information is not available after BITS begins transferring the job's data or the client exits.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>\_Réseau BG \_ E \_ déconnecté (0x80200010)</span><span class="sxs-lookup"><span data-stu-id="26dd1-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG\_E\_NETWORK\_DISCONNECTED (0x80200010)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-136">La carte réseau est inactive ou déconnectée.</span><span class="sxs-lookup"><span data-stu-id="26dd1-136">The network adapter is inactive or disconnected.</span></span> <span data-ttu-id="26dd1-137">Toutes les tâches sont placées dans \_ l' \_ \_ État d' \_ erreur temporaire de l’état de travail BG.</span><span class="sxs-lookup"><span data-stu-id="26dd1-137">All jobs are placed in the BG\_JOB\_STATE\_TRANSIENT\_ERROR state.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>\_ \_ Taille de fichier manquante BG E \_ \_ (0x80200011)</span><span class="sxs-lookup"><span data-stu-id="26dd1-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG\_E\_MISSING\_FILE\_SIZE (0x80200011)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-139">Le serveur n’a pas retourné la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="26dd1-139">The server did not return the file size.</span></span> <span data-ttu-id="26dd1-140">BITS transfère uniquement le contenu statique et nécessite que le serveur HTTP retourne l’en-tête Content-Length.</span><span class="sxs-lookup"><span data-stu-id="26dd1-140">BITS only transfers static content and requires the HTTP server to return the Content-Length header.</span></span> <span data-ttu-id="26dd1-141">La demande de transfert échoue si l’URL pointe vers du contenu dynamique.</span><span class="sxs-lookup"><span data-stu-id="26dd1-141">The transfer request fails if the URL points to dynamic content.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>\_ \_ \_ Prise en charge http insuffisante de BG E \_ (0x80200012)</span><span class="sxs-lookup"><span data-stu-id="26dd1-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG\_E\_INSUFFICIENT\_HTTP\_SUPPORT (0x80200012)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-143">Le serveur ne prend pas en charge le protocole HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="26dd1-143">The server does not support the HTTP/1.1 protocol.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>\_ \_ Prise en charge de la plage BG E insuffisante \_ \_ (0x80200013)</span><span class="sxs-lookup"><span data-stu-id="26dd1-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG\_E\_INSUFFICIENT\_RANGE\_SUPPORT (0x80200013)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-145">Le serveur ne prend pas en charge l’en-tête Content-Range.</span><span class="sxs-lookup"><span data-stu-id="26dd1-145">The server does not support the Content-Range header.</span></span> <span data-ttu-id="26dd1-146">En règle générale, cette erreur s’affiche lorsque vous essayez de télécharger du contenu dynamique.</span><span class="sxs-lookup"><span data-stu-id="26dd1-146">Typically, you receive this error when you try to download dynamic content.</span></span> <span data-ttu-id="26dd1-147">Vous pouvez également recevoir cette erreur si un proxy intermédiaire supprime l’en-tête Content-Range ou Content-Length.</span><span class="sxs-lookup"><span data-stu-id="26dd1-147">You can also receive this error if an intermediate proxy is removing the Content-Range or Content-Length header.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG \_ E \_ Remote \_ non \_ pris en charge (0x80200014)</span><span class="sxs-lookup"><span data-stu-id="26dd1-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG\_E\_REMOTE\_NOT\_SUPPORTED (0x80200014)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-149">L’utilisation à distance de BITS n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="26dd1-149">Remote use of BITS is not supported.</span></span> <span data-ttu-id="26dd1-150">Pour plus d’informations, consultez [utilisateurs et connexions réseau](users-and-network-connections.md).</span><span class="sxs-lookup"><span data-stu-id="26dd1-150">For more information, see [Users and Network Connections](users-and-network-connections.md).</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>\_ \_ Mappage diff du nouveau propriétaire BG E \_ \_ \_ (0x80200015)</span><span class="sxs-lookup"><span data-stu-id="26dd1-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG\_E\_NEW\_OWNER\_DIFF\_MAPPING (0x80200015)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-152">Le mappage de lecteur réseau pour le fichier local est différent pour le propriétaire actuel que pour le propriétaire précédent.</span><span class="sxs-lookup"><span data-stu-id="26dd1-152">The network drive mapping for the local file is different for the current owner than for the previous owner.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ nouveau \_ propriétaire \_ aucun \_ \_ accès aux fichiers (0x80200016)</span><span class="sxs-lookup"><span data-stu-id="26dd1-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG\_E\_NEW\_OWNER\_NO\_FILE\_ACCESS (0x80200016)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-154">Le nouveau propriétaire ne dispose pas des autorisations suffisantes pour les fichiers de tâche temporaires.</span><span class="sxs-lookup"><span data-stu-id="26dd1-154">The new owner has insufficient permissions to the temporary job files.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>\_ \_ Liste de proxy BG E \_ \_ trop \_ grande (0x80200018)</span><span class="sxs-lookup"><span data-stu-id="26dd1-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG\_E\_PROXY\_LIST\_TOO\_LARGE (0x80200018)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-156">La liste de proxy HTTP est trop longue.</span><span class="sxs-lookup"><span data-stu-id="26dd1-156">The HTTP proxy list is too long.</span></span> <span data-ttu-id="26dd1-157">La liste ne doit pas dépasser 32 Ko.</span><span class="sxs-lookup"><span data-stu-id="26dd1-157">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>\_ \_ Liste de contournement du proxy BG E \_ \_ \_ trop \_ grande (0x80200019)</span><span class="sxs-lookup"><span data-stu-id="26dd1-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG\_E\_PROXY\_BYPASS\_LIST\_TOO\_LARGE (0x80200019)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-159">La liste de contournement du proxy HTTP est trop longue.</span><span class="sxs-lookup"><span data-stu-id="26dd1-159">The HTTP proxy bypass list is too long.</span></span> <span data-ttu-id="26dd1-160">La liste ne doit pas dépasser 32 Ko.</span><span class="sxs-lookup"><span data-stu-id="26dd1-160">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ E \_ \_ \_ de fichiers trop nombreux (0x8020001C)</span><span class="sxs-lookup"><span data-stu-id="26dd1-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG\_E\_TOO\_MANY\_FILES (0x8020001C)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-162">Vous ne pouvez pas ajouter plusieurs fichiers à un travail de chargement.</span><span class="sxs-lookup"><span data-stu-id="26dd1-162">You cannot add more than one file to an upload job.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>\_ \_ Fichier local BG \_ E \_ modifié (0x8020001D)</span><span class="sxs-lookup"><span data-stu-id="26dd1-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG\_E\_LOCAL\_FILE\_CHANGED (0x8020001D)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-164">Le contenu du fichier local a été modifié après le début du processus de transfert.</span><span class="sxs-lookup"><span data-stu-id="26dd1-164">The contents of the local file changed after the transfer process began.</span></span> <span data-ttu-id="26dd1-165">Le contenu du fichier local ne peut pas être modifié après le début du processus de transfert sur un travail de chargement ou de chargement-réponse.</span><span class="sxs-lookup"><span data-stu-id="26dd1-165">The contents of the local file cannot change after the transfer process begins on an upload or upload-reply job.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ trop \_ grande (0x80200020)</span><span class="sxs-lookup"><span data-stu-id="26dd1-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG\_E\_TOO\_LARGE (0x80200020)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-167">La taille du fichier de chargement dépasse la taille de téléchargement maximale autorisée spécifiée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="26dd1-167">The size of the upload file exceeds the maximum allowed upload size specified on the server.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>\_Chaîne BG \_ E \_ trop \_ longue (0x80200021)</span><span class="sxs-lookup"><span data-stu-id="26dd1-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG\_E\_STRING\_TOO\_LONG (0x80200021)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-169">La chaîne spécifiée est trop longue.</span><span class="sxs-lookup"><span data-stu-id="26dd1-169">The specified string is too long.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>\_Incompatibilité \_ de protocole du serveur client BG E \_ \_ \_ (0x80200022)</span><span class="sxs-lookup"><span data-stu-id="26dd1-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>BG\_E\_CLIENT\_SERVER\_PROTOCOL\_MISMATCH (0x80200022)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-171">Le client et le serveur n’ont pas pu négocier un protocole à utiliser pour le travail de chargement.</span><span class="sxs-lookup"><span data-stu-id="26dd1-171">The client and server were unable to negotiate a protocol to use for the upload job.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>\_Exécution du serveur BG E \_ \_ \_ activée (0x80200023)</span><span class="sxs-lookup"><span data-stu-id="26dd1-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG\_E\_SERVER\_EXECUTE\_ENABLED (0x80200023)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-173">Les autorisations de script ou d’exécution sont activées sur le répertoire virtuel IIS associé au travail.</span><span class="sxs-lookup"><span data-stu-id="26dd1-173">Scripting or execute permissions are enabled on the IIS virtual directory associated with the job.</span></span> <span data-ttu-id="26dd1-174">Pour charger des fichiers dans le répertoire virtuel, désactivez les autorisations de script et d’exécution sur le répertoire virtuel.</span><span class="sxs-lookup"><span data-stu-id="26dd1-174">To upload files to the virtual directory, disable the scripting and execute permissions on the virtual directory.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>\_ \_ Nom d’utilisateur BG E \_ trop \_ grand (0x80200025)</span><span class="sxs-lookup"><span data-stu-id="26dd1-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG\_E\_USERNAME\_TOO\_LARGE (0x80200025)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-176">Le nom d’utilisateur ne peut pas dépasser 300 caractères.</span><span class="sxs-lookup"><span data-stu-id="26dd1-176">The user name cannot exceed 300 characters.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>\_ \_ Mot de passe BG E \_ trop \_ grand (0x80200026)</span><span class="sxs-lookup"><span data-stu-id="26dd1-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG\_E\_PASSWORD\_TOO\_LARGE (0x80200026)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-178">Le mot de passe ne peut pas dépasser 65535 caractères.</span><span class="sxs-lookup"><span data-stu-id="26dd1-178">The password cannot exceed 65535 characters.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG \_ E \_ cible d’authentification non valide \_ \_ (0x80200027)</span><span class="sxs-lookup"><span data-stu-id="26dd1-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG\_E\_INVALID\_AUTH\_TARGET (0x80200027)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-180">La cible d’authentification spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="26dd1-180">The specified authentication target is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG \_ E \_ schéma d’authentification non valide \_ \_ (0x80200028)</span><span class="sxs-lookup"><span data-stu-id="26dd1-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG\_E\_INVALID\_AUTH\_SCHEME (0x80200028)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-182">Le schéma d’authentification spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="26dd1-182">The specified authentication scheme is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>\_Plage BG E \_ non valide \_ (0x8020002B)</span><span class="sxs-lookup"><span data-stu-id="26dd1-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG\_E\_INVALID\_RANGE (0x8020002B)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-184">La plage d’octets spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="26dd1-184">The specified byte range is invalid.</span></span> <span data-ttu-id="26dd1-185">La plage d’octets doit exister dans le fichier distant spécifié.</span><span class="sxs-lookup"><span data-stu-id="26dd1-185">The byte range must exist within the specified remote file.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>\_ \_ Plages superposées BG E \_ (0x8020002C)</span><span class="sxs-lookup"><span data-stu-id="26dd1-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG\_E\_OVERLAPPING\_RANGES (0x8020002C)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-187">La liste de plages d’octets contient des plages qui se chevauchent ou qui ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="26dd1-187">The list of byte ranges contains overlapping or duplicate ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ bloqué \_ par la \_ stratégie (0x8020003E)</span><span class="sxs-lookup"><span data-stu-id="26dd1-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG\_E\_BLOCKED\_BY\_POLICY (0x8020003E)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-189">Stratégie de groupe paramètres empêchent l’exécution des tâches en arrière-plan pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="26dd1-189">Group Policy settings prevent background jobs from running at this time.</span></span> <span data-ttu-id="26dd1-190">Pour plus d’informations, consultez la stratégie [MaxInternetBandwidth](group-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="26dd1-190">For details, see the [MaxInternetBandwidth](group-policies.md) policy.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>\_ \_ Informations de proxy BG E non valide \_ \_ (0x8020003F)</span><span class="sxs-lookup"><span data-stu-id="26dd1-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG\_E\_INVALID\_PROXY\_INFO (0x8020003F)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-192">Erreur d’exécution qui indique la liste de proxy ou la liste de contournement du proxy que vous avez spécifiée à l’aide de la méthode [**méthode ibackgroundcopyjob :: setproxysettings n'**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="26dd1-192">Run-time error that indicates the proxy list or proxy bypass list that you specified using the [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) method is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG \_ E \_ \_ informations d’identification non valides (0x80200040)</span><span class="sxs-lookup"><span data-stu-id="26dd1-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG\_E\_INVALID\_CREDENTIALS (0x80200040)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-194">Le format des informations d’identification de sécurité fournies n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="26dd1-194">The format of the supplied security credentials is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>\_Enregistrement BG \_ E \_ supprimé (0x80200042)</span><span class="sxs-lookup"><span data-stu-id="26dd1-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG\_E\_RECORD\_DELETED (0x80200042)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-196">L’enregistrement du cache a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="26dd1-196">The cache record has been deleted.</span></span> <span data-ttu-id="26dd1-197">La tentative de mise à jour a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="26dd1-197">The attempt to update it has been abandoned.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>\_Erreur de plug-in BG E \_ \_ (0x80200045)</span><span class="sxs-lookup"><span data-stu-id="26dd1-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG\_E\_UPNP\_ERROR (0x80200045)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-199">Une erreur UPnP (Universal Plug-and-Play) s’est produite.</span><span class="sxs-lookup"><span data-stu-id="26dd1-199">A Universal Plug and Play (UPnP) error has occurred.</span></span> <span data-ttu-id="26dd1-200">Vérifiez votre périphérique de passerelle Internet.</span><span class="sxs-lookup"><span data-stu-id="26dd1-200">Please check your Internet Gateway Device.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>En \_ - \_ cache BG E \_ désactivé (0x80200047)</span><span class="sxs-lookup"><span data-stu-id="26dd1-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG\_E\_PEERCACHING\_DISABLED (0x80200047)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-202">La mise en cache d’homologue est désactivée.</span><span class="sxs-lookup"><span data-stu-id="26dd1-202">Peer-caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048)</span><span class="sxs-lookup"><span data-stu-id="26dd1-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG\_E\_BUSYCACHERECORD (0x80200048)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-204">L’enregistrement du cache est en cours d’utilisation et ne peut pas être modifié ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="26dd1-204">The cache record is in use and cannot be changed or deleted.</span></span> <span data-ttu-id="26dd1-205">Réessayez après quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="26dd1-205">Try again after a few seconds.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E \_ trop \_ \_ de travaux \_ par \_ utilisateur (0x80200049)</span><span class="sxs-lookup"><span data-stu-id="26dd1-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_USER (0x80200049)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-207">Le nombre de tâches pour l’utilisateur a dépassé la limite de tâches par utilisateur définie par le paramètre de stratégie de groupe MaxJobsPerUser.</span><span class="sxs-lookup"><span data-stu-id="26dd1-207">The job count for the user has exceeded the per user job limit set by the MaxJobsPerUser Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E \_ trop \_ \_ de travaux \_ par \_ ordinateur (0x80200050)</span><span class="sxs-lookup"><span data-stu-id="26dd1-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_MACHINE (0x80200050)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-209">Le nombre de tâches de l’ordinateur a dépassé la limite par ordinateur définie par le paramètre de stratégie de groupe MaxJobsPerMachine.</span><span class="sxs-lookup"><span data-stu-id="26dd1-209">The job count for the computer has exceeded the per computer job limit set by the MaxJobsPerMachine Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E \_ \_ \_ de fichiers trop nombreux dans le \_ \_ travail (0x80200051)</span><span class="sxs-lookup"><span data-stu-id="26dd1-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG\_E\_TOO\_MANY\_FILES\_IN\_JOB (0x80200051)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-211">Le nombre de fichiers pour le travail a dépassé la limite de fichiers par tâche définie par le paramètre de stratégie de groupe MaxFilesPerJob.</span><span class="sxs-lookup"><span data-stu-id="26dd1-211">The file count for the job has exceeded the per job file limit set by the MaxFilesPerJob Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E \_ trop \_ \_ de plages \_ dans le \_ fichier (0x80200052)</span><span class="sxs-lookup"><span data-stu-id="26dd1-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG\_E\_TOO\_MANY\_RANGES\_IN\_FILE (0x80200052)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-213">Le nombre de plages du fichier a dépassé la limite de plages par fichier définie par le paramètre de stratégie de groupe MaxRangesPerFile.</span><span class="sxs-lookup"><span data-stu-id="26dd1-213">The range count for the file has exceeded the per file range limit set by the MaxRangesPerFile Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>\_ \_ Échec de la validation BG E \_ (0x80200053)</span><span class="sxs-lookup"><span data-stu-id="26dd1-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG\_E\_VALIDATION\_FAILED (0x80200053)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-215">L’application a demandé des données à partir d’un site Web, mais la réponse n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="26dd1-215">The application requested data from a website, but the response was not valid.</span></span> <span data-ttu-id="26dd1-216">Pour plus d’informations, utilisez observateur d’événements pour afficher le \\ Journal des opérations des journaux des applications Microsoft \\ Windows \\ bits-client \\ .</span><span class="sxs-lookup"><span data-stu-id="26dd1-216">For details, use Event Viewer to view the Application Logs\\Microsoft\\Windows\\Bits-client\\Operational log.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>\_ \_ \_ Délai d’expiration de MAXDOWNLOAD BG E (0x80200054)</span><span class="sxs-lookup"><span data-stu-id="26dd1-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG\_E\_MAXDOWNLOAD\_TIMEOUT (0x80200054)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-218">Le service BITS a dépassé le délai de téléchargement du travail.</span><span class="sxs-lookup"><span data-stu-id="26dd1-218">BITS timed out downloading the job.</span></span> <span data-ttu-id="26dd1-219">Le téléchargement ne s’est pas terminé dans le délai de téléchargement maximal défini sur le travail ou le paramètre de stratégie de groupe MaxDownloadTime.</span><span class="sxs-lookup"><span data-stu-id="26dd1-219">The download did not complete within the maximum download time set on the job or the MaxDownloadTime Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>\_Erreur BG \_ E \_ http \_ 400 (0x80190190)</span><span class="sxs-lookup"><span data-stu-id="26dd1-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG\_E\_HTTP\_ERROR\_400 (0x80190190)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-221">Le serveur n’a pas pu traiter la demande de transfert car la syntaxe du nom de fichier distant n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="26dd1-221">The server could not process the transfer request because the syntax of the remote file name is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>\_Erreur BG \_ E \_ http \_ 401 (0x80190191)</span><span class="sxs-lookup"><span data-stu-id="26dd1-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG\_E\_HTTP\_ERROR\_401 (0x80190191)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-223">L’utilisateur n’a pas l’autorisation d’accéder au fichier distant.</span><span class="sxs-lookup"><span data-stu-id="26dd1-223">The user does not have permission to access the remote file.</span></span> <span data-ttu-id="26dd1-224">La ressource demandée nécessite l'authentification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="26dd1-224">The requested resource requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>\_Erreur BG \_ E \_ http \_ 404 (0x80190194)</span><span class="sxs-lookup"><span data-stu-id="26dd1-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG\_E\_HTTP\_ERROR\_404 (0x80190194)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-226">L’URL demandée n’existe pas sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="26dd1-226">The requested URL does not exist on the server.</span></span>

<span data-ttu-id="26dd1-227">Dans IIS 7, cette erreur peut indiquer</span><span class="sxs-lookup"><span data-stu-id="26dd1-227">In IIS 7, this error can indicate</span></span>

-   <span data-ttu-id="26dd1-228">Les téléchargements BITS ne sont pas activés sur le répertoire virtuel (vdir) sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="26dd1-228">That BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>
-   <span data-ttu-id="26dd1-229">Que la taille de téléchargement dépasse la limite maximale de chargement (pour plus d’informations, consultez la propriété d’extension IIS [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) ).</span><span class="sxs-lookup"><span data-stu-id="26dd1-229">That the upload size exceeds the maximum upload limit (for details, see the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property).</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>\_Erreur BG \_ E \_ http \_ 407 (0x80190197)</span><span class="sxs-lookup"><span data-stu-id="26dd1-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG\_E\_HTTP\_ERROR\_407 (0x80190197)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-231">L’utilisateur n’a pas l’autorisation d’accéder au proxy.</span><span class="sxs-lookup"><span data-stu-id="26dd1-231">The user does not have permission to access the proxy.</span></span> <span data-ttu-id="26dd1-232">Le proxy requiert l’authentification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="26dd1-232">The proxy requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>\_Erreur BG \_ E \_ http \_ 414 (0x8019019E)</span><span class="sxs-lookup"><span data-stu-id="26dd1-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG\_E\_HTTP\_ERROR\_414 (0x8019019E)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-234">Le serveur ne peut pas traiter la demande de transfert.</span><span class="sxs-lookup"><span data-stu-id="26dd1-234">The server cannot process the transfer request.</span></span> <span data-ttu-id="26dd1-235">Le Uniform Resource Identifier (URI) dans le nom de fichier distant est plus long que le serveur ne peut interpréter.</span><span class="sxs-lookup"><span data-stu-id="26dd1-235">The Uniform Resource Identifier (URI) in the remote file name is longer than the server can interpret.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>\_Erreur BG \_ E \_ http \_ 501 (0x801901F5)</span><span class="sxs-lookup"><span data-stu-id="26dd1-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG\_E\_HTTP\_ERROR\_501 (0x801901F5)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-237">Le serveur ne prend pas en charge les fonctionnalités requises pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="26dd1-237">The server does not support the functionality required to fulfill the request.</span></span> <span data-ttu-id="26dd1-238">Dans IIS 6, cette erreur indique que les téléchargements BITS ne sont pas activés sur le répertoire virtuel (vdir) sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="26dd1-238">In IIS 6, this error indicates that BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>\_Erreur BG \_ E \_ http \_ 503 (0x801901F7)</span><span class="sxs-lookup"><span data-stu-id="26dd1-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG\_E\_HTTP\_ERROR\_503 (0x801901F7)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-240">Le service est temporairement surchargé et ne peut pas traiter la requête.</span><span class="sxs-lookup"><span data-stu-id="26dd1-240">The service is temporarily overloaded and cannot process the request.</span></span> <span data-ttu-id="26dd1-241">Reprendre la tâche ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="26dd1-241">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>\_Erreur BG \_ E \_ http \_ 504 (0x801901F8)</span><span class="sxs-lookup"><span data-stu-id="26dd1-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG\_E\_HTTP\_ERROR\_504 (0x801901F8)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-243">La demande de transfert a expiré pendant l’attente d’une passerelle.</span><span class="sxs-lookup"><span data-stu-id="26dd1-243">The transfer request timed out while waiting for a gateway.</span></span> <span data-ttu-id="26dd1-244">Reprendre la tâche ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="26dd1-244">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="26dd1-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>\_Erreur BG \_ E \_ http \_ 505 (0x801901F9)</span><span class="sxs-lookup"><span data-stu-id="26dd1-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG\_E\_HTTP\_ERROR\_505 (0x801901F9)</span></span>
</dt> <dd>

<span data-ttu-id="26dd1-246">Le serveur ne prend pas en charge la version du protocole HTTP spécifiée dans le nom du fichier distant.</span><span class="sxs-lookup"><span data-stu-id="26dd1-246">The server does not support the HTTP protocol version specified in the remote file name.</span></span>

</dd> </dl>

<span data-ttu-id="26dd1-247">Le fichier d’en-tête Bitsmsg. h contient des valeurs de retour HTTP supplémentaires non listées ci-dessus que BITS utilise en interne.</span><span class="sxs-lookup"><span data-stu-id="26dd1-247">The Bitsmsg.h header file contains additional HTTP return values not listed above that BITS uses internally.</span></span> <span data-ttu-id="26dd1-248">Pour plus d’informations sur ces valeurs et sur les autres valeurs de retour HTTP que vous pouvez recevoir, consultez la spécification RFC 2616 de la page IETF (Internet Engineering Task Force) à l’adresse [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .</span><span class="sxs-lookup"><span data-stu-id="26dd1-248">For information on these and other HTTP return values you can receive, see the RFC 2616 specification from the Internet Engineering Task Force at [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10).</span></span>

 

 
---
description: 'En savoir plus sur : fonction JetGetTruncateLogInfoInstance'
title: JetGetTruncateLogInfoInstance fonction)
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d51243ff6ca4b2bbaec77233bbe00437f55e0f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519543"
---
# <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="76007-103">JetGetTruncateLogInfoInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="76007-103">JetGetTruncateLogInfoInstance Function</span></span>


<span data-ttu-id="76007-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="76007-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="76007-105">JetGetTruncateLogInfoInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="76007-105">JetGetTruncateLogInfoInstance Function</span></span>

<span data-ttu-id="76007-106">La fonction **JetGetTruncateLogInfoInstance** est utilisée lors d’une sauvegarde initiée par [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) pour interroger une instance afin d’obtenir les noms des fichiers journaux des transactions qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée.</span><span class="sxs-lookup"><span data-stu-id="76007-106">The **JetGetTruncateLogInfoInstance** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="76007-107">**Windows XP :**  **JetGetTruncateLogInfoInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76007-107">**Windows XP:**  **JetGetTruncateLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="76007-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76007-108">Parameters</span></span>

<span data-ttu-id="76007-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="76007-109">*instance*</span></span>

<span data-ttu-id="76007-110">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="76007-110">The instance to use for this call.</span></span>

<span data-ttu-id="76007-111">*szz*</span><span class="sxs-lookup"><span data-stu-id="76007-111">*szz*</span></span>

<span data-ttu-id="76007-112">Mémoire tampon de sortie qui reçoit la liste des chaînes terminées par le caractère null qui décrivent l’ensemble des fichiers journaux des transactions qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée.</span><span class="sxs-lookup"><span data-stu-id="76007-112">The output buffer that receives the list of null-terminated strings describing the set of transaction log files that can be safely deleted after the backup has been completed successfully.</span></span>

<span data-ttu-id="76007-113">La liste des chaînes retournées dans cette mémoire tampon est au même format qu’une chaîne multiple utilisée par le registre.</span><span class="sxs-lookup"><span data-stu-id="76007-113">The list of strings that are returned in this buffer is in the same format as a multi-string that is used by the registry.</span></span> <span data-ttu-id="76007-114">Chaque chaîne terminée par le caractère NULL est retournée dans l’ordre et suivie d’une marque de fin null finale.</span><span class="sxs-lookup"><span data-stu-id="76007-114">Each null-terminated string is returned in sequence and followed by a final null terminator.</span></span>

<span data-ttu-id="76007-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="76007-115">*cbMax*</span></span>

<span data-ttu-id="76007-116">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="76007-116">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="76007-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="76007-117">*pcbActual*</span></span>

<span data-ttu-id="76007-118">Pointeur vers la mémoire tampon de sortie qui reçoit la quantité réelle de données de chaîne.</span><span class="sxs-lookup"><span data-stu-id="76007-118">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="76007-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="76007-119">Return Value</span></span>

<span data-ttu-id="76007-120">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="76007-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="76007-121">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="76007-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76007-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="76007-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="76007-123">Description</span><span class="sxs-lookup"><span data-stu-id="76007-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76007-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="76007-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="76007-125">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="76007-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76007-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="76007-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="76007-127">L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a entraîné un résultat inattendu.</span><span class="sxs-lookup"><span data-stu-id="76007-127">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="76007-128"><strong>Windows XP et versions ultérieures :</strong>  Cela peut se produire pour <strong>JetGetTruncateLogInfoInstance</strong> lorsque le handle d’instance spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="76007-128"><strong>Windows XP and later:</strong>  This can happen for <strong>JetGetTruncateLogInfoInstance</strong> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76007-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="76007-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="76007-130">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="76007-130">The operation cannot complete because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76007-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="76007-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="76007-132">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="76007-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76007-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="76007-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="76007-134">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="76007-134">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="76007-135"><strong>Windows XP :</strong>  Cette valeur de retour a été introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76007-135"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76007-136">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="76007-136">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="76007-137">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="76007-137">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="76007-138"><strong>Windows XP :</strong>  Cette valeur de retour a été introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76007-138"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76007-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="76007-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="76007-140">L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</span><span class="sxs-lookup"><span data-stu-id="76007-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76007-141">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="76007-141">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="76007-142">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="76007-142">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76007-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="76007-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="76007-144">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="76007-144">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76007-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="76007-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="76007-146">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="76007-146">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76007-147"><strong>JetGetTruncateLogInfoInstance</strong></span><span class="sxs-lookup"><span data-stu-id="76007-147"><strong>JetGetTruncateLogInfoInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="76007-148">Des descripteurs de fichiers en attente ont été créés à l’aide de <a href="gg269249(v=exchg.10).md">JetOpenFile</a> pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="76007-148">There are outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="76007-149">Si cette fonction réussit, les informations demandées sur l’ensemble des fichiers journaux des transactions qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée, sont placées dans les tampons de sortie où elles sont fournies.</span><span class="sxs-lookup"><span data-stu-id="76007-149">If this function succeeds, the requested information about the set of transaction log files that can be safely deleted after the backup has been completed successfully will be placed in the output buffers where they are provided.</span></span> <span data-ttu-id="76007-150">L’ordinateur d’état de sauvegarde est avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée.</span><span class="sxs-lookup"><span data-stu-id="76007-150">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="76007-151">Seuls les fichiers de correctifs de base de données et les fichiers journaux de transactions peuvent être ouverts pour la sauvegarde au-delà de ce point.</span><span class="sxs-lookup"><span data-stu-id="76007-151">Only database patch files and transaction log files can be opened for backup beyond this point.</span></span>

<span data-ttu-id="76007-152">Si cette fonction échoue, l’état des mémoires tampons de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="76007-152">If this function fails, the state of the output buffers is undefined.</span></span> <span data-ttu-id="76007-153">L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance.</span><span class="sxs-lookup"><span data-stu-id="76007-153">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="76007-154">Notes</span><span class="sxs-lookup"><span data-stu-id="76007-154">Remarks</span></span>

<span data-ttu-id="76007-155">Cette API ne retourne pas d’erreur ou d’avertissement si la mémoire tampon de sortie est trop petite pour accepter la liste complète des fichiers qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="76007-155">This API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="76007-156">L’application doit toujours fournir une mémoire tampon pour recevoir la taille réelle de cette liste et utiliser ces informations pour déterminer si la liste a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="76007-156">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="76007-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76007-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76007-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="76007-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="76007-159">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76007-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76007-160"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="76007-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="76007-161">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="76007-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76007-162"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="76007-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="76007-163">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="76007-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76007-164"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="76007-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="76007-165">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="76007-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76007-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="76007-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="76007-167">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="76007-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76007-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="76007-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="76007-169">Implémenté en tant que <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) et <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="76007-169">Implemented as <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) and <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="76007-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76007-170">See Also</span></span>

[<span data-ttu-id="76007-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="76007-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="76007-172">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="76007-172">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="76007-173">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="76007-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="76007-174">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="76007-174">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="76007-175">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="76007-175">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="76007-176">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="76007-176">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="76007-177">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="76007-177">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="76007-178">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="76007-178">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="76007-179">JetRollback</span><span class="sxs-lookup"><span data-stu-id="76007-179">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="76007-180">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="76007-180">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="76007-181">JetStopService</span><span class="sxs-lookup"><span data-stu-id="76007-181">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="76007-182">JetTerm</span><span class="sxs-lookup"><span data-stu-id="76007-182">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="76007-183">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="76007-183">JetTerm2</span></span>](./jetterm2-function.md)

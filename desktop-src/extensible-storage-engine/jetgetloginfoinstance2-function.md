---
description: 'En savoir plus sur : fonction JetGetLogInfoInstance2'
title: JetGetLogInfoInstance2 fonction)
TOCTitle: JetGetLogInfoInstance2 Function
ms:assetid: 50fdae92-611c-4dbf-846e-86cc836a23db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269247(v=EXCHG.10)
ms:contentKeyID: 32765549
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance2W
- JetGetLogInfoInstance2
- JetGetLogInfoInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f58a04c49a82604fb5ded09b6328e9e03df7963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525086"
---
# <a name="jetgetloginfoinstance2-function"></a><span data-ttu-id="892a0-103">JetGetLogInfoInstance2 fonction)</span><span class="sxs-lookup"><span data-stu-id="892a0-103">JetGetLogInfoInstance2 Function</span></span>


<span data-ttu-id="892a0-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="892a0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfoinstance2-function"></a><span data-ttu-id="892a0-105">JetGetLogInfoInstance2 fonction)</span><span class="sxs-lookup"><span data-stu-id="892a0-105">JetGetLogInfoInstance2 Function</span></span>

<span data-ttu-id="892a0-106">La fonction **JetGetLogInfoInstance2** est utilisée lors d’une sauvegarde lancée par [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) pour interroger une instance pour obtenir les noms des fichiers de correctifs de base de données et des fichiers journaux des transactions qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="892a0-106">The **JetGetLogInfoInstance2** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="892a0-107">Ces fichiers peuvent être ouverts par la suite à l’aide de [JetOpenFile](./jetopenfile-function.md) et lus à l’aide de [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="892a0-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

<span data-ttu-id="892a0-108">**Windows XP : JetGetLogInfoInstance2** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="892a0-108">**Windows XP:  JetGetLogInfoInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfoInstance2(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in_out_opt  JET_LOGINFO* pLogInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="892a0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="892a0-109">Parameters</span></span>

<span data-ttu-id="892a0-110">*instancié*</span><span class="sxs-lookup"><span data-stu-id="892a0-110">*instance*</span></span>

<span data-ttu-id="892a0-111">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="892a0-111">The instance to use for this call.</span></span>

<span data-ttu-id="892a0-112">Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="892a0-112">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="892a0-113">L’utilisation de cette instance globale est implicitement dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="892a0-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="892a0-114">Pour Windows XP et les versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) alors qu’une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="892a0-114">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="892a0-115">Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="892a0-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="892a0-116">*szz*</span><span class="sxs-lookup"><span data-stu-id="892a0-116">*szz*</span></span>

<span data-ttu-id="892a0-117">Mémoire tampon de sortie qui recevra la liste des chaînes terminées par un caractère null qui décrivent l’ensemble des fichiers de correctifs de base de données et des fichiers journaux des transactions qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="892a0-117">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="892a0-118">La liste de chaînes retournée dans cette mémoire tampon est dans le même format qu’une chaîne multiple utilisée par le registre.</span><span class="sxs-lookup"><span data-stu-id="892a0-118">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="892a0-119">Chaque chaîne se terminant par une valeur null est retournée dans la séquence suivie d’une marque de fin null finale.</span><span class="sxs-lookup"><span data-stu-id="892a0-119">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="892a0-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="892a0-120">*cbMax*</span></span>

<span data-ttu-id="892a0-121">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="892a0-121">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="892a0-122">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="892a0-122">*pcbActual*</span></span>

<span data-ttu-id="892a0-123">Reçoit le volume réel de données de chaîne reçues dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="892a0-123">Receives the actual amount of string data received in the output buffer.</span></span>

<span data-ttu-id="892a0-124">*pLogInfo*</span><span class="sxs-lookup"><span data-stu-id="892a0-124">*pLogInfo*</span></span>

<span data-ttu-id="892a0-125">Reçoit des informations structurées sur les fichiers du journal des transactions qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="892a0-125">Receives structured information on the transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="892a0-126">Lorsque ce paramètre n’est pas présent, sa valeur est supposée être NULL.</span><span class="sxs-lookup"><span data-stu-id="892a0-126">When this parameter is not present, its value is presumed to be NULL.</span></span>

### <a name="return-value"></a><span data-ttu-id="892a0-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="892a0-127">Return Value</span></span>

<span data-ttu-id="892a0-128">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="892a0-128">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="892a0-129">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="892a0-129">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="892a0-130">Code de retour</span><span class="sxs-lookup"><span data-stu-id="892a0-130">Return code</span></span></p></th>
<th><p><span data-ttu-id="892a0-131">Description</span><span class="sxs-lookup"><span data-stu-id="892a0-131">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="892a0-132">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="892a0-132">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="892a0-133">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="892a0-133">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="892a0-134">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="892a0-134">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="892a0-135">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="892a0-135">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="892a0-136">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="892a0-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="892a0-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="892a0-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="892a0-138">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="892a0-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="892a0-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="892a0-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="892a0-140">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="892a0-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="892a0-141">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="892a0-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="892a0-142">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="892a0-142">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="892a0-143">L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</span><span class="sxs-lookup"><span data-stu-id="892a0-143">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="892a0-144"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> retourne cette erreur s’il existe des descripteurs de fichiers en attente créés à l’aide de <a href="gg269249(v=exchg.10).md">JetOpenFile</a> pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="892a0-144"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="892a0-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="892a0-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="892a0-146">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="892a0-146">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="892a0-147">Cela peut se produire pour <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> lorsque le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="892a0-147">This can happen for <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="892a0-148">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="892a0-148">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="892a0-149">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="892a0-149">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="892a0-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="892a0-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="892a0-151">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="892a0-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="892a0-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="892a0-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="892a0-153">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="892a0-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="892a0-154">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="892a0-154">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="892a0-155">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="892a0-155">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="892a0-156">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="892a0-156">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="892a0-157">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="892a0-157">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="892a0-158">En cas de réussite, les informations demandées sur l’ensemble des fichiers de correctifs de base de données et les fichiers journaux des transactions qui doivent faire partie du jeu de fichiers de sauvegarde seront placées dans les tampons de sortie, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="892a0-158">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="892a0-159">L’ordinateur d’état de sauvegarde est avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée.</span><span class="sxs-lookup"><span data-stu-id="892a0-159">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="892a0-160">Seuls les fichiers de correctifs de base de données et les fichiers journaux des transactions sont autorisés à être ouverts pour la sauvegarde au-delà de ce point.</span><span class="sxs-lookup"><span data-stu-id="892a0-160">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="892a0-161">En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="892a0-161">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="892a0-162">L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance.</span><span class="sxs-lookup"><span data-stu-id="892a0-162">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="892a0-163">Notes</span><span class="sxs-lookup"><span data-stu-id="892a0-163">Remarks</span></span>

<span data-ttu-id="892a0-164">Il est important de noter que cette API ne retourne pas d’erreur ou d’avertissement si la mémoire tampon de sortie est trop petite pour accepter la liste complète des fichiers qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="892a0-164">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="892a0-165">L’application doit toujours fournir une mémoire tampon pour recevoir la taille réelle de cette liste et utiliser ces informations pour déterminer si la liste a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="892a0-165">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="892a0-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="892a0-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="892a0-167"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="892a0-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="892a0-168">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="892a0-168">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="892a0-169"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="892a0-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="892a0-170">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="892a0-170">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="892a0-171"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="892a0-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="892a0-172">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="892a0-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="892a0-173"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="892a0-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="892a0-174">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="892a0-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="892a0-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="892a0-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="892a0-176">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="892a0-176">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="892a0-177"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="892a0-177"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="892a0-178">Implémenté en tant que <strong>JetGetLogInfoInstance2W</strong> (Unicode) et <strong>JetGetLogInfoInstance2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="892a0-178">Implemented as <strong>JetGetLogInfoInstance2W</strong> (Unicode) and <strong>JetGetLogInfoInstance2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="892a0-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="892a0-179">See Also</span></span>

[<span data-ttu-id="892a0-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="892a0-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="892a0-181">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="892a0-181">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="892a0-182">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="892a0-182">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="892a0-183">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="892a0-183">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="892a0-184">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="892a0-184">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="892a0-185">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="892a0-185">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="892a0-186">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="892a0-186">JetStopBackup</span></span>](./jetstopbackup-function.md)

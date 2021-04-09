---
description: 'En savoir plus sur : fonction JetGetLogInfo'
title: JetGetLogInfo fonction)
TOCTitle: JetGetLogInfo Function
ms:assetid: a9d14830-d731-4d47-bdc2-c0660a08678e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294055(v=EXCHG.10)
ms:contentKeyID: 32765665
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoA
- JetGetLogInfoW
- JetGetLogInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c96827be0ac62502e7545a9acb1fe157f3b28fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758487"
---
# <a name="jetgetloginfo-function"></a><span data-ttu-id="bb565-103">JetGetLogInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="bb565-103">JetGetLogInfo Function</span></span>


<span data-ttu-id="bb565-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="bb565-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfo-function"></a><span data-ttu-id="bb565-105">JetGetLogInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="bb565-105">JetGetLogInfo Function</span></span>

<span data-ttu-id="bb565-106">La fonction **JetGetLogInfo** est utilisée lors d’une sauvegarde lancée par [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) pour interroger une instance pour obtenir les noms des fichiers de correctifs de base de données et des fichiers journaux des transactions qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="bb565-106">The **JetGetLogInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="bb565-107">Ces fichiers peuvent être ouverts par la suite à l’aide de [JetOpenFile](./jetopenfile-function.md) et lus à l’aide de [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="bb565-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="bb565-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb565-108">Parameters</span></span>

<span data-ttu-id="bb565-109">*szz*</span><span class="sxs-lookup"><span data-stu-id="bb565-109">*szz*</span></span>

<span data-ttu-id="bb565-110">Mémoire tampon de sortie qui recevra la liste des chaînes terminées par un caractère null qui décrivent l’ensemble des fichiers de correctifs de base de données et des fichiers journaux des transactions qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="bb565-110">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="bb565-111">La liste de chaînes retournée dans cette mémoire tampon est dans le même format qu’une chaîne multiple utilisée par le registre.</span><span class="sxs-lookup"><span data-stu-id="bb565-111">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="bb565-112">Chaque chaîne se terminant par une valeur null est retournée dans la séquence suivie d’une marque de fin null finale.</span><span class="sxs-lookup"><span data-stu-id="bb565-112">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="bb565-113">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="bb565-113">*cbMax*</span></span>

<span data-ttu-id="bb565-114">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="bb565-114">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="bb565-115">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="bb565-115">*pcbActual*</span></span>

<span data-ttu-id="bb565-116">Reçoit le volume réel de données de chaîne reçues dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="bb565-116">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="bb565-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb565-117">Return Value</span></span>

<span data-ttu-id="bb565-118">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="bb565-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bb565-119">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bb565-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb565-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bb565-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="bb565-121">Description</span><span class="sxs-lookup"><span data-stu-id="bb565-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb565-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bb565-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bb565-123">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="bb565-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb565-124">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="bb565-124">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="bb565-125">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="bb565-125">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="bb565-126">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bb565-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb565-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bb565-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bb565-128">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="bb565-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb565-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bb565-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bb565-130">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="bb565-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="bb565-131">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bb565-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb565-132">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="bb565-132">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="bb565-133">L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</span><span class="sxs-lookup"><span data-stu-id="bb565-133">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="bb565-134"><strong>JetGetLogInfo</strong> retourne cette erreur s’il existe des descripteurs de fichiers en attente créés à l’aide de <a href="gg269249(v=exchg.10).md">JetOpenFile</a> pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="bb565-134"><strong>JetGetLogInfo</strong> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb565-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="bb565-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="bb565-136">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="bb565-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="bb565-137">Cela peut se produire pour <strong>JetGetLogInfo</strong> lorsque le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="bb565-137">This can happen for <strong>JetGetLogInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb565-138">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="bb565-138">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="bb565-139">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="bb565-139">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb565-140">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bb565-140">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bb565-141">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="bb565-141">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb565-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bb565-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bb565-143">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="bb565-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb565-144">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="bb565-144">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="bb565-145">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="bb565-145">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb565-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bb565-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bb565-147">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="bb565-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bb565-148">En cas de réussite, les informations demandées sur l’ensemble des fichiers de correctifs de base de données et les fichiers journaux des transactions qui doivent faire partie du jeu de fichiers de sauvegarde seront placées dans les tampons de sortie, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="bb565-148">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="bb565-149">L’ordinateur d’état de sauvegarde est avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée.</span><span class="sxs-lookup"><span data-stu-id="bb565-149">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="bb565-150">Seuls les fichiers de correctifs de base de données et les fichiers journaux des transactions sont autorisés à être ouverts pour la sauvegarde au-delà de ce point.</span><span class="sxs-lookup"><span data-stu-id="bb565-150">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="bb565-151">En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="bb565-151">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="bb565-152">L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance.</span><span class="sxs-lookup"><span data-stu-id="bb565-152">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bb565-153">Notes</span><span class="sxs-lookup"><span data-stu-id="bb565-153">Remarks</span></span>

<span data-ttu-id="bb565-154">Il est important de noter que cette API ne retourne pas d’erreur ou d’avertissement si la mémoire tampon de sortie est trop petite pour accepter la liste complète des fichiers qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="bb565-154">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="bb565-155">L’application doit toujours fournir une mémoire tampon pour recevoir la taille réelle de cette liste et utiliser ces informations pour déterminer si la liste a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="bb565-155">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bb565-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb565-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb565-157"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bb565-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bb565-158">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="bb565-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb565-159"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="bb565-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bb565-160">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bb565-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb565-161"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="bb565-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bb565-162">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="bb565-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb565-163"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="bb565-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bb565-164">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bb565-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb565-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bb565-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bb565-166">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bb565-166">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb565-167"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bb565-167"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bb565-168">Implémenté en tant que <strong>JetGetLogInfoW</strong> (Unicode) et <strong>JetGetLogInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bb565-168">Implemented as <strong>JetGetLogInfoW</strong> (Unicode) and <strong>JetGetLogInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bb565-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb565-169">See Also</span></span>

[<span data-ttu-id="bb565-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bb565-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bb565-171">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bb565-171">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="bb565-172">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="bb565-172">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="bb565-173">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="bb565-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="bb565-174">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="bb565-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="bb565-175">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="bb565-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="bb565-176">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="bb565-176">JetStopBackup</span></span>](./jetstopbackup-function.md)

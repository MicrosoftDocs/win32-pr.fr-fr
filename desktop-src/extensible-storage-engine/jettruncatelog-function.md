---
description: 'En savoir plus sur : fonction JetTruncateLog'
title: JetTruncateLog fonction)
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e196a1570f769d8ae2619e962521bb181d506d63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750477"
---
# <a name="jettruncatelog-function"></a><span data-ttu-id="55952-103">JetTruncateLog fonction)</span><span class="sxs-lookup"><span data-stu-id="55952-103">JetTruncateLog Function</span></span>


<span data-ttu-id="55952-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="55952-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncatelog-function"></a><span data-ttu-id="55952-105">JetTruncateLog fonction)</span><span class="sxs-lookup"><span data-stu-id="55952-105">JetTruncateLog Function</span></span>

<span data-ttu-id="55952-106">La fonction **JetTruncateLog** est utilisée lors d’une sauvegarde initiée par [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) pour supprimer tous les fichiers journaux des transactions qui ne seront plus nécessaires une fois la sauvegarde en cours terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="55952-106">The **JetTruncateLog** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a><span data-ttu-id="55952-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55952-107">Parameters</span></span>

<span data-ttu-id="55952-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="55952-108">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="55952-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="55952-109">Return Value</span></span>

<span data-ttu-id="55952-110">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="55952-110">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="55952-111">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="55952-111">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55952-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="55952-112">Return code</span></span></p></th>
<th><p><span data-ttu-id="55952-113">Description</span><span class="sxs-lookup"><span data-stu-id="55952-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55952-114">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="55952-114">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="55952-115">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="55952-115">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55952-116">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="55952-116">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="55952-117">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="55952-117">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="55952-118"><strong>Windows Server 2003 :</strong>  Cette valeur de retour est introduite dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="55952-118"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55952-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="55952-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="55952-120">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="55952-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55952-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="55952-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="55952-122">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="55952-122">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="55952-123"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="55952-123"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55952-124">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="55952-124">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="55952-125">L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</span><span class="sxs-lookup"><span data-stu-id="55952-125">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="55952-126"><strong>JetTruncateLog</strong> retourne cette erreur s’il existe des descripteurs de fichiers en attente qui ont été créés à l’aide de <a href="gg269249(v=exchg.10).md">JetOpenFile</a> pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="55952-126"><strong>JetTruncateLog</strong> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55952-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="55952-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="55952-128">L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs paramètres a généré un résultat inattendu.</span><span class="sxs-lookup"><span data-stu-id="55952-128">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="55952-129">Cela peut se produire pour <strong>JetTruncateLog</strong> lorsque le handle d’instance spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="55952-129">This can happen for <strong>JetTruncateLog</strong> when the specified instance handle is invalid.</span></span></p>
<p><span data-ttu-id="55952-130"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="55952-130"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55952-131">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="55952-131">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="55952-132">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="55952-132">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55952-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="55952-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="55952-134">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="55952-134">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55952-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="55952-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="55952-136">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="55952-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55952-137">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="55952-137">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="55952-138">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge, alors que en fait, plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="55952-138">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55952-139">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="55952-139">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="55952-140">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="55952-140">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55952-141">Si cette fonction réussit, l’ensemble des fichiers journaux des transactions qui ne seront plus nécessaires une fois la sauvegarde actuelle terminée est supprimé.</span><span class="sxs-lookup"><span data-stu-id="55952-141">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="55952-142">L’ordinateur d’état de sauvegarde est avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée.</span><span class="sxs-lookup"><span data-stu-id="55952-142">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="55952-143">Seuls les fichiers de correctifs de base de données et les fichiers journaux des transactions sont autorisés à être ouverts pour la sauvegarde au-delà de ce point.</span><span class="sxs-lookup"><span data-stu-id="55952-143">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="55952-144">Si cette fonction échoue, l’ordinateur d’état de sauvegarde peut être avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée.</span><span class="sxs-lookup"><span data-stu-id="55952-144">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="55952-145">Un certain nombre de fichiers journaux de transactions peuvent être supprimés moins que le nombre souhaité, mais ils seront toujours supprimés du plus ancien au plus récent.</span><span class="sxs-lookup"><span data-stu-id="55952-145">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="55952-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55952-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55952-147"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="55952-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="55952-148">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="55952-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55952-149"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="55952-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="55952-150">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="55952-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55952-151"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="55952-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="55952-152">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="55952-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55952-153"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="55952-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="55952-154">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="55952-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55952-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="55952-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="55952-156">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="55952-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="55952-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55952-157">See Also</span></span>

[<span data-ttu-id="55952-158">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="55952-158">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="55952-159">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="55952-159">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="55952-160">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="55952-160">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="55952-161">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="55952-161">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="55952-162">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="55952-162">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="55952-163">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="55952-163">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="55952-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="55952-164">JetStopService</span></span>](./jetstopservice-function.md)

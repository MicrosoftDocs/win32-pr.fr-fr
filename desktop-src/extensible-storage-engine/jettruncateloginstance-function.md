---
description: 'En savoir plus sur : fonction JetTruncateLogInstance'
title: JetTruncateLogInstance fonction)
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7286b97b80c323eb6bba7b9d28057bf45eec3920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515058"
---
# <a name="jettruncateloginstance-function"></a><span data-ttu-id="32edd-103">JetTruncateLogInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="32edd-103">JetTruncateLogInstance Function</span></span>


<span data-ttu-id="32edd-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="32edd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncateloginstance-function"></a><span data-ttu-id="32edd-105">JetTruncateLogInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="32edd-105">JetTruncateLogInstance Function</span></span>

<span data-ttu-id="32edd-106">La fonction **JetTruncateLogInstance** est utilisée lors d’une sauvegarde lancée par [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) pour supprimer tous les fichiers journaux des transactions qui ne seront plus nécessaires une fois la sauvegarde en cours terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="32edd-106">The **JetTruncateLogInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="32edd-107">**Windows XP :**  **JetTruncateLogInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="32edd-107">**Windows XP:**  **JetTruncateLogInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="32edd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32edd-108">Parameters</span></span>

<span data-ttu-id="32edd-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="32edd-109">*instance*</span></span>

<span data-ttu-id="32edd-110">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="32edd-110">The instance to use for this call.</span></span>

<span data-ttu-id="32edd-111">Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="32edd-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="32edd-112">L’utilisation de cette instance globale est implicitement dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="32edd-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="32edd-113">Pour Windows XP et versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) lorsqu’une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="32edd-113">For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="32edd-114">Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="32edd-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="32edd-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="32edd-115">Return Value</span></span>

<span data-ttu-id="32edd-116">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="32edd-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="32edd-117">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="32edd-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32edd-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="32edd-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="32edd-119">Description</span><span class="sxs-lookup"><span data-stu-id="32edd-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32edd-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="32edd-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="32edd-121">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="32edd-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32edd-122">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="32edd-122">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="32edd-123"><strong>Windows Server 2003 :</strong>  Cette valeur de retour est introduite dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="32edd-123"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="32edd-124">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="32edd-124">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32edd-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="32edd-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="32edd-126">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="32edd-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32edd-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="32edd-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="32edd-128">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="32edd-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="32edd-129">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="32edd-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32edd-130">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="32edd-130">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="32edd-131">L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</span><span class="sxs-lookup"><span data-stu-id="32edd-131">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="32edd-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> retourne cette erreur s’il existe des descripteurs de fichiers en attente qui ont été créés à l’aide de <a href="gg269249(v=exchg.10).md">JetOpenFile</a> pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="32edd-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32edd-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="32edd-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="32edd-134">L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs paramètres a généré un résultat inattendu.</span><span class="sxs-lookup"><span data-stu-id="32edd-134">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="32edd-135">Cela peut se produire pour <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> lorsque le handle d’instance spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="32edd-135">This can happen for <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32edd-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="32edd-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="32edd-137">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="32edd-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32edd-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="32edd-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="32edd-139">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="32edd-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32edd-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="32edd-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="32edd-141">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="32edd-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32edd-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="32edd-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="32edd-143">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="32edd-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32edd-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="32edd-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="32edd-145">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="32edd-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="32edd-146">Si cette fonction réussit, l’ensemble des fichiers journaux des transactions qui ne seront plus nécessaires une fois la sauvegarde actuelle terminée est supprimé.</span><span class="sxs-lookup"><span data-stu-id="32edd-146">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="32edd-147">L’ordinateur d’état de sauvegarde est avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée.</span><span class="sxs-lookup"><span data-stu-id="32edd-147">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="32edd-148">Seuls les fichiers de correctifs de base de données et les fichiers journaux des transactions sont autorisés à être ouverts pour la sauvegarde au-delà de ce point.</span><span class="sxs-lookup"><span data-stu-id="32edd-148">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="32edd-149">Si cette fonction échoue, l’ordinateur d’état de sauvegarde peut être avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée.</span><span class="sxs-lookup"><span data-stu-id="32edd-149">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="32edd-150">Un certain nombre de fichiers journaux de transactions peuvent être supprimés moins que le nombre souhaité, mais ils seront toujours supprimés du plus ancien au plus récent.</span><span class="sxs-lookup"><span data-stu-id="32edd-150">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="32edd-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32edd-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32edd-152"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="32edd-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="32edd-153">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="32edd-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32edd-154"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="32edd-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="32edd-155">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="32edd-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32edd-156"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="32edd-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="32edd-157">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="32edd-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32edd-158"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="32edd-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="32edd-159">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="32edd-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32edd-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="32edd-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="32edd-161">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="32edd-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="32edd-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32edd-162">See Also</span></span>

[<span data-ttu-id="32edd-163">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="32edd-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="32edd-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="32edd-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="32edd-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="32edd-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="32edd-166">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="32edd-166">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="32edd-167">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="32edd-167">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="32edd-168">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="32edd-168">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="32edd-169">JetStopService</span><span class="sxs-lookup"><span data-stu-id="32edd-169">JetStopService</span></span>](./jetstopservice-function.md)

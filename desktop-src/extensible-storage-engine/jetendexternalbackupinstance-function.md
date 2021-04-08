---
description: 'En savoir plus sur : fonction JetEndExternalBackupInstance'
title: JetEndExternalBackupInstance fonction)
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a017a0dbb4fa2f92c3e43a9dd2ff5649b65ee375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034906"
---
# <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="c5545-103">JetEndExternalBackupInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="c5545-103">JetEndExternalBackupInstance Function</span></span>


<span data-ttu-id="c5545-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c5545-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="c5545-105">JetEndExternalBackupInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="c5545-105">JetEndExternalBackupInstance Function</span></span>

<span data-ttu-id="c5545-106">La fonction **JetEndExternalBackupInstance** met fin à une session de sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="c5545-106">The **JetEndExternalBackupInstance** function ends an external backup session.</span></span> <span data-ttu-id="c5545-107">Cette API est la dernière API d’une série d’API qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).</span><span class="sxs-lookup"><span data-stu-id="c5545-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="c5545-108">**Windows XP : JetEndExternalBackupInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5545-108">**Windows XP:  JetEndExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="c5545-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5545-109">Parameters</span></span>

<span data-ttu-id="c5545-110">*instancié*</span><span class="sxs-lookup"><span data-stu-id="c5545-110">*instance*</span></span>

<span data-ttu-id="c5545-111">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="c5545-111">The instance to use for this call.</span></span>

<span data-ttu-id="c5545-112">**Windows 2000 :** Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c5545-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="c5545-113">L’utilisation de cette instance globale est implicitement dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="c5545-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="c5545-114">**Windows XP :** Pour Windows XP et versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) lorsqu’une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c5545-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="c5545-115">Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="c5545-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="c5545-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c5545-116">Return Value</span></span>

<span data-ttu-id="c5545-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="c5545-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c5545-118">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c5545-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5545-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c5545-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="c5545-120">Description</span><span class="sxs-lookup"><span data-stu-id="c5545-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5545-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c5545-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c5545-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c5545-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5545-123">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="c5545-123">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="c5545-124"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5545-124"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="c5545-125">L’appelant a interrompu une sauvegarde au milieu de la séquence de sauvegarde sans signaler l’intention avec <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="c5545-125">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="c5545-126">Cette erreur est le résultat d’un bogue dans le client de sauvegarde de Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c5545-126">This error is the result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="c5545-127">Sur Windows XP, cette erreur est retournée pour un arrêt intentionnel de la séquence de sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="c5545-127">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5545-128">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="c5545-128">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="c5545-129"><strong>Windows Server 2003 :  </strong> Cette valeur de retour est introduite dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c5545-129"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="c5545-130">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="c5545-130">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5545-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c5545-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c5545-132">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c5545-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5545-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c5545-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c5545-134"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5545-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="c5545-135">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="c5545-135">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5545-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="c5545-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="c5545-137">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="c5545-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5545-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c5545-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c5545-139">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="c5545-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5545-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c5545-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c5545-141">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="c5545-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5545-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="c5545-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="c5545-143">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge, alors que en fait, plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="c5545-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5545-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c5545-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c5545-145">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="c5545-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5545-146">Si la fonction réussit, la sauvegarde externe était un succès.</span><span class="sxs-lookup"><span data-stu-id="c5545-146">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="c5545-147">Success indique que tous les fichiers (par exemple, les bases de données et les journaux) qui sont appropriés pour le type de sauvegarde (spécifié dans [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) ont été récupérés à partir du moteur de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="c5545-147">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="c5545-148">Les fichiers sauvegardés peuvent être récupérés avec la récupération matérielle ([JetExternalRestore](./jetexternalrestore-function.md)).</span><span class="sxs-lookup"><span data-stu-id="c5545-148">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="c5545-149">Si cette fonction échoue, la sauvegarde externe se termine généralement.</span><span class="sxs-lookup"><span data-stu-id="c5545-149">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="c5545-150">L’échec signifie que la sauvegarde n’est pas valide en raison d’une erreur de client ou d’utilisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="c5545-150">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="c5545-151">Il est important de vérifier le code de retour de cette API pour vérifier que la séquence de sauvegarde a réussi.</span><span class="sxs-lookup"><span data-stu-id="c5545-151">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c5545-152">Notes</span><span class="sxs-lookup"><span data-stu-id="c5545-152">Remarks</span></span>

<span data-ttu-id="c5545-153">Si le moteur est configuré pour consigner les événements, un événement est consigné pour indiquer la résolution de la sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="c5545-153">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="c5545-154">Si la séquence de sauvegarde n’est pas exécutée dans l’ordre et avec un appel réussi à [JetEndExternalBackup](./jetendexternalbackup-function.md), les sauvegardes incrémentielles suivantes peuvent contenir plus de données que celles prévues par l’application.</span><span class="sxs-lookup"><span data-stu-id="c5545-154">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="c5545-155">Pour plus d’informations sur la séquence de l’API de sauvegarde externe, consultez [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5545-155">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="c5545-156">Avant Windows Vista, si la troncation du journal n’a pas été effectuée, le moteur a considéré que la sauvegarde était une sauvegarde de copie.</span><span class="sxs-lookup"><span data-stu-id="c5545-156">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="c5545-157">Toutefois, la sauvegarde peut être une sauvegarde normale pour laquelle la troncation n’a pas été effectuée (par exemple, s’il y a des bases de données détachées).</span><span class="sxs-lookup"><span data-stu-id="c5545-157">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="c5545-158">L’option JET_bitBackupTruncateDone peut être utilisée pour informer le moteur du moteur et permettre des modifications d’en-tête de base de données appropriées.</span><span class="sxs-lookup"><span data-stu-id="c5545-158">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow proper database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c5545-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5545-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5545-160"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c5545-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c5545-161">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5545-161">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5545-162"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="c5545-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c5545-163">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c5545-163">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5545-164"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="c5545-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c5545-165">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="c5545-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5545-166"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="c5545-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c5545-167">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c5545-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5545-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c5545-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c5545-169">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c5545-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c5545-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5545-170">See Also</span></span>

[<span data-ttu-id="c5545-171">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="c5545-171">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="c5545-172">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="c5545-172">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="c5545-173">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="c5545-173">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="c5545-174">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="c5545-174">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="c5545-175">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="c5545-175">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="c5545-176">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="c5545-176">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="c5545-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c5545-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c5545-178">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="c5545-178">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="c5545-179">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="c5545-179">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="c5545-180">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="c5545-180">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="c5545-181">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c5545-181">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="c5545-182">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="c5545-182">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="c5545-183">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="c5545-183">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="c5545-184">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="c5545-184">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="c5545-185">JetStopService</span><span class="sxs-lookup"><span data-stu-id="c5545-185">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="c5545-186">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="c5545-186">JetTruncateLog</span></span>](./jettruncatelog-function.md)

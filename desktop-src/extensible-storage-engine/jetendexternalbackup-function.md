---
description: 'En savoir plus sur : fonction JetEndExternalBackup'
title: Fonction JetEndExternalBackup
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91f3db40fef483114313bbaa5f01e592d860bde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522840"
---
# <a name="jetendexternalbackup-function"></a><span data-ttu-id="c66ce-103">Fonction JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="c66ce-103">JetEndExternalBackup Function</span></span>


<span data-ttu-id="c66ce-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c66ce-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackup-function"></a><span data-ttu-id="c66ce-105">Fonction JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="c66ce-105">JetEndExternalBackup Function</span></span>

<span data-ttu-id="c66ce-106">La fonction **JetEndExternalBackup** met fin à une session de sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="c66ce-106">The **JetEndExternalBackup** function ends an external backup session.</span></span> <span data-ttu-id="c66ce-107">Cette fonction est le dernier élément d’API d’une série d’éléments d’API qui doivent être appelés pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).</span><span class="sxs-lookup"><span data-stu-id="c66ce-107">This function is the last API element in a series of API elements that must be called to execute a successful online (non-VSS based) backup.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="c66ce-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c66ce-108">Parameters</span></span>

<span data-ttu-id="c66ce-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c66ce-109">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="c66ce-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c66ce-110">Return Value</span></span>

<span data-ttu-id="c66ce-111">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="c66ce-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c66ce-112">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c66ce-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c66ce-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c66ce-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="c66ce-114">Description</span><span class="sxs-lookup"><span data-stu-id="c66ce-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c66ce-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c66ce-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c66ce-116">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c66ce-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c66ce-117">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c66ce-117">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c66ce-118">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="c66ce-118">The operation cannot complete because the instance that is associated with the session has not been yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c66ce-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c66ce-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c66ce-120">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c66ce-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c66ce-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c66ce-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c66ce-122"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP</span><span class="sxs-lookup"><span data-stu-id="c66ce-122"><strong>Windows XP:  </strong>This return value is introduced in Windows XP</span></span></p>
<p><span data-ttu-id="c66ce-123">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui nécessite l’accès à toutes les données pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="c66ce-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c66ce-124">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c66ce-124">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c66ce-125">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="c66ce-125">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c66ce-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c66ce-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c66ce-127">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="c66ce-127">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c66ce-128">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="c66ce-128">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="c66ce-129">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="c66ce-129">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c66ce-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="c66ce-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="c66ce-131"><strong>Windows Server 2003 :  </strong> Cette valeur de retour est introduite dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c66ce-131"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="c66ce-132">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="c66ce-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c66ce-133">errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="c66ce-133">errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="c66ce-134"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c66ce-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="c66ce-135">L’appelant a interrompu une sauvegarde au milieu de la séquence de sauvegarde sans signaler l’intention avec <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="c66ce-135">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="c66ce-136">Cette erreur est le résultat d’un bogue dans le client de sauvegarde de Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c66ce-136">This error is a result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="c66ce-137">Sur Windows XP, cette erreur est retournée pour un arrêt intentionnel de la séquence de sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="c66ce-137">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c66ce-138">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="c66ce-138">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="c66ce-139">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge, alors que en fait, plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="c66ce-139">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c66ce-140">Si cette fonction réussit, la sauvegarde externe était un succès.</span><span class="sxs-lookup"><span data-stu-id="c66ce-140">If this function succeeds, the external backup was a success.</span></span> <span data-ttu-id="c66ce-141">Success indique que tous les fichiers (par exemple, les bases de données et les journaux) qui sont appropriés pour le type de sauvegarde (spécifié dans [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) ont été récupérés à partir du moteur de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="c66ce-141">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="c66ce-142">Les fichiers sauvegardés peuvent être récupérés avec la récupération matérielle ([JetExternalRestore](./jetexternalrestore-function.md)).</span><span class="sxs-lookup"><span data-stu-id="c66ce-142">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="c66ce-143">Si cette fonction échoue, la sauvegarde externe se termine généralement.</span><span class="sxs-lookup"><span data-stu-id="c66ce-143">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="c66ce-144">L’échec signifie que la sauvegarde n’est pas valide en raison d’une erreur de client ou d’utilisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="c66ce-144">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="c66ce-145">Il est important de vérifier le code de retour de cette API pour vérifier que la séquence de sauvegarde a réussi.</span><span class="sxs-lookup"><span data-stu-id="c66ce-145">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c66ce-146">Notes</span><span class="sxs-lookup"><span data-stu-id="c66ce-146">Remarks</span></span>

<span data-ttu-id="c66ce-147">Si le moteur est configuré pour consigner les événements, un événement est consigné pour indiquer la résolution de la sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="c66ce-147">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="c66ce-148">Si la séquence de sauvegarde n’est pas exécutée dans l’ordre et avec un appel réussi à **JetEndExternalBackup**, les sauvegardes incrémentielles suivantes peuvent contenir plus de données que celles prévues par l’application.</span><span class="sxs-lookup"><span data-stu-id="c66ce-148">If the backup sequence is not completed in order and with a successful call to **JetEndExternalBackup**, subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="c66ce-149">Pour plus d’informations sur la séquence de l’API de sauvegarde externe, consultez [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="c66ce-149">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="c66ce-150">Avant Windows Vista, si la troncation du journal n’a pas été effectuée, le moteur a considéré que la sauvegarde était une sauvegarde de copie.</span><span class="sxs-lookup"><span data-stu-id="c66ce-150">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="c66ce-151">Toutefois, la sauvegarde peut être une sauvegarde normale pour laquelle la troncation n’a pas été effectuée (par exemple, s’il y a des bases de données détachées).</span><span class="sxs-lookup"><span data-stu-id="c66ce-151">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="c66ce-152">L’option JET_bitBackupTruncateDone peut être utilisée pour informer le moteur du moteur et autoriser les modifications d’en-tête de base de données appropriées.</span><span class="sxs-lookup"><span data-stu-id="c66ce-152">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c66ce-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c66ce-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c66ce-154"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c66ce-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c66ce-155">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="c66ce-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c66ce-156"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="c66ce-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c66ce-157">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c66ce-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c66ce-158"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="c66ce-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c66ce-159">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="c66ce-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c66ce-160"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="c66ce-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c66ce-161">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c66ce-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c66ce-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c66ce-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c66ce-163">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c66ce-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c66ce-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c66ce-164">See Also</span></span>

[<span data-ttu-id="c66ce-165">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="c66ce-165">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="c66ce-166">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="c66ce-166">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="c66ce-167">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="c66ce-167">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="c66ce-168">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="c66ce-168">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="c66ce-169">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="c66ce-169">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="c66ce-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c66ce-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c66ce-171">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="c66ce-171">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="c66ce-172">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="c66ce-172">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="c66ce-173">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="c66ce-173">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="c66ce-174">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="c66ce-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="c66ce-175">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="c66ce-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="c66ce-176">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="c66ce-176">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="c66ce-177">JetStopService</span><span class="sxs-lookup"><span data-stu-id="c66ce-177">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="c66ce-178">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="c66ce-178">JetTruncateLog</span></span>](./jettruncatelog-function.md)

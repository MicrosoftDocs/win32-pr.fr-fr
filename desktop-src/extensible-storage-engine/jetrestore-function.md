---
description: 'En savoir plus sur : fonction JetRestore'
title: Fonction JetRestore
TOCTitle: JetRestore Function
ms:assetid: cdfb8823-6260-46f2-adfc-77e2512a68fd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294093(v=EXCHG.10)
ms:contentKeyID: 32765708
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore
- JetRestoreW
- JetRestoreA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ed164bb6775150f9745cb0e6d9b158a5f03f146
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103954037"
---
# <a name="jetrestore-function"></a><span data-ttu-id="90441-103">Fonction JetRestore</span><span class="sxs-lookup"><span data-stu-id="90441-103">JetRestore Function</span></span>


<span data-ttu-id="90441-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="90441-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore-function"></a><span data-ttu-id="90441-105">Fonction JetRestore</span><span class="sxs-lookup"><span data-stu-id="90441-105">JetRestore Function</span></span>

<span data-ttu-id="90441-106">La fonction **JetRestore** restaure et récupère une sauvegarde en continu d’une instance, y compris toutes les bases de données attachées.</span><span class="sxs-lookup"><span data-stu-id="90441-106">The **JetRestore** function restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="90441-107">Cette fonction est principalement utilisée à des fins de compatibilité descendante avec Windows 2000 et des moteurs de base de données antérieurs, où une seule instance de base de données est autorisée.</span><span class="sxs-lookup"><span data-stu-id="90441-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="90441-108">Dans ce cas, l’instance active est l’instance qui est restaurée.</span><span class="sxs-lookup"><span data-stu-id="90441-108">In this case, the active instance is the instance that is restored.</span></span> <span data-ttu-id="90441-109">Avec **JetRestore**, l’emplacement des bases de données restaurées ne peut pas être spécifié.</span><span class="sxs-lookup"><span data-stu-id="90441-109">With **JetRestore**, the location for the restored databases cannot be specified.</span></span>

```cpp
JET_ERR JET_API JetRestore(
  __in          JET_PCSTR sz,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="90441-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90441-110">Parameters</span></span>

<span data-ttu-id="90441-111">*SZ*</span><span class="sxs-lookup"><span data-stu-id="90441-111">*sz*</span></span>

<span data-ttu-id="90441-112">Dossier dans lequel se trouve la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="90441-112">The folder where the backup is located.</span></span> <span data-ttu-id="90441-113">La sauvegarde doit avoir été générée à l’aide de la fonction [JetBackup](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="90441-113">The backup should have been generated using the [JetBackup](./jetbackup-function.md) function.</span></span>

<span data-ttu-id="90441-114">*PFN*</span><span class="sxs-lookup"><span data-stu-id="90441-114">*pfn*</span></span>

<span data-ttu-id="90441-115">Pointeur facultatif vers la fonction qui sera appelée en tant qu’informations de notification sur la progression de l’opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="90441-115">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="90441-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="90441-116">Return Value</span></span>

<span data-ttu-id="90441-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="90441-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="90441-118">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="90441-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90441-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="90441-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="90441-120">Description</span><span class="sxs-lookup"><span data-stu-id="90441-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90441-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="90441-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="90441-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="90441-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90441-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="90441-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="90441-124">L’opération a échoué, car le moteur est déjà initialisé pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="90441-124">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90441-125">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="90441-125">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="90441-126">Le jeu de fichiers journaux du jeu de sauvegarde et du chemin d’accès du journal actuel ne correspond pas.</span><span class="sxs-lookup"><span data-stu-id="90441-126">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90441-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="90441-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="90441-128">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="90441-128">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90441-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="90441-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="90441-130">L’opération a échoué, car certains chemins d’accès fournis ne sont pas valides (le chemin de sauvegarde, le chemin d’accès de destination, le journal ou le chemin d’accès du système pour l’instance).</span><span class="sxs-lookup"><span data-stu-id="90441-130">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90441-131">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="90441-131">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="90441-132">L’opération a échoué car le moteur est configuré pour utiliser une taille de page de base de données (à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> pour <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) qui ne correspond pas à la taille de page de la base de données utilisée pour créer les fichiers du journal des transactions ou les bases de données associées aux fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="90441-132">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90441-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="90441-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="90441-134">L’opération a échoué, car les paramètres ont impliqué le mode d’instance unique (mode de compatibilité de Windows 2000) et le moteur est déjà en mode multi-instance.</span><span class="sxs-lookup"><span data-stu-id="90441-134">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="90441-135">En cas de réussite, les fichiers de base de données du jeu de sauvegarde sont restaurés dans leur emplacement et la récupération est exécutée de sorte que les bases de données se trouvent dans un état de cohérence des transactions propre.</span><span class="sxs-lookup"><span data-stu-id="90441-135">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="90441-136">La récupération va relire les fichiers journaux du jeu de sauvegarde et les fichiers journaux du chemin d’accès du journal, si ces fichiers existent.</span><span class="sxs-lookup"><span data-stu-id="90441-136">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="90441-137">Cette récupération entraîne des modifications du fichier de point de contrôle, des fichiers journaux des transactions et des bases de données référencées par ces fichiers journaux de transactions.</span><span class="sxs-lookup"><span data-stu-id="90441-137">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="90441-138">En cas d’échec, l’instance reste dans un État non initialisé.</span><span class="sxs-lookup"><span data-stu-id="90441-138">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="90441-139">L’état des fichiers du journal des transactions et des bases de données référencées par ces fichiers du journal des transactions aura probablement été modifié lors de la tentative d’initialisation de la restauration et de récupération des bases de données.</span><span class="sxs-lookup"><span data-stu-id="90441-139">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="90441-140">Notes</span><span class="sxs-lookup"><span data-stu-id="90441-140">Remarks</span></span>

<span data-ttu-id="90441-141">Le processus de récupération reconstruira les bases de données attachées à l’instance au cours de la sauvegarde et enregistrera les modifications dans les fichiers de la base de données.</span><span class="sxs-lookup"><span data-stu-id="90441-141">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="90441-142">Le résultat sera celui des bases de données qui sont cohérentes avec les transactions.</span><span class="sxs-lookup"><span data-stu-id="90441-142">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="90441-143">Si possible, il enregistrera également dans la base de données les modifications apportées depuis la sauvegarde jusqu’à la dernière modification trouvée dans les journaux des transactions.</span><span class="sxs-lookup"><span data-stu-id="90441-143">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="90441-144">Cela est possible si les journaux des transactions générés depuis la sauvegarde sont toujours présents dans le répertoire du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="90441-144">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="90441-145">Notez que si la journalisation circulaire a été activée pour l’instance, les journaux de transactions générés sont réutilisés afin que la récupération puisse enregistrer les modifications apportées jusqu’à l’heure de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="90441-145">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="90441-146">Dans tous les cas, il est possible que ce processus prenne un certain temps si le nombre de fichiers du journal des transactions à relire sur les bases de données est important.</span><span class="sxs-lookup"><span data-stu-id="90441-146">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="90441-147">Les fonctions **JetRestore** doivent être appelées sur une instance avant que [JetInit](./jetinit-function.md) soit appelé pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="90441-147">**JetRestore** functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="90441-148">Étant donné que, lors de la récupération, un nombre important de pages de base de données et de journaux de transactions sera utilisé, il existe une série complète d’erreurs qui peuvent être renvoyées par ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="90441-148">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="90441-149">Ces erreurs peuvent provenir d’échecs d’allocation de ressources, comme Jet_errOutOfMemory aux erreurs qui représentent des altérations physiques comme JET_errReadVerifyFailure, JET_errLogFileCorrupt ou JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="90441-149">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="90441-150">Ces erreurs sont presque toujours dues à des problèmes matériels et ne peuvent donc pas être évitées.</span><span class="sxs-lookup"><span data-stu-id="90441-150">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="90441-151">La gestion des fichiers se manifeste le plus souvent en tant que JET_errMissingLogFile ou JET_errAttachedDatabaseMismatch ou JET_errDatabaseSharingViolation ou JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="90441-151">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="90441-152">Ces erreurs sont empêchables par l’application.</span><span class="sxs-lookup"><span data-stu-id="90441-152">These errors are preventable by the application.</span></span> <span data-ttu-id="90441-153">L’application doit veiller à protéger le référentiel de ces fichiers contre les manipulations en dehors des forces, telles que l’utilisateur ou d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="90441-153">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="90441-154">Si l’application souhaite détruire entièrement une instance, tous les fichiers associés à l’instance doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="90441-154">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="90441-155">Celles-ci incluent le fichier de point de contrôle, les fichiers journaux des transactions et les fichiers de base de données attachés à l’instance.</span><span class="sxs-lookup"><span data-stu-id="90441-155">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="90441-156">Les différentes étapes de la récupération auront des entrées de journal des événements générées, notamment la progression de la relecture du journal des transactions et le résultat final de la restauration.</span><span class="sxs-lookup"><span data-stu-id="90441-156">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="90441-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90441-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90441-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="90441-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="90441-159">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="90441-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90441-160"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="90441-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="90441-161">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="90441-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90441-162"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="90441-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="90441-163">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="90441-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90441-164"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="90441-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="90441-165">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="90441-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90441-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="90441-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="90441-167">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="90441-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90441-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="90441-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="90441-169">Implémenté en tant que <strong>JetRestoreW</strong> (Unicode) et <strong>JetRestoreA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="90441-169">Implemented as <strong>JetRestoreW</strong> (Unicode) and <strong>JetRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="90441-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90441-170">See Also</span></span>

[<span data-ttu-id="90441-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="90441-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="90441-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="90441-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="90441-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="90441-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="90441-174">JetBackup</span><span class="sxs-lookup"><span data-stu-id="90441-174">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="90441-175">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="90441-175">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="90441-176">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="90441-176">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="90441-177">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="90441-177">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)

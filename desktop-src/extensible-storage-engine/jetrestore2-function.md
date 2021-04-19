---
description: 'En savoir plus sur : fonction JetRestore2'
title: Fonction JetRestore2
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb297aac0bc26e50bba519206eff346abb7943c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541992"
---
# <a name="jetrestore2-function"></a><span data-ttu-id="42274-103">Fonction JetRestore2</span><span class="sxs-lookup"><span data-stu-id="42274-103">JetRestore2 Function</span></span>


<span data-ttu-id="42274-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="42274-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore2-function"></a><span data-ttu-id="42274-105">Fonction JetRestore2</span><span class="sxs-lookup"><span data-stu-id="42274-105">JetRestore2 Function</span></span>

<span data-ttu-id="42274-106">**JetRestore2** restaure et récupère une sauvegarde en continu d’une instance, y compris toutes les bases de données attachées.</span><span class="sxs-lookup"><span data-stu-id="42274-106">The **JetRestore2** restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="42274-107">Cette fonction est principalement utilisée à des fins de compatibilité descendante avec Windows 2000 et des moteurs de base de données antérieurs, où une seule instance de base de données est autorisée.</span><span class="sxs-lookup"><span data-stu-id="42274-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="42274-108">Dans ce cas, l’instance active est l’instance qui est restaurée.</span><span class="sxs-lookup"><span data-stu-id="42274-108">In this case, the active instance is the instance that is restored.</span></span>

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="42274-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42274-109">Parameters</span></span>

<span data-ttu-id="42274-110">*SZ*</span><span class="sxs-lookup"><span data-stu-id="42274-110">*sz*</span></span>

<span data-ttu-id="42274-111">Dossier dans lequel se trouve la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="42274-111">The folder where the backup is located.</span></span> <span data-ttu-id="42274-112">La sauvegarde doit avoir été générée à l’aide des API [JetBackup](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="42274-112">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="42274-113">*szDest*</span><span class="sxs-lookup"><span data-stu-id="42274-113">*szDest*</span></span>

<span data-ttu-id="42274-114">Nom du dossier dans lequel les fichiers de base de données du jeu de sauvegarde seront copiés et récupérés.</span><span class="sxs-lookup"><span data-stu-id="42274-114">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="42274-115">Si la valeur est NULL (ce qui est le cas pour le [JetRestore](./jetrestore-function.md)hérité), les fichiers de base de données sont copiés et récupérés à leur emplacement d’origine.</span><span class="sxs-lookup"><span data-stu-id="42274-115">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="42274-116">*PFN*</span><span class="sxs-lookup"><span data-stu-id="42274-116">*pfn*</span></span>

<span data-ttu-id="42274-117">Pointeur facultatif vers la fonction qui sera appelée en tant qu’informations de notification sur la progression de l’opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="42274-117">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="42274-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="42274-118">Return Value</span></span>

<span data-ttu-id="42274-119">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="42274-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="42274-120">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="42274-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42274-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="42274-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="42274-122">Description</span><span class="sxs-lookup"><span data-stu-id="42274-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42274-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="42274-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="42274-124">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="42274-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42274-125">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="42274-125">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="42274-126">L’opération a échoué, car le moteur est déjà initialisé pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="42274-126">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42274-127">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="42274-127">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="42274-128">Le jeu de fichiers journaux du jeu de sauvegarde et du chemin d’accès du journal actuel ne correspond pas.</span><span class="sxs-lookup"><span data-stu-id="42274-128">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42274-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="42274-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="42274-130">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="42274-130">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="42274-131">Cette erreur est retournée par <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> lorsque le moteur est en mode multi-instance et pinstance fait référence à une instance non valide de Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="42274-131">This error will be returned by <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42274-132">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="42274-132">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="42274-133">L’opération a échoué, car certains chemins d’accès fournis ne sont pas valides (le chemin de sauvegarde, le chemin d’accès de destination, le journal ou le chemin d’accès du système pour l’instance).</span><span class="sxs-lookup"><span data-stu-id="42274-133">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42274-134">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="42274-134">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="42274-135">L’opération a échoué car le moteur est configuré pour utiliser une taille de page de base de données (à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> pour <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) qui ne correspond pas à la taille de page de la base de données utilisée pour créer les fichiers du journal des transactions ou les bases de données associées aux fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="42274-135">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42274-136">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="42274-136">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="42274-137">L’opération a échoué, car les paramètres ont impliqué le mode d’instance unique (mode de compatibilité de Windows 2000) et le moteur est déjà en mode multi-instance.</span><span class="sxs-lookup"><span data-stu-id="42274-137">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42274-138">En cas de réussite, les fichiers de base de données du jeu de sauvegarde sont restaurés dans leur emplacement et la récupération est exécutée de sorte que les bases de données se trouvent dans un état de cohérence des transactions propre.</span><span class="sxs-lookup"><span data-stu-id="42274-138">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="42274-139">La récupération va relire les fichiers journaux du jeu de sauvegarde et les fichiers journaux du chemin d’accès du journal, si ces fichiers existent.</span><span class="sxs-lookup"><span data-stu-id="42274-139">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="42274-140">Cette récupération entraîne des modifications du fichier de point de contrôle, des fichiers journaux des transactions et des bases de données référencées par ces fichiers journaux de transactions.</span><span class="sxs-lookup"><span data-stu-id="42274-140">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="42274-141">En cas d’échec, l’instance reste dans un État non initialisé.</span><span class="sxs-lookup"><span data-stu-id="42274-141">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="42274-142">L’état des fichiers du journal des transactions et des bases de données référencées par ces fichiers du journal des transactions aura probablement été modifié lors de la tentative d’initialisation de la restauration et de récupération des bases de données.</span><span class="sxs-lookup"><span data-stu-id="42274-142">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="42274-143">Notes</span><span class="sxs-lookup"><span data-stu-id="42274-143">Remarks</span></span>

<span data-ttu-id="42274-144">Le processus de récupération reconstruira les bases de données attachées à l’instance au cours de la sauvegarde et enregistrera les modifications dans les fichiers de la base de données.</span><span class="sxs-lookup"><span data-stu-id="42274-144">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="42274-145">Le résultat sera celui des bases de données qui sont cohérentes avec les transactions.</span><span class="sxs-lookup"><span data-stu-id="42274-145">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="42274-146">Si possible, il enregistrera également dans la base de données les modifications apportées depuis la sauvegarde jusqu’à la dernière modification trouvée dans les journaux des transactions.</span><span class="sxs-lookup"><span data-stu-id="42274-146">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="42274-147">Cela est possible si les journaux des transactions générés depuis la sauvegarde sont toujours présents dans le répertoire du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="42274-147">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="42274-148">Notez que si la journalisation circulaire a été activée pour l’instance, les journaux de transactions générés sont réutilisés afin que la récupération puisse enregistrer les modifications apportées jusqu’à l’heure de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="42274-148">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="42274-149">Dans tous les cas, il est possible que ce processus prenne un certain temps si le nombre de fichiers du journal des transactions à relire sur les bases de données est important.</span><span class="sxs-lookup"><span data-stu-id="42274-149">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="42274-150">Les fonctions [JetRestore](./jetrestore-function.md) doivent être appelées sur une instance avant que [JetInit](./jetinit-function.md) soit appelé pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="42274-150">[JetRestore](./jetrestore-function.md) functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="42274-151">Étant donné que, lors de la récupération, un nombre important de pages de base de données et de journaux de transactions sera utilisé, il existe une série complète d’erreurs qui peuvent être renvoyées par ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="42274-151">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="42274-152">Ces erreurs peuvent provenir d’échecs d’allocation de ressources, comme Jet_errOutOfMemory aux erreurs qui représentent des altérations physiques comme JET_errReadVerifyFailure, JET_errLogFileCorrupt ou JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="42274-152">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="42274-153">Ces erreurs sont presque toujours dues à des problèmes matériels et ne peuvent donc pas être évitées.</span><span class="sxs-lookup"><span data-stu-id="42274-153">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="42274-154">La gestion des fichiers se manifeste le plus souvent en tant que JET_errMissingLogFile ou JET_errAttachedDatabaseMismatch ou JET_errDatabaseSharingViolation ou JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="42274-154">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="42274-155">Ces erreurs sont empêchables par l’application.</span><span class="sxs-lookup"><span data-stu-id="42274-155">These errors are preventable by the application.</span></span> <span data-ttu-id="42274-156">L’application doit veiller à protéger le référentiel de ces fichiers contre les manipulations en dehors des forces, telles que l’utilisateur ou d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="42274-156">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="42274-157">Si l’application souhaite détruire entièrement une instance, tous les fichiers associés à l’instance doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="42274-157">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="42274-158">Celles-ci incluent le fichier de point de contrôle, les fichiers journaux des transactions et les fichiers de base de données attachés à l’instance.</span><span class="sxs-lookup"><span data-stu-id="42274-158">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="42274-159">Les différentes étapes de la récupération auront des entrées de journal des événements générées, notamment la progression de la relecture du journal des transactions et le résultat final de la restauration.</span><span class="sxs-lookup"><span data-stu-id="42274-159">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="42274-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42274-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42274-161"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="42274-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="42274-162">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="42274-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42274-163"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="42274-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="42274-164">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="42274-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42274-165"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="42274-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="42274-166">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="42274-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42274-167"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="42274-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="42274-168">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="42274-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42274-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="42274-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="42274-170">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="42274-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42274-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="42274-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="42274-172">Implémenté en tant que <strong>JetRestore2W</strong> (Unicode) et <strong>JetRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="42274-172">Implemented as <strong>JetRestore2W</strong> (Unicode) and <strong>JetRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="42274-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42274-173">See Also</span></span>

[<span data-ttu-id="42274-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="42274-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="42274-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="42274-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="42274-176">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="42274-176">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="42274-177">JetBackup</span><span class="sxs-lookup"><span data-stu-id="42274-177">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="42274-178">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="42274-178">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="42274-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="42274-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="42274-180">JetInit</span><span class="sxs-lookup"><span data-stu-id="42274-180">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="42274-181">JetRestore</span><span class="sxs-lookup"><span data-stu-id="42274-181">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="42274-182">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="42274-182">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="42274-183">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="42274-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)

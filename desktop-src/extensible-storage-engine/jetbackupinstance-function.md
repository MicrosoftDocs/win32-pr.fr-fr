---
description: 'En savoir plus sur : fonction JetBackupInstance'
title: Fonction JetBackupInstance
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112059"
---
# <a name="jetbackupinstance-function"></a><span data-ttu-id="fd34d-103">Fonction JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="fd34d-103">JetBackupInstance Function</span></span>


<span data-ttu-id="fd34d-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="fd34d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackupinstance-function"></a><span data-ttu-id="fd34d-105">Fonction JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="fd34d-105">JetBackupInstance Function</span></span>

<span data-ttu-id="fd34d-106">La fonction **JetBackupInstance** effectue une sauvegarde en continu d’une instance, y compris toutes les bases de données attachées, vers un répertoire.</span><span class="sxs-lookup"><span data-stu-id="fd34d-106">The **JetBackupInstance** function performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="fd34d-107">Avec plusieurs méthodes de sauvegarde prises en charge par le moteur, il s’agit de la fonction la plus simple et la plus encapsulée.</span><span class="sxs-lookup"><span data-stu-id="fd34d-107">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="fd34d-108">**Windows XP : JetBackupInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd34d-108">**Windows XP:  JetBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="fd34d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd34d-109">Parameters</span></span>

<span data-ttu-id="fd34d-110">*instancié*</span><span class="sxs-lookup"><span data-stu-id="fd34d-110">*instance*</span></span>

<span data-ttu-id="fd34d-111">Instance de la base de données à sauvegarder.</span><span class="sxs-lookup"><span data-stu-id="fd34d-111">The instance of the database to backup.</span></span>

<span data-ttu-id="fd34d-112">*szBackupPath*</span><span class="sxs-lookup"><span data-stu-id="fd34d-112">*szBackupPath*</span></span>

<span data-ttu-id="fd34d-113">Répertoire dans lequel la sauvegarde est stockée.</span><span class="sxs-lookup"><span data-stu-id="fd34d-113">The directory where the backup is stored.</span></span> <span data-ttu-id="fd34d-114">Si le chemin d’accès de sauvegarde a la valeur NULL pour utiliser, la fonction tronque les journaux, si possible.</span><span class="sxs-lookup"><span data-stu-id="fd34d-114">If the backup path is NULL to use the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="fd34d-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="fd34d-115">*grbit*</span></span>

<span data-ttu-id="fd34d-116">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="fd34d-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd34d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd34d-117">Value</span></span></p></th>
<th><p><span data-ttu-id="fd34d-118">Signification</span><span class="sxs-lookup"><span data-stu-id="fd34d-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="fd34d-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="fd34d-120">Crée une sauvegarde complète de la base de données.</span><span class="sxs-lookup"><span data-stu-id="fd34d-120">Creates a full backup of the database.</span></span> <span data-ttu-id="fd34d-121">Cela permet la conservation d’une sauvegarde existante dans le même répertoire en cas d’échec de la nouvelle sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="fd34d-121">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="fd34d-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="fd34d-123">Crée une sauvegarde incrémentielle par opposition à une sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="fd34d-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="fd34d-124">Cela signifie que seuls les fichiers journaux créés depuis la dernière sauvegarde complète ou incrémentielle sont sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="fd34d-124">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="fd34d-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="fd34d-126">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="fd34d-126">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fd34d-127">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="fd34d-127">*pfnStatus*</span></span>

<span data-ttu-id="fd34d-128">Pointeur vers la fonction de rappel [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , qui fournit des informations de notification sur la progression de l’opération de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="fd34d-128">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="fd34d-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fd34d-129">Return Value</span></span>

<span data-ttu-id="fd34d-130">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="fd34d-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fd34d-131">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fd34d-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd34d-132">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fd34d-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="fd34d-133">Description</span><span class="sxs-lookup"><span data-stu-id="fd34d-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fd34d-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fd34d-135">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="fd34d-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-136">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="fd34d-136">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="fd34d-137">Une sauvegarde est déjà en cours pour la même instance.</span><span class="sxs-lookup"><span data-stu-id="fd34d-137">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="fd34d-138">Plusieurs sauvegardes ne sont pas autorisées en même temps.</span><span class="sxs-lookup"><span data-stu-id="fd34d-138">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-139">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="fd34d-139">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="fd34d-140">L’instance n’est pas encore prête pour la sauvegarde lors de son initialisation.</span><span class="sxs-lookup"><span data-stu-id="fd34d-140">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fd34d-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fd34d-142">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="fd34d-142">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fd34d-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fd34d-144">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="fd34d-144">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="fd34d-145"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd34d-145"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-146">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="fd34d-146">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="fd34d-147">Une sauvegarde incrémentielle n’est pas autorisée si l’enregistrement circulaire est activé.</span><span class="sxs-lookup"><span data-stu-id="fd34d-147">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-148">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="fd34d-148">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="fd34d-149">Les options spécifiées ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="fd34d-149">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="fd34d-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="fd34d-151">Un paramètre non valide a été passé dans l’API.</span><span class="sxs-lookup"><span data-stu-id="fd34d-151">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="fd34d-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="fd34d-153">Le chemin d’accès de destination n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="fd34d-153">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-154">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="fd34d-154">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="fd34d-155">L’instance est en cours d’exécution sans journalisation.</span><span class="sxs-lookup"><span data-stu-id="fd34d-155">The instance is running without logging.</span></span> <span data-ttu-id="fd34d-156">Aucune sauvegarde n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="fd34d-156">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-157">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="fd34d-157">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="fd34d-158">Une erreur de vérification de la somme de contrôle s’est produite sur un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="fd34d-158">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-159">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="fd34d-159">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="fd34d-160">La journalisation de l’instance est désactivée de façon temporaire ou définitive en raison d’une erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="fd34d-160">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-161">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fd34d-161">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fd34d-162">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="fd34d-162">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-163">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="fd34d-163">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="fd34d-164">Une erreur de vérification de la somme de contrôle s’est produite sur une page de base de données.</span><span class="sxs-lookup"><span data-stu-id="fd34d-164">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fd34d-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fd34d-166">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="fd34d-166">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="fd34d-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="fd34d-168">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="fd34d-168">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="fd34d-169"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd34d-169"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fd34d-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fd34d-171">L’opération ne peut pas se terminer car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="fd34d-171">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fd34d-172">Une fois que la fonction a retourné une réussite, dans le répertoire de sauvegarde, tous les fichiers nécessaires à une restauration jusqu’au moment de la sauvegarde sont présents.</span><span class="sxs-lookup"><span data-stu-id="fd34d-172">After the function returns success, in the backup directory all the files needed for a restore up to the moment of the backup will be present.</span></span> <span data-ttu-id="fd34d-173">S’il s’agit d’une sauvegarde complète, les fichiers sont les fichiers de base de données et les fichiers journaux nécessaires pour ramener la base de données à un état cohérent.</span><span class="sxs-lookup"><span data-stu-id="fd34d-173">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="fd34d-174">S’il s’agit d’une sauvegarde incrémentielle, seuls les fichiers journaux sont ajoutés aux répertoires, mais les fichiers déjà existants (bases de données et fichiers journaux) ainsi que les nouveaux fichiers journaux peuvent être restaurés et ramener la base de données à l’État au moment de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="fd34d-174">If this is an incremental backup, only log files will be added to the directories but the already existing files (databases and log files) together with the new log files will be able to be restored and bring the database back to the state at the moment of the backup.</span></span>

<span data-ttu-id="fd34d-175">En tant qu’effet secondaire de la sauvegarde, les fichiers journaux qui ne sont plus nécessaires sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="fd34d-175">As a side effect of the backup, the log files which are not longer needed will be truncated.</span></span>

<span data-ttu-id="fd34d-176">En même temps, les en-têtes de base de données sont mis à jour avec les informations lors de la dernière sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="fd34d-176">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="fd34d-177">En cas d’échec, aucun fichier n’est présent dans la destination du répertoire de sauvegarde, ce qui signifie qu’aucune restauration n’est possible.</span><span class="sxs-lookup"><span data-stu-id="fd34d-177">On failure, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="fd34d-178">En même temps, les fichiers journaux actuels ne seront pas tronqués.</span><span class="sxs-lookup"><span data-stu-id="fd34d-178">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fd34d-179">Notes</span><span class="sxs-lookup"><span data-stu-id="fd34d-179">Remarks</span></span>

<span data-ttu-id="fd34d-180">Les différentes étapes de la sauvegarde auront des entrées de journal des événements générées, y compris les noms de fichiers, la troncation du journal et le résultat final de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="fd34d-180">The different steps of the backup will have Event Log entries generated including the file names, the log truncation and the final result of the backup.</span></span>

<span data-ttu-id="fd34d-181">La sauvegarde incrémentielle n’est possible qu’après avoir effectué une sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="fd34d-181">Incremental backup are possible only after a full backup was taken.</span></span> <span data-ttu-id="fd34d-182">En outre, les sauvegardes incrémentielles sont possibles uniquement si la journalisation circulaire est désactivée.</span><span class="sxs-lookup"><span data-stu-id="fd34d-182">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="fd34d-183">Il est recommandé de ne pas inclure d’autres fichiers dans le répertoire de sauvegarde, celui impliqué dans la sauvegarde ou ajouté par une sauvegarde précédente réussie.</span><span class="sxs-lookup"><span data-stu-id="fd34d-183">It is recommended that the backup directory should not contain other files then the one involved in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="fd34d-184">Le répertoire de sauvegarde doit exister, sauf si le paramètre *JET_paramCreatePathIfNotExist* est défini pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="fd34d-184">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="fd34d-185">Pour plus d’informations, consultez [paramètres système](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fd34d-185">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="fd34d-186">La sauvegarde effectue une vérification de la somme de contrôle sur toutes les pages de base de données utilisées et à partir de Windows Server 2003, également sur les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="fd34d-186">The backup will do checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="fd34d-187">Cela donne la possibilité d’estimer l’intégrité de la base de données même pour les pages qui ne sont pas lues pendant des opérations normales.</span><span class="sxs-lookup"><span data-stu-id="fd34d-187">This gives an opportunity to estimate the health of the database even for pages which are not read during normal operations.</span></span> <span data-ttu-id="fd34d-188">Si une telle altération est détectée, la sauvegarde échoue.</span><span class="sxs-lookup"><span data-stu-id="fd34d-188">If any such corruption will be encountered, the backup will fail.</span></span>

<span data-ttu-id="fd34d-189">Au cours de la sauvegarde, le fichier journal actuel est terminé et une nouvelle génération de journal est lancée.</span><span class="sxs-lookup"><span data-stu-id="fd34d-189">During the backup, the current log file will be finished and we will start a new log generation.</span></span> <span data-ttu-id="fd34d-190">Cela permet de copier les fichiers journaux nécessaires, car le dernier fichier nécessaire n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="fd34d-190">This will allow copying the needed log files because the last needed one will not be in use anymore.</span></span>

<span data-ttu-id="fd34d-191">Il est vivement recommandé de ne pas utiliser la sauvegarde pour d’autres fonctions, puis la sauvegarde et la restauration au niveau du moteur.</span><span class="sxs-lookup"><span data-stu-id="fd34d-191">It is strongly recommended that the backup should not be used for other purposed other then the backup and restored at the engine level.</span></span> <span data-ttu-id="fd34d-192">Cela réduira la modification de l’obtention des erreurs pendant les opérations de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="fd34d-192">This will minimize the change of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fd34d-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd34d-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-194"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fd34d-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fd34d-195">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd34d-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-196"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="fd34d-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fd34d-197">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fd34d-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-198"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="fd34d-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fd34d-199">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="fd34d-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-200"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="fd34d-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fd34d-201">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fd34d-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd34d-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fd34d-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fd34d-203">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fd34d-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd34d-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="fd34d-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fd34d-205">Implémenté en tant que <strong>JetBackupInstanceW</strong> (Unicode) et <strong>JetBackupInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fd34d-205">Implemented as <strong>JetBackupInstanceW</strong> (Unicode) and <strong>JetBackupInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fd34d-206">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd34d-206">See Also</span></span>

[<span data-ttu-id="fd34d-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fd34d-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fd34d-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fd34d-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fd34d-209">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="fd34d-209">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="fd34d-210">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="fd34d-210">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="fd34d-211">JetRestore</span><span class="sxs-lookup"><span data-stu-id="fd34d-211">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="fd34d-212">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="fd34d-212">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="fd34d-213">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="fd34d-213">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="fd34d-214">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="fd34d-214">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)  
[<span data-ttu-id="fd34d-215">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="fd34d-215">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

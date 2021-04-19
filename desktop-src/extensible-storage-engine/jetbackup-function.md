---
description: 'En savoir plus sur : fonction JetBackup'
title: Fonction JetBackup
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531192"
---
# <a name="jetbackup-function"></a><span data-ttu-id="ddad9-103">Fonction JetBackup</span><span class="sxs-lookup"><span data-stu-id="ddad9-103">JetBackup Function</span></span>


<span data-ttu-id="ddad9-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="ddad9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackup-function"></a><span data-ttu-id="ddad9-105">Fonction JetBackup</span><span class="sxs-lookup"><span data-stu-id="ddad9-105">JetBackup Function</span></span>

<span data-ttu-id="ddad9-106">La fonction **JetBackup** crée une sauvegarde de la base de données pendant que la base de données est en ligne.</span><span class="sxs-lookup"><span data-stu-id="ddad9-106">The **JetBackup** function creates a backup of the database while the database is online.</span></span> <span data-ttu-id="ddad9-107">Cette fonction est principalement utilisée à des fins de compatibilité descendante avec Windows 2000 et des moteurs de base de données antérieurs, où une seule instance de base de données est autorisée.</span><span class="sxs-lookup"><span data-stu-id="ddad9-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="ddad9-108">Dans ce cas, l’instance active est l’instance qui est sauvegardée.</span><span class="sxs-lookup"><span data-stu-id="ddad9-108">In this case, the active instance is the instance that is backed up.</span></span>

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="ddad9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddad9-109">Parameters</span></span>

<span data-ttu-id="ddad9-110">*szBackupPath*</span><span class="sxs-lookup"><span data-stu-id="ddad9-110">*szBackupPath*</span></span>

<span data-ttu-id="ddad9-111">Répertoire dans lequel la sauvegarde est stockée.</span><span class="sxs-lookup"><span data-stu-id="ddad9-111">The directory where the backup is stored.</span></span> <span data-ttu-id="ddad9-112">Si le chemin d’accès de sauvegarde est NULL, la fonction tronque les journaux, si possible.</span><span class="sxs-lookup"><span data-stu-id="ddad9-112">If the backup path is NULL, the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="ddad9-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ddad9-113">*grbit*</span></span>

<span data-ttu-id="ddad9-114">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="ddad9-114">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ddad9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddad9-115">Value</span></span></p></th>
<th><p><span data-ttu-id="ddad9-116">Signification</span><span class="sxs-lookup"><span data-stu-id="ddad9-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-117">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="ddad9-117">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="ddad9-118">Crée une sauvegarde complète de la base de données.</span><span class="sxs-lookup"><span data-stu-id="ddad9-118">Creates a full backup of the database.</span></span> <span data-ttu-id="ddad9-119">Cela permet la conservation d’une sauvegarde existante dans le même répertoire en cas d’échec de la nouvelle sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="ddad9-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-120">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="ddad9-120">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="ddad9-121">Crée une sauvegarde incrémentielle par opposition à une sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="ddad9-121">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="ddad9-122">Cela signifie que seuls les fichiers journaux depuis la dernière sauvegarde complète ou incrémentielle sont sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="ddad9-122">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ddad9-123">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="ddad9-123">*pfnStatus*</span></span>

<span data-ttu-id="ddad9-124">Pointeur vers la fonction de rappel [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , qui fournit des informations de notification sur la progression de l’opération de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="ddad9-124">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="ddad9-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ddad9-125">Return Value</span></span>

<span data-ttu-id="ddad9-126">La fonction retourne l’un des codes d’erreur [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="ddad9-126">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="ddad9-127">Les éléments suivants sont les plus couramment renvoyés.</span><span class="sxs-lookup"><span data-stu-id="ddad9-127">The following are the most commonly returned.</span></span> <span data-ttu-id="ddad9-128">(Pour obtenir la liste complète des erreurs pour cette API, consultez [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md).)</span><span class="sxs-lookup"><span data-stu-id="ddad9-128">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ddad9-129">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ddad9-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="ddad9-130">Description</span><span class="sxs-lookup"><span data-stu-id="ddad9-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ddad9-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ddad9-132">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ddad9-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-133">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="ddad9-133">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="ddad9-134">Une sauvegarde est déjà en cours pour la même instance.</span><span class="sxs-lookup"><span data-stu-id="ddad9-134">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="ddad9-135">Plusieurs sauvegardes ne sont pas autorisées en même temps.</span><span class="sxs-lookup"><span data-stu-id="ddad9-135">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-136">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="ddad9-136">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="ddad9-137">L’instance n’est pas encore prête pour la sauvegarde lors de son initialisation.</span><span class="sxs-lookup"><span data-stu-id="ddad9-137">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-138">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ddad9-138">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ddad9-139">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="ddad9-139">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ddad9-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ddad9-141">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="ddad9-141">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="ddad9-142"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ddad9-142"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-143">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="ddad9-143">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="ddad9-144">Une sauvegarde incrémentielle n’est pas autorisée si l’enregistrement circulaire est activé.</span><span class="sxs-lookup"><span data-stu-id="ddad9-144">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-145">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="ddad9-145">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="ddad9-146">Les options spécifiées ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="ddad9-146">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-147">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ddad9-147">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ddad9-148">Un paramètre non valide a été passé dans l’API.</span><span class="sxs-lookup"><span data-stu-id="ddad9-148">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-149">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="ddad9-149">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="ddad9-150">Le chemin d’accès de destination n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="ddad9-150">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-151">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="ddad9-151">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="ddad9-152">L’instance est en cours d’exécution sans journalisation.</span><span class="sxs-lookup"><span data-stu-id="ddad9-152">The instance is running without logging.</span></span> <span data-ttu-id="ddad9-153">Aucune sauvegarde n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="ddad9-153">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-154">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="ddad9-154">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="ddad9-155">Une erreur de vérification de la somme de contrôle s’est produite sur un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="ddad9-155">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-156">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="ddad9-156">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="ddad9-157">La journalisation de l’instance est désactivée de façon temporaire ou définitive en raison d’une erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="ddad9-157">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ddad9-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ddad9-159">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="ddad9-159">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-160">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="ddad9-160">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="ddad9-161">Une erreur de vérification de la somme de contrôle s’est produite sur une page de base de données.</span><span class="sxs-lookup"><span data-stu-id="ddad9-161">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ddad9-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ddad9-163">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="ddad9-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="ddad9-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="ddad9-165">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="ddad9-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="ddad9-166"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ddad9-166"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ddad9-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ddad9-168">L’opération ne peut pas se terminer car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ddad9-168">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ddad9-169">Si la fonction s’exécute correctement, tous les fichiers nécessaires à une restauration jusqu’au moment de la sauvegarde seront contenus dans le répertoire de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="ddad9-169">If the function succeeds, all the files needed for a restore up to the moment of the backup will be contained in the backup directory.</span></span> <span data-ttu-id="ddad9-170">S’il s’agit d’une sauvegarde complète, les fichiers sont les fichiers de base de données et les fichiers journaux nécessaires pour ramener la base de données à un état cohérent.</span><span class="sxs-lookup"><span data-stu-id="ddad9-170">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="ddad9-171">S’il s’agit d’une sauvegarde incrémentielle, seuls les fichiers journaux sont ajoutés aux répertoires, mais les fichiers déjà existants (bases de données et fichiers journaux), ainsi que les nouveaux fichiers journaux, peuvent être restaurés pour ramener la base de données dans l’État où elle se trouvait au moment où la sauvegarde a commencé.</span><span class="sxs-lookup"><span data-stu-id="ddad9-171">If this is an incremental backup, only log files will be added to the directories, but the already existing files (databases and log files), together with the new log files, will be able to be restored to bring the database back to the state it was in at the moment that the backup began.</span></span>

<span data-ttu-id="ddad9-172">En tant qu’effet secondaire de la sauvegarde, les fichiers journaux qui ne sont plus nécessaires sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="ddad9-172">As a side effect of the backup, the log files which are no longer needed will be truncated.</span></span>

<span data-ttu-id="ddad9-173">En même temps, les en-têtes de base de données sont mis à jour avec les informations lors de la dernière sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="ddad9-173">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="ddad9-174">Si la fonction échoue, il n’y aura aucun fichier dans la destination du répertoire de sauvegarde, aucune restauration n’est donc possible.</span><span class="sxs-lookup"><span data-stu-id="ddad9-174">If the function fails, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="ddad9-175">En même temps, les fichiers journaux actuels ne seront pas tronqués.</span><span class="sxs-lookup"><span data-stu-id="ddad9-175">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ddad9-176">Notes</span><span class="sxs-lookup"><span data-stu-id="ddad9-176">Remarks</span></span>

<span data-ttu-id="ddad9-177">Les différentes étapes de la sauvegarde auront des entrées de journal des événements générées, y compris les noms de fichiers, la troncation du journal et le résultat final de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="ddad9-177">The different steps of the backup will have Event Log entries generated, including the file names, the log truncation, and the final result of the backup.</span></span>

<span data-ttu-id="ddad9-178">Les sauvegardes incrémentielles sont possibles uniquement après la prise d’une sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="ddad9-178">Incremental backups are possible only after a full backup was taken.</span></span> <span data-ttu-id="ddad9-179">En outre, les sauvegardes incrémentielles sont possibles uniquement si la journalisation circulaire est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ddad9-179">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="ddad9-180">Il est recommandé que le répertoire de sauvegarde ne contienne aucun fichier autre que celui utilisé dans la sauvegarde ou ajouté par une sauvegarde précédente réussie.</span><span class="sxs-lookup"><span data-stu-id="ddad9-180">It is recommended that the backup directory should not contain any files other than the one used in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="ddad9-181">Le répertoire de sauvegarde doit exister, sauf si le paramètre *JET_paramCreatePathIfNotExist* est défini pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="ddad9-181">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="ddad9-182">Pour plus d’informations, consultez [paramètres système](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ddad9-182">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="ddad9-183">La sauvegarde effectue une vérification de la somme de contrôle sur toutes les pages de base de données utilisées et à partir de Windows Server 2003, également sur les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="ddad9-183">The backup will do a checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="ddad9-184">Cela donne la possibilité d’estimer l’intégrité de la base de données, même pour les pages qui ne sont pas lues pendant des opérations normales.</span><span class="sxs-lookup"><span data-stu-id="ddad9-184">This gives an opportunity to estimate the health of the database, even for pages which are not read during normal operations.</span></span> <span data-ttu-id="ddad9-185">Si une telle altération est détectée, la sauvegarde échoue.</span><span class="sxs-lookup"><span data-stu-id="ddad9-185">If any such corruption is encountered, the backup will fail.</span></span>

<span data-ttu-id="ddad9-186">Pendant la sauvegarde, le fichier journal actuel est terminé et un nouveau journal est généré.</span><span class="sxs-lookup"><span data-stu-id="ddad9-186">During the backup, the current log file will be finished and a new log will be generated.</span></span> <span data-ttu-id="ddad9-187">De cette façon, tous les fichiers journaux nécessaires peuvent être des copies, car le journal actuel n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="ddad9-187">This way, all of the necessary log files can be copies, because the current log will not be in use anymore.</span></span>

<span data-ttu-id="ddad9-188">Il est vivement recommandé de ne pas utiliser la sauvegarde à des fins autres que la sauvegarde et la restauration au niveau du moteur.</span><span class="sxs-lookup"><span data-stu-id="ddad9-188">It is strongly recommended that the backup not be used for any purpose other than the backup and restore at the engine level.</span></span> <span data-ttu-id="ddad9-189">Cela réduira le risque d’obtenir des erreurs pendant les opérations de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="ddad9-189">This will minimize the chance of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ddad9-190">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddad9-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-191"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ddad9-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ddad9-192">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="ddad9-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-193"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="ddad9-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ddad9-194">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ddad9-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-195"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="ddad9-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ddad9-196">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="ddad9-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-197"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="ddad9-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ddad9-198">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ddad9-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddad9-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ddad9-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ddad9-200">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ddad9-200">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddad9-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ddad9-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ddad9-202">Implémenté en tant que <strong>JetBackupW</strong> (Unicode) et <strong>JetBackupA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ddad9-202">Implemented as <strong>JetBackupW</strong> (Unicode) and <strong>JetBackupA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ddad9-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddad9-203">See Also</span></span>

[<span data-ttu-id="ddad9-204">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="ddad9-204">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="ddad9-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ddad9-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ddad9-206">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ddad9-206">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ddad9-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="ddad9-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="ddad9-208">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="ddad9-208">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="ddad9-209">JetRestore</span><span class="sxs-lookup"><span data-stu-id="ddad9-209">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="ddad9-210">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="ddad9-210">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="ddad9-211">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="ddad9-211">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="ddad9-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="ddad9-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="ddad9-213">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="ddad9-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

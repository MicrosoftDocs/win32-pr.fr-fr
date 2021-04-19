---
description: 'En savoir plus sur : fonction JetExternalRestore'
title: JetExternalRestore fonction)
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106542207"
---
# <a name="jetexternalrestore-function"></a><span data-ttu-id="aeedd-103">JetExternalRestore fonction)</span><span class="sxs-lookup"><span data-stu-id="aeedd-103">JetExternalRestore Function</span></span>


<span data-ttu-id="aeedd-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="aeedd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore-function"></a><span data-ttu-id="aeedd-105">JetExternalRestore fonction)</span><span class="sxs-lookup"><span data-stu-id="aeedd-105">JetExternalRestore Function</span></span>

<span data-ttu-id="aeedd-106">La fonction **JetExternalRestore** restaure une sauvegarde externe qui a été effectuée avec les API de sauvegarde externes et spécifie une plage de numéros de fichier journal à relire pendant le processus de restauration.</span><span class="sxs-lookup"><span data-stu-id="aeedd-106">The **JetExternalRestore** function restores an external backup that was taken with the external backup APIs and specifies a range of log file numbers to replay during the restore process.</span></span> <span data-ttu-id="aeedd-107">C’est ce que l’on appelle la récupération matérielle, qui est semblable à mais différente de la récupération logicielle telle qu’elle est exécutée par la fonction [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="aeedd-107">This is known as hard recovery, which is similar to but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="aeedd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aeedd-108">Parameters</span></span>

<span data-ttu-id="aeedd-109">*szCheckpointFilePath*</span><span class="sxs-lookup"><span data-stu-id="aeedd-109">*szCheckpointFilePath*</span></span>

<span data-ttu-id="aeedd-110">Chemin d’accès du fichier de point de contrôle à utiliser pendant la récupération si *szTargetInstanceCheckpointPath* n’est pas spécifié ou s’il dispose déjà d’une instance active ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="aeedd-110">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or already has an active or running instance.</span></span>

<span data-ttu-id="aeedd-111">*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="aeedd-111">*szLogPath*</span></span>

<span data-ttu-id="aeedd-112">Chemin d’accès ou répertoire des journaux pour la phase finale (annulation) de la récupération et éventuellement pour les journaux de restauration par progression.</span><span class="sxs-lookup"><span data-stu-id="aeedd-112">The path or directory for the logs for the final phase (undo) of recovery, and possibly for the roll forward logs.</span></span> <span data-ttu-id="aeedd-113">Ce chemin d’accès peut être le même que le *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="aeedd-113">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="aeedd-114">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="aeedd-114">*rgrstmap*</span></span>

<span data-ttu-id="aeedd-115">Il s’agit d’un tableau de structures [JET_RSTMAP](./jet-rstmap-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="aeedd-115">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="aeedd-116">Il s’agit d’une table de chemins d’accès ou de noms de fichiers anciens et nouveaux.</span><span class="sxs-lookup"><span data-stu-id="aeedd-116">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="aeedd-117">Cela est utilisé, car les bases de données peuvent devoir être récupérées dans un emplacement autre que l’emplacement à partir duquel elles ont été sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="aeedd-117">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="aeedd-118">Dans le cas où plusieurs bases de données sont attachées à un seul jeu de journalisation, le mappage de restauration peut spécifier un sous-ensemble de bases de données à restaurer.</span><span class="sxs-lookup"><span data-stu-id="aeedd-118">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of databases to restore.</span></span>

<span data-ttu-id="aeedd-119">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="aeedd-119">*crstfilemap*</span></span>

<span data-ttu-id="aeedd-120">Nombre d’entrées dans le paramètre de tableau *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="aeedd-120">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="aeedd-121">*szBackupLogPath*</span><span class="sxs-lookup"><span data-stu-id="aeedd-121">*szBackupLogPath*</span></span>

<span data-ttu-id="aeedd-122">Chemin d’accès au répertoire dans lequel les fichiers journaux sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="aeedd-122">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="aeedd-123">Il s’agit des journaux qui ont été lus pendant la séquence de sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="aeedd-123">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="aeedd-124">Ce chemin d’accès peut être le même que le szLogPath.</span><span class="sxs-lookup"><span data-stu-id="aeedd-124">This path may be the same as the szLogPath.</span></span>

<span data-ttu-id="aeedd-125">*genLow*</span><span class="sxs-lookup"><span data-stu-id="aeedd-125">*genLow*</span></span>

<span data-ttu-id="aeedd-126">Numéro de fichier journal le plus bas à relire à partir de *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="aeedd-126">The lowest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="aeedd-127">La fidélité complète d’un long non signé doit être conservée, mais dans les versions actuelles du moteur, ce nombre est un nombre hexadécimal compris entre 0x00000 et 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="aeedd-127">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="aeedd-128">Cela peut changer dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="aeedd-128">This may change in future versions.</span></span>

<span data-ttu-id="aeedd-129">*genHigh*</span><span class="sxs-lookup"><span data-stu-id="aeedd-129">*genHigh*</span></span>

<span data-ttu-id="aeedd-130">Numéro de fichier journal le plus élevé à relire à partir de *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="aeedd-130">The highest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="aeedd-131">La fidélité complète d’un long non signé doit être conservée, mais dans les versions actuelles du moteur, ce nombre est un nombre hexadécimal compris entre 0x00000 et 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="aeedd-131">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="aeedd-132">Cela peut changer dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="aeedd-132">This may change in future versions.</span></span>

<span data-ttu-id="aeedd-133">*PFN*</span><span class="sxs-lookup"><span data-stu-id="aeedd-133">*pfn*</span></span>

<span data-ttu-id="aeedd-134">Rappel d’État pour signaler la progression de la récupération.</span><span class="sxs-lookup"><span data-stu-id="aeedd-134">The status callback, to report progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="aeedd-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aeedd-135">Return Value</span></span>

<span data-ttu-id="aeedd-136">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="aeedd-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="aeedd-137">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="aeedd-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aeedd-138">Code de retour</span><span class="sxs-lookup"><span data-stu-id="aeedd-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="aeedd-139">Description</span><span class="sxs-lookup"><span data-stu-id="aeedd-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aeedd-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="aeedd-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="aeedd-141">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="aeedd-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aeedd-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="aeedd-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="aeedd-143">L’opération a échoué, car la mémoire peut être allouée pour être terminée.</span><span class="sxs-lookup"><span data-stu-id="aeedd-143">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aeedd-144">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="aeedd-144">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="aeedd-145">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="aeedd-145">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="aeedd-146">Cela peut se produire pour <strong>JetExternalRestore</strong>, et ainsi de suite lorsque le <em>SzTargetCheckpointPath</em> et le <em>szTargetInstanceLogPath</em> ne sont pas tous les deux spécifiés ou non spécifiés.</span><span class="sxs-lookup"><span data-stu-id="aeedd-146">This can happen for <strong>JetExternalRestore</strong>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="aeedd-147">Autrement dit, ils doivent correspondre et être spécifiés ou non spécifiés.</span><span class="sxs-lookup"><span data-stu-id="aeedd-147">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aeedd-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="aeedd-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="aeedd-149">Cela indique que la base de données a été endommagée ou un fichier non reconnu.</span><span class="sxs-lookup"><span data-stu-id="aeedd-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aeedd-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="aeedd-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="aeedd-151">L’opération a échoué, car elle n’a pas pu ouvrir le fichier demandé, car il est introuvable dans le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="aeedd-151">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aeedd-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="aeedd-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="aeedd-153">L’opération a échoué, car le chemin d’accès spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="aeedd-153">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aeedd-154">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="aeedd-154">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="aeedd-155">Cette erreur est retournée si le fichier de base de données spécifié lors de la restauration n’est pas une base de données qui a été sauvegardée avec une sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="aeedd-155">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aeedd-156">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="aeedd-156">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="aeedd-157">Cette erreur est retournée si l’un des fichiers journaux dans <em>szBackupLogPath</em>a une génération de journal ci-dessous, spécifiée par <em>genLow</em> ou <em>pLogInfo. ulGenLow</em>.</span><span class="sxs-lookup"><span data-stu-id="aeedd-157">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aeedd-158">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="aeedd-158">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="aeedd-159">Cette erreur est retournée si l’un des fichiers journaux dans le <em>szBackupLogPath</em>a une génération de journal supérieure à celle spécifiée dans <em>genHigh</em> ou <em>pLogInfo. ulGenHigh</em>.</span><span class="sxs-lookup"><span data-stu-id="aeedd-159">This error is returned if one fo the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aeedd-160">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="aeedd-160">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="aeedd-161">Le <em>szTargetInstanceLogPath</em> spécifié n’appartient pas à une instance initialisée.</span><span class="sxs-lookup"><span data-stu-id="aeedd-161">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="aeedd-162">Cette erreur est renvoyée uniquement dans Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="aeedd-162">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aeedd-163">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="aeedd-163">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="aeedd-164">Le moteur de base de données ne peut pas exécuter une restauration externe ou une récupération matérielle en mode instance unique.</span><span class="sxs-lookup"><span data-stu-id="aeedd-164">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="aeedd-165">Cette erreur est renvoyée uniquement dans Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="aeedd-165">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aeedd-166">En cas de réussite, toutes les bases de données du *rgrstmap* sont entièrement récupérées et dans un état propre ou cohérent.</span><span class="sxs-lookup"><span data-stu-id="aeedd-166">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="aeedd-167">À ce stade, la base de données peut être remontée sur une instance existante.</span><span class="sxs-lookup"><span data-stu-id="aeedd-167">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="aeedd-168">En cas d’échec, le moteur n’a pas pu récupérer la base de données.</span><span class="sxs-lookup"><span data-stu-id="aeedd-168">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="aeedd-169">La base de données est dans un État non valide et, afin de retenter la récupération matérielle, la base de données entière doit être restaurée à nouveau.</span><span class="sxs-lookup"><span data-stu-id="aeedd-169">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="aeedd-170">En règle générale, la source d’une telle situation est l’endommagement du disque ou du journal, ou une autre forme de gestion des journaux ou un ensemble de journaux non continus.</span><span class="sxs-lookup"><span data-stu-id="aeedd-170">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="aeedd-171">Notes</span><span class="sxs-lookup"><span data-stu-id="aeedd-171">Remarks</span></span>

<span data-ttu-id="aeedd-172">Pour comprendre le fonctionnement d’une récupération « dure », vous devez comprendre qu’il existe trois phases de récupération et que la deuxième phase peut avoir deux parties.</span><span class="sxs-lookup"><span data-stu-id="aeedd-172">To understand how a "hard" recovery works, you must understand that there are three phases of recovery, and the second phase can have two parts.</span></span> <span data-ttu-id="aeedd-173">Dans la phase I, les journaux sont requis pour ramener une base de données sauvegardée à la cohérence (ou un ensemble initial de journaux incrémentiels peut être utilisé).</span><span class="sxs-lookup"><span data-stu-id="aeedd-173">In Phase I, logs are required to bring a backed up database to consistency (or an initial set of incremental logs can be used).</span></span> <span data-ttu-id="aeedd-174">Au cours de la phase II, tous les journaux de restauration par progression supplémentaires disponibles sont utilisés pour rendre la base de données cohérente.</span><span class="sxs-lookup"><span data-stu-id="aeedd-174">In Phase II, any additional roll forward logs that are available are consumed to make the database consistent.</span></span> <span data-ttu-id="aeedd-175">Il y a également une relecture des journaux de restauration par progression supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="aeedd-175">There is also a replay of the additional roll forward logs.</span></span> <span data-ttu-id="aeedd-176">La phase III est la phase d’annulation de la récupération.</span><span class="sxs-lookup"><span data-stu-id="aeedd-176">Phase III is the undo phase of recovery.</span></span>

<span data-ttu-id="aeedd-177">Phase I : la relecture de l’ensemble des journaux qui doivent être restaurés pour que la base de données soit placée dans un état cohérent (ou un ensemble initial de fichiers journaux) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="aeedd-177">Phase I: The replay of the set of logs that must be restored for the database to be brought to a consistent state (or an initial set of log files) is performed.</span></span> <span data-ttu-id="aeedd-178">Fondamentalement, il s’agit de la relecture de l’ensemble des fichiers journaux qui ne sont pas facultatifs pour les bases de données en cours de restauration.</span><span class="sxs-lookup"><span data-stu-id="aeedd-178">Basically, this is the replay of the set of log files that are not optional for the databases being restored.</span></span> <span data-ttu-id="aeedd-179">S’il manque des journaux dans cette plage de journaux, la restauration échoue.</span><span class="sxs-lookup"><span data-stu-id="aeedd-179">If there are missing logs from this range of logs then the restore will fail.</span></span> <span data-ttu-id="aeedd-180">Ces journaux doivent être placés dans le répertoire spécifié dans le paramètre *szBackupLogPath* .</span><span class="sxs-lookup"><span data-stu-id="aeedd-180">These logs should be put in the directory specified in the *szBackupLogPath* parameter.</span></span>

<span data-ttu-id="aeedd-181">Phase II : éventuellement, il peut y avoir certains ensembles de fichiers journaux qui sont des fichiers journaux de restauration par progression issus de sauvegardes incrémentielles ou différentielles et des fichiers journaux d’une instance active.</span><span class="sxs-lookup"><span data-stu-id="aeedd-181">Phase II: Optionally, there may be some sets of log files that are roll forward log files that come from incremental or differential backups and from the log files of an active instance.</span></span> <span data-ttu-id="aeedd-182">Dans le cas de fichiers journaux issus de sauvegardes incrémentielles ou différentielles, les fichiers journaux peuvent être placés dans les répertoires spécifiés dans les paramètres *szBackupLogPath* ou *szTargetInstanceLogPath* , l’ancien étant le répertoire recommandé.</span><span class="sxs-lookup"><span data-stu-id="aeedd-182">In the case of log files from incremental or differential backups, the log files can be placed in the directories specified in either the *szBackupLogPath* or the *szTargetInstanceLogPath* parameters, with the former being the recommended directory.</span></span> <span data-ttu-id="aeedd-183">Les journaux utilisés pour la phase de restauration par progression (phase II) doivent provenir de la même série de journaux joués au cours de la phase I et doivent incrémenter continuellement les numéros de journal sans aucun écart par rapport à la phase I.</span><span class="sxs-lookup"><span data-stu-id="aeedd-183">The logs used for the roll forward phase (phase II) should come from the same series of logs played during Phase I and should have continuously incrementing log numbers with no gaps from the Phase I logs.</span></span> <span data-ttu-id="aeedd-184">Pour qu’une base de données soit entièrement à jour avec les fichiers journaux en cours d’utilisation par une instance active, les paramètres *szTargetInstanceLogPath* et *szTargetInstanceCheckpointPath* doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="aeedd-184">To play a database to be fully up to date with the log files currently being used by an active instance, the *szTargetInstanceLogPath* and *szTargetInstanceCheckpointPath* parameters must be specified.</span></span> <span data-ttu-id="aeedd-185">Cela peut être fait même si d’autres bases de données sont attachées à ce jeu de journaux.</span><span class="sxs-lookup"><span data-stu-id="aeedd-185">This can be done even while other databases are attached to that log set.</span></span>

<span data-ttu-id="aeedd-186">Phase III : dans la dernière phase de la récupération, toutes les transactions non validées sont restaurées, ce qui nécessite la génération de nouveaux fichiers journaux et la mise à jour du fichier de point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="aeedd-186">Phase III: In the final phase of recovery, any uncommitted transactions are rolled back, which requires generating new log files and updating the checkpoint file.</span></span> <span data-ttu-id="aeedd-187">Cette phase est parfois appelée « annulation ».</span><span class="sxs-lookup"><span data-stu-id="aeedd-187">This phase is sometimes referred to as "undo".</span></span> <span data-ttu-id="aeedd-188">Le chemin d’accès au fichier de point de contrôle à utiliser au cours de cette phase est le chemin d’accès analogue à l’emplacement du journal de la phase III, autrement dit, si *szLogPath* est utilisé pour la phase III, *szCheckpointFilePath* sera utilisé, si *szTargetInstanceLogPath* est utilisé pour la phase III de la récupération *szTargetInstanceCheckpointPath* sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="aeedd-188">The checkpoint file path to use during this phase is the path analogous to the phase III log location, that is, if *szLogPath* is used for Phase III, *szCheckpointFilePath* will be used, if *szTargetInstanceLogPath* is used for phase III of recovery *szTargetInstanceCheckpointPath* will be used.</span></span>

<span data-ttu-id="aeedd-189">Pour comprendre le fonctionnement des tracés, utilisez cet organigramme :</span><span class="sxs-lookup"><span data-stu-id="aeedd-189">To understand how the paths work, use this flow chart:</span></span>

<span data-ttu-id="aeedd-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span><span class="sxs-lookup"><span data-stu-id="aeedd-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span></span>

#### <a name="requirements"></a><span data-ttu-id="aeedd-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aeedd-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aeedd-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="aeedd-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aeedd-193">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="aeedd-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aeedd-194"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="aeedd-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aeedd-195">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="aeedd-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aeedd-196"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="aeedd-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aeedd-197">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="aeedd-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aeedd-198"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="aeedd-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="aeedd-199">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="aeedd-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aeedd-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="aeedd-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="aeedd-201">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="aeedd-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aeedd-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="aeedd-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="aeedd-203">Implémenté en tant que <strong>JetExternalRestoreW</strong> (Unicode) et <strong>JetExternalRestoreA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="aeedd-203">Implemented as <strong>JetExternalRestoreW</strong> (Unicode) and <strong>JetExternalRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="aeedd-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aeedd-204">See Also</span></span>

[<span data-ttu-id="aeedd-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="aeedd-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="aeedd-206">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="aeedd-206">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="aeedd-207">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="aeedd-207">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="aeedd-208">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="aeedd-208">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="aeedd-209">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="aeedd-209">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="aeedd-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="aeedd-210">JetInit</span></span>](./jetinit-function.md)

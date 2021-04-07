---
description: 'En savoir plus sur : fonction JetExternalRestore2'
title: Fonction JetExternalRestore2
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952445"
---
# <a name="jetexternalrestore2-function"></a><span data-ttu-id="024b9-103">Fonction JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="024b9-103">JetExternalRestore2 Function</span></span>


<span data-ttu-id="024b9-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="024b9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore2-function"></a><span data-ttu-id="024b9-105">Fonction JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="024b9-105">JetExternalRestore2 Function</span></span>

<span data-ttu-id="024b9-106">La fonction **JetExternalRestore2** restaure une sauvegarde externe qui a été effectuée avec les API de sauvegarde externes et fournit des points de contrôle à utiliser pour les opérations de journalisation circulaire.</span><span class="sxs-lookup"><span data-stu-id="024b9-106">The **JetExternalRestore2** function restores an external backup that was taken with the external backup APIs and provides checkpoints to use for circular logging operations.</span></span> <span data-ttu-id="024b9-107">C’est ce que l’on appelle la récupération matérielle, qui est similaire, mais différente de la récupération logicielle, telle qu’elle est exécutée par la fonction [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="024b9-107">This is known as hard recovery, which is similar but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

<span data-ttu-id="024b9-108">**Windows XP : JetExternalRestore2** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="024b9-108">**Windows XP:  JetExternalRestore2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="024b9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="024b9-109">Parameters</span></span>

<span data-ttu-id="024b9-110">*szCheckpointFilePath*</span><span class="sxs-lookup"><span data-stu-id="024b9-110">*szCheckpointFilePath*</span></span>

<span data-ttu-id="024b9-111">Chemin d’accès pour le fichier de point de contrôle à utiliser pendant la récupération si *szTargetInstanceCheckpointPath* n’est pas spécifié ou si le chemin d’accès a une instance active ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="024b9-111">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or that path has an active or running instance.</span></span>

<span data-ttu-id="024b9-112">*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="024b9-112">*szLogPath*</span></span>

<span data-ttu-id="024b9-113">Chemin d’accès ou répertoire des journaux pour la phase finale (annulation) de la récupération et éventuellement pour les journaux de restauration par progression.</span><span class="sxs-lookup"><span data-stu-id="024b9-113">The path or directory for the logs for the final phase (undo) of the recovery and possibly for the roll forward logs.</span></span> <span data-ttu-id="024b9-114">Ce chemin d’accès peut être le même que le *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="024b9-114">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="024b9-115">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="024b9-115">*rgrstmap*</span></span>

<span data-ttu-id="024b9-116">Il s’agit d’un tableau de structures [JET_RSTMAP](./jet-rstmap-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="024b9-116">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="024b9-117">Il s’agit d’une table de chemins d’accès ou de noms de fichiers anciens et nouveaux.</span><span class="sxs-lookup"><span data-stu-id="024b9-117">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="024b9-118">Cela est utilisé, car les bases de données peuvent devoir être récupérées dans un emplacement autre que l’emplacement à partir duquel elles ont été sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="024b9-118">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="024b9-119">Dans le cas où plusieurs bases de données sont attachées à un seul jeu de journalisation, le mappage de restauration peut spécifier un sous-ensemble des bases de données à restaurer.</span><span class="sxs-lookup"><span data-stu-id="024b9-119">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of the databases to restore.</span></span>

<span data-ttu-id="024b9-120">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="024b9-120">*crstfilemap*</span></span>

<span data-ttu-id="024b9-121">Nombre d’entrées dans le paramètre de tableau *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="024b9-121">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="024b9-122">*szBackupLogPath*</span><span class="sxs-lookup"><span data-stu-id="024b9-122">*szBackupLogPath*</span></span>

<span data-ttu-id="024b9-123">Chemin d’accès au répertoire dans lequel les fichiers journaux sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="024b9-123">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="024b9-124">Il s’agit des journaux qui ont été lus pendant la séquence de sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="024b9-124">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="024b9-125">Ce chemin d’accès peut être le même que le *szLogPath*.</span><span class="sxs-lookup"><span data-stu-id="024b9-125">This path may be the same as the *szLogPath*.</span></span>

<span data-ttu-id="024b9-126">*pLogInfo*</span><span class="sxs-lookup"><span data-stu-id="024b9-126">*pLogInfo*</span></span>

<span data-ttu-id="024b9-127">Le *pLogInfo* décrit plusieurs aspects des journaux de sauvegarde à récupérer. ce paramètre permet à **JetExternalRestore2** de prendre les paramètres *genLow* et *genHigh* explicites que **JetExternalRestore2** a, ainsi que le nom du journal de base, au lieu d’un nom de base de journal présumé « edb ».</span><span class="sxs-lookup"><span data-stu-id="024b9-127">The *pLogInfo* describes several aspects of the backup logs to recovery, this parameter allows **JetExternalRestore2** to take the explicit *genLow* and *genHigh* parameters that **JetExternalRestore2** has, as well as the base log name, instead of a presumed log base name of "edb".</span></span>

<span data-ttu-id="024b9-128">*szTargetInstanceName*</span><span class="sxs-lookup"><span data-stu-id="024b9-128">*szTargetInstanceName*</span></span>

<span data-ttu-id="024b9-129">Ce paramètre est déconseillé et ne peut pas être utilisé dans votre application.</span><span class="sxs-lookup"><span data-stu-id="024b9-129">This parameter is deprecated and cannot be used in your application.</span></span>

<span data-ttu-id="024b9-130">*szTargetInstanceLogPath*</span><span class="sxs-lookup"><span data-stu-id="024b9-130">*szTargetInstanceLogPath*</span></span>

<span data-ttu-id="024b9-131">Le chemin d’accès pour les journaux de restauration par progression si l’emplacement des journaux que vous souhaitez restaurer par progression se trouve dans un ensemble ou une instance de journalisation active.</span><span class="sxs-lookup"><span data-stu-id="024b9-131">The path for the roll forward logs if the location of the logs you would like to roll forward are in an active logging set or instance.</span></span> <span data-ttu-id="024b9-132">Cela ne doit pas être spécifié si l’instance cible utilise la journalisation circulaire.</span><span class="sxs-lookup"><span data-stu-id="024b9-132">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="024b9-133">*szTargetInstanceCheckpointPath*</span><span class="sxs-lookup"><span data-stu-id="024b9-133">*szTargetInstanceCheckpointPath*</span></span>

<span data-ttu-id="024b9-134">Chemin d’accès du point de contrôle pendant la récupération si aucune instance active n’est en cours d’exécution sur cette cible.</span><span class="sxs-lookup"><span data-stu-id="024b9-134">The path for the checkpoint during recovery if there is no active instance running at this target.</span></span> <span data-ttu-id="024b9-135">Cela ne doit pas être spécifié si l’instance cible utilise la journalisation circulaire.</span><span class="sxs-lookup"><span data-stu-id="024b9-135">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="024b9-136">*PFN*</span><span class="sxs-lookup"><span data-stu-id="024b9-136">*pfn*</span></span>

<span data-ttu-id="024b9-137">Rappel d’État qui indique la progression de la récupération.</span><span class="sxs-lookup"><span data-stu-id="024b9-137">The status callback, which reports the progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="024b9-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="024b9-138">Return Value</span></span>

<span data-ttu-id="024b9-139">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="024b9-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="024b9-140">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="024b9-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="024b9-141">Code de retour</span><span class="sxs-lookup"><span data-stu-id="024b9-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="024b9-142">Description</span><span class="sxs-lookup"><span data-stu-id="024b9-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="024b9-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="024b9-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="024b9-144">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="024b9-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="024b9-145">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="024b9-145">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="024b9-146">Le <em>szTargetInstanceLogPath</em> spécifié n’appartient pas à une instance initialisée.</span><span class="sxs-lookup"><span data-stu-id="024b9-146">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="024b9-147">Cette erreur est renvoyée uniquement dans Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="024b9-147">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="024b9-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="024b9-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="024b9-149">Cela indique que la base de données a été endommagée ou un fichier non reconnu.</span><span class="sxs-lookup"><span data-stu-id="024b9-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="024b9-150">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="024b9-150">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="024b9-151">Cette erreur est retournée si l’une des fichiers journaux dans le <em>szBackupLogPath</em>a une génération de journal supérieure à celle spécifiée dans <em>genHigh</em> ou <em>pLogInfo. ulGenHigh</em>.</span><span class="sxs-lookup"><span data-stu-id="024b9-151">This error is returned if one for the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="024b9-152">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="024b9-152">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="024b9-153">L’opération a échoué, car elle n’a pas pu ouvrir le fichier demandé, car il est introuvable dans le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="024b9-153">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="024b9-154">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="024b9-154">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="024b9-155">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="024b9-155">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="024b9-156">Cela peut se produire pour <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, et ainsi de suite lorsque le <em>SzTargetCheckpointPath</em> et le <em>szTargetInstanceLogPath</em> ne sont pas tous les deux spécifiés ou non spécifiés.</span><span class="sxs-lookup"><span data-stu-id="024b9-156">This can happen for <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="024b9-157">Autrement dit, ils doivent correspondre et être spécifiés ou non spécifiés.</span><span class="sxs-lookup"><span data-stu-id="024b9-157">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="024b9-158">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="024b9-158">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="024b9-159">L’opération a échoué, car le chemin d’accès spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="024b9-159">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="024b9-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="024b9-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="024b9-161">L’opération a échoué, car la mémoire peut être allouée pour être terminée.</span><span class="sxs-lookup"><span data-stu-id="024b9-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="024b9-162">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="024b9-162">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="024b9-163">Cette erreur est retournée si le fichier de base de données spécifié lors de la restauration n’est pas une base de données qui a été sauvegardée avec une sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="024b9-163">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="024b9-164">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="024b9-164">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="024b9-165">Le moteur de base de données ne peut pas exécuter une restauration externe ou une récupération matérielle en mode instance unique.</span><span class="sxs-lookup"><span data-stu-id="024b9-165">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="024b9-166">Cette erreur est renvoyée uniquement dans Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="024b9-166">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="024b9-167">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="024b9-167">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="024b9-168">Cette erreur est retournée si l’un des fichiers journaux dans <em>szBackupLogPath</em>a une génération de journal ci-dessous, spécifiée par <em>genLow</em> ou <em>pLogInfo. ulGenLow</em>.</span><span class="sxs-lookup"><span data-stu-id="024b9-168">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="024b9-169">En cas de réussite, toutes les bases de données du *rgrstmap* sont entièrement récupérées et dans un état propre ou cohérent.</span><span class="sxs-lookup"><span data-stu-id="024b9-169">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="024b9-170">À ce stade, la base de données peut être remontée sur une instance existante.</span><span class="sxs-lookup"><span data-stu-id="024b9-170">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="024b9-171">En cas d’échec, le moteur n’a pas pu récupérer la base de données.</span><span class="sxs-lookup"><span data-stu-id="024b9-171">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="024b9-172">La base de données est dans un État non valide et, afin de retenter la récupération matérielle, la base de données entière doit être restaurée à nouveau.</span><span class="sxs-lookup"><span data-stu-id="024b9-172">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="024b9-173">En règle générale, la source d’une telle situation est l’endommagement du disque ou du journal, ou une autre forme de gestion des journaux ou un ensemble de journaux non continus.</span><span class="sxs-lookup"><span data-stu-id="024b9-173">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="024b9-174">Notes</span><span class="sxs-lookup"><span data-stu-id="024b9-174">Remarks</span></span>

<span data-ttu-id="024b9-175">Consultez [JetExternalRestore](./jetexternalrestore-function.md).</span><span class="sxs-lookup"><span data-stu-id="024b9-175">See [JetExternalRestore](./jetexternalrestore-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="024b9-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="024b9-176">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="024b9-177"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="024b9-177"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="024b9-178">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="024b9-178">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="024b9-179"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="024b9-179"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="024b9-180">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="024b9-180">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="024b9-181"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="024b9-181"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="024b9-182">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="024b9-182">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="024b9-183"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="024b9-183"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="024b9-184">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="024b9-184">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="024b9-185"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="024b9-185"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="024b9-186">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="024b9-186">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="024b9-187"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="024b9-187"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="024b9-188">Implémenté en tant que <strong>JetExternalRestore2W</strong> (Unicode) et <strong>JetExternalRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="024b9-188">Implemented as <strong>JetExternalRestore2W</strong> (Unicode) and <strong>JetExternalRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="024b9-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="024b9-189">See Also</span></span>

[<span data-ttu-id="024b9-190">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="024b9-190">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="024b9-191">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="024b9-191">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="024b9-192">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="024b9-192">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="024b9-193">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="024b9-193">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="024b9-194">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="024b9-194">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="024b9-195">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="024b9-195">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="024b9-196">JetInit</span><span class="sxs-lookup"><span data-stu-id="024b9-196">JetInit</span></span>](./jetinit-function.md)

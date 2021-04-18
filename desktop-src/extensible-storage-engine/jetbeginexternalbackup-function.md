---
description: 'En savoir plus sur : fonction JetBeginExternalBackup'
title: JetBeginExternalBackup fonction)
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520167"
---
# <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="12237-103">JetBeginExternalBackup fonction)</span><span class="sxs-lookup"><span data-stu-id="12237-103">JetBeginExternalBackup Function</span></span>


<span data-ttu-id="12237-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="12237-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="12237-105">JetBeginExternalBackup fonction)</span><span class="sxs-lookup"><span data-stu-id="12237-105">JetBeginExternalBackup Function</span></span>

<span data-ttu-id="12237-106">La fonction **JetBeginExternalBackup** lance une sauvegarde externe alors que le moteur et la base de données sont en ligne et actifs.</span><span class="sxs-lookup"><span data-stu-id="12237-106">The **JetBeginExternalBackup** function initiates an external backup while the engine and database is online and active.</span></span> <span data-ttu-id="12237-107">**JetBeginExternalBackup** est le premier d’une série de fonctions qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).</span><span class="sxs-lookup"><span data-stu-id="12237-107">**JetBeginExternalBackup** is the first in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="12237-108">Une sauvegarde externe peut être utilisée pour implémenter des sauvegardes complètes, incrémentielles ou différentielles.</span><span class="sxs-lookup"><span data-stu-id="12237-108">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="12237-109">La sauvegarde sera approximative, car la sauvegarde sera cohérente à un point unique dans le temps dans l’historique des transactions, mais le contrôle du point exact dans le temps n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="12237-109">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="12237-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12237-110">Parameters</span></span>

<span data-ttu-id="12237-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="12237-111">*grbit*</span></span>

<span data-ttu-id="12237-112">Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="12237-112">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12237-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="12237-113">Value</span></span></p></th>
<th><p><span data-ttu-id="12237-114">Signification</span><span class="sxs-lookup"><span data-stu-id="12237-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12237-115">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="12237-115">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="12237-116">Cet indicateur est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="12237-116">This flag is deprecated.</span></span> <span data-ttu-id="12237-117">L’utilisation de ce bit entraîne le retour de JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="12237-117">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-118">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="12237-118">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="12237-119">Crée une sauvegarde incrémentielle par opposition à une sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="12237-119">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="12237-120">Cela signifie que seuls les fichiers journaux depuis la dernière sauvegarde complète ou incrémentielle sont sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="12237-120">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-121">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="12237-121">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="12237-122">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="12237-122">Reserved for future use.</span></span> <span data-ttu-id="12237-123">Défini pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="12237-123">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="12237-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="12237-124">Return Value</span></span>

<span data-ttu-id="12237-125">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="12237-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="12237-126">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="12237-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12237-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="12237-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="12237-128">Description</span><span class="sxs-lookup"><span data-stu-id="12237-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12237-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="12237-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="12237-130">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="12237-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="12237-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="12237-132">Si une sauvegarde externe ou de capture instantanée est déjà en cours, cette erreur est retournée, jusqu’à ce que <strong>JetBeginExternalBackup</strong> (ou l’une des variantes de celle-ci) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="12237-132">If an external backup or snapshot backup is already in process, this error will be returned, until <strong>JetBeginExternalBackup</strong> (or one of the variants of it) is called.</span></span> <span data-ttu-id="12237-133">ESE n’autorise qu’une seule sauvegarde en ligne à la fois.</span><span class="sxs-lookup"><span data-stu-id="12237-133">ESE allows only one online backup at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-134">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="12237-134">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="12237-135">L’instance ou le moteur de base de données est en mode de récupération ou d’arrêt ou d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="12237-135">The instance or database engine is either in recovery or in a shutdown or termination phase.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-136">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="12237-136">JET_errCheckpointCorrupt</span></span></p></td>
<td><p><span data-ttu-id="12237-137">Sur une sauvegarde complète, le fichier de point de contrôle n’a pas pu être lu ou le fichier n’a pas pu être vérifié.</span><span class="sxs-lookup"><span data-stu-id="12237-137">On a full backup, the checkpoint file could not be read, or the file could not be verified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-138">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="12237-138">JET_errCheckpointFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="12237-139">Dans le cas d’une sauvegarde complète, le fichier de point de contrôle est introuvable.</span><span class="sxs-lookup"><span data-stu-id="12237-139">On a full backup, the checkpoint file could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="12237-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="12237-141">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="12237-141">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="12237-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="12237-143">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="12237-143">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="12237-144"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="12237-144"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-145">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="12237-145">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="12237-146">L’enregistrement circulaire est activé et le type de sauvegarde spécifié est JET_bitBackupIncremental.</span><span class="sxs-lookup"><span data-stu-id="12237-146">Circular logging is enabled and the backup type specified is JET_bitBackupIncremental.</span></span> <span data-ttu-id="12237-147">Pour plus d’informations sur la façon de contrôler la journalisation circulaire ou non circulaire, consultez <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> dans les <strong>Erreurs du journal des transactions</strong> .</span><span class="sxs-lookup"><span data-stu-id="12237-147">See <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> in the <strong>Transaction Log Errors</strong> for information about how to control circular or non-circular logging.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-148">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="12237-148">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="12237-149">Un ou plusieurs des membres <em>Grbit</em> ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="12237-149">One or more of the <em>grbit</em> members was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-150">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="12237-150">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="12237-151">La récupération ou la journalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="12237-151">Recovery or logging is disabled.</span></span> <span data-ttu-id="12237-152">Vous ne pouvez pas effectuer une sauvegarde en ligne si la journalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="12237-152">You cannot do an online backup if logging is disabled.</span></span> <span data-ttu-id="12237-153">Pour plus d’informations sur la journalisation et la récupération, consultez <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span><span class="sxs-lookup"><span data-stu-id="12237-153">For more information about logging and recovery, see <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-154">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="12237-154">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="12237-155">Le moteur a cessé d’écrire sur le lecteur de journal, en raison d’erreurs d’e/s disque complètes ou d’e/s disque.</span><span class="sxs-lookup"><span data-stu-id="12237-155">The engine has stopped writing to the log drive, due to log being full or disk IO errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-156">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="12237-156">JET_errMissingFullBackup</span></span></p></td>
<td><p><span data-ttu-id="12237-157">La sauvegarde incrémentielle a été spécifiée (avec JET_bitBackupIncremental) et jamais une sauvegarde complète de l’une des bases de données attachées pour le jeu de journalisation.</span><span class="sxs-lookup"><span data-stu-id="12237-157">The incremental backup was specified (with JET_bitBackupIncremental), and never was a full backup taken for one of the attached databases for the logging set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="12237-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="12237-159">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="12237-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="12237-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="12237-161">L’opération a échoué, car la mémoire peut être allouée pour être terminée.</span><span class="sxs-lookup"><span data-stu-id="12237-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="12237-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="12237-163">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="12237-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-164">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="12237-164">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="12237-165">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="12237-165">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="12237-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="12237-167">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="12237-167">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="12237-168">Si la fonction est réussie, une sauvegarde externe est lancée et le moteur d’état de sauvegarde est initialisé.</span><span class="sxs-lookup"><span data-stu-id="12237-168">If the function succeeds, an external backup is initiated and the backup state engine is initialized.</span></span> <span data-ttu-id="12237-169">Les API suivantes peuvent maintenant être appelées pour terminer la séquence de sauvegarde externe et diffuser ou lire le fichier de base de données, le fichier de correctif de base de données (si pris en charge) et le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="12237-169">Subsequent APIs can now be called to complete the external backup sequence and stream or read off the database file, the database patch file (if supported), and the log file.</span></span> <span data-ttu-id="12237-170">Un événement peut être enregistré au début d’une sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="12237-170">An event can be logged that an external backup has begun.</span></span>

<span data-ttu-id="12237-171">Si la fonction échoue, la session de sauvegarde ne sera pas initiée.</span><span class="sxs-lookup"><span data-stu-id="12237-171">If the function fails, the backup session will not be initiated.</span></span> <span data-ttu-id="12237-172">Si une autre session de sauvegarde est en cours, elle ne sera pas annulée.</span><span class="sxs-lookup"><span data-stu-id="12237-172">If another backup session is in progress, it will not be cancelled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="12237-173">Notes</span><span class="sxs-lookup"><span data-stu-id="12237-173">Remarks</span></span>

<span data-ttu-id="12237-174">Le processus de sauvegarde externe (tel qu’il a été démarré par **JetBeginExternalBackup**) est conçu pour permettre une sauvegarde en ligne de transactions approximatives de la totalité de l’instance sur un appareil cible en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="12237-174">The external backup process (as started by **JetBeginExternalBackup**) is designed to allow a fuzzy transaction online backup of the entire instance to a target device as a stream.</span></span> <span data-ttu-id="12237-175">La sauvegarde contient tous les fichiers de base de données qui sont attachés à l’instance à l’aide de [JetAttachDatabase](./jetattachdatabase-function.md) (pour une sauvegarde complète), suivis des fichiers correctifs de base de données associés (si pris en charge), et enfin des fichiers journaux des transactions qui ont été générés pendant le processus de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="12237-175">The backup will contain all the database files that are attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) (for a full backup), followed by their associated database patch files (if supported), and finally by the transaction log files that were generated during the backup process.</span></span> <span data-ttu-id="12237-176">Le résultat final est un ensemble de fichiers qui peuvent être restaurés à partir du flux, éventuellement combinés avec des fichiers de base de données et des fichiers journaux existants, et enfin récupérés dans un état cohérent.</span><span class="sxs-lookup"><span data-stu-id="12237-176">The end result will be a set of files that can be restored from the stream, possibly combined with existing database and log files, and finally recovered to a consistent state.</span></span>

<span data-ttu-id="12237-177">L’ordre général des opérations pour une sauvegarde complète est constitué des appels suivants.</span><span class="sxs-lookup"><span data-stu-id="12237-177">The general order of operations for a full backup consists of the following calls.</span></span> <span data-ttu-id="12237-178">Tout d’abord, **JetBeginExternalBackup** est appelé pour démarrer le processus de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="12237-178">First, **JetBeginExternalBackup** is called to start the backup process.</span></span> <span data-ttu-id="12237-179">Ensuite, [JetGetAttachInfo](./jetgetattachinfo-function.md) est appelé pour récupérer la liste des bases de données qui sont attachées à l’instance qui doit être sauvegardée.</span><span class="sxs-lookup"><span data-stu-id="12237-179">Then, [JetGetAttachInfo](./jetgetattachinfo-function.md) is called to get the list of databases that are attached to the instance that needs to be backed up.</span></span> <span data-ttu-id="12237-180">Pour chacune de ces bases de données, [JetOpenFile](./jetopenfile-function.md) est appelé, suivi d’un certain nombre d’appels [JetReadFile](./jetreadfile-function.md) , puis d’un appel à [JetCloseFile](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="12237-180">For each of these databases, [JetOpenFile](./jetopenfile-function.md) is called, followed by a number of [JetReadFile](./jetreadfile-function.md) calls, and then by a call to [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="12237-181">Ensuite, [JetGetLogInfo](./jetgetloginfo-function.md) est appelé pour obtenir la liste des fichiers journaux et des correctifs de base de données à sauvegarder.</span><span class="sxs-lookup"><span data-stu-id="12237-181">Then, [JetGetLogInfo](./jetgetloginfo-function.md) is called to get a list of database patch and log files to be backed up.</span></span> <span data-ttu-id="12237-182">Pour chacun de ces fichiers, une autre séquence d’appels [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md)et [JetCloseFile](./jetclosefile-function.md) est effectuée.</span><span class="sxs-lookup"><span data-stu-id="12237-182">For each of these files, another sequence of [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md), and [JetCloseFile](./jetclosefile-function.md) calls are made.</span></span> <span data-ttu-id="12237-183">Ensuite, tous les fichiers journaux de transactions non souhaités sont supprimés à l’aide de [JetTruncateLog](./jettruncatelog-function.md).</span><span class="sxs-lookup"><span data-stu-id="12237-183">Then, any undesired transaction log files are deleted using [JetTruncateLog](./jettruncatelog-function.md).</span></span> <span data-ttu-id="12237-184">Enfin, la sauvegarde est terminée par un appel à [JetEndExternalBackup](./jetendexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="12237-184">Finally, the backup is ended by a call to [JetEndExternalBackup](./jetendexternalbackup-function.md).</span></span>

<span data-ttu-id="12237-185">Il est également possible de modifier cet ensemble d’étapes pour effectuer une sauvegarde incrémentielle de l’instance.</span><span class="sxs-lookup"><span data-stu-id="12237-185">It is also possible to modify this set of steps to perform an incremental backup of the instance.</span></span> <span data-ttu-id="12237-186">Une sauvegarde incrémentielle énumère et sauvegarde les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="12237-186">An incremental backup enumerates and backs up log files.</span></span> <span data-ttu-id="12237-187">Les sauvegardes incrémentielles sont possibles uniquement si l’enregistrement circulaire n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="12237-187">Incremental backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="12237-188">Il est également possible de modifier cet ensemble d’étapes pour permettre l’exécution de sauvegardes différentielles ultérieures de l’instance.</span><span class="sxs-lookup"><span data-stu-id="12237-188">It is also possible to modify this set of steps to allow subsequent differential backups of the instance to be performed.</span></span> <span data-ttu-id="12237-189">Pour effectuer une sauvegarde différentielle, n’appelez pas [JetTruncateLog](./jettruncatelog-function.md) dans la sauvegarde complète ou incrémentielle précédente.</span><span class="sxs-lookup"><span data-stu-id="12237-189">To perform a differential backup, do not call [JetTruncateLog](./jettruncatelog-function.md) in the previous full or incremental backup.</span></span> <span data-ttu-id="12237-190">Si vous n’appelez pas [JetTruncateLog](./jettruncatelog-function.md), vous autorisez les sauvegardes suivantes à être différentielles en ce qui concerne la dernière sauvegarde complète ou incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="12237-190">By not calling [JetTruncateLog](./jettruncatelog-function.md), you enable subsequent backups to be differential with respect to the last full or incremental backup.</span></span> <span data-ttu-id="12237-191">Les sauvegardes différentielles ne sont possibles que si l’enregistrement circulaire n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="12237-191">Differential backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="12237-192">Le fichier de correctif de base de données est un fichier auxiliaire spécial qui est utilisé pour stocker les images de page de base de données dans certaines circonstances pendant la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="12237-192">The database patch file is a special auxiliary file that is used to store database page images under certain circumstances during the backup.</span></span> <span data-ttu-id="12237-193">Ce fichier doit être présent dans le même emplacement que la base de données qui lui est associée au cours d’une opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="12237-193">This file must be present in the same location as its associated database during a restore operation.</span></span> <span data-ttu-id="12237-194">Ce fichier est utilisé uniquement dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="12237-194">This file is only used in Windows 2000.</span></span> <span data-ttu-id="12237-195">Par conséquent, toute application écrite pour fonctionner sur Windows 2000 et d’autres versions doit prendre en charge les fichiers correctifs de base de données, le cas échéant, mais elle ne doit pas non plus échouer si elles ne sont pas présentes.</span><span class="sxs-lookup"><span data-stu-id="12237-195">As a result, any application that is written to work against Windows 2000 and other releases must support database patch files, if they are present, but also must not fail if they are not present.</span></span>

#### <a name="requirements"></a><span data-ttu-id="12237-196">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12237-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12237-197"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="12237-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="12237-198">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="12237-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-199"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="12237-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="12237-200">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="12237-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-201"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="12237-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="12237-202">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="12237-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12237-203"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="12237-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="12237-204">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="12237-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12237-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="12237-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="12237-206">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="12237-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="12237-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12237-207">See Also</span></span>

[<span data-ttu-id="12237-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="12237-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="12237-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="12237-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="12237-210">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="12237-210">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="12237-211">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="12237-211">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="12237-212">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="12237-212">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="12237-213">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="12237-213">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="12237-214">JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="12237-214">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="12237-215">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="12237-215">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="12237-216">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="12237-216">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="12237-217">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="12237-217">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="12237-218">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="12237-218">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="12237-219">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="12237-219">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="12237-220">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="12237-220">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="12237-221">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="12237-221">JetTruncateLog</span></span>](./jettruncatelog-function.md)

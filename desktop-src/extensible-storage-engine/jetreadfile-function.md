---
description: 'En savoir plus sur : fonction JetReadFile'
title: JetReadFile fonction)
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203889"
---
# <a name="jetreadfile-function"></a><span data-ttu-id="09eb7-103">JetReadFile fonction)</span><span class="sxs-lookup"><span data-stu-id="09eb7-103">JetReadFile Function</span></span>


<span data-ttu-id="09eb7-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="09eb7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfile-function"></a><span data-ttu-id="09eb7-105">JetReadFile fonction)</span><span class="sxs-lookup"><span data-stu-id="09eb7-105">JetReadFile Function</span></span>

<span data-ttu-id="09eb7-106">La fonction **JetReadFile** récupère le contenu d’un fichier ouvert avec [JetOpenFile](./jetopenfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="09eb7-106">The **JetReadFile** function retrieves the contents of a file opened with [JetOpenFile](./jetopenfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="09eb7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09eb7-107">Parameters</span></span>

<span data-ttu-id="09eb7-108">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="09eb7-108">*hfFile*</span></span>

<span data-ttu-id="09eb7-109">Handle du fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="09eb7-109">The handle of the file to be read.</span></span>

<span data-ttu-id="09eb7-110">*va*</span><span class="sxs-lookup"><span data-stu-id="09eb7-110">*pv*</span></span>

<span data-ttu-id="09eb7-111">Mémoire tampon de sortie qui recevra les données du fichier.</span><span class="sxs-lookup"><span data-stu-id="09eb7-111">Output buffer that will receive the file data.</span></span>

<span data-ttu-id="09eb7-112">*libéré*</span><span class="sxs-lookup"><span data-stu-id="09eb7-112">*cb*</span></span>

<span data-ttu-id="09eb7-113">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="09eb7-113">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="09eb7-114">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="09eb7-114">*pcbActual*</span></span>

<span data-ttu-id="09eb7-115">Reçoit la quantité réelle de données de fichier récupérées.</span><span class="sxs-lookup"><span data-stu-id="09eb7-115">Receives the actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="09eb7-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="09eb7-116">Return Value</span></span>

<span data-ttu-id="09eb7-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="09eb7-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="09eb7-118">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="09eb7-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09eb7-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="09eb7-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="09eb7-120">Description</span><span class="sxs-lookup"><span data-stu-id="09eb7-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09eb7-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="09eb7-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="09eb7-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="09eb7-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eb7-123">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="09eb7-123">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="09eb7-124">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="09eb7-124">The operation failed because the current external backup has been aborted by a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span> <span data-ttu-id="09eb7-125">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="09eb7-125">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eb7-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="09eb7-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="09eb7-127">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="09eb7-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eb7-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="09eb7-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="09eb7-129">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="09eb7-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="09eb7-130">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="09eb7-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eb7-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="09eb7-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="09eb7-132">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="09eb7-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="09eb7-133">Cela peut se produire pour <strong>JetReadFile</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="09eb7-133">This can happen for <strong>JetReadFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="09eb7-134">Le handle d’instance spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="09eb7-134">The specified instance handle is invalid.</span></span> <span data-ttu-id="09eb7-135">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="09eb7-135">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="09eb7-136">La taille de la mémoire tampon de sortie n’est pas un multiple de la taille de page de la base de données (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="09eb7-136">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="09eb7-137">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="09eb7-137">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="09eb7-138">La taille de la mémoire tampon de sortie est inférieure à trois pages de base de données (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) et il s’agit du premier appel à <strong>JetReadFile</strong> pour le handle spécifié.</span><span class="sxs-lookup"><span data-stu-id="09eb7-138">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) and this is the first call to <strong>JetReadFile</strong> for the specified handle.</span></span> <span data-ttu-id="09eb7-139">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="09eb7-139">Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eb7-140">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="09eb7-140">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="09eb7-141">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="09eb7-141">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eb7-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="09eb7-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="09eb7-143">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="09eb7-143">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eb7-144">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="09eb7-144">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="09eb7-145">L’opération a échoué car des données non récupérables ont été détectées lors de la lecture d’une page de base de données dans un fichier de base de données ou un fichier correctif de base de données.</span><span class="sxs-lookup"><span data-stu-id="09eb7-145">The operation failed because non-recoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eb7-146">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="09eb7-146">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="09eb7-147">L’opération a échoué car des données non récupérables ont été détectées lors de la lecture d’un fichier journal de transactions.</span><span class="sxs-lookup"><span data-stu-id="09eb7-147">The operation failed because non-recoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="09eb7-148">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="09eb7-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eb7-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="09eb7-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="09eb7-150">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="09eb7-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eb7-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="09eb7-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="09eb7-152">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="09eb7-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eb7-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="09eb7-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="09eb7-154">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="09eb7-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09eb7-155">En cas de réussite, le segment de données suivant du fichier est lu dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="09eb7-155">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="09eb7-156">Le nombre réel d’octets récupérés est également retourné.</span><span class="sxs-lookup"><span data-stu-id="09eb7-156">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="09eb7-157">Le décalage de fichier à partir duquel la lecture suivante aura lieu sera avancé par ce montant.</span><span class="sxs-lookup"><span data-stu-id="09eb7-157">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="09eb7-158">En cas d’échec, l’état de la mémoire tampon de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="09eb7-158">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="09eb7-159">L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance.</span><span class="sxs-lookup"><span data-stu-id="09eb7-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="09eb7-160">Sur Windows XP et versions ultérieures, la sauvegarde n’est pas annulée si une erreur s’est produite lors de la lecture d’un fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="09eb7-160">On Windows XP and later releases, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="09eb7-161">Toutefois, la sauvegarde de ce fichier de base de données restera annulée et le descripteur correspondant sera automatiquement fermé.</span><span class="sxs-lookup"><span data-stu-id="09eb7-161">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="09eb7-162">Notes</span><span class="sxs-lookup"><span data-stu-id="09eb7-162">Remarks</span></span>

<span data-ttu-id="09eb7-163">Tout appel à **JetReadFile** à l’aide d’un handle qui a déjà retourné toutes les données du fichier sous-jacent (par exemple, un appel précédent ayant retourné moins d’octets que la taille de la mémoire tampon de sortie) fonctionne toujours, mais retourne zéro octet de données.</span><span class="sxs-lookup"><span data-stu-id="09eb7-163">Any call to **JetReadFile** using a handle that has already returned all the data in the underlying file (such as a previous call returned less bytes than the size of the output buffer) will always succeed but return zero bytes of data.</span></span>

<span data-ttu-id="09eb7-164">Un grand tampon de sortie doit être utilisé pour optimiser les performances de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="09eb7-164">A large output buffer should be used to maximize backup performance.</span></span> <span data-ttu-id="09eb7-165">Certaines expérimentations peuvent être nécessaires pour trouver le bon compromis entre la consommation des ressources et le débit pour une situation donnée.</span><span class="sxs-lookup"><span data-stu-id="09eb7-165">Some experimentation may be required to find the right tradeoff between resource consumption and throughput for a given situation.</span></span> <span data-ttu-id="09eb7-166">Dans tous les cas, la mémoire tampon de sortie ne doit pas être inférieure à 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="09eb7-166">The output buffer should be no smaller than 64KB in any case.</span></span>

<span data-ttu-id="09eb7-167">Plusieurs appels simultanés à **JetReadFile** à l’aide du même descripteur de fichier ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="09eb7-167">Multiple concurrent calls to **JetReadFile** using the same file handle are not supported.</span></span> <span data-ttu-id="09eb7-168">Cela signifie qu’il n’est pas possible de mettre en file d’attente plusieurs mémoires tampons en lecture simultanée sur le même fichier pour obtenir un débit séquentiel élevé.</span><span class="sxs-lookup"><span data-stu-id="09eb7-168">This means that it is not possible to queue several buffers for read concurrently against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="09eb7-169">Une seule mémoire tampon de grande taille doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="09eb7-169">A single large buffer should be used instead.</span></span>

<span data-ttu-id="09eb7-170">Si l’instance est configurée de telle sorte que le nettoyage des pages de base de données est activé (voir JET_paramZeroDatabaseDuringBackup dans les paramètres système), les données supprimées seront supprimées de la base de données en tant qu’effet secondaire d’un appel à **JetReadFile** dans le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="09eb7-170">If the instance is configured such that database page scrubbing is enabled (see JET_paramZeroDatabaseDuringBackup in System Parameters) then deleted data will be removed from the database as a side effect of a call to **JetReadFile** against the database file.</span></span>

<span data-ttu-id="09eb7-171">Il est très important de comprendre comment la sauvegarde et l’altération des données interagissent.</span><span class="sxs-lookup"><span data-stu-id="09eb7-171">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="09eb7-172">Si le moteur de base de données détecte une altération des données au cours d’une sauvegarde, il échouera à la sauvegarde de la base de données affectée ou de la totalité de l’instance.</span><span class="sxs-lookup"><span data-stu-id="09eb7-172">If the database engine detects data corruption during a backup then it will either fail the backup of the affected database or of the entire instance.</span></span> <span data-ttu-id="09eb7-173">Il s’agit d’une décision de conception consciente destinée à vous protéger contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="09eb7-173">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="09eb7-174">Si le moteur de base de données a permis une sauvegarde réussie là où la corruption des données était présente, il est possible qu’une sauvegarde plus ancienne et non endommagée soit ignorée.</span><span class="sxs-lookup"><span data-stu-id="09eb7-174">If the database engine allowed a backup to succeed where data corruption was present then it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="09eb7-175">Cela peut être un problème, car il serait possible de corriger l’altération des données sur l’instance en direct en restaurant cette sauvegarde et en relisant tous les fichiers du journal des transactions sur cette base de données.</span><span class="sxs-lookup"><span data-stu-id="09eb7-175">This would be unfortunate because it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="09eb7-176">Ce scénario de perte de données nulle suppose que l’enregistrement circulaire n’est pas activé (voir [JET_paramCircularLog](./transaction-log-parameters.md) dans les [paramètres système](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="09eb7-176">This zero data loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="09eb7-177">Il est également important de comprendre que lorsque la corruption des données est présente, la sauvegarde en continu est la plus probable où elle sera détectée en premier.</span><span class="sxs-lookup"><span data-stu-id="09eb7-177">It is also important to understand that when data corruption is present streaming backup will be the most likely place that it will first be detected.</span></span> <span data-ttu-id="09eb7-178">C’est le cas parce que la sauvegarde en continu est le seul processus qui analyse régulièrement chaque page d’un fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="09eb7-178">This is the case because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="09eb7-179">Il est également probable que la sauvegarde en continu sera le premier processus de détection des signes précoces de défaillance matérielle, comme le manifestent les erreurs de corruption de données intermittentes.</span><span class="sxs-lookup"><span data-stu-id="09eb7-179">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors.</span></span> <span data-ttu-id="09eb7-180">Cela est dû à la quantité de données récupérées par la sauvegarde et à la vitesse à laquelle elles sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="09eb7-180">This is due to the amount of data retrieved by backup as well as the speed at which it is retrieved.</span></span>

<span data-ttu-id="09eb7-181">La corruption des données est détectée par le moteur de base de données via l’utilisation de sommes de contrôle de bloc.</span><span class="sxs-lookup"><span data-stu-id="09eb7-181">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="09eb7-182">Ces sommes de contrôle sont définies juste avant l’écriture d’une page de base de données et sont vérifiées lors de la lecture d’une page de base de données.</span><span class="sxs-lookup"><span data-stu-id="09eb7-182">These checksums are set just prior to a database page write and are verified on a database page read.</span></span> <span data-ttu-id="09eb7-183">Ce schéma permet au moteur de base de données de déterminer si les données ont été endommagées à un moment donné, mais elles ne permettent pas au moteur de base de données de déterminer la source de cette altération.</span><span class="sxs-lookup"><span data-stu-id="09eb7-183">This scheme enables the database engine to determine that data has been corrupted at some point but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="09eb7-184">Historiquement, la cause dominante de cette altération a été constatée comme provenant de sources autres que le moteur de base de données lui-même.</span><span class="sxs-lookup"><span data-stu-id="09eb7-184">Historically, the predominant cause of such corruption has been found to come from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="09eb7-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09eb7-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09eb7-186"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="09eb7-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="09eb7-187">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="09eb7-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eb7-188"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="09eb7-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="09eb7-189">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="09eb7-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eb7-190"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="09eb7-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="09eb7-191">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="09eb7-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09eb7-192"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="09eb7-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="09eb7-193">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="09eb7-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09eb7-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="09eb7-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="09eb7-195">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="09eb7-195">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="09eb7-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09eb7-196">See Also</span></span>

[<span data-ttu-id="09eb7-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="09eb7-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="09eb7-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="09eb7-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="09eb7-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="09eb7-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="09eb7-200">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="09eb7-200">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="09eb7-201">JetStopService</span><span class="sxs-lookup"><span data-stu-id="09eb7-201">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="09eb7-202">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="09eb7-202">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

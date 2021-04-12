---
description: 'En savoir plus sur : fonction JetDefragment'
title: JetDefragment fonction)
TOCTitle: JetDefragment Function
ms:assetid: 8215fd00-f1b8-4ebd-8d55-9bce11d7dc9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269317(v=EXCHG.10)
ms:contentKeyID: 32765607
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragmentA
- JetDefragment
- JetDefragmentW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88495f90e726f8c28128a6456566124f23a17381
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320950"
---
# <a name="jetdefragment-function"></a><span data-ttu-id="43305-103">JetDefragment fonction)</span><span class="sxs-lookup"><span data-stu-id="43305-103">JetDefragment Function</span></span>


<span data-ttu-id="43305-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="43305-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment-function"></a><span data-ttu-id="43305-105">JetDefragment fonction)</span><span class="sxs-lookup"><span data-stu-id="43305-105">JetDefragment Function</span></span>

<span data-ttu-id="43305-106">La fonction **JetDefragment** démarre et arrête les tâches de défragmentation de base de données qui améliorent l’Organisation des données dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="43305-106">The **JetDefragment** function starts and stops database defragmentation tasks that improves data organization within a database.</span></span> <span data-ttu-id="43305-107">Cela permet de limiter la croissance de la base de données en utilisant l’allocation de disque existante plus efficacement dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="43305-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="43305-108">Elle peut également réduire la plage de travail en garantissant un compactage plus étroit des données.</span><span class="sxs-lookup"><span data-stu-id="43305-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="43305-109">Enfin, il peut améliorer les performances des applications en accélérant les opérations courantes via une meilleure organisation des données.</span><span class="sxs-lookup"><span data-stu-id="43305-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="43305-110">La défragmentation de base de données est une opération en ligne et n’interrompt pas l’activité normale de la base de données, telle que les opérations de requête ou les mises à jour de données.</span><span class="sxs-lookup"><span data-stu-id="43305-110">Database defragmentation is an online operation and does not interrupt regular database activity, such as query operations or data updates.</span></span> <span data-ttu-id="43305-111">**JetDefragment** ne fait pas non plus de copie de toutes les données existantes.</span><span class="sxs-lookup"><span data-stu-id="43305-111">**JetDefragment** also does not make a copy of all existing data.</span></span> <span data-ttu-id="43305-112">Au lieu de cela, elle défragmente une base de données sur place.</span><span class="sxs-lookup"><span data-stu-id="43305-112">Instead, it defragments a database in place.</span></span> <span data-ttu-id="43305-113">Enfin, **JetDefragment** récupère l’espace de la base de données interne en vue de sa réutilisation, mais ne libère pas d’espace supplémentaire dans le système de fichiers du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="43305-113">Lastly, **JetDefragment** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="43305-114">Le format des données résultant peut être bien plus efficace, mais n’est généralement pas optimal.</span><span class="sxs-lookup"><span data-stu-id="43305-114">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="43305-115">La défragmentation est limitée à la libération des pages de base de données à réutiliser qui contiennent des données qui ont déjà été logiquement supprimées.</span><span class="sxs-lookup"><span data-stu-id="43305-115">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="43305-116">La défragmentation rend également les pages de base de données disponibles pour une réutilisation dans certains cas en combinant les données de deux pages quand elles peuvent tenir sur une seule page.</span><span class="sxs-lookup"><span data-stu-id="43305-116">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="43305-117">Cette opération est différente de [JetCompact](./jetcompact-function.md) qui fait une copie d’une base de données en lecture seule dans un format très optimal.</span><span class="sxs-lookup"><span data-stu-id="43305-117">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
    JET_ERR JET_API JetDefragment(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __out_opt     unsigned long* pcPasses,
      __out_opt     unsigned long* pcSeconds,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="43305-118">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43305-118">Parameters</span></span>

<span data-ttu-id="43305-119">*sesid*</span><span class="sxs-lookup"><span data-stu-id="43305-119">*sesid*</span></span>

<span data-ttu-id="43305-120">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="43305-120">The session to use for this call.</span></span>

<span data-ttu-id="43305-121">*dbid*</span><span class="sxs-lookup"><span data-stu-id="43305-121">*dbid*</span></span>

<span data-ttu-id="43305-122">Base de données qui sera défragmentée.</span><span class="sxs-lookup"><span data-stu-id="43305-122">The database that will be defragmented.</span></span>

<span data-ttu-id="43305-123">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="43305-123">*szTableName*</span></span>

<span data-ttu-id="43305-124">Paramètre inutilisé.</span><span class="sxs-lookup"><span data-stu-id="43305-124">Unused parameter.</span></span> <span data-ttu-id="43305-125">La défragmentation est effectuée pour l’ensemble de la base de données décrite par l’ID de base de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="43305-125">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="43305-126">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="43305-126">*pcPasses*</span></span>

<span data-ttu-id="43305-127">Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre d’entrée définit le nombre maximal de passes de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="43305-127">When starting an online defragmentation task, this input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="43305-128">Lors de l’arrêt d’une tâche de défragmentation en ligne, cette mémoire tampon de sortie est définie sur le nombre de passes effectuées.</span><span class="sxs-lookup"><span data-stu-id="43305-128">When stopping an online defragmentation task, this output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="43305-129">Lorsque ce paramètre a la valeur NULL, le nombre de passes de défragmentation en ligne est illimité.</span><span class="sxs-lookup"><span data-stu-id="43305-129">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="43305-130">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="43305-130">*pcSeconds*</span></span>

<span data-ttu-id="43305-131">Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre d’entrée définit la durée maximale de la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="43305-131">When starting an online defragmentation task, this input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="43305-132">Lors de l’arrêt d’une tâche de défragmentation en ligne, cette mémoire tampon de sortie est définie sur la durée utilisée pour la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="43305-132">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="43305-133">Lorsque ce paramètre est défini sur NULL ou si *pcSeconds* pointe vers une valeur négative, la durée maximale de la défragmentation est illimitée.</span><span class="sxs-lookup"><span data-stu-id="43305-133">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="43305-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="43305-134">*grbit*</span></span>

<span data-ttu-id="43305-135">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="43305-135">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43305-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="43305-136">Value</span></span></p></th>
<th><p><span data-ttu-id="43305-137">Signification</span><span class="sxs-lookup"><span data-stu-id="43305-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43305-138">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="43305-138">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="43305-139">Défragmente la partie d’espace disponible de l’allocation de l’espace de la base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="43305-139">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="43305-140">L’espace de la base de données est divisé en deux types, l’espace détenu et l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="43305-140">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="43305-141">L’espace détenu est alloué à une table ou à un index, alors que l’espace disponible est prêt à être utilisé dans la table ou l’index, respectivement.</span><span class="sxs-lookup"><span data-stu-id="43305-141">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="43305-142">L’espace disponible est bien plus dynamique dans le comportement et nécessite une défragmentation en ligne plus qu’un espace détenu ou des données de table ou d’index.</span><span class="sxs-lookup"><span data-stu-id="43305-142">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-143">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="43305-143">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="43305-144">Démarre une nouvelle tâche de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="43305-144">Starts a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43305-145">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="43305-145">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="43305-146">Arrête une tâche de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="43305-146">Stops a defragmentation task.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="43305-147">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="43305-147">Return Value</span></span>

<span data-ttu-id="43305-148">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="43305-148">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="43305-149">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="43305-149">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43305-150">Code de retour</span><span class="sxs-lookup"><span data-stu-id="43305-150">Return code</span></span></p></th>
<th><p><span data-ttu-id="43305-151">Description</span><span class="sxs-lookup"><span data-stu-id="43305-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43305-152">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="43305-152">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="43305-153">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="43305-153">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-154">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="43305-154">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="43305-155">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="43305-155">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43305-156">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="43305-156">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="43305-157">La base de données choisie pour la défragmentation est en lecture seule et ne peut pas être mise à jour de quelque façon que ce soit, y compris la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="43305-157">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="43305-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="43305-159">La session donnée est dans l’état préparé pour valider et ne peut pas commencer les nouvelles mises à jour tant que la transaction en cours n’est pas validée ou annulée.</span><span class="sxs-lookup"><span data-stu-id="43305-159">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43305-160">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="43305-160">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="43305-161">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="43305-161">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="43305-162">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="43305-162">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-163">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="43305-163">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="43305-164">L’ID de base de données spécifié ne correspond pas à une base de données connue dans l’instance.</span><span class="sxs-lookup"><span data-stu-id="43305-164">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43305-165">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="43305-165">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="43305-166">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="43305-166">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="43305-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="43305-168">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="43305-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43305-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="43305-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="43305-170">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="43305-170">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="43305-171">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="43305-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="43305-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="43305-173">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="43305-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43305-174">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="43305-174">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="43305-175">La session donnée a uniquement des privilèges en lecture seule et ne peut pas démarrer une tâche qui peut effectuer une mise à jour, y compris une défragmentation.</span><span class="sxs-lookup"><span data-stu-id="43305-175">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-176">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="43305-176">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="43305-177">Cette erreur se produit lorsque la taille de la Banque des versions configurée est insuffisante pour contenir toutes les mises à jour en suspens.</span><span class="sxs-lookup"><span data-stu-id="43305-177">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43305-178">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="43305-178">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="43305-179">L’option JET_bitDefragmentBatchStart a été passée, mais une tâche de défragmentation exécute déjà la défragmentation sur la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="43305-179">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-180">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="43305-180">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="43305-181">L’option JET_bitDefragmentBatchStop a été passée, mais aucune tâche de défragmentation n’est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="43305-181">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43305-182">En cas de réussite, l’action demandée de démarrage d’une tâche de défragmentation pour des données données avec les options spécifiées est effectuée, ou l’action d’arrêt d’une tâche de défragmentation existante est effectuée.</span><span class="sxs-lookup"><span data-stu-id="43305-182">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="43305-183">En cas d’échec, l’action demandée de démarrage ou d’arrêt d’un travail de défragmentation en ligne n’est pas effectuée.</span><span class="sxs-lookup"><span data-stu-id="43305-183">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="43305-184">Aucun autre effet secondaire ne se produit.</span><span class="sxs-lookup"><span data-stu-id="43305-184">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="43305-185">Notes</span><span class="sxs-lookup"><span data-stu-id="43305-185">Remarks</span></span>

<span data-ttu-id="43305-186">La défragmentation en ligne est contrôlée à la fois par un paramètre, ainsi que par cette API.</span><span class="sxs-lookup"><span data-stu-id="43305-186">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="43305-187">La valeur par défaut du paramètre système est JET_OnlineDefragAll, ce qui signifie que la défragmentation est activée pour toutes les structures de données prises en charge.</span><span class="sxs-lookup"><span data-stu-id="43305-187">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="43305-188">Toutefois, à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md), il est possible de désactiver la défragmentation en ligne ou de l’activer de manière sélective pour les arborescences d’espace de base de données uniquement, les bases de données uniquement, les fichiers de streaming uniquement ou une combinaison de ces options.</span><span class="sxs-lookup"><span data-stu-id="43305-188">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="43305-189">Si le paramètre système de la défragmentation en ligne est défini sur un paramètre obsolète, **JetDefragment** traite le paramètre comme JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="43305-189">If the system setting for online defragmentation is set to an obsolete setting, **JetDefragment** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="43305-190">Il peut y avoir au plus une tâche en cours d’exécution pour chaque base de données.</span><span class="sxs-lookup"><span data-stu-id="43305-190">There can at most be one task running for each database.</span></span> <span data-ttu-id="43305-191">La tâche s’exécute en tant que thread dans le processus hébergeant le moteur ESE.</span><span class="sxs-lookup"><span data-stu-id="43305-191">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="43305-192">La session utilisée pour démarrer la tâche de défragmentation en ligne peut être utilisée par la suite pour les opérations de base de données pendant que la tâche de défragmentation se poursuit, car la tâche de défragmentation alloue sa propre session.</span><span class="sxs-lookup"><span data-stu-id="43305-192">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="43305-193">La session donnée est utilisée uniquement pour vérifier les autorisations associées à la session de démarrage de la tâche et n’est pas réellement utilisée pour les opérations de défragmentation elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="43305-193">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="43305-194">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43305-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43305-195"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="43305-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="43305-196">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="43305-196">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-197"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="43305-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="43305-198">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="43305-198">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43305-199"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="43305-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="43305-200">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="43305-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-201"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="43305-201"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="43305-202">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="43305-202">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43305-203"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="43305-203"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="43305-204">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="43305-204">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43305-205"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="43305-205"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="43305-206">Implémenté en tant que <strong>JetDefragmentW</strong> (Unicode) et <strong>JetDefragmentA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="43305-206">Implemented as <strong>JetDefragmentW</strong> (Unicode) and <strong>JetDefragmentA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="43305-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43305-207">See Also</span></span>

[<span data-ttu-id="43305-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="43305-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="43305-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="43305-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="43305-210">JetCompact</span><span class="sxs-lookup"><span data-stu-id="43305-210">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="43305-211">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="43305-211">JetDefragment2</span></span>](./jetdefragment2-function.md)  
[<span data-ttu-id="43305-212">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="43305-212">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="43305-213">JetStopService</span><span class="sxs-lookup"><span data-stu-id="43305-213">JetStopService</span></span>](./jetstopservice-function.md)

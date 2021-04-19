---
description: 'En savoir plus sur : fonction JetDefragment2'
title: JetDefragment2 fonction)
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8064ae996831f61869d74ff1fd7c0f2222257b85
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106538366"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="3ef7f-103">JetDefragment2 fonction)</span><span class="sxs-lookup"><span data-stu-id="3ef7f-103">JetDefragment2 Function</span></span>


<span data-ttu-id="3ef7f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="3ef7f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="3ef7f-105">JetDefragment2 fonction)</span><span class="sxs-lookup"><span data-stu-id="3ef7f-105">JetDefragment2 Function</span></span>

<span data-ttu-id="3ef7f-106">La fonction **JetDefragment2** démarre et arrête les tâches de défragmentation de base de données qui améliorent l’Organisation des données dans une base de données, avec un paramètre de rappel disponible pour signaler la progression de la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="3ef7f-107">Cela permet de limiter la croissance de la base de données en utilisant l’allocation de disque existante plus efficacement dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="3ef7f-108">Elle peut également réduire la plage de travail en garantissant un compactage plus étroit des données.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="3ef7f-109">Enfin, il peut améliorer les performances des applications en accélérant les opérations courantes via une meilleure organisation des données.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="3ef7f-110">**Windows XP :**  **JetDefragment2** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="3ef7f-111">**JetDefragment2** contient également un paramètre de fonction de rappel utilisé pour signaler la progression du processus de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="3ef7f-112">La défragmentation de base de données est une opération en ligne et n’interrompt pas l’activité normale de la base de données, comme les opérations de requête ou les mises à jour des données.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="3ef7f-113">**JetDefragment2** ne fait pas non plus de copie de toutes les données existantes.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="3ef7f-114">Au lieu de cela, elle défragmente une base de données sur place.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="3ef7f-115">Enfin, **JetDefragment2** récupère l’espace de la base de données interne en vue de sa réutilisation, mais ne libère pas d’espace supplémentaire dans le système de fichiers du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="3ef7f-116">Le format des données résultant peut être bien plus efficace, mais n’est généralement pas optimal.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="3ef7f-117">La défragmentation est limitée à la libération des pages de base de données à réutiliser qui contiennent des données qui ont déjà été logiquement supprimées.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="3ef7f-118">La défragmentation rend également les pages de base de données disponibles pour une réutilisation dans certains cas en combinant les données de deux pages quand elles peuvent tenir sur une seule page.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="3ef7f-119">Cette opération est différente de [JetCompact](./jetcompact-function.md) qui fait une copie d’une base de données en lecture seule dans un format très optimal.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="3ef7f-120">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ef7f-120">Parameters</span></span>

<span data-ttu-id="3ef7f-121">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3ef7f-121">*sesid*</span></span>

<span data-ttu-id="3ef7f-122">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-122">The session to use for this call.</span></span>

<span data-ttu-id="3ef7f-123">*dbid*</span><span class="sxs-lookup"><span data-stu-id="3ef7f-123">*dbid*</span></span>

<span data-ttu-id="3ef7f-124">Base de données à défragmenter.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-124">The database to defragment.</span></span>

<span data-ttu-id="3ef7f-125">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="3ef7f-125">*szTableName*</span></span>

<span data-ttu-id="3ef7f-126">Paramètre inutilisé.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-126">Unused parameter.</span></span> <span data-ttu-id="3ef7f-127">La défragmentation est effectuée pour l’ensemble de la base de données décrite par l’ID de base de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-127">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="3ef7f-128">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="3ef7f-128">*pcPasses*</span></span>

<span data-ttu-id="3ef7f-129">Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre d’entrée facultatif définit le nombre maximal de passes de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-129">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="3ef7f-130">Lors de l’arrêt d’une tâche de défragmentation en ligne, cette mémoire tampon de sortie facultative est définie sur le nombre de passes effectuées.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-130">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="3ef7f-131">Lorsque ce paramètre a la valeur NULL, le nombre de passes de défragmentation en ligne est illimité.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-131">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="3ef7f-132">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="3ef7f-132">*pcSeconds*</span></span>

<span data-ttu-id="3ef7f-133">Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre d’entrée facultatif définit la durée maximale de la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-133">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="3ef7f-134">Lors de l’arrêt d’une tâche de défragmentation en ligne, cette mémoire tampon de sortie facultative est définie sur la durée utilisée pour la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-134">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="3ef7f-135">Lorsque ce paramètre est défini sur NULL ou si *pcSeconds* pointe vers une valeur négative, la durée maximale de la défragmentation est illimitée.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-135">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="3ef7f-136">*rappel*</span><span class="sxs-lookup"><span data-stu-id="3ef7f-136">*callback*</span></span>

<span data-ttu-id="3ef7f-137">Fonction de rappel que la défragmentation appelle régulièrement pour signaler la progression.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-137">Callback function that defragmentation calls regularly to report progress.</span></span>

<span data-ttu-id="3ef7f-138">*grbit*</span><span class="sxs-lookup"><span data-stu-id="3ef7f-138">*grbit*</span></span>

<span data-ttu-id="3ef7f-139">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-139">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ef7f-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ef7f-140">Value</span></span></p></th>
<th><p><span data-ttu-id="3ef7f-141">Signification</span><span class="sxs-lookup"><span data-stu-id="3ef7f-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-142">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="3ef7f-142">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-143">Cette option est utilisée pour défragmenter la partie espace disponible de l’allocation de l’espace de la base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-143">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="3ef7f-144">L’espace de la base de données est divisé en deux types, l’espace détenu et l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-144">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="3ef7f-145">L’espace détenu est alloué à une table ou à un index, alors que l’espace disponible est prêt à être utilisé dans la table ou l’index, respectivement.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-145">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="3ef7f-146">L’espace disponible est bien plus dynamique dans le comportement et nécessite une défragmentation en ligne plus qu’un espace détenu ou des données de table ou d’index.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-146">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-147">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="3ef7f-147">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-148">Cette option permet de démarrer une nouvelle tâche de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-148">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-149">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="3ef7f-149">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-150">Cette option est utilisée pour arrêter une tâche de défragmentation démarrée existante.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-150">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-151">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="3ef7f-151">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-152">Cette option est utilisée pour défragmenter une arborescence binaire (B-Tree).</span><span class="sxs-lookup"><span data-stu-id="3ef7f-152">This option is used to defrag a B-Tree.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3ef7f-153">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3ef7f-153">Return Value</span></span>

<span data-ttu-id="3ef7f-154">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-154">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3ef7f-155">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3ef7f-155">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ef7f-156">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3ef7f-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="3ef7f-157">Description</span><span class="sxs-lookup"><span data-stu-id="3ef7f-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3ef7f-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-159">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-159">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-160">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3ef7f-160">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-161">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-161">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-162">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="3ef7f-162">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-163">La base de données choisie pour la défragmentation est en lecture seule et ne peut pas être mise à jour de quelque façon que ce soit, y compris la défragmentation.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-163">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="3ef7f-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-165">La session donnée est dans l’état préparé pour valider et ne peut pas commencer les nouvelles mises à jour tant que la transaction en cours n’est pas validée ou annulée.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-165">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-166">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3ef7f-166">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-167">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-167">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="3ef7f-168">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-169">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="3ef7f-169">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-170">L’ID de base de données spécifié ne correspond pas à une base de données connue dans l’instance.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-170">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-171">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3ef7f-171">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-172">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-172">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3ef7f-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-174">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-175">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="3ef7f-175">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-176">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-176">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="3ef7f-177">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-177">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-178">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3ef7f-178">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-179">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-179">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-180">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="3ef7f-180">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-181">La session donnée a uniquement des privilèges en lecture seule et ne peut pas démarrer une tâche qui peut effectuer une mise à jour, y compris une défragmentation.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-181">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-182">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="3ef7f-182">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-183">Cette erreur se produit lorsque la taille de la Banque des versions configurée est insuffisante pour contenir toutes les mises à jour en suspens.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-183">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-184">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="3ef7f-184">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-185">L’option JET_bitDefragmentBatchStart a été passée, mais une tâche de défragmentation exécute déjà la défragmentation sur la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-185">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-186">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="3ef7f-186">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="3ef7f-187">L’option JET_bitDefragmentBatchStop a été passée, mais aucune tâche de défragmentation n’est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-187">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ef7f-188">En cas de réussite, l’action demandée de démarrage d’une tâche de défragmentation pour des données données avec les options spécifiées est effectuée, ou l’action d’arrêt d’une tâche de défragmentation existante est effectuée.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-188">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="3ef7f-189">En cas d’échec, l’action demandée de démarrage ou d’arrêt d’un travail de défragmentation en ligne n’est pas effectuée.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-189">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="3ef7f-190">Aucun autre effet secondaire ne se produit.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-190">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3ef7f-191">Notes</span><span class="sxs-lookup"><span data-stu-id="3ef7f-191">Remarks</span></span>

<span data-ttu-id="3ef7f-192">La défragmentation en ligne est contrôlée à la fois par un paramètre, ainsi que par cette API.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-192">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="3ef7f-193">La valeur par défaut du paramètre système est JET_OnlineDefragAll, ce qui signifie que la défragmentation est activée pour toutes les structures de données prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-193">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="3ef7f-194">Toutefois, à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md), il est possible de désactiver la défragmentation en ligne ou de l’activer de manière sélective pour les arborescences d’espace de base de données uniquement, les bases de données uniquement, les fichiers de streaming uniquement ou une combinaison de ces options.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-194">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="3ef7f-195">Si le paramètre système pour la défragmentation en ligne est un paramètre obsolète, **JetDefragment2** traite le paramètre comme JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-195">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="3ef7f-196">Il peut y avoir au plus une tâche en cours d’exécution pour chaque base de données.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-196">There can at most be one task running for each database.</span></span> <span data-ttu-id="3ef7f-197">La tâche s’exécute en tant que thread dans le processus hébergeant le moteur ESE.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-197">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="3ef7f-198">La session utilisée pour démarrer la tâche de défragmentation en ligne peut être utilisée par la suite pour les opérations de base de données pendant que la tâche de défragmentation se poursuit, car la tâche de défragmentation alloue sa propre session.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-198">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="3ef7f-199">La session donnée est utilisée uniquement pour vérifier les autorisations associées à la session de démarrage de la tâche et n’est pas réellement utilisée pour les opérations de défragmentation elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-199">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3ef7f-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ef7f-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3ef7f-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3ef7f-202">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-202">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-203"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="3ef7f-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3ef7f-204">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-204">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-205"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="3ef7f-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3ef7f-206">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-207"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="3ef7f-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3ef7f-208">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ef7f-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3ef7f-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3ef7f-210">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3ef7f-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ef7f-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3ef7f-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3ef7f-212">Implémenté en tant que <strong>JetDefragment2W</strong> (Unicode) et <strong>JetDefragment2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3ef7f-212">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3ef7f-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ef7f-213">See Also</span></span>

[<span data-ttu-id="3ef7f-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3ef7f-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3ef7f-215">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3ef7f-215">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3ef7f-216">JetCompact</span><span class="sxs-lookup"><span data-stu-id="3ef7f-216">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="3ef7f-217">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="3ef7f-217">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="3ef7f-218">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="3ef7f-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="3ef7f-219">JetStopService</span><span class="sxs-lookup"><span data-stu-id="3ef7f-219">JetStopService</span></span>](./jetstopservice-function.md)

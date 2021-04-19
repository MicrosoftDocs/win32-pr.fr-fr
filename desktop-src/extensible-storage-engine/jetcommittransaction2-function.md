---
description: 'En savoir plus sur : fonction JetCommitTransaction2'
title: JetCommitTransaction2 fonction)
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24dfecd091de027f51ed8f69c0441fbc7cbd57af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535591"
---
# <a name="jetcommittransaction2-function"></a><span data-ttu-id="6cf8d-103">JetCommitTransaction2 fonction)</span><span class="sxs-lookup"><span data-stu-id="6cf8d-103">JetCommitTransaction2 Function</span></span>


<span data-ttu-id="6cf8d-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="6cf8d-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="6cf8d-105">La fonction **JetCommitTransaction2** valide les modifications apportées à l’état de la base de données pendant le point d’enregistrement en cours et les migre vers le point d’enregistrement précédent.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-105">The **JetCommitTransaction2** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="6cf8d-106">Si le point d’enregistrement le plus à l’extérieur est validé, les modifications apportées pendant ce point d’enregistrement sont validées à l’état de la base de données et la session quitte la transaction.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-106">If the outermost save point is committed, the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="6cf8d-107">La fonction **JetCommitTransaction2** a été introduite dans le système d’exploitation Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-107">The **JetCommitTransaction2** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a><span data-ttu-id="6cf8d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cf8d-108">Parameters</span></span>

<span data-ttu-id="6cf8d-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6cf8d-109">*sesid*</span></span>

<span data-ttu-id="6cf8d-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-110">The session to use for this call.</span></span>

<span data-ttu-id="6cf8d-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6cf8d-111">*grbit*</span></span>

<span data-ttu-id="6cf8d-112">Groupe de bits qui spécifient zéro, une ou plusieurs des valeurs énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-112">A group of bits that specify zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cf8d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cf8d-113">Value</span></span></p></th>
<th><p><span data-ttu-id="6cf8d-114">Signification</span><span class="sxs-lookup"><span data-stu-id="6cf8d-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cf8d-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="6cf8d-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-116">La transaction est validée normalement, mais cette API n’attend pas que la transaction soit vidée dans le fichier journal des transactions avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="6cf8d-117">Cela réduit considérablement la durée d’une opération de validation au détriment de la durabilité.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="6cf8d-118">Toute transaction qui n’est pas vidée dans le journal avant un incident est automatiquement abandonnée lors de la récupération après incident lors du prochain appel à la fonction <a href="gg294068(v=exchg.10).md">JetInit</a> .</span><span class="sxs-lookup"><span data-stu-id="6cf8d-118">Any transaction that is not flushed to the log before a crash will automatically be aborted during crash recovery during the next call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function.</span></span></p>
<p><span data-ttu-id="6cf8d-119">Si JET_bitWaitLastLevel0Commit ou JET_bitWaitAllLevel0Commit sont spécifiés, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="6cf8d-120">Si cet appel à <strong>JetCommitTransaction2</strong> ne correspond pas au premier appel à la fonction <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> pour cette session, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-120">If this call to <strong>JetCommitTransaction2</strong> does not match the first call to the <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> function for this session, this option is ignored.</span></span> <span data-ttu-id="6cf8d-121">Cela est dû au fait que la dernière action qui se produit sur le point d’enregistrement le plus à l’extérieur est le facteur déterminant si l’intégralité de la transaction est réellement validée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf8d-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="6cf8d-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-123">Toutes les transactions précédemment validées par une session qui n’ont pas encore été vidées dans le fichier journal des transactions seront vidées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="6cf8d-124">Cette API attend que les transactions aient été vidées avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="6cf8d-125">Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="6cf8d-126">Cette option ne peut pas être utilisée conjointement avec une autre option.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="6cf8d-127">Cette option est disponible dans les versions du système d’exploitation Windows Server à partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-127">This option is available in versions of the Windows Server operating system starting with Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf8d-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="6cf8d-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-129">Si la session a précédemment validé des transactions et qu’elles n’ont pas encore été vidées dans le fichier journal des transactions, elles doivent être vidées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="6cf8d-130">Cette API attend que les transactions aient été vidées avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="6cf8d-131">Cela est utile si l’application a précédemment validé plusieurs transactions à l’aide de JET_bitCommitLazyFlush et souhaite maintenant les vider sur le disque.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="6cf8d-132">Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="6cf8d-133">Cette option ne peut pas être utilisée conjointement avec une autre option.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6cf8d-134">*cmsecDurableCommit*</span><span class="sxs-lookup"><span data-stu-id="6cf8d-134">*cmsecDurableCommit*</span></span>

<span data-ttu-id="6cf8d-135">Durée de validation d’une transaction paresseuse.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-135">The duration to commit a lazy transaction.</span></span>

<span data-ttu-id="6cf8d-136">*pCommitID*</span><span class="sxs-lookup"><span data-stu-id="6cf8d-136">*pCommitID*</span></span>

<span data-ttu-id="6cf8d-137">ID de validation associé à cet enregistrement de validation.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-137">The Commit-ID associated with this commit record.</span></span>

### <a name="return-value"></a><span data-ttu-id="6cf8d-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cf8d-138">Return value</span></span>

<span data-ttu-id="6cf8d-139">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-139">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="6cf8d-140">Pour plus d’informations sur les erreurs ESE (Extensible Storage Engine) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6cf8d-140">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cf8d-141">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6cf8d-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="6cf8d-142">Description</span><span class="sxs-lookup"><span data-stu-id="6cf8d-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cf8d-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6cf8d-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-144">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf8d-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6cf8d-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-146">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a cessé à la suite d’un appel à la fonction <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="6cf8d-146">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf8d-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6cf8d-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-148">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="6cf8d-149">Cette erreur est renvoyée uniquement par les versions du système d’exploitation Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-149">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf8d-150">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="6cf8d-150">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-151">L’une des options demandées n’est pas valide ou n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-151">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="6cf8d-152">Cette erreur est retournée par la fonction <strong>JetCommitTransaction2</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="6cf8d-152">This error will be returned by the <strong>JetCommitTransaction2</strong> function when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="6cf8d-153">Un <em>Grbit</em> illégal est spécifié.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-153">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="6cf8d-154">JET_bitWaitLastLevel0Commit a été spécifié en combinaison avec un autre <em>Grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-154">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="6cf8d-155">JET_bitWaitAllLevel0Commit a été spécifié en combinaison avec un autre <em>Grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-155">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf8d-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6cf8d-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-157">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf8d-158">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="6cf8d-158">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-159">L’opération a échoué, car la session spécifiée n’est pas dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-159">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf8d-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6cf8d-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-161">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf8d-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6cf8d-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-163">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-163">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="6cf8d-164">Cette erreur est renvoyée uniquement par les versions du système d’exploitation Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-164">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf8d-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6cf8d-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6cf8d-166">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6cf8d-167">En cas de réussite, toute modification apportée à la base de données pendant le point d’enregistrement actuel pour la session donnée est validée et le point d’enregistrement est terminé.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-167">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="6cf8d-168">Si le dernier point d’enregistrement de la session est terminé, la transaction est éventuellement vidée dans le fichier journal des transactions et la session quitte la transaction.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-168">If the last save point for the session was ended, the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="6cf8d-169">En cas d’échec, l’état transactionnel de la session reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-169">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="6cf8d-170">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-170">No change to the database state will occur.</span></span> <span data-ttu-id="6cf8d-171">L’application doit appeler la fonction [JetRollback](./jetrollback-function.md) pour abandonner la transaction.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-171">The application should call the [JetRollback](./jetrollback-function.md) function to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6cf8d-172">Notes</span><span class="sxs-lookup"><span data-stu-id="6cf8d-172">Remarks</span></span>

<span data-ttu-id="6cf8d-173">Il doit y avoir un appel à **JetCommitTransaction2** ou [JetRollback](./jetrollback-function.md) pour qu’il corresponde à chaque appel à [JetBeginTransaction](./jetbegintransaction-function.md) pour une session donnée.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-173">There must be one call to **JetCommitTransaction2** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6cf8d-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cf8d-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cf8d-175"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6cf8d-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6cf8d-176">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-176">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf8d-177"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="6cf8d-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6cf8d-178">Requiert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-178">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf8d-179"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="6cf8d-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6cf8d-180">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cf8d-181"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="6cf8d-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6cf8d-182">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cf8d-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6cf8d-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6cf8d-184">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6cf8d-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6cf8d-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cf8d-185">See also</span></span>

[<span data-ttu-id="6cf8d-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6cf8d-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6cf8d-187">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6cf8d-187">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6cf8d-188">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6cf8d-188">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6cf8d-189">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="6cf8d-189">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="6cf8d-190">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="6cf8d-190">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="6cf8d-191">JetRollback</span><span class="sxs-lookup"><span data-stu-id="6cf8d-191">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="6cf8d-192">JetStopService</span><span class="sxs-lookup"><span data-stu-id="6cf8d-192">JetStopService</span></span>](./jetstopservice-function.md)

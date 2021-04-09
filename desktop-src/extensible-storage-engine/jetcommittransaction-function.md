---
description: 'En savoir plus sur : fonction JetCommitTransaction'
title: Fonction JetCommitTransaction
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2fe42891aa916a428d63fb68c99f42f38e78993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952929"
---
# <a name="jetcommittransaction-function"></a><span data-ttu-id="9ca12-103">Fonction JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="9ca12-103">JetCommitTransaction Function</span></span>


<span data-ttu-id="9ca12-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="9ca12-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcommittransaction-function"></a><span data-ttu-id="9ca12-105">Fonction JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="9ca12-105">JetCommitTransaction Function</span></span>

<span data-ttu-id="9ca12-106">La fonction **JetCommitTransaction** valide les modifications apportées à l’état de la base de données pendant le point d’enregistrement en cours et les migre vers le point d’enregistrement précédent.</span><span class="sxs-lookup"><span data-stu-id="9ca12-106">The **JetCommitTransaction** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="9ca12-107">Si le point d’enregistrement le plus à l’extérieur est validé, les modifications apportées pendant ce point d’enregistrement sont validées à l’état de la base de données et la session quitte la transaction.</span><span class="sxs-lookup"><span data-stu-id="9ca12-107">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="9ca12-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ca12-108">Parameters</span></span>

<span data-ttu-id="9ca12-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9ca12-109">*sesid*</span></span>

<span data-ttu-id="9ca12-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="9ca12-110">The session to use for this call.</span></span>

<span data-ttu-id="9ca12-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9ca12-111">*grbit*</span></span>

<span data-ttu-id="9ca12-112">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="9ca12-112">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ca12-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ca12-113">Value</span></span></p></th>
<th><p><span data-ttu-id="9ca12-114">Signification</span><span class="sxs-lookup"><span data-stu-id="9ca12-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ca12-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="9ca12-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="9ca12-116">La transaction est validée normalement, mais cette API n’attend pas que la transaction soit vidée dans le fichier journal des transactions avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9ca12-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="9ca12-117">Cela réduit considérablement la durée d’une opération de validation au détriment de la durabilité.</span><span class="sxs-lookup"><span data-stu-id="9ca12-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="9ca12-118">Toute transaction qui n’est pas vidée dans le journal avant un incident est automatiquement abandonnée lors de la récupération après incident lors du prochain appel à <a href="gg294068(v=exchg.10).md">JetInit</a>.</span><span class="sxs-lookup"><span data-stu-id="9ca12-118">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to <a href="gg294068(v=exchg.10).md">JetInit</a>.</span></span></p>
<p><span data-ttu-id="9ca12-119">Si JET_bitWaitLastLevel0Commit ou JET_bitWaitAllLevel0Commit sont spécifiés, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="9ca12-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="9ca12-120">Si cet appel à <strong>JetCommitTransaction</strong> ne correspond pas au premier appel à <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> pour cette session, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="9ca12-120">If this call to <strong>JetCommitTransaction</strong> does not match the first call to <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> for this session, this option is ignored.</span></span> <span data-ttu-id="9ca12-121">Cela est dû au fait que la dernière action qui se produit sur le point d’enregistrement le plus à l’extérieur est le facteur déterminant si l’intégralité de la transaction est réellement validée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="9ca12-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca12-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="9ca12-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="9ca12-123">Toutes les transactions précédemment validées par une session qui n’ont pas encore été vidées dans le fichier journal des transactions seront vidées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="9ca12-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="9ca12-124">Cette API attend que les transactions aient été vidées avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9ca12-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="9ca12-125">Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="9ca12-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="9ca12-126">Cette option ne peut pas être utilisée conjointement avec une autre option.</span><span class="sxs-lookup"><span data-stu-id="9ca12-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="9ca12-127">Cette option est disponible uniquement à partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9ca12-127">This option is only available as of Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca12-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="9ca12-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="9ca12-129">Si la session a précédemment validé des transactions et qu’elles n’ont pas encore été vidées dans le fichier journal des transactions, elles doivent être vidées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="9ca12-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="9ca12-130">Cette API attend que les transactions aient été vidées avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9ca12-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="9ca12-131">Cela est utile si l’application a précédemment validé plusieurs transactions à l’aide de JET_bitCommitLazyFlush et souhaite maintenant les vider sur le disque.</span><span class="sxs-lookup"><span data-stu-id="9ca12-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="9ca12-132">Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="9ca12-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="9ca12-133">Cette option ne peut pas être utilisée conjointement avec une autre option.</span><span class="sxs-lookup"><span data-stu-id="9ca12-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9ca12-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ca12-134">Return Value</span></span>

<span data-ttu-id="9ca12-135">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="9ca12-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9ca12-136">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9ca12-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ca12-137">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9ca12-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="9ca12-138">Description</span><span class="sxs-lookup"><span data-stu-id="9ca12-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ca12-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9ca12-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9ca12-140">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="9ca12-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca12-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9ca12-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9ca12-142">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9ca12-142">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca12-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9ca12-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9ca12-144">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="9ca12-144">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9ca12-145">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9ca12-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca12-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="9ca12-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="9ca12-147">L’une des options demandées n’est pas valide ou n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9ca12-147">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="9ca12-148">Cette erreur est retournée par <strong>JetCommitTransaction</strong> quand :</span><span class="sxs-lookup"><span data-stu-id="9ca12-148">This error will be returned by <strong>JetCommitTransaction</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="9ca12-149">Un <em>Grbit</em> illégal est spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ca12-149">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="9ca12-150">JET_bitWaitLastLevel0Commit a été spécifié en combinaison avec un autre <em>Grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="9ca12-150">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="9ca12-151">JET_bitWaitAllLevel0Commit a été spécifié en combinaison avec un autre <em>Grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="9ca12-151">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca12-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9ca12-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9ca12-153">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="9ca12-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca12-154">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="9ca12-154">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="9ca12-155">L’opération a échoué, car la session spécifiée n’est pas dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="9ca12-155">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca12-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9ca12-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9ca12-157">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="9ca12-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca12-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9ca12-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9ca12-159">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="9ca12-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="9ca12-160">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9ca12-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca12-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9ca12-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9ca12-162">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="9ca12-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9ca12-163">En cas de réussite, toute modification apportée à la base de données pendant le point d’enregistrement actuel pour la session donnée est validée et le point d’enregistrement est terminé.</span><span class="sxs-lookup"><span data-stu-id="9ca12-163">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="9ca12-164">Si le dernier point d’enregistrement de la session a été interrompu, la transaction est éventuellement vidée dans le fichier journal des transactions et la session quitte la transaction.</span><span class="sxs-lookup"><span data-stu-id="9ca12-164">If the last save point for the session was ended then the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="9ca12-165">En cas d’échec, l’état transactionnel de la session reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="9ca12-165">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="9ca12-166">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="9ca12-166">No change to the database state will occur.</span></span> <span data-ttu-id="9ca12-167">L’application doit appeler [JetRollback](./jetrollback-function.md) pour abandonner la transaction.</span><span class="sxs-lookup"><span data-stu-id="9ca12-167">The application should call [JetRollback](./jetrollback-function.md) to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9ca12-168">Notes</span><span class="sxs-lookup"><span data-stu-id="9ca12-168">Remarks</span></span>

<span data-ttu-id="9ca12-169">Il doit y avoir un appel à **JetCommitTransaction** ou [JetRollback](./jetrollback-function.md) pour qu’il corresponde à chaque appel à [JetBeginTransaction](./jetbegintransaction-function.md) pour une session donnée.</span><span class="sxs-lookup"><span data-stu-id="9ca12-169">There must be one call to **JetCommitTransaction** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9ca12-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ca12-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ca12-171"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9ca12-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9ca12-172">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="9ca12-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca12-173"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="9ca12-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9ca12-174">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9ca12-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca12-175"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="9ca12-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9ca12-176">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="9ca12-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca12-177"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="9ca12-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9ca12-178">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9ca12-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca12-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9ca12-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9ca12-180">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9ca12-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9ca12-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ca12-181">See Also</span></span>

[<span data-ttu-id="9ca12-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9ca12-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9ca12-183">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9ca12-183">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9ca12-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9ca12-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9ca12-185">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="9ca12-185">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="9ca12-186">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="9ca12-186">JetCommitTransaction</span></span>]()  
[<span data-ttu-id="9ca12-187">JetRollback</span><span class="sxs-lookup"><span data-stu-id="9ca12-187">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="9ca12-188">JetStopService</span><span class="sxs-lookup"><span data-stu-id="9ca12-188">JetStopService</span></span>](./jetstopservice-function.md)

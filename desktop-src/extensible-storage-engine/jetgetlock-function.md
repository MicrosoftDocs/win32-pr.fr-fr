---
description: 'En savoir plus sur : fonction JetGetLock'
title: JetGetLock fonction)
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104116318"
---
# <a name="jetgetlock-function"></a><span data-ttu-id="0b037-103">JetGetLock fonction)</span><span class="sxs-lookup"><span data-stu-id="0b037-103">JetGetLock Function</span></span>


<span data-ttu-id="0b037-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="0b037-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetlock-function"></a><span data-ttu-id="0b037-105">JetGetLock fonction)</span><span class="sxs-lookup"><span data-stu-id="0b037-105">JetGetLock Function</span></span>

<span data-ttu-id="0b037-106">La fonction **JetGetLock** fournit un moyen de réserver explicitement la possibilité de mettre à jour une ligne, un verrou en écriture ou d’empêcher explicitement une ligne d’être mise à jour par une autre session, verrou de lecture.</span><span class="sxs-lookup"><span data-stu-id="0b037-106">The **JetGetLock** function provides a means to explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="0b037-107">Normalement, les verrous d’écriture de ligne sont acquis implicitement en raison de la mise à jour des lignes.</span><span class="sxs-lookup"><span data-stu-id="0b037-107">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="0b037-108">Les verrous de lecture ne sont généralement pas requis en raison du contrôle de version des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="0b037-108">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="0b037-109">Toutefois, dans certains cas, une transaction peut souhaiter verrouiller explicitement une ligne pour appliquer la sérialisation, ou pour s’assurer qu’une opération suivante réussira en vertu du fait que les verrous requis ont déjà été pris.</span><span class="sxs-lookup"><span data-stu-id="0b037-109">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed by virtue that required locks have already been taken.</span></span>

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="0b037-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b037-110">Parameters</span></span>

<span data-ttu-id="0b037-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="0b037-111">*sesid*</span></span>

<span data-ttu-id="0b037-112">Session qui sera utilisée pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="0b037-112">The session that will be used for this call.</span></span>

<span data-ttu-id="0b037-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="0b037-113">*tableid*</span></span>

<span data-ttu-id="0b037-114">Curseur qui sera utilisé pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="0b037-114">The cursor that will be used for this call.</span></span>

<span data-ttu-id="0b037-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="0b037-115">*grbit*</span></span>

<span data-ttu-id="0b037-116">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0b037-116">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b037-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b037-117">Value</span></span></p></th>
<th><p><span data-ttu-id="0b037-118">Signification</span><span class="sxs-lookup"><span data-stu-id="0b037-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b037-119">JET_bitReadLock</span><span class="sxs-lookup"><span data-stu-id="0b037-119">JET_bitReadLock</span></span></p></td>
<td><p><span data-ttu-id="0b037-120">Cet indicateur provoque l’acquisition d’un verrou de lecture sur l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="0b037-120">This flag causes a read lock to be acquired on the current record.</span></span> <span data-ttu-id="0b037-121">Les verrous de lecture sont incompatibles avec les verrous d’écriture déjà détenues par d’autres sessions, mais sont compatibles avec les verrous de lecture détenus par d’autres sessions.</span><span class="sxs-lookup"><span data-stu-id="0b037-121">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b037-122">JET_bitWriteLock</span><span class="sxs-lookup"><span data-stu-id="0b037-122">JET_bitWriteLock</span></span></p></td>
<td><p><span data-ttu-id="0b037-123">Cet indicateur provoque l’acquisition d’un verrou d’écriture sur l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="0b037-123">This flag causes a write lock to be acquired on the current record.</span></span> <span data-ttu-id="0b037-124">Les verrous d’écriture ne sont pas compatibles avec les verrous d’écriture ou de lecture détenus par d’autres sessions, mais sont compatibles avec les verrous de lecture détenus par la même session.</span><span class="sxs-lookup"><span data-stu-id="0b037-124">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0b037-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0b037-125">Return Value</span></span>

<span data-ttu-id="0b037-126">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="0b037-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0b037-127">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0b037-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b037-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0b037-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="0b037-129">Description</span><span class="sxs-lookup"><span data-stu-id="0b037-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b037-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0b037-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0b037-131">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0b037-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b037-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="0b037-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="0b037-133">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="0b037-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b037-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="0b037-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="0b037-135">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="0b037-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="0b037-136">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0b037-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b037-137">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="0b037-137">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="0b037-138">Le <em>Grbit</em> donné n’est ni JET_bitReadLock ni JET_bitWriteLock.</span><span class="sxs-lookup"><span data-stu-id="0b037-138">The given <em>grbit</em> is neither JET_bitReadLock or JET_bitWriteLock.</span></span> <span data-ttu-id="0b037-139">Il doit s’agir de l’un de ces deux indicateurs.</span><span class="sxs-lookup"><span data-stu-id="0b037-139">It must be one of these two flags.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b037-140">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="0b037-140">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="0b037-141">Le curseur doit se trouver sur un enregistrement pour pouvoir acquérir un verrou.</span><span class="sxs-lookup"><span data-stu-id="0b037-141">Cursor must be on a record in order to acquire a lock.</span></span> <span data-ttu-id="0b037-142">Les verrous sont des enregistrements Always on.</span><span class="sxs-lookup"><span data-stu-id="0b037-142">Locks are always on records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b037-143">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="0b037-143">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="0b037-144">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="0b037-144">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b037-145">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="0b037-145">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="0b037-146">Les verrous ne peuvent être obtenus que par les sessions dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="0b037-146">Locks can only be acquired by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b037-147">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="0b037-147">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="0b037-148">Le curseur ne peut pas être en lecture seule et acquérir un verrou en écriture.</span><span class="sxs-lookup"><span data-stu-id="0b037-148">Cursor cannot be read only and acquire a write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b037-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="0b037-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="0b037-150">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="0b037-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b037-151">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="0b037-151">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="0b037-152">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="0b037-152">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="0b037-153">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0b037-153">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b037-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="0b037-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="0b037-155">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="0b037-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b037-156">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="0b037-156">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="0b037-157">La session doit avoir des autorisations d’écriture pour acquérir un verrou d’écriture.</span><span class="sxs-lookup"><span data-stu-id="0b037-157">Session must have write permissions to acquire write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b037-158">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="0b037-158">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="0b037-159">L’erreur retournée lorsqu’un verrou en conflit est demandé.</span><span class="sxs-lookup"><span data-stu-id="0b037-159">The error returned when a conflicting lock is requested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b037-160">En cas de réussite, la session a acquis le verrou demandé.</span><span class="sxs-lookup"><span data-stu-id="0b037-160">On success, session has acquired requested lock.</span></span>

<span data-ttu-id="0b037-161">En cas d’échec, la session n’a pas acquis le verrou demandé.</span><span class="sxs-lookup"><span data-stu-id="0b037-161">On failure, session has not acquired requested lock.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0b037-162">Notes</span><span class="sxs-lookup"><span data-stu-id="0b037-162">Remarks</span></span>

<span data-ttu-id="0b037-163">Les verrous d’écriture ne peuvent pas être obtenus avec les sessions ou les curseurs qui ont des autorisations en lecture seule, même si la session et le curseur n’effectuent pas d’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0b037-163">Write locks cannot be acquired with sessions or cursors that have read-only permissions, even if the session and cursor ultimately do not perform an update operation.</span></span> <span data-ttu-id="0b037-164">La session et le curseur doivent tous deux avoir des privilèges d’écriture pour acquérir un verrou d’écriture.</span><span class="sxs-lookup"><span data-stu-id="0b037-164">Both the session and the cursor must have write privileges in order to acquire a write lock.</span></span>

<span data-ttu-id="0b037-165">Les verrous de lecture et d’écriture sont un moyen de verrouillage pessimiste.</span><span class="sxs-lookup"><span data-stu-id="0b037-165">Read and write locks are a means of pessimistic locking.</span></span> <span data-ttu-id="0b037-166">Le verrouillage pessimiste s’attend à ce que plusieurs sessions simultanées soient en conflit et acquièrent des verrous à l’avance pour s’assurer que leurs opérations se déroulent correctement.</span><span class="sxs-lookup"><span data-stu-id="0b037-166">Pessimistic locking expects multiple concurrent sessions to conflict and acquire locks in advance to ensure that their operations succeed.</span></span>

<span data-ttu-id="0b037-167">La plupart des opérations seront sérialisables en raison des verrous pris implicitement.</span><span class="sxs-lookup"><span data-stu-id="0b037-167">Most operations will be serializable by virtue of locks implicitly taken.</span></span> <span data-ttu-id="0b037-168">Toutefois, certaines opérations ne le seront pas.</span><span class="sxs-lookup"><span data-stu-id="0b037-168">However, some operations will not.</span></span> <span data-ttu-id="0b037-169">Pour illustrer cela, examinez les deux transactions,</span><span class="sxs-lookup"><span data-stu-id="0b037-169">To illustrate this, consider the two transactions,</span></span>

<span data-ttu-id="0b037-170">T1 : R (A), U (B)</span><span class="sxs-lookup"><span data-stu-id="0b037-170">T1 : R(A), U(B)</span></span>

<span data-ttu-id="0b037-171">T2 : R (B), U (A)</span><span class="sxs-lookup"><span data-stu-id="0b037-171">T2 : R(B), U(A)</span></span>

<span data-ttu-id="0b037-172">Le contrôle de version de l’enregistrement garantit que chaque transaction exécutée simultanément verra les valeurs d’origine pour A et B. Il n’y a pas d’ordre d’exécution en série qui peut produire les mêmes résultats pour A et B dans le cas où les résultats sont dépendants des données lues.</span><span class="sxs-lookup"><span data-stu-id="0b037-172">Record level versioning will ensure that each transaction when executed concurrently will see the original values for A and B. There is no serial order of execution that could produce the same results for A and B in the case that the results are dependent upon the data read.</span></span> <span data-ttu-id="0b037-173">Pour que l’application puisse sérialiser cette transaction, elle doit acquérir un verrou de lecture explicite sur A et B dans chaque transaction lorsque la valeur est lue.</span><span class="sxs-lookup"><span data-stu-id="0b037-173">In order for the application to make this transaction serializable, it should acquire an explicit read lock on A and B in each transaction when the value is read.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0b037-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b037-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b037-175"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0b037-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0b037-176">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="0b037-176">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b037-177"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="0b037-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0b037-178">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0b037-178">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b037-179"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="0b037-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0b037-180">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="0b037-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b037-181"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="0b037-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0b037-182">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0b037-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b037-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0b037-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0b037-184">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0b037-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0b037-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b037-185">See Also</span></span>

[<span data-ttu-id="0b037-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0b037-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0b037-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0b037-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0b037-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0b037-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0b037-189">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="0b037-189">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="0b037-190">JetStopService</span><span class="sxs-lookup"><span data-stu-id="0b037-190">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="0b037-191">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="0b037-191">JetUpdate</span></span>](./jetupdate-function.md)

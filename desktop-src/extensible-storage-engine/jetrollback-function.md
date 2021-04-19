---
description: 'En savoir plus sur : fonction JetRollback'
title: JetRollback fonction)
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eda0c8947e9609717bbb3f1a16999b450d7e4882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535590"
---
# <a name="jetrollback-function"></a><span data-ttu-id="c3e1e-103">JetRollback fonction)</span><span class="sxs-lookup"><span data-stu-id="c3e1e-103">JetRollback Function</span></span>


<span data-ttu-id="c3e1e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c3e1e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrollback-function"></a><span data-ttu-id="c3e1e-105">JetRollback fonction)</span><span class="sxs-lookup"><span data-stu-id="c3e1e-105">JetRollback Function</span></span>

<span data-ttu-id="c3e1e-106">La fonction **JetRollback** annule les modifications apportées à l’état de la base de données et retourne au dernier point d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-106">The **JetRollback** function undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="c3e1e-107">**JetRollback** ferme également tous les curseurs ouverts pendant le point d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-107">**JetRollback** will also close any cursors opened during the save point.</span></span> <span data-ttu-id="c3e1e-108">Si le point d’enregistrement le plus à l’extérieur est annulé, la session va quitter la transaction.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-108">If the outermost save point is undone, the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c3e1e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3e1e-109">Parameters</span></span>

<span data-ttu-id="c3e1e-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c3e1e-110">*sesid*</span></span>

<span data-ttu-id="c3e1e-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-111">The session to use for this call.</span></span>

<span data-ttu-id="c3e1e-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c3e1e-112">*grbit*</span></span>

<span data-ttu-id="c3e1e-113">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c3e1e-113">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3e1e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3e1e-114">Value</span></span></p></th>
<th><p><span data-ttu-id="c3e1e-115">Signification</span><span class="sxs-lookup"><span data-stu-id="c3e1e-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3e1e-116">JET_bitRollbackAll</span><span class="sxs-lookup"><span data-stu-id="c3e1e-116">JET_bitRollbackAll</span></span></p></td>
<td><p><span data-ttu-id="c3e1e-117">Cette option demande que toutes les modifications apportées à l’état de la base de données au cours de tous les points d’enregistrement soient annulées.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-117">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="c3e1e-118">Par conséquent, la session va quitter la transaction.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-118">As a result, the session will exit the transaction.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c3e1e-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c3e1e-119">Return Value</span></span>

<span data-ttu-id="c3e1e-120">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c3e1e-121">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c3e1e-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3e1e-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c3e1e-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="c3e1e-123">Description</span><span class="sxs-lookup"><span data-stu-id="c3e1e-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3e1e-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c3e1e-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c3e1e-125">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e1e-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c3e1e-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c3e1e-127">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e1e-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c3e1e-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c3e1e-129">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c3e1e-130">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e1e-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c3e1e-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c3e1e-132">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-132">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e1e-133">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="c3e1e-133">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="c3e1e-134">L’opération a échoué, car la session spécifiée n’est pas dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-134">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e1e-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c3e1e-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c3e1e-136">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e1e-137">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="c3e1e-137">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="c3e1e-138">Il n’était pas possible de restaurer les modifications en raison d’une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-138">It was not possible to rollback the changes due to a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e1e-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c3e1e-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c3e1e-140">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="c3e1e-141">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e1e-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c3e1e-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c3e1e-143">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c3e1e-144">En cas de réussite, toute modification apportée à la base de données pendant le point d’enregistrement actuel pour la session donnée est annulée et le point d’enregistrement est terminé.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-144">On success, any changes made to the database during the current save point for the given session will be undone and that save point will be ended.</span></span> <span data-ttu-id="c3e1e-145">Si le dernier point d’enregistrement de la session a été interrompu, la session quitte la transaction.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-145">If the last save point for the session was ended then the session will exit the transaction.</span></span>

<span data-ttu-id="c3e1e-146">En cas d’échec, l’état transactionnel de la session reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="c3e1e-147">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-147">No change to the database state will occur.</span></span> <span data-ttu-id="c3e1e-148">Un échec lors de la restauration est considéré comme une erreur catastrophique de la base de données.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-148">A failure during rollback is considered to be a catastrophic database error.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c3e1e-149">Notes</span><span class="sxs-lookup"><span data-stu-id="c3e1e-149">Remarks</span></span>

<span data-ttu-id="c3e1e-150">Il doit y avoir un appel à [JetCommitTransaction](./jetcommittransaction-function.md) ou **JetRollback** pour qu’il corresponde à chaque appel à [JetBeginTransaction](./jetbegintransaction-function.md) pour une session donnée.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-150">There must be one call to [JetCommitTransaction](./jetcommittransaction-function.md) or **JetRollback** to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

<span data-ttu-id="c3e1e-151">Si des curseurs ont été ouverts (à l’aide de [JetOpenTable](./jetopentable-function.md), par exemple) au cours d’un point d’enregistrement en cours de restauration, ce curseur est fermé.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-151">If any cursors were opened (using [JetOpenTable](./jetopentable-function.md), for example) during a save point that is being rolled back then that cursor will be closed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c3e1e-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3e1e-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3e1e-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c3e1e-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e1e-154">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e1e-155"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="c3e1e-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e1e-156">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e1e-157"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="c3e1e-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e1e-158">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3e1e-159"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="c3e1e-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e1e-160">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3e1e-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c3e1e-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c3e1e-162">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c3e1e-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c3e1e-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3e1e-163">See Also</span></span>

[<span data-ttu-id="c3e1e-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c3e1e-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c3e1e-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c3e1e-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c3e1e-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c3e1e-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c3e1e-167">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="c3e1e-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="c3e1e-168">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="c3e1e-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)

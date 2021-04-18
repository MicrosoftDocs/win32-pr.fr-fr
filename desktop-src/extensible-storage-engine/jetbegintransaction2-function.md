---
description: 'En savoir plus sur : fonction JetBeginTransaction2'
title: Fonction JetBeginTransaction2
TOCTitle: JetBeginTransaction2 Function
ms:assetid: 638af3f1-b342-46bd-9fd0-dc281936355c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269268(v=EXCHG.10)
ms:contentKeyID: 32765570
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d21bb88301a1f5d30df673a56032ef91c3847599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536191"
---
# <a name="jetbegintransaction2-function"></a><span data-ttu-id="53d69-103">Fonction JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="53d69-103">JetBeginTransaction2 Function</span></span>


<span data-ttu-id="53d69-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="53d69-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction2-function"></a><span data-ttu-id="53d69-105">Fonction JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="53d69-105">JetBeginTransaction2 Function</span></span>

<span data-ttu-id="53d69-106">La fonction **JetBeginTransaction2** oblige une session à entrer dans une transaction et à créer un nouveau point d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="53d69-106">The **JetBeginTransaction2** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="53d69-107">Cette fonction peut être appelée plusieurs fois dans une seule session pour créer des points d’enregistrement supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="53d69-107">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="53d69-108">Ces points d’enregistrement peuvent être utilisés pour conserver ou abandonner les modifications apportées à la base de données de manière sélective.</span><span class="sxs-lookup"><span data-stu-id="53d69-108">These save points can be used to selectively to keep or discard changes to the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction2(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="53d69-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53d69-109">Parameters</span></span>

<span data-ttu-id="53d69-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="53d69-110">*sesid*</span></span>

<span data-ttu-id="53d69-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="53d69-111">The session to use for this call.</span></span>

<span data-ttu-id="53d69-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="53d69-112">*grbit*</span></span>

<span data-ttu-id="53d69-113">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="53d69-113">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53d69-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="53d69-114">Value</span></span></p></th>
<th><p><span data-ttu-id="53d69-115">Signification</span><span class="sxs-lookup"><span data-stu-id="53d69-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53d69-116">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="53d69-116">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="53d69-117">La transaction ne modifie pas la base de données.</span><span class="sxs-lookup"><span data-stu-id="53d69-117">The transaction will not modify the database.</span></span> <span data-ttu-id="53d69-118">Si une mise à jour est tentée, cette opération échouera avec JET_errTransReadOnly.</span><span class="sxs-lookup"><span data-stu-id="53d69-118">If an update is attempted, that operation will fail with JET_errTransReadOnly.</span></span> <span data-ttu-id="53d69-119">Cette option est ignorée sauf si elle est demandée lorsque la session donnée n’est pas déjà dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="53d69-119">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="53d69-120">Cette option est disponible uniquement à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="53d69-120">This option is only available as of Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="53d69-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="53d69-121">Return Value</span></span>

<span data-ttu-id="53d69-122">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="53d69-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="53d69-123">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="53d69-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53d69-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="53d69-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="53d69-125">Description</span><span class="sxs-lookup"><span data-stu-id="53d69-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53d69-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="53d69-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="53d69-127">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="53d69-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53d69-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="53d69-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="53d69-129">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="53d69-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53d69-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="53d69-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="53d69-131">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="53d69-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="53d69-132">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="53d69-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53d69-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="53d69-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="53d69-134">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="53d69-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53d69-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="53d69-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="53d69-136">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="53d69-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53d69-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="53d69-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="53d69-138">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="53d69-138">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="53d69-139">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="53d69-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53d69-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="53d69-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="53d69-141">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="53d69-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53d69-142">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="53d69-142">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="53d69-143">Une nouvelle transaction ne peut pas être démarrée, car la session est déjà à la profondeur de point d’enregistrement maximale autorisée par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="53d69-143">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="53d69-144">En cas de réussite, la session fournie se trouve à l’intérieur d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="53d69-144">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="53d69-145">Si la session était précédemment à l’intérieur d’une transaction, un nouveau point d’enregistrement sera créé.</span><span class="sxs-lookup"><span data-stu-id="53d69-145">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="53d69-146">En cas d’échec, l’état transactionnel de la session reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="53d69-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="53d69-147">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="53d69-147">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="53d69-148">Notes</span><span class="sxs-lookup"><span data-stu-id="53d69-148">Remarks</span></span>

<span data-ttu-id="53d69-149">Pour plus d’informations sur le fonctionnement des transactions, consultez [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="53d69-149">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="53d69-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53d69-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53d69-151"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="53d69-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="53d69-152">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="53d69-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53d69-153"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="53d69-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="53d69-154">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="53d69-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53d69-155"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="53d69-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="53d69-156">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="53d69-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53d69-157"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="53d69-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="53d69-158">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="53d69-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53d69-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="53d69-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="53d69-160">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="53d69-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="53d69-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53d69-161">See Also</span></span>

[<span data-ttu-id="53d69-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="53d69-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="53d69-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="53d69-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="53d69-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="53d69-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="53d69-165">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="53d69-165">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="53d69-166">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="53d69-166">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="53d69-167">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="53d69-167">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="53d69-168">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="53d69-168">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="53d69-169">JetRollback</span><span class="sxs-lookup"><span data-stu-id="53d69-169">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="53d69-170">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="53d69-170">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="53d69-171">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="53d69-171">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

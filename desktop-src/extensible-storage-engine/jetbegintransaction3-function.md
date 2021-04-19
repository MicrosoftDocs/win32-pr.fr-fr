---
description: 'En savoir plus sur : fonction JetBeginTransaction3'
title: Fonction JetBeginTransaction3
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b263cb18c09df8205a49e1c4a1a683e339803f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513968"
---
# <a name="jetbegintransaction3-function"></a><span data-ttu-id="750a2-103">Fonction JetBeginTransaction3</span><span class="sxs-lookup"><span data-stu-id="750a2-103">JetBeginTransaction3 Function</span></span>


<span data-ttu-id="750a2-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="750a2-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="750a2-105">La fonction **JetBeginTransaction3** oblige une session à entrer dans une transaction et à créer un nouveau point d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="750a2-105">The **JetBeginTransaction3** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="750a2-106">Cette fonction peut être appelée plusieurs fois dans une seule session pour créer des points d’enregistrement supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="750a2-106">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="750a2-107">Ces points d’enregistrement peuvent être utilisés pour conserver ou abandonner les modifications apportées à la base de données de manière sélective.</span><span class="sxs-lookup"><span data-stu-id="750a2-107">These save points can be used to selectively to keep or discard changes to the database.</span></span>

<span data-ttu-id="750a2-108">La fonction **JetBeginTransaction3** a été introduite dans le système d’exploitation Windows 8.</span><span class="sxs-lookup"><span data-stu-id="750a2-108">The **JetBeginTransaction3** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="750a2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="750a2-109">Parameters</span></span>

<span data-ttu-id="750a2-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="750a2-110">*sesid*</span></span>

<span data-ttu-id="750a2-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="750a2-111">The session to use for this call.</span></span>

<span data-ttu-id="750a2-112">*trxid*</span><span class="sxs-lookup"><span data-stu-id="750a2-112">*trxid*</span></span>

<span data-ttu-id="750a2-113">Identificateur facultatif fourni par l’utilisateur pour identifier la transaction.</span><span class="sxs-lookup"><span data-stu-id="750a2-113">An optional identifier supplied by the user to identify the transaction.</span></span>

<span data-ttu-id="750a2-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="750a2-114">*grbit*</span></span>

<span data-ttu-id="750a2-115">Groupe de bits qui spécifie zéro, une ou plusieurs des valeurs d’option d’appel énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="750a2-115">A group of bits that that specifies zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="750a2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="750a2-116">Value</span></span></p></th>
<th><p><span data-ttu-id="750a2-117">Signification</span><span class="sxs-lookup"><span data-stu-id="750a2-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750a2-118">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="750a2-118">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="750a2-119">La transaction ne modifie pas la base de données.</span><span class="sxs-lookup"><span data-stu-id="750a2-119">The transaction will not modify the database.</span></span> <span data-ttu-id="750a2-120">Si une mise à jour est tentée, cette opération échoue avec JET_errTransReadOnly code de réponse.</span><span class="sxs-lookup"><span data-stu-id="750a2-120">If an update is attempted, that operation will fail with JET_errTransReadOnly response code.</span></span> <span data-ttu-id="750a2-121">Cette option est ignorée sauf si elle est demandée lorsque la session donnée n’est pas déjà dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="750a2-121">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="750a2-122">Cette option est disponible dans les versions du système d’exploitation Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="750a2-122">This option is available in versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="750a2-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="750a2-123">Return value</span></span>

<span data-ttu-id="750a2-124">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="750a2-124">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="750a2-125">Pour plus d’informations sur les erreurs ESE (Extensible Storage Engine) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="750a2-125">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="750a2-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="750a2-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="750a2-127">Description</span><span class="sxs-lookup"><span data-stu-id="750a2-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750a2-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="750a2-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="750a2-129">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="750a2-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750a2-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="750a2-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="750a2-131">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a cessé à la suite d’un appel à la fonction <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="750a2-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750a2-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="750a2-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="750a2-133">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="750a2-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="750a2-134">Ce code de retour est retourné par les versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="750a2-134">This return code is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750a2-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="750a2-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="750a2-136">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="750a2-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750a2-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="750a2-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="750a2-138">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="750a2-138">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750a2-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="750a2-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="750a2-140">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="750a2-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="750a2-141">Cette erreur est retournée par les versions de Windows à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="750a2-141">This error is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750a2-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="750a2-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="750a2-143">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="750a2-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750a2-144">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="750a2-144">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="750a2-145">Une nouvelle transaction ne peut pas être démarrée, car la session est déjà à la profondeur de point d’enregistrement maximale autorisée par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="750a2-145">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="750a2-146">En cas de réussite, la session fournie se trouve à l’intérieur d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="750a2-146">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="750a2-147">Si la session était précédemment à l’intérieur d’une transaction, un nouveau point d’enregistrement sera créé.</span><span class="sxs-lookup"><span data-stu-id="750a2-147">If the session was previously inside a transaction, a new save point will be created.</span></span>

<span data-ttu-id="750a2-148">En cas d’échec, l’état transactionnel de la session reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="750a2-148">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="750a2-149">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="750a2-149">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="750a2-150">Notes</span><span class="sxs-lookup"><span data-stu-id="750a2-150">Remarks</span></span>

<span data-ttu-id="750a2-151">Pour plus d’informations sur le fonctionnement des transactions, consultez [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="750a2-151">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="750a2-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="750a2-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750a2-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="750a2-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="750a2-154">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="750a2-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750a2-155"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="750a2-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="750a2-156">Requiert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="750a2-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750a2-157"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="750a2-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="750a2-158">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="750a2-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750a2-159"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="750a2-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="750a2-160">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="750a2-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750a2-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="750a2-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="750a2-162">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="750a2-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="750a2-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="750a2-163">See also</span></span>

[<span data-ttu-id="750a2-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="750a2-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="750a2-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="750a2-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="750a2-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="750a2-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="750a2-167">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="750a2-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="750a2-168">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="750a2-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="750a2-169">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="750a2-169">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="750a2-170">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="750a2-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="750a2-171">JetRollback</span><span class="sxs-lookup"><span data-stu-id="750a2-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="750a2-172">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="750a2-172">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="750a2-173">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="750a2-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

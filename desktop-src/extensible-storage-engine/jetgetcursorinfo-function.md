---
description: 'En savoir plus sur : fonction JetGetCursorInfo'
title: JetGetCursorInfo fonction)
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523068"
---
# <a name="jetgetcursorinfo-function"></a><span data-ttu-id="ebc4b-103">JetGetCursorInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="ebc4b-103">JetGetCursorInfo Function</span></span>


<span data-ttu-id="ebc4b-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="ebc4b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcursorinfo-function"></a><span data-ttu-id="ebc4b-105">JetGetCursorInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="ebc4b-105">JetGetCursorInfo Function</span></span>

<span data-ttu-id="ebc4b-106">La fonction **JetGetCursorInfo** est utilisée pour déterminer si une mise à jour de l’enregistrement en cours d’un curseur entraîne un conflit d’écriture, en fonction de l’état de mise à jour actuel de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-106">The **JetGetCursorInfo** function is used to determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="ebc4b-107">Il est possible qu’un conflit d’écriture soit retourné, même si **JetGetCursorInfo** retourne JET_errSuccess, car une autre session peut mettre à jour l’enregistrement avant que la session actuelle puisse mettre à jour le même enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-107">It is possible that a write conflict will ultimately be returned even if **JetGetCursorInfo** returns JET_errSuccess, because another session may update the record before the current session is able to update the same record.</span></span>

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="ebc4b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebc4b-108">Parameters</span></span>

<span data-ttu-id="ebc4b-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ebc4b-109">*sesid*</span></span>

<span data-ttu-id="ebc4b-110">Session qui sera utilisée pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-110">The session that will be used for this call.</span></span>

<span data-ttu-id="ebc4b-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="ebc4b-111">*tableid*</span></span>

<span data-ttu-id="ebc4b-112">Curseur qui sera utilisé pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-112">The cursor that will be used for this call.</span></span>

<span data-ttu-id="ebc4b-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="ebc4b-113">*pvResult*</span></span>

<span data-ttu-id="ebc4b-114">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-114">Reserved for future use.</span></span>

<span data-ttu-id="ebc4b-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="ebc4b-115">*cbMax*</span></span>

<span data-ttu-id="ebc4b-116">Doit être défini sur 0 (zéro), sinon inutilisé.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-116">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="ebc4b-117">Il est présent pour les fonctionnalités futures.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-117">It is present for future functionality.</span></span>

<span data-ttu-id="ebc4b-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="ebc4b-118">*InfoLevel*</span></span>

<span data-ttu-id="ebc4b-119">Doit être défini sur 0 (zéro), sinon inutilisé.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-119">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="ebc4b-120">Il est présent pour les fonctionnalités futures.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-120">It is present for future functionality.</span></span>

### <a name="return-value"></a><span data-ttu-id="ebc4b-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ebc4b-121">Return Value</span></span>

<span data-ttu-id="ebc4b-122">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ebc4b-123">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ebc4b-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ebc4b-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ebc4b-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="ebc4b-125">Description</span><span class="sxs-lookup"><span data-stu-id="ebc4b-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebc4b-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ebc4b-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ebc4b-127">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebc4b-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ebc4b-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ebc4b-129">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebc4b-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ebc4b-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ebc4b-131">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ebc4b-132">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebc4b-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ebc4b-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ebc4b-134"><em>CbMax</em> n’est pas égal à 0 (zéro) ou <em>InfoLevel</em> n’est pas égal à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="ebc4b-134">Either <em>cbMax</em> is not 0 (zero) or <em>InfoLevel</em> is not 0 (zero).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebc4b-135">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="ebc4b-135">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="ebc4b-136">Le curseur ne se trouve pas actuellement sur un enregistrement et les informations sur un enregistrement logique ne peuvent pas être retournées en conséquence.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-136">The cursor is not currently on a record and information on a logical record cannot be returned as a result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebc4b-137">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ebc4b-137">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ebc4b-138">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-138">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebc4b-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ebc4b-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ebc4b-140">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-140">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebc4b-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="ebc4b-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="ebc4b-142">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-142">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="ebc4b-143">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-143">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebc4b-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ebc4b-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ebc4b-145">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebc4b-146">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ebc4b-146">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="ebc4b-147">L’enregistrement actuel du curseur a été mis à jour par une autre session et une mise à jour de cet enregistrement par cette session entraîne un conflit d’écriture.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-147">The current record of the cursor has been updated by another session and an update of this record by this session will result in a write conflict.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ebc4b-148">En cas de réussite, cette opération n’a aucun effet sur l’emplacement du curseur, mais indique uniquement qu’aucune autre session n’a actuellement mis à jour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-148">On success, this operation has no effect on the location of the cursor but only indicates that no other session has currently updated this record.</span></span>

<span data-ttu-id="ebc4b-149">En cas d’échec, si un code d’erreur négatif est retourné, il n’y a aucun effet sur le curseur ou la base de données.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-149">On failure, if a negative error code is returned there are no effects to the cursor or the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ebc4b-150">Notes</span><span class="sxs-lookup"><span data-stu-id="ebc4b-150">Remarks</span></span>

<span data-ttu-id="ebc4b-151">Cette opération n’affecte pas l’état du curseur ou des données.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-151">This operation does not affect the state of the cursor or the data.</span></span> <span data-ttu-id="ebc4b-152">Elle retourne uniquement un code d’erreur qui décrit si une mise à jour de l’enregistrement en cours par la session appelante est connue pour générer un JET_errWriteConflict ou est inconnue pour retourner JET_errWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-152">It only returns an error code describing whether an update to the current record by the calling session is known to result in a JET_errWriteConflict, or is unknown to return JET_errWriteConflict.</span></span> <span data-ttu-id="ebc4b-153">Si une autre session a déjà mis à jour cet enregistrement pour l’utiliser, il est certain qu’une mise à jour de cet enregistrement par cette session entraîne un conflit d’écriture.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-153">If another session has already updated this record to use it is certain that an update of this record by this session will result in a write conflict.</span></span> <span data-ttu-id="ebc4b-154">La valeur est true jusqu’à ce que cette session valide ou restaure ses transactions au niveau de la transaction 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="ebc4b-154">This will be true until this session commits or rolls back its transactions to transaction level 0 (zero).</span></span> <span data-ttu-id="ebc4b-155">Toutefois, si **JetGetCursorInfo** retourne JET_errSuccess, il est toujours possible pour une autre session de mettre à jour cet enregistrement avant la session active. il est donc toujours possible qu’une mise à jour de l’enregistrement actif par cette session dans sa transaction actuelle entraîne un conflit d’écriture.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-155">However, if **JetGetCursorInfo** returns JET_errSuccess, it is still possible for another session to update this record before the current session and thus it is still possible that an update of the current record by this session in its current transaction will result in a write conflict.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ebc4b-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebc4b-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebc4b-157"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ebc4b-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ebc4b-158">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebc4b-159"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="ebc4b-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ebc4b-160">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebc4b-161"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="ebc4b-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ebc4b-162">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebc4b-163"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="ebc4b-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ebc4b-164">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebc4b-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ebc4b-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ebc4b-166">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ebc4b-166">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ebc4b-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebc4b-167">See Also</span></span>

[<span data-ttu-id="ebc4b-168">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ebc4b-168">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ebc4b-169">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ebc4b-169">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ebc4b-170">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ebc4b-170">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ebc4b-171">JetGetLock</span><span class="sxs-lookup"><span data-stu-id="ebc4b-171">JetGetLock</span></span>](./jetgetlock-function.md)  
[<span data-ttu-id="ebc4b-172">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="ebc4b-172">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="ebc4b-173">JetStopService</span><span class="sxs-lookup"><span data-stu-id="ebc4b-173">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="ebc4b-174">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="ebc4b-174">JetUpdate</span></span>](./jetupdate-function.md)

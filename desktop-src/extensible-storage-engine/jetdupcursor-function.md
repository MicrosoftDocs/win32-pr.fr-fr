---
description: 'En savoir plus sur : fonction JetDupCursor'
title: Fonction JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 590b9b08c5386aaf1cd2dd541ac496a5fa0871d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538711"
---
# <a name="jetdupcursor-function"></a><span data-ttu-id="decf9-103">Fonction JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="decf9-103">JetDupCursor Function</span></span>


<span data-ttu-id="decf9-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="decf9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupcursor-function"></a><span data-ttu-id="decf9-105">Fonction JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="decf9-105">JetDupCursor Function</span></span>

<span data-ttu-id="decf9-106">La fonction **JetDupCursor** duplique un curseur ouvert et retourne un descripteur au curseur dupliqué.</span><span class="sxs-lookup"><span data-stu-id="decf9-106">The **JetDupCursor** function duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="decf9-107">Si le curseur qui était dupliqué était un curseur en lecture seule, le curseur dupliqué est également un curseur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="decf9-107">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="decf9-108">Tout État lié à la construction d’une clé de recherche ou à la mise à jour d’un enregistrement n’est pas copié dans le curseur dupliqué.</span><span class="sxs-lookup"><span data-stu-id="decf9-108">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="decf9-109">En outre, l’emplacement du curseur d’origine n’est pas dupliqué dans le curseur dupliqué.</span><span class="sxs-lookup"><span data-stu-id="decf9-109">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="decf9-110">Le curseur dupliqué est toujours ouvert sur l’index cluster et son emplacement est toujours sur la première ligne de la table.</span><span class="sxs-lookup"><span data-stu-id="decf9-110">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="decf9-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="decf9-111">Parameters</span></span>

<span data-ttu-id="decf9-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="decf9-112">*sesid*</span></span>

<span data-ttu-id="decf9-113">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="decf9-113">The session to use for this call.</span></span>

<span data-ttu-id="decf9-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="decf9-114">*tableid*</span></span>

<span data-ttu-id="decf9-115">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="decf9-115">The cursor to use for this call.</span></span>

<span data-ttu-id="decf9-116">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="decf9-116">*ptableid*</span></span>

<span data-ttu-id="decf9-117">Pointeur vers *TableID*.</span><span class="sxs-lookup"><span data-stu-id="decf9-117">Pointer to *tableid*.</span></span>

<span data-ttu-id="decf9-118">*grbit*</span><span class="sxs-lookup"><span data-stu-id="decf9-118">*grbit*</span></span>

<span data-ttu-id="decf9-119">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="decf9-119">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="decf9-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="decf9-120">Return Value</span></span>

<span data-ttu-id="decf9-121">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="decf9-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="decf9-122">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="decf9-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="decf9-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="decf9-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="decf9-124">Description</span><span class="sxs-lookup"><span data-stu-id="decf9-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="decf9-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="decf9-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="decf9-126">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="decf9-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="decf9-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="decf9-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="decf9-128">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="decf9-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="decf9-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="decf9-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="decf9-130">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="decf9-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="decf9-131">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="decf9-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="decf9-132">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="decf9-132">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="decf9-133">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="decf9-133">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="decf9-134">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="decf9-134">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="decf9-135">Il n’existe aucune ressource de curseur disponible.</span><span class="sxs-lookup"><span data-stu-id="decf9-135">No available cursor resources exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="decf9-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="decf9-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="decf9-137">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="decf9-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="decf9-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="decf9-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="decf9-139">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="decf9-139">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="decf9-140">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="decf9-140">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="decf9-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="decf9-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="decf9-142">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="decf9-142">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="decf9-143">En cas de réussite, *pTableID* est défini sur un curseur dupliqué.</span><span class="sxs-lookup"><span data-stu-id="decf9-143">On success, *ptableid* is set to a duplicated cursor.</span></span>

<span data-ttu-id="decf9-144">En cas d’échec, aucune modification n’est apportée.</span><span class="sxs-lookup"><span data-stu-id="decf9-144">On failure, no changes are made.</span></span> <span data-ttu-id="decf9-145">L’état de *TableID* est inchangé.</span><span class="sxs-lookup"><span data-stu-id="decf9-145">The state of *tableid* is unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="decf9-146">Notes</span><span class="sxs-lookup"><span data-stu-id="decf9-146">Remarks</span></span>

<span data-ttu-id="decf9-147">Le curseur dupliqué n’a pas l’état de curseur entier copié.</span><span class="sxs-lookup"><span data-stu-id="decf9-147">The duplicated cursor does not have the entire cursor state copied.</span></span> <span data-ttu-id="decf9-148">L’emplacement du curseur dupliqué, y compris l’index actuel, est généralement différent du curseur donné.</span><span class="sxs-lookup"><span data-stu-id="decf9-148">The location of the duplicated cursor, including the current index, is usually different from the given cursor.</span></span> <span data-ttu-id="decf9-149">Le curseur dupliqué est toujours retourné sur l’index cluster et sur la première ligne de la table.</span><span class="sxs-lookup"><span data-stu-id="decf9-149">The duplicated cursor is always returned on the clustered index and on the first row in the table.</span></span> <span data-ttu-id="decf9-150">Si la table est vide, le curseur dupliqué ne figure pas sur une ligne.</span><span class="sxs-lookup"><span data-stu-id="decf9-150">If the table is empty, the duplicated cursor is not on any row.</span></span>

<span data-ttu-id="decf9-151">Les tables ouvertes avec **JetDupCursor** doivent généralement être fermées avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="decf9-151">Tables opened with **JetDupCursor** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="decf9-152">L’exception à cette règle se produit lorsque **JetDupCursor** est appelé dans une transaction et que la transaction est restaurée (avec [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="decf9-152">The exception to this rule happens when **JetDupCursor** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="decf9-153">Lors de la restauration d’une transaction, le curseur est automatiquement fermé.</span><span class="sxs-lookup"><span data-stu-id="decf9-153">When rolling back a transaction, the cursor is automatically closed.</span></span> <span data-ttu-id="decf9-154">Dans ce cas, il s’agit d’une erreur de fermeture de la table avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="decf9-154">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="decf9-155">Le nombre de tables pouvant être ouvertes simultanément est directement affecté par [JET_paramMaxOpenTables](./resource-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="decf9-155">The number of tables that can be opened simultaneously is affected directly by [JET_paramMaxOpenTables](./resource-parameters.md).</span></span> <span data-ttu-id="decf9-156">Pour plus d’informations, consultez [paramètres système](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="decf9-156">See [System Parameters](./extensible-storage-engine-system-parameters.md) for details.</span></span>

#### <a name="requirements"></a><span data-ttu-id="decf9-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="decf9-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="decf9-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="decf9-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="decf9-159">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="decf9-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="decf9-160"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="decf9-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="decf9-161">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="decf9-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="decf9-162"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="decf9-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="decf9-163">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="decf9-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="decf9-164"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="decf9-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="decf9-165">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="decf9-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="decf9-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="decf9-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="decf9-167">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="decf9-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="decf9-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="decf9-168">See Also</span></span>

[<span data-ttu-id="decf9-169">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="decf9-169">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="decf9-170">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="decf9-170">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="decf9-171">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="decf9-171">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="decf9-172">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="decf9-172">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="decf9-173">JetRollback</span><span class="sxs-lookup"><span data-stu-id="decf9-173">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="decf9-174">JetStopService</span><span class="sxs-lookup"><span data-stu-id="decf9-174">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="decf9-175">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="decf9-175">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

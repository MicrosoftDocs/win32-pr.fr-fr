---
description: 'En savoir plus sur : fonction JetComputeStats'
title: JetComputeStats fonction)
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c6856a50ae2f1c01b1cfde0666d0c535ad37e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210838"
---
# <a name="jetcomputestats-function"></a><span data-ttu-id="bfe12-103">JetComputeStats fonction)</span><span class="sxs-lookup"><span data-stu-id="bfe12-103">JetComputeStats Function</span></span>


<span data-ttu-id="bfe12-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="bfe12-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcomputestats-function"></a><span data-ttu-id="bfe12-105">JetComputeStats fonction)</span><span class="sxs-lookup"><span data-stu-id="bfe12-105">JetComputeStats Function</span></span>

<span data-ttu-id="bfe12-106">La fonction **JetComputeStats** parcourt chaque index d’une table pour calculer exactement le nombre d’entrées dans un index et le nombre de clés distinctes dans un index.</span><span class="sxs-lookup"><span data-stu-id="bfe12-106">The **JetComputeStats** function walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="bfe12-107">Ces informations, ainsi que le nombre de pages de base de données allouées pour un index et l’heure actuelle du calcul, sont stockées dans les métadonnées d’index dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="bfe12-107">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="bfe12-108">Ces données peuvent être récupérées par la suite avec les opérations d’informations.</span><span class="sxs-lookup"><span data-stu-id="bfe12-108">This data can be subsequently retrieved with information operations.</span></span>

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="bfe12-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfe12-109">Parameters</span></span>

<span data-ttu-id="bfe12-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bfe12-110">*sesid*</span></span>

<span data-ttu-id="bfe12-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="bfe12-111">The session to use for this call.</span></span>

<span data-ttu-id="bfe12-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="bfe12-112">*tableid*</span></span>

<span data-ttu-id="bfe12-113">Curseur qui sera utilisé pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="bfe12-113">The cursor that will be used for this call.</span></span> <span data-ttu-id="bfe12-114">Décrit la table sur laquelle calculer les statistiques.</span><span class="sxs-lookup"><span data-stu-id="bfe12-114">Describes the table to compute statistics on.</span></span>

### <a name="return-value"></a><span data-ttu-id="bfe12-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bfe12-115">Return Value</span></span>

<span data-ttu-id="bfe12-116">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="bfe12-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bfe12-117">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bfe12-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bfe12-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bfe12-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="bfe12-119">Description</span><span class="sxs-lookup"><span data-stu-id="bfe12-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfe12-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bfe12-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bfe12-121">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="bfe12-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfe12-122">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bfe12-122">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bfe12-123">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="bfe12-123">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfe12-124">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bfe12-124">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bfe12-125">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="bfe12-125">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="bfe12-126">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bfe12-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfe12-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bfe12-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bfe12-128">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="bfe12-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfe12-129">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bfe12-129">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bfe12-130">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="bfe12-130">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfe12-131">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="bfe12-131">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="bfe12-132">Une erreur s’est produite lors de l’annulation de l’opération de restauration de toutes les modifications, mais la restauration de la transaction a échoué.</span><span class="sxs-lookup"><span data-stu-id="bfe12-132">An error occurred requiring this operation to rollback all changes, but the transaction rollback itself failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfe12-133">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bfe12-133">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bfe12-134">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="bfe12-134">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="bfe12-135">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bfe12-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfe12-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bfe12-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bfe12-137">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="bfe12-137">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bfe12-138">En cas de réussite, les statistiques à jour sont stockées dans les catalogues de base de données pour la table décrite avec le curseur donné.</span><span class="sxs-lookup"><span data-stu-id="bfe12-138">On success, up-to-date statistics are stored in the database catalogs for the table described with the given cursor.</span></span>

<span data-ttu-id="bfe12-139">En cas d’échec, aucune mise à jour de n’importe quel type n’est effectuée dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="bfe12-139">On failure, no updates of any kind are made to the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bfe12-140">Notes</span><span class="sxs-lookup"><span data-stu-id="bfe12-140">Remarks</span></span>

<span data-ttu-id="bfe12-141">Cette opération peut consommer des ressources puisque chaque index d’une table doit être parcouru dans son intégralité.</span><span class="sxs-lookup"><span data-stu-id="bfe12-141">This operation can be resource consuming since each index in a table must be walked in its entirety.</span></span> <span data-ttu-id="bfe12-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) peut être utilisé pour obtenir une estimation approximative du nombre d’entrées dans un index, mais il ne peut pas estimer lui-même le nombre de valeurs distinctes dans un index.</span><span class="sxs-lookup"><span data-stu-id="bfe12-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) can be used to get a rough estimate of the number of entries in an index, but it cannot by itself estimate the number of distinct values in an index.</span></span>

<span data-ttu-id="bfe12-143">Les données calculées par cette opération commencent à devenir obsolètes et la table est mise à jour par la suite.</span><span class="sxs-lookup"><span data-stu-id="bfe12-143">The data computed by this operation begins to become out of date and the table is subsequently updated.</span></span>

<span data-ttu-id="bfe12-144">Les mises à jour apportées à la base de données par **JetComputeStats** sont effectuées de manière différée.</span><span class="sxs-lookup"><span data-stu-id="bfe12-144">Updates to the database made by **JetComputeStats** are made in a lazy fashion.</span></span> <span data-ttu-id="bfe12-145">Cela signifie qu’aucun vidage du journal n’est accompagné de cette opération et qu’un incident système se produit suite à un retour de JET_errSuccess par **JetComputeStats** peut toujours entraîner la perte de ces mises à jour.</span><span class="sxs-lookup"><span data-stu-id="bfe12-145">This means that no log flush will be accompanied by this operation and a system crash subsequent to a return of JET_errSuccess by **JetComputeStats** can still cause these updates to be lost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bfe12-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfe12-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfe12-147"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bfe12-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bfe12-148">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="bfe12-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfe12-149"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="bfe12-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bfe12-150">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bfe12-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfe12-151"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="bfe12-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bfe12-152">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="bfe12-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfe12-153"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="bfe12-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bfe12-154">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bfe12-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfe12-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bfe12-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bfe12-156">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bfe12-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bfe12-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfe12-157">See Also</span></span>

[<span data-ttu-id="bfe12-158">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bfe12-158">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bfe12-159">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bfe12-159">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bfe12-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bfe12-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bfe12-161">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="bfe12-161">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="bfe12-162">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="bfe12-162">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="bfe12-163">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="bfe12-163">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="bfe12-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="bfe12-164">JetStopService</span></span>](./jetstopservice-function.md)

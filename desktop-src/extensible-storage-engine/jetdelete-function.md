---
description: 'En savoir plus sur : fonction JetDelete'
title: Fonction JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541902"
---
# <a name="jetdelete-function"></a><span data-ttu-id="59bcd-103">Fonction JetDelete</span><span class="sxs-lookup"><span data-stu-id="59bcd-103">JetDelete Function</span></span>


<span data-ttu-id="59bcd-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="59bcd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdelete-function"></a><span data-ttu-id="59bcd-105">Fonction JetDelete</span><span class="sxs-lookup"><span data-stu-id="59bcd-105">JetDelete Function</span></span>

<span data-ttu-id="59bcd-106">La fonction **JetDelete** supprime l’enregistrement en cours dans une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="59bcd-106">The **JetDelete** function deletes the current record in a database table.</span></span>

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="59bcd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59bcd-107">Parameters</span></span>

<span data-ttu-id="59bcd-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="59bcd-108">*sesid*</span></span>

<span data-ttu-id="59bcd-109">Contexte de session de base de données qui sera utilisé pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="59bcd-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="59bcd-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="59bcd-110">*tableid*</span></span>

<span data-ttu-id="59bcd-111">Curseur sur une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="59bcd-111">The cursor on a database table.</span></span> <span data-ttu-id="59bcd-112">La ligne actuelle sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="59bcd-112">The current row will be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="59bcd-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="59bcd-113">Return Value</span></span>

<span data-ttu-id="59bcd-114">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="59bcd-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="59bcd-115">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="59bcd-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59bcd-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="59bcd-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="59bcd-117">Description</span><span class="sxs-lookup"><span data-stu-id="59bcd-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="59bcd-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="59bcd-119">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="59bcd-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bcd-120">JET_errCallbackFailed</span><span class="sxs-lookup"><span data-stu-id="59bcd-120">JET_errCallbackFailed</span></span></p></td>
<td><p><span data-ttu-id="59bcd-121">La fonction de rappel a échoué de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="59bcd-121">The callback function failed in some manner.</span></span> <span data-ttu-id="59bcd-122">Par exemple, les violations d’accès dans les fonctions de rappel sont interceptées et converties en JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="59bcd-122">For example, access violations in callback functions are caught and translated into JET_errCallbackFailed.</span></span> <span data-ttu-id="59bcd-123">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="59bcd-123">This error will only be returned by Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="59bcd-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="59bcd-125">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="59bcd-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bcd-126">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="59bcd-126">JET_errIllegalOperation</span></span></p></td>
<td><p><span data-ttu-id="59bcd-127">Le curseur spécifié par <em>TableID</em> ne prend pas en charge la suppression.</span><span class="sxs-lookup"><span data-stu-id="59bcd-127">The cursor specified by <em>tableid</em> does not support deletion.</span></span> <span data-ttu-id="59bcd-128">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="59bcd-128">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="59bcd-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="59bcd-130">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="59bcd-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="59bcd-131">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="59bcd-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bcd-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="59bcd-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="59bcd-133">Le curseur spécifié par <em>TableID</em> n’est pas sur un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="59bcd-133">The cursor specified by <em>tableid</em> is not on a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="59bcd-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="59bcd-135">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="59bcd-135">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bcd-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="59bcd-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="59bcd-137">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="59bcd-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="59bcd-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="59bcd-139">Le moteur de base de données ne dispose pas des autorisations suffisantes pour supprimer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="59bcd-139">The database engine does not have sufficient permissions to delete the record.</span></span> <span data-ttu-id="59bcd-140">Cela peut se produire si le fichier de base de données a été ouvert avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="59bcd-140">This may happen if the database file was opened with read-only access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bcd-141">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="59bcd-141">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="59bcd-142">Une mémoire tampon de mise à jour (consultez <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) existe, mais toutes les modifications apportées aux colonnes de type JET_coltypLongText et/ou les colonnes de type JET_coltypLongBinary peuvent être restaurées.</span><span class="sxs-lookup"><span data-stu-id="59bcd-142">An update buffer (see <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) exists, but not all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary could be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-143">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="59bcd-143">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="59bcd-144">Il n’est pas conforme d’utiliser la même session à partir de plusieurs threads en même temps.</span><span class="sxs-lookup"><span data-stu-id="59bcd-144">It is illegal to use the same session from more than one thread at the same time.</span></span> <span data-ttu-id="59bcd-145">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="59bcd-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bcd-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="59bcd-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="59bcd-147">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="59bcd-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-148">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="59bcd-148">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="59bcd-149">La transaction est une transaction en lecture seule et ne prend pas en charge les suppressions.</span><span class="sxs-lookup"><span data-stu-id="59bcd-149">The transaction is a read-only transaction, and does not support deletes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bcd-150">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="59bcd-150">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="59bcd-151">L’opération a échoué, car il n’y a pas assez de mémoire pour conserver les informations transactionnelles sur la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="59bcd-151">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-152">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="59bcd-152">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="59bcd-153">Une autre session a déjà verrouillé l’enregistrement pour la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="59bcd-153">Another session has previously locked the record for update.</span></span> <span data-ttu-id="59bcd-154">La mise à jour tentée par cette session échoue.</span><span class="sxs-lookup"><span data-stu-id="59bcd-154">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="59bcd-155">En cas de réussite, la devise est conservée juste avant l’enregistrement suivant.</span><span class="sxs-lookup"><span data-stu-id="59bcd-155">On success, the currency is left just before the next record.</span></span> <span data-ttu-id="59bcd-156">Si l’enregistrement supprimé était le dernier dans la table, la devise est laissée à la fin de la table (autrement dit, après le nouveau dernier enregistrement).</span><span class="sxs-lookup"><span data-stu-id="59bcd-156">If the deleted record was the last in the table, the currency is left at the end of the table (that is, after the new last record).</span></span> <span data-ttu-id="59bcd-157">Si l’enregistrement supprimé était le seul enregistrement dans la table, la devise est définie au début.</span><span class="sxs-lookup"><span data-stu-id="59bcd-157">If the deleted record was the only record in the table, the currency is set to the beginning.</span></span>

<span data-ttu-id="59bcd-158">Les index appropriés sont automatiquement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="59bcd-158">The appropriate indexes are automatically updated.</span></span>

<span data-ttu-id="59bcd-159">Si une mise à jour est préparée (à l’aide de [JetPrepareUpdate](./jetprepareupdate-function.md)), elle sera annulée.</span><span class="sxs-lookup"><span data-stu-id="59bcd-159">If an update is prepared (using [JetPrepareUpdate](./jetprepareupdate-function.md)), it will be canceled.</span></span> <span data-ttu-id="59bcd-160">La mémoire tampon de mise à jour sera réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="59bcd-160">The update buffer will be reset.</span></span>

<span data-ttu-id="59bcd-161">En cas d’échec, la devise reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="59bcd-161">On failure, the currency remains unchanged.</span></span> <span data-ttu-id="59bcd-162">Si une mise à jour est préparée (voir [JetPrepareUpdate](./jetprepareupdate-function.md)), la mémoire tampon de mise à jour peut être réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="59bcd-162">If an update is prepared (see [JetPrepareUpdate](./jetprepareupdate-function.md)), the update buffer may be reset.</span></span>

#### <a name="remarks"></a><span data-ttu-id="59bcd-163">Notes</span><span class="sxs-lookup"><span data-stu-id="59bcd-163">Remarks</span></span>

<span data-ttu-id="59bcd-164">Toutes les tables ne prennent pas en charge la suppression de lignes.</span><span class="sxs-lookup"><span data-stu-id="59bcd-164">Not all tables support deletion of rows.</span></span> <span data-ttu-id="59bcd-165">Une table temporaire ne prend normalement pas en charge la suppression de lignes.</span><span class="sxs-lookup"><span data-stu-id="59bcd-165">A temporary table does not normally support deletion of rows.</span></span> <span data-ttu-id="59bcd-166">La suppression des enregistrements peut être activée sur les tables temporaires pour de nombreuses raisons, dont certaines sont :</span><span class="sxs-lookup"><span data-stu-id="59bcd-166">Deletion of records may be enabled on temporary tables for many reasons, some of which are:</span></span>

  - <span data-ttu-id="59bcd-167">JET_bitTTUpdatable a été spécifié lors de la création.</span><span class="sxs-lookup"><span data-stu-id="59bcd-167">JET_bitTTUpdatable was specified during creation.</span></span>

  - <span data-ttu-id="59bcd-168">Les tables temporaires volumineuses peuvent prendre en charge la suppression si elles ont été créées avec JET_bitTTScrollable ou JET_bitTTIndexed.</span><span class="sxs-lookup"><span data-stu-id="59bcd-168">Large temporary tables can support deletion if they were created with JET_bitTTScrollable or JET_bitTTIndexed.</span></span> <span data-ttu-id="59bcd-169">Le seuil auquel une table temporaire devient « grande » est actuellement de 64 kilo-octets, mais elle peut être modifiée dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="59bcd-169">The threshold at which a temporary table becomes "large" is currently 64 kilobytes, but it may be changed in future releases.</span></span>

<span data-ttu-id="59bcd-170">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="59bcd-170">Windows XP and later.</span></span> <span data-ttu-id="59bcd-171">Les fonctions de rappel peuvent être appelées par **JetDelete**, y compris JET_cbtypBeforeDelete et JET_cbtypAfterDelete.</span><span class="sxs-lookup"><span data-stu-id="59bcd-171">Callback functions can be invoked by **JetDelete**, including JET_cbtypBeforeDelete and JET_cbtypAfterDelete.</span></span>

<span data-ttu-id="59bcd-172">Il est important de comprendre l’impact de l’exécution d’un grand nombre d’opérations de mise à jour au sein d’une même transaction.</span><span class="sxs-lookup"><span data-stu-id="59bcd-172">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="59bcd-173">Chaque mise à jour de la base de données doit être suivie par le moteur de base de données dans la Banque des versions.</span><span class="sxs-lookup"><span data-stu-id="59bcd-173">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="59bcd-174">La Banque des versions contient un enregistrement dynamique de toutes les différentes versions de chaque entrée d’enregistrement ou d’index dans la base de données qui peuvent être vues par toutes les transactions actives.</span><span class="sxs-lookup"><span data-stu-id="59bcd-174">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="59bcd-175">Ces versions sont utilisées pour prendre en charge le contrôle d’accès concurrentiel multiversion utilisé par le moteur de base de données pour prendre en charge les transactions à l’aide de l’isolation d’instantané.</span><span class="sxs-lookup"><span data-stu-id="59bcd-175">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="59bcd-176">Une fois que le moteur de base de données a épuisé les ressources utilisées pour stocker ces versions, il ne peut plus accepter de modifications tant que certaines transactions n’ont pas été terminées pour permettre la récupération de ces ressources.</span><span class="sxs-lookup"><span data-stu-id="59bcd-176">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="59bcd-177">Lorsque le moteur est dans cet État, toutes les mises à jour échouent avec JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="59bcd-177">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="59bcd-178">Les ressources disponibles pour le moteur de base de données pour stocker ces versions peuvent être contrôlées à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec *JET_paramMaxVerPages* et *JET_paramGlobalMinVerPages*.</span><span class="sxs-lookup"><span data-stu-id="59bcd-178">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxVerPages* and *JET_paramGlobalMinVerPages*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="59bcd-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59bcd-179">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-180"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="59bcd-180"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="59bcd-181">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="59bcd-181">Requires Windows Vista, Windows XP or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bcd-182"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="59bcd-182"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="59bcd-183">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="59bcd-183">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-184"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="59bcd-184"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="59bcd-185">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="59bcd-185">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59bcd-186"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="59bcd-186"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="59bcd-187">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="59bcd-187">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59bcd-188"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="59bcd-188"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="59bcd-189">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="59bcd-189">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="59bcd-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59bcd-190">See Also</span></span>

[<span data-ttu-id="59bcd-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="59bcd-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="59bcd-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="59bcd-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="59bcd-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="59bcd-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="59bcd-194">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="59bcd-194">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="59bcd-195">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="59bcd-195">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="59bcd-196">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="59bcd-196">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

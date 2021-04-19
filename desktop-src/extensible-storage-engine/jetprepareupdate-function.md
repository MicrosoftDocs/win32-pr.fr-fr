---
description: 'En savoir plus sur : fonction JetPrepareUpdate'
title: JetPrepareUpdate fonction)
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535680"
---
# <a name="jetprepareupdate-function"></a><span data-ttu-id="c6d57-103">JetPrepareUpdate fonction)</span><span class="sxs-lookup"><span data-stu-id="c6d57-103">JetPrepareUpdate Function</span></span>


<span data-ttu-id="c6d57-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c6d57-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprepareupdate-function"></a><span data-ttu-id="c6d57-105">JetPrepareUpdate fonction)</span><span class="sxs-lookup"><span data-stu-id="c6d57-105">JetPrepareUpdate Function</span></span>

<span data-ttu-id="c6d57-106">La fonction **JetPrepareUpdate** est la première opération d’exécution d’une mise à jour, dans le cadre de l’insertion d’un nouvel enregistrement ou du remplacement d’un enregistrement existant par de nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="c6d57-106">The **JetPrepareUpdate** function is the first operation in performing an update, for the purposes of inserting a new record or replacing an existing record with new values.</span></span> <span data-ttu-id="c6d57-107">Les mises à jour sont effectuées en appelant **JetPrepareUpdate**, puis en appelant [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) zéro, une ou plusieurs fois et enfin en appelant [JetUpdate](./jetupdate-function.md) pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="c6d57-107">Updates are done by calling **JetPrepareUpdate**, then calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) zero or more times and finally by calling [JetUpdate](./jetupdate-function.md) to complete the operation.</span></span> <span data-ttu-id="c6d57-108">**JetPrepareUpdate** et [JetUpdate](./jetupdate-function.md) définissent les limites d’une opération de mise à jour et sont importants pour que seul l’état de mise à jour final d’un enregistrement soit entré dans les index.</span><span class="sxs-lookup"><span data-stu-id="c6d57-108">**JetPrepareUpdate** and [JetUpdate](./jetupdate-function.md) set the boundaries for an update operation and are important in having only the final update state of a record entered into indexes.</span></span> <span data-ttu-id="c6d57-109">Cela est à la fois plus efficace, mais également requis dans les cas où les données doivent correspondre à un état valide par rapport à l’opération de définition de colonne.</span><span class="sxs-lookup"><span data-stu-id="c6d57-109">This is both more efficient, but also required in cases where data must match a valid state through more than on set column operation.</span></span>

<span data-ttu-id="c6d57-110">Il existe différentes options pour l’insertion ou le remplacement des enregistrements, et elles sont décrites plus en détail ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c6d57-110">There are a few different options for inserting or replacing records and they are described in more detail below.</span></span>

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a><span data-ttu-id="c6d57-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6d57-111">Parameters</span></span>

<span data-ttu-id="c6d57-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c6d57-112">*sesid*</span></span>

<span data-ttu-id="c6d57-113">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="c6d57-113">The session to use for this call.</span></span>

<span data-ttu-id="c6d57-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c6d57-114">*tableid*</span></span>

<span data-ttu-id="c6d57-115">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="c6d57-115">The cursor to use for this call.</span></span>

<span data-ttu-id="c6d57-116">*préparation*</span><span class="sxs-lookup"><span data-stu-id="c6d57-116">*prep*</span></span>

<span data-ttu-id="c6d57-117">Options qui peuvent être utilisées pour préparer une mise à jour, notamment les suivantes.</span><span class="sxs-lookup"><span data-stu-id="c6d57-117">The options that can be used to prepare for an update, which include the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6d57-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6d57-118">Value</span></span></p></th>
<th><p><span data-ttu-id="c6d57-119">Signification</span><span class="sxs-lookup"><span data-stu-id="c6d57-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-120">JET_prepCancel</span><span class="sxs-lookup"><span data-stu-id="c6d57-120">JET_prepCancel</span></span></p></td>
<td><p><span data-ttu-id="c6d57-121">Cet indicateur Force <strong>JetPrepareUpdate</strong> à annuler la mise à jour pour ce curseur.</span><span class="sxs-lookup"><span data-stu-id="c6d57-121">This flag causes <strong>JetPrepareUpdate</strong> to cancel the update for this cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-122">JET_prepInsert</span><span class="sxs-lookup"><span data-stu-id="c6d57-122">JET_prepInsert</span></span></p></td>
<td><p><span data-ttu-id="c6d57-123">Cet indicateur force le curseur à préparer une insertion d’un nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c6d57-123">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="c6d57-124">Toutes les données sont initialisées à l’État par défaut de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c6d57-124">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="c6d57-125">Si la table comporte une colonne à incrémentation automatique, une nouvelle valeur est affectée à cet enregistrement, que la mise à jour réussisse ou non, échoue ou est annulée.</span><span class="sxs-lookup"><span data-stu-id="c6d57-125">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-126">JET_prepInsertCopy</span><span class="sxs-lookup"><span data-stu-id="c6d57-126">JET_prepInsertCopy</span></span></p></td>
<td><p><span data-ttu-id="c6d57-127">Cet indicateur force le curseur à préparer une insertion d’une copie de l’enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="c6d57-127">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="c6d57-128">Il doit y avoir un enregistrement actif si cette option est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c6d57-128">There must be a current record if this option is used.</span></span> <span data-ttu-id="c6d57-129">L’état initial du nouvel enregistrement est copié à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="c6d57-129">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="c6d57-130">Les valeurs longues qui sont stockées hors enregistrement sont virtuellement copiées.</span><span class="sxs-lookup"><span data-stu-id="c6d57-130">Long values that are stored off-record are virtually copied.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-131">JET_prepInsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="c6d57-131">JET_prepInsertCopyDeleteOriginal</span></span></p></td>
<td><p><span data-ttu-id="c6d57-132">Cet indicateur force le curseur à préparer une insertion du même enregistrement, ainsi qu’une suppression ou l’enregistrement d’origine.</span><span class="sxs-lookup"><span data-stu-id="c6d57-132">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="c6d57-133">Il est utilisé dans les cas où la clé primaire a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="c6d57-133">It is used in cases in which the primary key has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-134">JET_prepReplace</span><span class="sxs-lookup"><span data-stu-id="c6d57-134">JET_prepReplace</span></span></p></td>
<td><p><span data-ttu-id="c6d57-135">Cet indicateur force le curseur à préparer un remplacement de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="c6d57-135">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="c6d57-136">Si la table contient une colonne version, la colonne version est définie sur la valeur suivante dans sa séquence.</span><span class="sxs-lookup"><span data-stu-id="c6d57-136">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="c6d57-137">Si cette mise à jour ne se termine pas, la valeur de la version dans l’enregistrement n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="c6d57-137">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="c6d57-138">Un verrou de mise à jour est appliqué à l’enregistrement pour empêcher d’autres sessions de mettre à jour cet enregistrement avant la fin de cette session.</span><span class="sxs-lookup"><span data-stu-id="c6d57-138">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-139">JET_prepReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="c6d57-139">JET_prepReplaceNoLock</span></span></p></td>
<td><p><span data-ttu-id="c6d57-140">Cet indicateur est similaire à JET_prepReplace, mais aucun verrou n’est pris pour empêcher d’autres sessions de mettre à jour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c6d57-140">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="c6d57-141">Au lieu de cela, cette session peut recevoir des JET_errWriteConflict lorsqu’elle appelle <a href="gg269288(v=exchg.10).md">JetUpdate</a> pour terminer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c6d57-141">Instead, this session may receive JET_errWriteConflict when it calls <a href="gg269288(v=exchg.10).md">JetUpdate</a> to complete the update.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c6d57-142">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c6d57-142">Return Value</span></span>

<span data-ttu-id="c6d57-143">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="c6d57-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c6d57-144">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c6d57-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6d57-145">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c6d57-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="c6d57-146">Description</span><span class="sxs-lookup"><span data-stu-id="c6d57-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c6d57-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c6d57-148">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c6d57-148">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-149">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="c6d57-149">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="c6d57-150"><strong>JetPrepareUpdate</strong> a été appelé avec un indicateur valide pour PREP mais pas JET_prepCancel et le curseur était déjà à l’état préparé.</span><span class="sxs-lookup"><span data-stu-id="c6d57-150"><strong>JetPrepareUpdate</strong> was called with a valid flag for prep but not JET_prepCancel and the cursor was already in the prepared state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-151">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c6d57-151">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c6d57-152">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c6d57-152">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-153">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c6d57-153">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c6d57-154">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="c6d57-154">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c6d57-155">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c6d57-155">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c6d57-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c6d57-157">L’indicateur PREP donné n’est pas un indicateur valide.</span><span class="sxs-lookup"><span data-stu-id="c6d57-157">The given prep flag is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c6d57-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c6d57-159">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="c6d57-159">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-160">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="c6d57-160">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="c6d57-161"><strong>JetPrepareUpdate</strong> a été appelé pour remplacer un enregistrement qui avait des colonnes SLV.</span><span class="sxs-lookup"><span data-stu-id="c6d57-161"><strong>JetPrepareUpdate</strong> was called to replace a record which had SLV columns.</span></span> <span data-ttu-id="c6d57-162">Colonnes SLV.</span><span class="sxs-lookup"><span data-stu-id="c6d57-162">SLV columns.</span></span> <span data-ttu-id="c6d57-163">Notez que les colonnes SLV sont une fonctionnalité qui n’est pas destinée à une utilisation générale.</span><span class="sxs-lookup"><span data-stu-id="c6d57-163">Please note that SLV columns are a feature not intended for general usage.</span></span> <span data-ttu-id="c6d57-164">Cette fonctionnalité est utilisée pour prendre en charge l’infrastructure Microsoft Exchange et n’est pas destinée à être utilisée dans votre application.</span><span class="sxs-lookup"><span data-stu-id="c6d57-164">This feature is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c6d57-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c6d57-166">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="c6d57-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-167">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="c6d57-167">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="c6d57-168"><strong>JetPrepareUpdate</strong> a été appelé avec JET_prepCancel mais n’a pas pu restaurer toutes les modifications apportées aux colonnes de type JET_coltypLongText et/ou les colonnes de type JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="c6d57-168"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but could not rollback all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c6d57-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c6d57-170">Cet indicateur ne peut pas être utilisé avec la même session à partir de plusieurs threads en même temps.</span><span class="sxs-lookup"><span data-stu-id="c6d57-170">This flag cannot be used with the same session from more than one thread at the same time.</span></span> <span data-ttu-id="c6d57-171">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c6d57-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c6d57-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c6d57-173">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="c6d57-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-174">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="c6d57-174">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="c6d57-175"><strong>JetPrepareUpdate</strong> a été appelé avec JET_prepCancel mais le curseur n’était pas dans l’état préparé.</span><span class="sxs-lookup"><span data-stu-id="c6d57-175"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c6d57-176">En cas de réussite, le curseur passe à l’état préparé dans le cadre de la mise à jour souhaitée, ou dans le cas de JET_prepCancel, le curseur est rétabli à l’état non préparé et toutes les modifications sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="c6d57-176">On success, the cursor is changed to the prepared state for the purpose of the desired update, or in the case of JET_prepCancel, the cursor is reverted to the non-prepared state and any changes are discarded.</span></span>

<span data-ttu-id="c6d57-177">En cas d’échec, l’état du curseur reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="c6d57-177">On failure, the cursor state is left unchanged.</span></span> <span data-ttu-id="c6d57-178">Si l’échec a été JET_errRollbackError, l’état du curseur passe à l’état non préparé, mais les modifications ne sont pas toutes annulées.</span><span class="sxs-lookup"><span data-stu-id="c6d57-178">If the failure was JET_errRollbackError then the cursor state is changed to the non-prepared state but not all of the changes have been reverted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c6d57-179">Notes</span><span class="sxs-lookup"><span data-stu-id="c6d57-179">Remarks</span></span>

<span data-ttu-id="c6d57-180">L’insertion d’une copie d’un enregistrement est une optimisation importante lorsque les enregistrements partagent des données de type JET_coltypLongText et/ou JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="c6d57-180">Inserting a copy of a record is an important optimization when records share data of type JET_coltypLongText and/or JET_coltypLongBinary.</span></span> <span data-ttu-id="c6d57-181">Ces données sont stockées hors-enregistrement lorsqu’elles sont volumineuses et il est possible que plusieurs enregistrements partagent la même représentation physique des données.</span><span class="sxs-lookup"><span data-stu-id="c6d57-181">This data is stored off-record when large and it is possible for multiple records to share the same physical representation of the data.</span></span> <span data-ttu-id="c6d57-182">Dans ce cas, les données peuvent être mises à jour à partir de l’un ou l’autre enregistrement, mais cela entraînera une rafale des données, de sorte que chaque enregistrement possède sa propre copie.</span><span class="sxs-lookup"><span data-stu-id="c6d57-182">In this case, the data can be updated from either record, but doing so will cause the data to be burst such that each record has its own copy.</span></span> <span data-ttu-id="c6d57-183">Il n’est pas possible de modifier les données d’un enregistrement par une modification d’un autre enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c6d57-183">It is not possible to change data in one record by a modification from another record.</span></span> <span data-ttu-id="c6d57-184">En outre, il n’est pas possible de bloquer la mise à jour d’un enregistrement à l’aide d’une mise à jour d’un autre enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c6d57-184">Also, it is not possible to block an update of one record by an update of another record.</span></span> <span data-ttu-id="c6d57-185">Il s’agit d’une fonctionnalité centrale de ESE qui porte le nom de verrouillage au niveau des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c6d57-185">This is a central feature to ESE and is known as Record Level Locking.</span></span>

<span data-ttu-id="c6d57-186">Les opérations [JetUpdate](./jetupdate-function.md) qui échouent laissent le curseur dans l’état préparé de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c6d57-186">[JetUpdate](./jetupdate-function.md) operations which fail leave the cursor in the update prepared state.</span></span> <span data-ttu-id="c6d57-187">Cela permet de corriger certaines erreurs, telles qu’une valeur de colonne incorrecte, sans nécessiter la recréation de l’état de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c6d57-187">This is to permit correction to some errors, such as a wrong column value, without requiring the update state to be recreated.</span></span> <span data-ttu-id="c6d57-188">Cela signifie que dans tous les cas où un curseur abandonne une mise à jour, il doit explicitement appeler **JetPrepareUpdate** avec JET_prepCancel.</span><span class="sxs-lookup"><span data-stu-id="c6d57-188">This means that in all cases where a cursor abandons an update, it must explicitly call **JetPrepareUpdate** with JET_prepCancel.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c6d57-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6d57-189">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-190"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c6d57-190"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c6d57-191">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="c6d57-191">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-192"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="c6d57-192"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c6d57-193">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c6d57-193">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-194"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="c6d57-194"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c6d57-195">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="c6d57-195">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6d57-196"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="c6d57-196"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c6d57-197">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c6d57-197">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6d57-198"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c6d57-198"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c6d57-199">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c6d57-199">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c6d57-200">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6d57-200">See Also</span></span>

[<span data-ttu-id="c6d57-201">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c6d57-201">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c6d57-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c6d57-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c6d57-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c6d57-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c6d57-204">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="c6d57-204">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="c6d57-205">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="c6d57-205">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="c6d57-206">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="c6d57-206">JetUpdate</span></span>](./jetupdate-function.md)

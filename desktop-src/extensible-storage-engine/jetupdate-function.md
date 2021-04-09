---
description: 'En savoir plus sur : fonction JetUpdate'
title: Fonction JetUpdate
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38e17c5bc5ac32ab3b904456f2d97aa465fca670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862893"
---
# <a name="jetupdate-function"></a><span data-ttu-id="ec320-103">Fonction JetUpdate</span><span class="sxs-lookup"><span data-stu-id="ec320-103">JetUpdate Function</span></span>


<span data-ttu-id="ec320-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="ec320-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate-function"></a><span data-ttu-id="ec320-105">Fonction JetUpdate</span><span class="sxs-lookup"><span data-stu-id="ec320-105">JetUpdate Function</span></span>

<span data-ttu-id="ec320-106">La fonction **JetUpdate** effectue une opération de mise à jour, notamment l’insertion d’une nouvelle ligne dans une table ou la mise à jour d’une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="ec320-106">The **JetUpdate** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="ec320-107">La suppression d’une ligne de table s’effectue en appelant [JetDelete](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="ec320-107">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="ec320-108">**JetUpdate** est la dernière étape de l’exécution d’une instruction INSERT ou Update.</span><span class="sxs-lookup"><span data-stu-id="ec320-108">**JetUpdate** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="ec320-109">La mise à jour commence par appeler [JetPrepareUpdate](./jetprepareupdate-function.md) , puis en appelant [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) une ou plusieurs fois pour définir l’état de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ec320-109">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="ec320-110">Enfin, **JetUpdate** est appelé pour terminer l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ec320-110">Finally, **JetUpdate** is called to complete the update operation.</span></span> <span data-ttu-id="ec320-111">Les index sont mis à jour uniquement par **JetUpdate** ou [JetUpdate2](./jetupdate2-function.md), et non pendant [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="ec320-111">Indexes are updated only by **JetUpdate** or [JetUpdate2](./jetupdate2-function.md), and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="ec320-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec320-112">Parameters</span></span>

<span data-ttu-id="ec320-113">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ec320-113">*sesid*</span></span>

<span data-ttu-id="ec320-114">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="ec320-114">The session to use for this call.</span></span>

<span data-ttu-id="ec320-115">*TableID*</span><span class="sxs-lookup"><span data-stu-id="ec320-115">*tableid*</span></span>

<span data-ttu-id="ec320-116">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="ec320-116">The cursor to use for this call.</span></span>

<span data-ttu-id="ec320-117">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="ec320-117">*pvBookmark*</span></span>

<span data-ttu-id="ec320-118">Pointeur vers un signet retourné pour une ligne insérée.</span><span class="sxs-lookup"><span data-stu-id="ec320-118">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="ec320-119">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="ec320-119">*cbBookmark*</span></span>

<span data-ttu-id="ec320-120">Taille de la mémoire tampon vers laquelle pointe *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="ec320-120">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="ec320-121">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="ec320-121">*pcbActual*</span></span>

<span data-ttu-id="ec320-122">Taille retournée du signet pour la ligne insérée retournée dans *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="ec320-122">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

### <a name="return-value"></a><span data-ttu-id="ec320-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ec320-123">Return Value</span></span>

<span data-ttu-id="ec320-124">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="ec320-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ec320-125">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ec320-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec320-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ec320-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="ec320-127">Description</span><span class="sxs-lookup"><span data-stu-id="ec320-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec320-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ec320-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ec320-129">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ec320-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-130">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="ec320-130">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="ec320-131">La mémoire tampon donnée pour le signet d’enregistrement n’est pas suffisamment grande pour stocker le signet de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ec320-131">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ec320-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ec320-133">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="ec320-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-134">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="ec320-134">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="ec320-135">Identique à JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="ec320-135">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-136">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="ec320-136">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="ec320-137">L’opération de mise à jour nécessite la croissance du fichier de base de données ou l’allocation des fichiers journaux, mais le lecteur de disque où se trouve le fichier de base de données ou la série de journaux est plein.</span><span class="sxs-lookup"><span data-stu-id="ec320-137">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="ec320-138">Sinon, le fichier de base de données se trouve sur un volume au format FAT32 et le fichier de base de données est déjà 4GBytes, la limite par fichier pour FAT32.</span><span class="sxs-lookup"><span data-stu-id="ec320-138">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ec320-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ec320-140">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="ec320-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="ec320-141"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ec320-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ec320-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ec320-143">Le paramètre <em>PREP</em> donné dans la fonction <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> n’est pas un indicateur valide.</span><span class="sxs-lookup"><span data-stu-id="ec320-143">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-144">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="ec320-144">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="ec320-145">Une clé d’index pour cet enregistrement est un doublon d’une autre clé d’index pour un autre enregistrement déjà dans la table et l’index n’autorise pas les doublons.</span><span class="sxs-lookup"><span data-stu-id="ec320-145">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-146">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="ec320-146">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="ec320-147">L’enregistrement inséré ou mis à jour a un ou plusieurs index pour lesquels la clé générée aurait dépassé la taille maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="ec320-147">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="ec320-148">Par conséquent, l’opération n’a pas pu empêcher la troncation de clé.</span><span class="sxs-lookup"><span data-stu-id="ec320-148">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-149">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="ec320-149">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="ec320-150">L’enregistrement inséré ou mis à jour a une colonne à valeurs multiples indexée avec au moins deux valeurs qui sont identiques dans la taille de clé de longueur maximale définie pour l’index.</span><span class="sxs-lookup"><span data-stu-id="ec320-150">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="ec320-151">Par conséquent, l’enregistrement a deux entrées identiques dans l’index, ce qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ec320-151">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ec320-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ec320-153">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="ec320-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-154">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="ec320-154">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="ec320-155">Une ou plusieurs colonnes de l’enregistrement à insérer ou à l’État mis à jour d’un enregistrement en cours de remplacement sont <strong>null</strong> , ce qui viole la contrainte définie pour ces colonnes.</span><span class="sxs-lookup"><span data-stu-id="ec320-155">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-156">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="ec320-156">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="ec320-157">Un ou plusieurs index sont définis de façon à ne pas autoriser une clé <strong>null</strong> et l’état inséré ou mis à jour d’un enregistrement qui est remplacé viole cette contrainte définie.</span><span class="sxs-lookup"><span data-stu-id="ec320-157">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-158">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="ec320-158">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="ec320-159">Une opération de remplacement d’enregistrement a mis à jour la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="ec320-159">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="ec320-160">Les mises à jour des colonnes clés primaires doivent être effectuées par le biais de la suppression de l’enregistrement existant et de l’insertion d’un nouvel enregistrement avec les données souhaitées.</span><span class="sxs-lookup"><span data-stu-id="ec320-160">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ec320-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ec320-162">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="ec320-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="ec320-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="ec320-164">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="ec320-164">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="ec320-165"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ec320-165"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ec320-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ec320-167">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ec320-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-168">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="ec320-168">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="ec320-169">Il n’est pas autorisé de tenter une mise à jour dans l’étendue d’une transaction en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ec320-169">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="ec320-170">Une transaction en lecture seule est une transaction qui a été démarrée à l’aide d’un appel à <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> avec JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="ec320-170">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="ec320-171"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ec320-171"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-172">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="ec320-172">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="ec320-173"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> a été appelé avec JET_prepCancel mais le curseur n’était pas dans l’état préparé.</span><span class="sxs-lookup"><span data-stu-id="ec320-173"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-174">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="ec320-174">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="ec320-175">L’opération a échoué, car il n’y a pas assez de mémoire pour conserver les informations transactionnelles sur la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ec320-175">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-176">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ec320-176">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="ec320-177">Une autre session a déjà verrouillé l’enregistrement pour la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ec320-177">Another session has previously locked the record for update.</span></span> <span data-ttu-id="ec320-178">La mise à jour tentée par cette session échoue.</span><span class="sxs-lookup"><span data-stu-id="ec320-178">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec320-179">En cas de réussite, l’opération d’ouverture de mise à jour sur le curseur est terminée.</span><span class="sxs-lookup"><span data-stu-id="ec320-179">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="ec320-180">Si une colonne d’incrémentation automatique est définie pour la table, cette valeur est définie pour les enregistrements insérés.</span><span class="sxs-lookup"><span data-stu-id="ec320-180">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="ec320-181">Si une colonne version est définie pour la table, sa valeur est initialisée pour les enregistrements nouvellement insérés, ou incrémentée chaque fois qu’un enregistrement est remplacé.</span><span class="sxs-lookup"><span data-stu-id="ec320-181">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="ec320-182">Tous les index, y compris les index cluster et non cluster, sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="ec320-182">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="ec320-183">En cas d’échec, aucune modification de type n’est apportée à la base de données.</span><span class="sxs-lookup"><span data-stu-id="ec320-183">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="ec320-184">Avant que les fonctions de rappel Insert et Before Replace aient été appelées, mais après l’appel d’insert et after Replace, les rappels n’auront pas été appelés, puisque ce dernier ne peut pas provoquer l’échec d’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ec320-184">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="ec320-185">Le tampon de copie de curseur reste dans son état préparé, afin que l’opportunité existe pour corriger de façon incrémentielle les problèmes qui ont provoqué des erreurs et retenter l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ec320-185">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ec320-186">Notes</span><span class="sxs-lookup"><span data-stu-id="ec320-186">Remarks</span></span>

<span data-ttu-id="ec320-187">Les fonctions de rappel peuvent être inscrites pour être appelées avant ou après l’insertion, et avant ou après la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ec320-187">Callback functions can be registered to be called before or after insert, and before or after update.</span></span>

<span data-ttu-id="ec320-188">Les limitations de taille d’enregistrement sont appliquées par [JetSetColumn](./jetsetcolumn-function.md), et non en général par **JetUpdate**.</span><span class="sxs-lookup"><span data-stu-id="ec320-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by **JetUpdate**.</span></span>

<span data-ttu-id="ec320-189">Il est important de comprendre l’impact de l’exécution d’un grand nombre d’opérations de mise à jour au sein d’une même transaction.</span><span class="sxs-lookup"><span data-stu-id="ec320-189">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="ec320-190">Chaque mise à jour de la base de données doit être suivie par le moteur de base de données dans la Banque des versions.</span><span class="sxs-lookup"><span data-stu-id="ec320-190">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="ec320-191">La Banque des versions contient un enregistrement dynamique de toutes les différentes versions de chaque entrée d’enregistrement ou d’index dans la base de données qui peuvent être vues par toutes les transactions actives.</span><span class="sxs-lookup"><span data-stu-id="ec320-191">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="ec320-192">Ces versions sont utilisées pour prendre en charge le contrôle d’accès concurrentiel multiversion utilisé par le moteur de base de données pour prendre en charge les transactions à l’aide de l’isolation d’instantané.</span><span class="sxs-lookup"><span data-stu-id="ec320-192">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="ec320-193">Une fois que le moteur de base de données a épuisé les ressources utilisées pour stocker ces versions, il ne peut plus accepter de modifications tant que certaines transactions n’ont pas été terminées pour permettre la récupération de ces ressources.</span><span class="sxs-lookup"><span data-stu-id="ec320-193">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="ec320-194">Lorsque le moteur est dans cet État, toutes les mises à jour échouent avec JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ec320-194">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="ec320-195">Les ressources disponibles pour le moteur de base de données pour stocker ces versions peuvent être contrôlées à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec [JET_paramMaxVerPages](./resource-parameters.md) et [JET_paramGlobalMinVerPages](./resource-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ec320-195">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramMaxVerPages](./resource-parameters.md) and [JET_paramGlobalMinVerPages](./resource-parameters.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="ec320-196">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec320-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec320-197"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ec320-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ec320-198">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="ec320-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-199"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="ec320-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ec320-200">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ec320-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-201"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="ec320-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ec320-202">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="ec320-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec320-203"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="ec320-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ec320-204">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ec320-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec320-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ec320-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ec320-206">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ec320-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ec320-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec320-207">See Also</span></span>

[<span data-ttu-id="ec320-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ec320-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ec320-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ec320-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ec320-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ec320-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ec320-211">JetDelete</span><span class="sxs-lookup"><span data-stu-id="ec320-211">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="ec320-212">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="ec320-212">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="ec320-213">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="ec320-213">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="ec320-214">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="ec320-214">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="ec320-215">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="ec320-215">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="ec320-216">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="ec320-216">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="ec320-217">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="ec320-217">JetSetColumns</span></span>](./jetsetcolumns-function.md)  
[<span data-ttu-id="ec320-218">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="ec320-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="ec320-219">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="ec320-219">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

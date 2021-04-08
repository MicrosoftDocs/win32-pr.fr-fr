---
description: 'En savoir plus sur : fonction JetUpdate2'
title: Fonction JetUpdate2
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750476"
---
# <a name="jetupdate2-function"></a><span data-ttu-id="2dcd0-103">Fonction JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="2dcd0-103">JetUpdate2 Function</span></span>


<span data-ttu-id="2dcd0-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2dcd0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate2-function"></a><span data-ttu-id="2dcd0-105">Fonction JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="2dcd0-105">JetUpdate2 Function</span></span>

<span data-ttu-id="2dcd0-106">La fonction **JetUpdate2** effectue une opération de mise à jour, notamment l’insertion d’une nouvelle ligne dans une table ou la mise à jour d’une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-106">The **JetUpdate2** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="2dcd0-107">Cette fonction contient une liste d’options *Grbit* qui peuvent être définies lors de l’exécution d’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-107">This function contains a list of *grbit* options that can be set while performing an update.</span></span> <span data-ttu-id="2dcd0-108">La suppression d’une ligne de table s’effectue en appelant [JetDelete](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="2dcd0-108">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="2dcd0-109">**Windows server 2003 : JetUpdate2** est introduit dans windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-109">**Windows Server 2003:  JetUpdate2** is introduced in Windows Server 2003.</span></span>

<span data-ttu-id="2dcd0-110">**JetUpdate2** est la dernière étape de l’exécution d’une instruction INSERT ou Update.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-110">**JetUpdate2** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="2dcd0-111">La mise à jour commence par appeler [JetPrepareUpdate](./jetprepareupdate-function.md) , puis en appelant [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) une ou plusieurs fois pour définir l’état de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-111">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="2dcd0-112">Enfin, **JetUpdate2** est appelé pour terminer l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-112">Finally, **JetUpdate2** is called to complete the update operation.</span></span> <span data-ttu-id="2dcd0-113">Les index sont mis à jour uniquement par [JetUpdate](./jetupdate-function.md) ou **JetUpdate2**, et non pendant [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="2dcd0-113">Indexes are updated only by [JetUpdate](./jetupdate-function.md) or **JetUpdate2**, and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="2dcd0-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2dcd0-114">Parameters</span></span>

<span data-ttu-id="2dcd0-115">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2dcd0-115">*sesid*</span></span>

<span data-ttu-id="2dcd0-116">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-116">The session to use for this call.</span></span>

<span data-ttu-id="2dcd0-117">*TableID*</span><span class="sxs-lookup"><span data-stu-id="2dcd0-117">*tableid*</span></span>

<span data-ttu-id="2dcd0-118">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-118">The cursor to use for this call.</span></span>

<span data-ttu-id="2dcd0-119">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="2dcd0-119">*pvBookmark*</span></span>

<span data-ttu-id="2dcd0-120">Pointeur vers un signet retourné pour une ligne insérée.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-120">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="2dcd0-121">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="2dcd0-121">*cbBookmark*</span></span>

<span data-ttu-id="2dcd0-122">Taille de la mémoire tampon vers laquelle pointe *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-122">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="2dcd0-123">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="2dcd0-123">*pcbActual*</span></span>

<span data-ttu-id="2dcd0-124">Taille retournée du signet pour la ligne insérée retournée dans *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-124">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

<span data-ttu-id="2dcd0-125">*grbit*</span><span class="sxs-lookup"><span data-stu-id="2dcd0-125">*grbit*</span></span>

<span data-ttu-id="2dcd0-126">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-126">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2dcd0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2dcd0-127">Value</span></span></p></th>
<th><p><span data-ttu-id="2dcd0-128">Signification</span><span class="sxs-lookup"><span data-stu-id="2dcd0-128">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-129">JET_bitUpdateCheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="2dcd0-129">JET_bitUpdateCheckESE97Compatibility</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-130">Cet indicateur force la mise à jour à retourner une erreur si la mise à jour n’aurait pas été possible dans la version Windows 2000 de ESE, qui appliquait un nombre maximal d’instances de colonne à valeurs multiples dans chaque enregistrement que les versions ultérieures de ESE.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-130">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="2dcd0-131">Cela est important uniquement pour les applications qui souhaitent répliquer des données entre des applications hébergées sur Windows 2000 et des applications hébergées sur Windows Server 2003 ou des versions ultérieures de ESE.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-131">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows Server 2003, or later versions of ESE.</span></span> <span data-ttu-id="2dcd0-132">Elle ne doit pas être nécessaire pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-132">It should not be necessary for most applications.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2dcd0-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2dcd0-133">Return Value</span></span>

<span data-ttu-id="2dcd0-134">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2dcd0-135">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2dcd0-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2dcd0-136">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2dcd0-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="2dcd0-137">Description</span><span class="sxs-lookup"><span data-stu-id="2dcd0-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2dcd0-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-139">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-140">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="2dcd0-140">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-141">La mémoire tampon donnée pour le signet d’enregistrement n’est pas suffisamment grande pour stocker le signet de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-141">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-142">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2dcd0-142">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-143">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-143">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-144">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="2dcd0-144">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-145">L’opération de mise à jour nécessite la croissance du fichier de base de données ou l’allocation des fichiers journaux, mais le lecteur de disque où se trouve le fichier de base de données ou la série de journaux est plein.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-145">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="2dcd0-146">Sinon, le fichier de base de données se trouve sur un volume au format FAT32 et le fichier de base de données est déjà 4GBytes, la limite par fichier pour FAT32.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-146">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2dcd0-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-148">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="2dcd0-149"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-149"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2dcd0-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-151">Le paramètre <em>PREP</em> donné dans la fonction <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> n’est pas un indicateur valide.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-151">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-152">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="2dcd0-152">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-153">Une clé d’index pour cet enregistrement est un doublon d’une autre clé d’index pour un autre enregistrement déjà dans la table et l’index n’autorise pas les doublons.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-153">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-154">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="2dcd0-154">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-155">L’enregistrement inséré ou mis à jour a un ou plusieurs index pour lesquels la clé générée aurait dépassé la taille maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-155">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="2dcd0-156">Par conséquent, l’opération n’a pas pu empêcher la troncation de clé.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-156">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-157">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="2dcd0-157">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-158">L’enregistrement inséré ou mis à jour a une colonne à valeurs multiples indexée avec au moins deux valeurs qui sont identiques dans la taille de clé de longueur maximale définie pour l’index.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-158">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="2dcd0-159">Par conséquent, l’enregistrement a deux entrées identiques dans l’index, ce qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-159">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2dcd0-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-161">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-162">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="2dcd0-162">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-163">Une ou plusieurs colonnes de l’enregistrement à insérer ou à l’État mis à jour d’un enregistrement en cours de remplacement sont <strong>null</strong> , ce qui viole la contrainte définie pour ces colonnes.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-163">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-164">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="2dcd0-164">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-165">Un ou plusieurs index sont définis de façon à ne pas autoriser une clé <strong>null</strong> et l’état inséré ou mis à jour d’un enregistrement qui est remplacé viole cette contrainte définie.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-165">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-166">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="2dcd0-166">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-167">Une opération de remplacement d’enregistrement a mis à jour la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-167">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="2dcd0-168">Les mises à jour des colonnes clés primaires doivent être effectuées par le biais de la suppression de l’enregistrement existant et de l’insertion d’un nouvel enregistrement avec les données souhaitées.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-168">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-169">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2dcd0-169">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-170">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-170">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-171">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="2dcd0-171">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-172">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-172">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="2dcd0-173"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-173"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2dcd0-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-175">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-176">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="2dcd0-176">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-177"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> a été appelé avec JET_prepCancel mais le curseur n’était pas dans l’état préparé.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-177"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-178">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="2dcd0-178">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="2dcd0-179">Une opération de remplacement d’enregistrement pour laquelle un verrou d’écriture n’a pas déjà été alloué peut rencontrer un conflit d’écriture au moment de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-179">A record replacement operation for which a write lock was not already allocated can encounter a write conflict at the time of update.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2dcd0-180">En cas de réussite, l’opération d’ouverture de mise à jour sur le curseur est terminée.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-180">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="2dcd0-181">Si une colonne d’incrémentation automatique est définie pour la table, cette valeur est définie pour les enregistrements insérés.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-181">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="2dcd0-182">Si une colonne version est définie pour la table, sa valeur est initialisée pour les enregistrements nouvellement insérés, ou incrémentée chaque fois qu’un enregistrement est remplacé.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-182">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="2dcd0-183">Tous les index, y compris les index cluster et non cluster, sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-183">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="2dcd0-184">En cas d’échec, aucune modification de type n’est apportée à la base de données.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-184">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="2dcd0-185">Avant que les fonctions de rappel Insert et Before Replace aient été appelées, mais après l’appel d’insert et after Replace, les rappels n’auront pas été appelés, puisque ce dernier ne peut pas provoquer l’échec d’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-185">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="2dcd0-186">Le tampon de copie de curseur reste dans son état préparé, afin que l’opportunité existe pour corriger de façon incrémentielle les problèmes qui ont provoqué des erreurs et retenter l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-186">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2dcd0-187">Notes</span><span class="sxs-lookup"><span data-stu-id="2dcd0-187">Remarks</span></span>

<span data-ttu-id="2dcd0-188">Les limitations de taille d’enregistrement sont appliquées par [JetSetColumn](./jetsetcolumn-function.md), et non en général par [JetUpdate](./jetupdate-function.md).</span><span class="sxs-lookup"><span data-stu-id="2dcd0-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by [JetUpdate](./jetupdate-function.md).</span></span> <span data-ttu-id="2dcd0-189">La seule exception est lorsque l’indicateur de compatibilité JET_bitUpdateCheckESE97Compatibility est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-189">The only exception is when the JET_bitUpdateCheckESE97Compatibility compatibility flag is being used.</span></span> <span data-ttu-id="2dcd0-190">Dans ce cas, l’enregistrement entier est vérifié, car une opération [JetSetColumn](./jetsetcolumn-function.md) individuelle qui a dépassé la limite peut être compensée par un appel ultérieur à [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="2dcd0-190">In this case, the whole record is checked since an individual [JetSetColumn](./jetsetcolumn-function.md) operation that exceeded the limit may be compensated by a subsequent call to [JetSetColumn](./jetsetcolumn-function.md).</span></span>

<span data-ttu-id="2dcd0-191">Pour plus d’informations, consultez la section Notes dans [JetUpdate](./jetupdate-function.md) .</span><span class="sxs-lookup"><span data-stu-id="2dcd0-191">See the Remarks section in [JetUpdate](./jetupdate-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2dcd0-192">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dcd0-192">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-193"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2dcd0-193"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2dcd0-194">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-194">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-195"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2dcd0-195"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2dcd0-196">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-196">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-197"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2dcd0-197"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2dcd0-198">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-198">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcd0-199"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="2dcd0-199"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2dcd0-200">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-200">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcd0-201"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2dcd0-201"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2dcd0-202">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2dcd0-202">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2dcd0-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dcd0-203">See Also</span></span>

[<span data-ttu-id="2dcd0-204">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2dcd0-204">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2dcd0-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2dcd0-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2dcd0-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2dcd0-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2dcd0-207">JetDelete</span><span class="sxs-lookup"><span data-stu-id="2dcd0-207">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="2dcd0-208">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="2dcd0-208">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="2dcd0-209">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="2dcd0-209">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="2dcd0-210">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="2dcd0-210">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="2dcd0-211">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="2dcd0-211">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="2dcd0-212">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="2dcd0-212">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="2dcd0-213">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="2dcd0-213">JetSetColumns</span></span>](./jetsetcolumns-function.md)

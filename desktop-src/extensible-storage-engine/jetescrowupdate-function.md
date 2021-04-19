---
description: 'En savoir plus sur : fonction JetEscrowUpdate'
title: Fonction JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534691"
---
# <a name="jetescrowupdate-function"></a><span data-ttu-id="95060-103">Fonction JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="95060-103">JetEscrowUpdate Function</span></span>


<span data-ttu-id="95060-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="95060-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetescrowupdate-function"></a><span data-ttu-id="95060-105">Fonction JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="95060-105">JetEscrowUpdate Function</span></span>

<span data-ttu-id="95060-106">La fonction **JetEscrowUpdate** effectue une opération d’addition atomique sur une colonne.</span><span class="sxs-lookup"><span data-stu-id="95060-106">The **JetEscrowUpdate** function performs an atomic addition operation on one column.</span></span> <span data-ttu-id="95060-107">Cette fonction permet à plusieurs sessions de mettre à jour le même enregistrement simultanément sans conflits.</span><span class="sxs-lookup"><span data-stu-id="95060-107">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="95060-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95060-108">Parameters</span></span>

<span data-ttu-id="95060-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="95060-109">*sesid*</span></span>

<span data-ttu-id="95060-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="95060-110">The session to use for this call.</span></span>

<span data-ttu-id="95060-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="95060-111">*tableid*</span></span>

<span data-ttu-id="95060-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="95060-112">The cursor to use for this call.</span></span>

<span data-ttu-id="95060-113">*ColumnID*</span><span class="sxs-lookup"><span data-stu-id="95060-113">*columnid*</span></span>

<span data-ttu-id="95060-114">*ColumnID* de la colonne à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="95060-114">The *columnid* of the column to be updated.</span></span>

<span data-ttu-id="95060-115">*va*</span><span class="sxs-lookup"><span data-stu-id="95060-115">*pv*</span></span>

<span data-ttu-id="95060-116">Pointeur vers une mémoire tampon contenant le addend pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="95060-116">A pointer to a buffer containing the addend for the column.</span></span>

<span data-ttu-id="95060-117">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="95060-117">*cbMax*</span></span>

<span data-ttu-id="95060-118">Taille de la mémoire tampon contenant le addend.</span><span class="sxs-lookup"><span data-stu-id="95060-118">The size of the buffer containing the addend.</span></span>

<span data-ttu-id="95060-119">*pvOld*</span><span class="sxs-lookup"><span data-stu-id="95060-119">*pvOld*</span></span>

<span data-ttu-id="95060-120">Mémoire tampon de sortie qui recevra la valeur actuelle de la colonne telle qu’elle est stockée dans la base de données (le contrôle de version est ignoré).</span><span class="sxs-lookup"><span data-stu-id="95060-120">The output buffer that will receive the current value of the column as stored in the database (versioning is ignored).</span></span>

<span data-ttu-id="95060-121">*cbOldMax*</span><span class="sxs-lookup"><span data-stu-id="95060-121">*cbOldMax*</span></span>

<span data-ttu-id="95060-122">Taille maximale de la mémoire tampon de sortie qui recevra la valeur actuelle de la colonne.</span><span class="sxs-lookup"><span data-stu-id="95060-122">The maximum size of the output buffer that will receive the current value of the column.</span></span> <span data-ttu-id="95060-123">Actuellement JET_coltypLong est pris en charge, la mémoire tampon doit avoir une longueur de 4 octets ou de 0 octets.</span><span class="sxs-lookup"><span data-stu-id="95060-123">Currently only JET_coltypLong is supported, so the buffer must either be 4 bytes or 0 bytes in length.</span></span> <span data-ttu-id="95060-124">Si *pvOld* a la valeur null, *cbOldMax* doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="95060-124">If *pvOld* is NULL then *cbOldMax* should be 0.</span></span>

<span data-ttu-id="95060-125">*pcbOldActual*</span><span class="sxs-lookup"><span data-stu-id="95060-125">*pcbOldActual*</span></span>

<span data-ttu-id="95060-126">Reçoit le volume réel de données de valeur brute reçues dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="95060-126">Receives the actual amount of raw value data received in the output buffer.</span></span>

<span data-ttu-id="95060-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="95060-127">*grbit*</span></span>

<span data-ttu-id="95060-128">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="95060-128">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95060-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="95060-129">Value</span></span></p></th>
<th><p><span data-ttu-id="95060-130">Signification</span><span class="sxs-lookup"><span data-stu-id="95060-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95060-131">JET_bitEscrowNoRollback</span><span class="sxs-lookup"><span data-stu-id="95060-131">JET_bitEscrowNoRollback</span></span></p></td>
<td><p><span data-ttu-id="95060-132">Cette mise à jour ne sera pas annulée même si la session effectuant la mise à jour du tiers de confiance a été restaurée.</span><span class="sxs-lookup"><span data-stu-id="95060-132">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="95060-133">Notez que dans la mesure où les enregistrements du journal ne peuvent pas être vidés sur le disque, les mises à jour de dépôt récentes effectuées avec cet indicateur peuvent être perdues en cas de panne.</span><span class="sxs-lookup"><span data-stu-id="95060-133">Note that as the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="95060-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="95060-134">Return Value</span></span>

<span data-ttu-id="95060-135">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="95060-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="95060-136">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="95060-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95060-137">Code de retour</span><span class="sxs-lookup"><span data-stu-id="95060-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="95060-138">Description</span><span class="sxs-lookup"><span data-stu-id="95060-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95060-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="95060-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="95060-140">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="95060-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-141">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="95060-141">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="95060-142">Le curseur a une mise à jour préparée avec <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="95060-142">The cursor has an update prepared with <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="95060-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="95060-144">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="95060-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-145">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="95060-145">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="95060-146">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="95060-146">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="95060-147">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="95060-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-148">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="95060-148">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="95060-149">Une taille de mémoire tampon non valide a été passée.</span><span class="sxs-lookup"><span data-stu-id="95060-149">An invalid buffer size has been passed in.</span></span> <span data-ttu-id="95060-150">Actuellement, seul JET_coltypLong est pris en charge. la mémoire tampon doit donc être de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="95060-150">Currently only JET_coltypLong is supported, so the buffer must be 4 bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="95060-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="95060-152">Une colonne non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="95060-152">An invalid column has been specified.</span></span> <span data-ttu-id="95060-153">La colonne doit être créée avec JET_bitColumnEscrowUpdate spécifié.</span><span class="sxs-lookup"><span data-stu-id="95060-153">The column must be created with JET_bitColumnEscrowUpdate specified.</span></span> <span data-ttu-id="95060-154">Seules les colonnes fixes de JET_coltypLong peuvent être spécifiées comme pouvant être mises à jour par tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="95060-154">Only fixed columns of JET_coltypLong can be specified as escrow updateable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="95060-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="95060-156">Le curseur doit se trouver sur un enregistrement pour pouvoir mettre à jour une colonne.</span><span class="sxs-lookup"><span data-stu-id="95060-156">Cursor must be on a record in order to update a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-157">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="95060-157">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="95060-158">Les mises à jour du tiers de confiance ne peuvent être effectuées que par les sessions dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="95060-158">Escrow updates can only be performed by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="95060-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="95060-160">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="95060-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-161">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="95060-161">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="95060-162">Le curseur ne peut pas être en lecture seule et mettre à jour un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="95060-162">Cursor cannot be read only and update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-163">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="95060-163">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="95060-164">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="95060-164">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-165">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="95060-165">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="95060-166">La même session ne peut pas être utilisée à partir de plusieurs threads en même temps.</span><span class="sxs-lookup"><span data-stu-id="95060-166">The same session cannot be used from more than one thread at the same time.</span></span> <span data-ttu-id="95060-167">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="95060-167">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-168">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="95060-168">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="95060-169">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="95060-169">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-170">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="95060-170">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="95060-171">La session doit avoir des autorisations en écriture pour mettre à jour un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="95060-171">Session must have write permissions to update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-172">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="95060-172">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="95060-173">L’erreur retournée lorsqu’une mise à jour en conflit est demandée.</span><span class="sxs-lookup"><span data-stu-id="95060-173">The error returned when a conflicting update is requested.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="95060-174">Notes</span><span class="sxs-lookup"><span data-stu-id="95060-174">Remarks</span></span>

<span data-ttu-id="95060-175">Normalement, si deux sessions tentent de mettre à jour un enregistrement simultanément, la deuxième session reçoit une erreur JET_errWriteConflict, sauf si les sessions sont complètement sérialisées.</span><span class="sxs-lookup"><span data-stu-id="95060-175">Normally, if two sessions attempt to update a record simultaneously, the second session will receive a JET_errWriteConflict error unless the sessions are completely serialized.</span></span> <span data-ttu-id="95060-176">Pour sérialiser deux sessions qui mettent à jour le même enregistrement, la deuxième session doit démarrer sa transaction une fois que la première transaction a validé sa transaction.</span><span class="sxs-lookup"><span data-stu-id="95060-176">To serialize two sessions that update the same record, the second session must start its transaction after the first transaction commits its transaction.</span></span> <span data-ttu-id="95060-177">Pour plus d’informations, consultez [JetBeginTransaction](./jetbegintransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="95060-177">See [JetBeginTransaction](./jetbegintransaction-function.md) for more information.</span></span>

<span data-ttu-id="95060-178">Le tiers de confiance peut mettre à jour plusieurs colonnes dans le même enregistrement.</span><span class="sxs-lookup"><span data-stu-id="95060-178">Multiple columns in the same record can be escrow updated.</span></span> <span data-ttu-id="95060-179">Les mises à jour n’affectent pas les unes les autres.</span><span class="sxs-lookup"><span data-stu-id="95060-179">The updates do not affect each other.</span></span>

<span data-ttu-id="95060-180">Seules les opérations **JetEscrowUpdate** sont compatibles les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="95060-180">Only **JetEscrowUpdate** operations are compatible with each other.</span></span> <span data-ttu-id="95060-181">Si deux sessions différentes essaient de préparer des mises à jour ou de supprimer le même enregistrement, un conflit d’écriture est généré.</span><span class="sxs-lookup"><span data-stu-id="95060-181">If two different sessions try to prepare updates or delete the same record, a write conflict will be generated.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p><span data-ttu-id="95060-182">Session B</span><span class="sxs-lookup"><span data-stu-id="95060-182">Session B</span></span><br /><span data-ttu-id="95060-183">
<strong>JetEscrowUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="95060-183">
<strong>JetEscrowUpdate</strong></span></span></p></th>
<th><p><span data-ttu-id="95060-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span><span class="sxs-lookup"><span data-stu-id="95060-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span></span></p></th>
<th><p><span data-ttu-id="95060-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="95060-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="95060-186"><strong>JetEscrowUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="95060-186"><strong>JetEscrowUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="95060-187">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="95060-187">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="95060-188">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="95060-188">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="95060-189">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="95060-189">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="95060-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span><span class="sxs-lookup"><span data-stu-id="95060-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="95060-191">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="95060-191">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="95060-192">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="95060-192">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="95060-193">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="95060-193">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-194">Session A</span><span class="sxs-lookup"><span data-stu-id="95060-194">Session A</span></span></p></td>
<td><p><span data-ttu-id="95060-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="95060-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></td>
<td><p><span data-ttu-id="95060-196">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="95060-196">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="95060-197">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="95060-197">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="95060-198">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="95060-198">JET_errWriteConflict</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95060-199">Les opérations de dépôt sont gérées par version et sont annulées à l’aide de [JetRollback](./jetrollback-function.md) (sauf si JET_bitEscrowNoRollback a été spécifié).</span><span class="sxs-lookup"><span data-stu-id="95060-199">Escrow operations are versioned and are undone using [JetRollback](./jetrollback-function.md) (unless JET_bitEscrowNoRollback was specified).</span></span> <span data-ttu-id="95060-200">**JetEscrowUpdate** retourne la valeur brute de la colonne stockée dans la base de données, car une application peut souhaiter exécuter une action spéciale quand une valeur de sentinelle est atteinte.</span><span class="sxs-lookup"><span data-stu-id="95060-200">**JetEscrowUpdate** returns the raw value of the column stored in the database, because an application may want to perform a special action when a sentinel value is hit.</span></span> <span data-ttu-id="95060-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) retourne la vue de version correcte de la colonne, en ignorant les mises à jour effectuées par les sessions simultanées.</span><span class="sxs-lookup"><span data-stu-id="95060-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) returns the correctly versioned view of the column, ignoring updates made by concurrent sessions.</span></span>

<span data-ttu-id="95060-202">À partir de deux sessions opérant sur la même colonne du même enregistrement, nous pouvons voir comment cela fonctionne.</span><span class="sxs-lookup"><span data-stu-id="95060-202">Given two sessions operating on the same column of the same record, we can see how this works.</span></span> <span data-ttu-id="95060-203">Supposons que la colonne commence par une valeur de 0.</span><span class="sxs-lookup"><span data-stu-id="95060-203">Assume the column starts with a value of 0.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95060-204">session</span><span class="sxs-lookup"><span data-stu-id="95060-204">Session</span></span></p></th>
<th><p><span data-ttu-id="95060-205">Opération</span><span class="sxs-lookup"><span data-stu-id="95060-205">Operation</span></span></p></th>
<th><p><span data-ttu-id="95060-206">Valeur stockée</span><span class="sxs-lookup"><span data-stu-id="95060-206">Stored value</span></span></p></th>
<th><p><span data-ttu-id="95060-207">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="95060-207">Returned value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95060-208">Un</span><span class="sxs-lookup"><span data-stu-id="95060-208">A</span></span></p></td>
<td><p><span data-ttu-id="95060-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span><span class="sxs-lookup"><span data-stu-id="95060-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-210">Un</span><span class="sxs-lookup"><span data-stu-id="95060-210">A</span></span></p></td>
<td><p><span data-ttu-id="95060-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span><span class="sxs-lookup"><span data-stu-id="95060-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="95060-212">0</span><span class="sxs-lookup"><span data-stu-id="95060-212">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-213">Un</span><span class="sxs-lookup"><span data-stu-id="95060-213">A</span></span></p></td>
<td><p><span data-ttu-id="95060-214"><strong>JetEscrowUpdate</strong> (4)</span><span class="sxs-lookup"><span data-stu-id="95060-214"><strong>JetEscrowUpdate</strong> (4)</span></span></p></td>
<td><p><span data-ttu-id="95060-215">4</span><span class="sxs-lookup"><span data-stu-id="95060-215">4</span></span></p></td>
<td><p><span data-ttu-id="95060-216">0</span><span class="sxs-lookup"><span data-stu-id="95060-216">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-217">Un</span><span class="sxs-lookup"><span data-stu-id="95060-217">A</span></span></p></td>
<td><p><span data-ttu-id="95060-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="95060-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="95060-219">4</span><span class="sxs-lookup"><span data-stu-id="95060-219">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-220">B</span><span class="sxs-lookup"><span data-stu-id="95060-220">B</span></span></p></td>
<td><p><span data-ttu-id="95060-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span><span class="sxs-lookup"><span data-stu-id="95060-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-222">B</span><span class="sxs-lookup"><span data-stu-id="95060-222">B</span></span></p></td>
<td><p><span data-ttu-id="95060-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="95060-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="95060-224">0</span><span class="sxs-lookup"><span data-stu-id="95060-224">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-225">B</span><span class="sxs-lookup"><span data-stu-id="95060-225">B</span></span></p></td>
<td><p><span data-ttu-id="95060-226"><strong>JetEscrowUpdate</strong> (3)</span><span class="sxs-lookup"><span data-stu-id="95060-226"><strong>JetEscrowUpdate</strong> (3)</span></span></p></td>
<td><p><span data-ttu-id="95060-227">7</span><span class="sxs-lookup"><span data-stu-id="95060-227">7</span></span></p></td>
<td><p><span data-ttu-id="95060-228">4</span><span class="sxs-lookup"><span data-stu-id="95060-228">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-229">B</span><span class="sxs-lookup"><span data-stu-id="95060-229">B</span></span></p></td>
<td><p><span data-ttu-id="95060-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="95060-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="95060-231">3</span><span class="sxs-lookup"><span data-stu-id="95060-231">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-232">Un</span><span class="sxs-lookup"><span data-stu-id="95060-232">A</span></span></p></td>
<td><p><span data-ttu-id="95060-233"><strong>JetEscrowUpdate</strong> (2)</span><span class="sxs-lookup"><span data-stu-id="95060-233"><strong>JetEscrowUpdate</strong> (2)</span></span></p></td>
<td><p><span data-ttu-id="95060-234">9</span><span class="sxs-lookup"><span data-stu-id="95060-234">9</span></span></p></td>
<td><p><span data-ttu-id="95060-235">7</span><span class="sxs-lookup"><span data-stu-id="95060-235">7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-236">Un</span><span class="sxs-lookup"><span data-stu-id="95060-236">A</span></span></p></td>
<td><p><span data-ttu-id="95060-237"><strong>JetEscrowUpdate</strong> (-7)</span><span class="sxs-lookup"><span data-stu-id="95060-237"><strong>JetEscrowUpdate</strong> (-7)</span></span></p></td>
<td><p><span data-ttu-id="95060-238">2</span><span class="sxs-lookup"><span data-stu-id="95060-238">2</span></span></p></td>
<td><p><span data-ttu-id="95060-239">9</span><span class="sxs-lookup"><span data-stu-id="95060-239">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-240">B</span><span class="sxs-lookup"><span data-stu-id="95060-240">B</span></span></p></td>
<td><p><span data-ttu-id="95060-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="95060-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="95060-242">3</span><span class="sxs-lookup"><span data-stu-id="95060-242">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-243">Un</span><span class="sxs-lookup"><span data-stu-id="95060-243">A</span></span></p></td>
<td><p><span data-ttu-id="95060-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="95060-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="95060-245">-1</span><span class="sxs-lookup"><span data-stu-id="95060-245">-1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-246">B</span><span class="sxs-lookup"><span data-stu-id="95060-246">B</span></span></p></td>
<td><p><span data-ttu-id="95060-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span><span class="sxs-lookup"><span data-stu-id="95060-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span></span></p></td>
<td><p><span data-ttu-id="95060-248">-1</span><span class="sxs-lookup"><span data-stu-id="95060-248">-1</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-249">Un</span><span class="sxs-lookup"><span data-stu-id="95060-249">A</span></span></p></td>
<td><p><span data-ttu-id="95060-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="95060-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="95060-251">-1</span><span class="sxs-lookup"><span data-stu-id="95060-251">-1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95060-252">Il n’est pas recommandé de remplacer un enregistrement dans la même transaction qui effectue des mises à jour de dépôt dans un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="95060-252">Replacing a record in the same transaction that performs escrow updates to a record is not recommended.</span></span> <span data-ttu-id="95060-253">En particulier, si une mise à jour d’un enregistrement est préparée avec un [JET_TABLEID](./jet-tableid.md) et qu’un autre [JET_TABLEID](./jet-tableid.md) est utilisé pour le dépôt de la mise à jour de l’enregistrement, le tiers de confiance mis à jour sera perdu lors de l’appel de [JetUpdate](./jetupdate-function.md) .</span><span class="sxs-lookup"><span data-stu-id="95060-253">In particular, if an update on a record is prepared with one [JET_TABLEID](./jet-tableid.md) and a different [JET_TABLEID](./jet-tableid.md) is used to escrow update the record then the escrow updated will be lost when [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="95060-254">Cela se produit même si la colonne du tiers de confiance n’a pas été définie lors de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="95060-254">This happens even if the escrow column was not set during the update.</span></span>

<span data-ttu-id="95060-255">Quand une colonne pouvant être mise à jour par dépôt a une valeur égale à zéro, un comportement spécial peut être déclenché.</span><span class="sxs-lookup"><span data-stu-id="95060-255">When an escrow updateable column has a value of zero, special behavior can be triggered.</span></span> <span data-ttu-id="95060-256">Ce comportement se produit uniquement si une opération **JetEscrowUpdate** provoque une valeur de zéro pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="95060-256">This behavior only happens if a **JetEscrowUpdate** operation causes the column to have a value of zero.</span></span> <span data-ttu-id="95060-257">L’action ne se produit pas immédiatement, mais elle se produit une fois que la transaction qui a provoqué la colonne a une valeur de zéro validations.</span><span class="sxs-lookup"><span data-stu-id="95060-257">The action does not happen immediately, but occurs sometime after the transaction which caused the column to have a value of zero commits.</span></span> <span data-ttu-id="95060-258">La colonne doit toujours avoir une valeur égale à zéro (autrement dit, si aucune autre session n’a modifié la colonne).</span><span class="sxs-lookup"><span data-stu-id="95060-258">The column must still have a value of zero (that is, if no other sessions have modified the column).</span></span> <span data-ttu-id="95060-259">Si la colonne a été créée avec JET_bitColumnDeleteOnZero, l’enregistrement contenant la colonne sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="95060-259">If the column was created with JET_bitColumnDeleteOnZero, the record containing the column will be deleted.</span></span> <span data-ttu-id="95060-260">Si la colonne a été créée avec JET_bitColumnFinalize, un rappel sera émis.</span><span class="sxs-lookup"><span data-stu-id="95060-260">If the column was created with JET_bitColumnFinalize then a callback will be issued.</span></span> <span data-ttu-id="95060-261">Un incident peut entraîner la non-utilisation de ces actions, mais la maintenance en ligne (à l’aide de la fonction [JetDefragment](./jetdefragment-function.md) ) rétablit correctement les actions.</span><span class="sxs-lookup"><span data-stu-id="95060-261">A crash may cause these actions not to happen, but online maintenance (using the [JetDefragment](./jetdefragment-function.md) function) will correctly redo the actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="95060-262">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95060-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95060-263"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="95060-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="95060-264">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="95060-264">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-265"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="95060-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="95060-266">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="95060-266">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-267"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="95060-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="95060-268">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="95060-268">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95060-269"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="95060-269"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="95060-270">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="95060-270">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95060-271"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="95060-271"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="95060-272">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="95060-272">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="95060-273">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95060-273">See Also</span></span>

[<span data-ttu-id="95060-274">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="95060-274">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="95060-275">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="95060-275">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="95060-276">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="95060-276">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="95060-277">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="95060-277">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="95060-278">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="95060-278">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="95060-279">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="95060-279">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="95060-280">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="95060-280">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="95060-281">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="95060-281">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="95060-282">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="95060-282">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="95060-283">JetRollback</span><span class="sxs-lookup"><span data-stu-id="95060-283">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="95060-284">JetStopService</span><span class="sxs-lookup"><span data-stu-id="95060-284">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="95060-285">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="95060-285">JetUpdate</span></span>](./jetupdate-function.md)

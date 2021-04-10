---
description: 'En savoir plus sur : fonction JetGetRecordPosition'
title: Fonction JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034608"
---
# <a name="jetgetrecordposition-function"></a><span data-ttu-id="92c33-103">Fonction JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="92c33-103">JetGetRecordPosition Function</span></span>


<span data-ttu-id="92c33-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="92c33-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordposition-function"></a><span data-ttu-id="92c33-105">Fonction JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="92c33-105">JetGetRecordPosition Function</span></span>

<span data-ttu-id="92c33-106">La fonction **JetGetRecordPosition** retourne la position fractionnaire de l’enregistrement actif dans l’index actuel sous la forme d’une structure [JET_RECPOS](./jet-recpos-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="92c33-106">The **JetGetRecordPosition** function returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-structure.md) structure.</span></span> <span data-ttu-id="92c33-107">Cette structure décrit les positions fractionnaires en termes de nombre approximatif d’entrées d’index avant l’enregistrement actif et un nombre total approximatif d’entrées dans l’index.</span><span class="sxs-lookup"><span data-stu-id="92c33-107">This structure describes fractional positions in terms of an approximate number of index entries before the current record and an approximate total number of entries in the index.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a><span data-ttu-id="92c33-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92c33-108">Parameters</span></span>

<span data-ttu-id="92c33-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="92c33-109">*sesid*</span></span>

<span data-ttu-id="92c33-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="92c33-110">The session to use for this call.</span></span>

<span data-ttu-id="92c33-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="92c33-111">*tableid*</span></span>

<span data-ttu-id="92c33-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="92c33-112">The cursor to use for this call.</span></span>

<span data-ttu-id="92c33-113">*precpos*</span><span class="sxs-lookup"><span data-stu-id="92c33-113">*precpos*</span></span>

<span data-ttu-id="92c33-114">Description de la fraction à utiliser pour obtenir la position de l’enregistrement actif dans l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="92c33-114">The description of the fraction to use in getting the position of the current record in the current index.</span></span>

<span data-ttu-id="92c33-115">*cbRecpos*</span><span class="sxs-lookup"><span data-stu-id="92c33-115">*cbRecpos*</span></span>

<span data-ttu-id="92c33-116">Taille de la mémoire allouée à *precpos*.</span><span class="sxs-lookup"><span data-stu-id="92c33-116">The size of memory allocated at *precpos*.</span></span>

### <a name="return-value"></a><span data-ttu-id="92c33-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="92c33-117">Return Value</span></span>

<span data-ttu-id="92c33-118">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="92c33-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="92c33-119">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="92c33-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92c33-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="92c33-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="92c33-121">Description</span><span class="sxs-lookup"><span data-stu-id="92c33-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92c33-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="92c33-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="92c33-123">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="92c33-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92c33-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="92c33-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="92c33-125">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="92c33-125">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92c33-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="92c33-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="92c33-127">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="92c33-127">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92c33-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="92c33-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="92c33-129">Impossible d’effectuer cette opération, car l’instance, associée à la session, a rencontré une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="92c33-129">This operation cannot complete because the instance, associated with the session, encountered a fatal error.</span></span> <span data-ttu-id="92c33-130">Il est nécessaire que l’accès à toutes les données soit révoqué afin de protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="92c33-130">It is required that access to all data be revoked in order to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="92c33-131"><strong>Windows 2000 :</strong>  Cette erreur ne sera pas retournée par le système d’exploitation Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="92c33-131"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92c33-132">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="92c33-132">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="92c33-133">La taille de la mémoire allouée sur <em>precpos</em> n’est pas suffisante.</span><span class="sxs-lookup"><span data-stu-id="92c33-133">The size of the allocated memory at <em>precpos</em> is not a sufficient size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92c33-134">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="92c33-134">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="92c33-135">Le curseur ne se trouve pas actuellement sur un enregistrement et ne peut pas retourner de position.</span><span class="sxs-lookup"><span data-stu-id="92c33-135">The cursor is not currently on a record and cannot return a position.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92c33-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="92c33-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="92c33-137">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="92c33-137">It is not possible to complete the operation because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92c33-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="92c33-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="92c33-139">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="92c33-139">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="92c33-140"><strong>Windows 2000 :</strong>  Cette erreur ne sera pas retournée par le système d’exploitation Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="92c33-140"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92c33-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="92c33-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="92c33-142">L’opération ne peut pas se terminer car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="92c33-142">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="92c33-143">En cas de réussite, le nombre approximatif d’entrées d’index précédant l’enregistrement en cours dans l’index est retourné dans precpos- \> centriesLT.</span><span class="sxs-lookup"><span data-stu-id="92c33-143">On success, the approximate number of index entries preceding the current record in the index are returned in precpos-\>centriesLT.</span></span> <span data-ttu-id="92c33-144">1 est retourné dans precpos- \> centriesInRange.</span><span class="sxs-lookup"><span data-stu-id="92c33-144">1 is returned in precpos-\>centriesInRange.</span></span> <span data-ttu-id="92c33-145">Le nombre approximatif d’entrées dans l’index est retourné dans precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="92c33-145">The approximate number of entries in the index is returned in precpos-\>centriesTotal.</span></span>

<span data-ttu-id="92c33-146">En cas d’échec, aucune modification n’est apportée à la mémoire allouée sur *precpos*.</span><span class="sxs-lookup"><span data-stu-id="92c33-146">On failure, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="92c33-147">Notes</span><span class="sxs-lookup"><span data-stu-id="92c33-147">Remarks</span></span>

<span data-ttu-id="92c33-148">Cette opération renvoie des données variables lorsque les mises à jour se produisent en continu sur la table.</span><span class="sxs-lookup"><span data-stu-id="92c33-148">This operation returns varying data when updates occur continuously on the table.</span></span> <span data-ttu-id="92c33-149">Les modifications apportées aux valeurs ne correspondent pas toujours aux attentes en fonction de la connaissance des mises à jour, car les valeurs sont des approximations basées sur les propriétés physiques de l’index.</span><span class="sxs-lookup"><span data-stu-id="92c33-149">The changes in the values will not always match expectations based on knowledge of the updates, since the values are approximations based on physical properties of the index.</span></span> <span data-ttu-id="92c33-150">L’isolation transactionnelle ne s’applique pas aux positions de **JetGetRecordPosition** , car les valeurs dépendent des propriétés physiques de l’index qui ne sont pas des transactions isolées.</span><span class="sxs-lookup"><span data-stu-id="92c33-150">Transactional isolation does not apply to positions from **JetGetRecordPosition** since the values depend on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="92c33-151">[JET_RECPOS](./jet-recpos-structure.md) ne doit pas être utilisé pour décrire un enregistrement dans une table ou pour repositionner un enregistrement à proximité d’un enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="92c33-151">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="92c33-152">Au lieu de cela, les signets d’un enregistrement existant doivent être récupérés, puis utilisés pour repositionner le même enregistrement.</span><span class="sxs-lookup"><span data-stu-id="92c33-152">Instead, bookmarks for an existing record should be retrieved and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="92c33-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92c33-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92c33-154"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="92c33-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="92c33-155">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="92c33-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92c33-156"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="92c33-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="92c33-157">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="92c33-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92c33-158"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="92c33-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="92c33-159">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="92c33-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92c33-160"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="92c33-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="92c33-161">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="92c33-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92c33-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="92c33-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="92c33-163">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="92c33-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="92c33-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92c33-164">See Also</span></span>

[<span data-ttu-id="92c33-165">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="92c33-165">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="92c33-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="92c33-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="92c33-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="92c33-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="92c33-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="92c33-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="92c33-169">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="92c33-169">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="92c33-170">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="92c33-170">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="92c33-171">JetGotoPosition</span><span class="sxs-lookup"><span data-stu-id="92c33-171">JetGotoPosition</span></span>](./jetgotoposition-function.md)  
[<span data-ttu-id="92c33-172">JetStopService</span><span class="sxs-lookup"><span data-stu-id="92c33-172">JetStopService</span></span>](./jetstopservice-function.md)

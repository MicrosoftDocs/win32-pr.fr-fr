---
description: 'En savoir plus sur : fonction JetIndexRecordCount'
title: JetIndexRecordCount fonction)
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524964"
---
# <a name="jetindexrecordcount-function"></a><span data-ttu-id="bf1d2-103">JetIndexRecordCount fonction)</span><span class="sxs-lookup"><span data-stu-id="bf1d2-103">JetIndexRecordCount Function</span></span>


<span data-ttu-id="bf1d2-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="bf1d2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetindexrecordcount-function"></a><span data-ttu-id="bf1d2-105">JetIndexRecordCount fonction)</span><span class="sxs-lookup"><span data-stu-id="bf1d2-105">JetIndexRecordCount Function</span></span>

<span data-ttu-id="bf1d2-106">La fonction **JetIndexRecordCount** compte le nombre d’entrées dans l’index actuel à partir de la position actuelle vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-106">The **JetIndexRecordCount** function counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="bf1d2-107">La position actuelle est incluse dans le nombre.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-107">The current position is included in the count.</span></span> <span data-ttu-id="bf1d2-108">Le nombre peut être supérieur au nombre total d’enregistrements dans la table si l’index actuel est sur une colonne à valeurs multiples et que les instances de la colonne ont des valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-108">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="bf1d2-109">Si la table est vide, la valeur 0 est retournée pour le nombre.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-109">If the table is empty, then 0 will be returned for the count.</span></span>

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a><span data-ttu-id="bf1d2-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf1d2-110">Parameters</span></span>

<span data-ttu-id="bf1d2-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bf1d2-111">*sesid*</span></span>

<span data-ttu-id="bf1d2-112">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-112">The session to use for this call.</span></span>

<span data-ttu-id="bf1d2-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="bf1d2-113">*tableid*</span></span>

<span data-ttu-id="bf1d2-114">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-114">The cursor to use for this call.</span></span>

<span data-ttu-id="bf1d2-115">*pcrec*</span><span class="sxs-lookup"><span data-stu-id="bf1d2-115">*pcrec*</span></span>

<span data-ttu-id="bf1d2-116">Pointeur vers une valeur long non signée pour recevoir le nombre.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-116">The pointer to an unsigned long value to receive the count.</span></span>

<span data-ttu-id="bf1d2-117">*crecMax*</span><span class="sxs-lookup"><span data-stu-id="bf1d2-117">*crecMax*</span></span>

<span data-ttu-id="bf1d2-118">Nombre maximal d’enregistrements à compter.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-118">The maximum number of records to count.</span></span> <span data-ttu-id="bf1d2-119">Une valeur *crecMax* de 0 indique que le nombre est illimité.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-119">A *crecMax* value of 0 indicates that the count is unlimited.</span></span>

### <a name="return-value"></a><span data-ttu-id="bf1d2-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bf1d2-120">Return Value</span></span>

<span data-ttu-id="bf1d2-121">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bf1d2-122">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bf1d2-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf1d2-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bf1d2-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="bf1d2-124">Description</span><span class="sxs-lookup"><span data-stu-id="bf1d2-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf1d2-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bf1d2-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bf1d2-126">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf1d2-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bf1d2-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bf1d2-128">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-128">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf1d2-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bf1d2-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bf1d2-130">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-130">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="bf1d2-131"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-131"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf1d2-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="bf1d2-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="bf1d2-133">Le curseur ne se trouve pas actuellement sur un enregistrement et la table n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-133">The cursor is not currently on a record and the table is not empty.</span></span></p>
<p><span data-ttu-id="bf1d2-134"><strong>Windows XP, Windows server 2003, windows 2000 Server et windows 2000 professionnel :</strong>  Si le curseur est positionné sur un index ou une plage d’index vide, <strong>JetIndexRecordCount</strong> retourne par erreur JET_errNoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-134"><strong>Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:</strong>  If the cursor is positioned on an empty index or index range then <strong>JetIndexRecordCount</strong> erroneously returns JET_errNoCurrentRecord.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf1d2-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bf1d2-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bf1d2-136">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-136">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf1d2-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bf1d2-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bf1d2-138">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-138">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf1d2-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bf1d2-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bf1d2-140">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-140">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="bf1d2-141"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf1d2-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bf1d2-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bf1d2-143">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf1d2-144">Si cette fonction a la valeur, le nombre exact d’entrées d’index, y compris la position actuelle et jusqu’à *crecMax* (si elle n’est pas 0), est retourné dans la valeur long pointée longue non signée par *pcrec*.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-144">If this function succeeds, the exact number of index entries including the current position and up to *crecMax* (if it is not 0), is returned in the unsigned long pointed to by *pcrec*.</span></span>

<span data-ttu-id="bf1d2-145">Si cette fonction échoue, aucune modification n’est apportée à la mémoire allouée sur *precpos*.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-145">If this function fails, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bf1d2-146">Notes</span><span class="sxs-lookup"><span data-stu-id="bf1d2-146">Remarks</span></span>

<span data-ttu-id="bf1d2-147">Si la table n’est pas vide, le curseur doit être positionné sur l’enregistrement à partir duquel commencer le décompte.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-147">If the table is not empty, then the cursor should be positioned onto the record from which to begin the count.</span></span> <span data-ttu-id="bf1d2-148">Le nombre inclura cet enregistrement, et le nombre sera reporté jusqu’à la limite donnée dans *crecMax*.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-148">The count will include this record, and count forward up to the given limit in *crecMax*.</span></span> <span data-ttu-id="bf1d2-149">Si *crecMax* a la valeur 0, l’opération continue à compter jusqu’à la fin de l’index.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-149">If *crecMax* is 0 then the operation will continue counting until the end of the index.</span></span>

<span data-ttu-id="bf1d2-150">Les plages d’index peuvent être utilisées pour construire des limitations de fin d’index artificielles pour le nombre.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-150">Index ranges can be used to construct artificial end-of-index limitations for the count.</span></span> <span data-ttu-id="bf1d2-151">De cette manière, les sous-plages d’un index peuvent être comptées exactement.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-151">In this way, subranges of an index can be counted exactly.</span></span> <span data-ttu-id="bf1d2-152">Le curseur doit être positionné sur la première ligne de la plage.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-152">The cursor should be positioned to the first row in the range.</span></span> <span data-ttu-id="bf1d2-153">La fin de la clé de la plage doit être établie, puis [JetSetIndexRange](./jetsetindexrange-function.md) doit être utilisé pour définir la plage supérieure, soit de manière inclusive, soit exclusivement.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-153">The end of the range key should be made and then [JetSetIndexRange](./jetsetindexrange-function.md) should be used to set the upper range, either inclusively or exclusively.</span></span> <span data-ttu-id="bf1d2-154">Enfin, **JetIndexRecordCount** doit être appelé pour compter exactement la plage.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-154">Lastly, **JetIndexRecordCount** should be called to exactly count the range.</span></span>

<span data-ttu-id="bf1d2-155">**JetIndexRecordCount** obéit à la sémantique de transaction et retourne un nombre précis pour cette session particulière dans son état transactionnel actuel.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-155">**JetIndexRecordCount** obeys transaction semantics and returns a count that is accurate for this particular session in its current transactional state.</span></span>

<span data-ttu-id="bf1d2-156">**JetIndexRecordCount** accède aux pages de feuille d’index afin de compter exactement les entrées.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-156">**JetIndexRecordCount** accesses index leaf pages in order to exactly count entries.</span></span> <span data-ttu-id="bf1d2-157">Par conséquent, il peut effectuer une grande quantité d’e/s et peut être lent.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-157">Consequently, it can perform a great deal of I/O and can be slow.</span></span> <span data-ttu-id="bf1d2-158">La limitation *crecMax* doit être utilisée pour empêcher une charge excessive.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-158">The *crecMax* limitation should be used to prevent excessive load.</span></span> <span data-ttu-id="bf1d2-159">Si une plage est volumineuse, il peut être possible de compter la plage de manière approximative à l’aide de [JetGetRecordPosition](./jetgetrecordposition-function.md).</span><span class="sxs-lookup"><span data-stu-id="bf1d2-159">If a range is large, then it might be possible to count the range in an approximated fashion using [JetGetRecordPosition](./jetgetrecordposition-function.md).</span></span>

<span data-ttu-id="bf1d2-160">**Windows XP, Windows server 2003, windows 2000 Server et windows 2000 professionnel :**  Si le curseur est positionné sur un index ou une plage d’index vide, **JetIndexRecordCount** retourne à tort JET_errNoCurrentRecord plutôt que de retourner un nombre d’enregistrements égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-160">**Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:**  If the cursor is positioned on an empty index or index range then **JetIndexRecordCount** erroneously returns JET_errNoCurrentRecord rather than returning a record count of zero.</span></span> <span data-ttu-id="bf1d2-161">Dans ce cas, l’application doit vérifier si l’index ou la plage d’index est vide.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-161">The application should check to see if the index or index range is empty in this case.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bf1d2-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf1d2-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf1d2-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bf1d2-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bf1d2-164">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-164">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf1d2-165"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="bf1d2-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bf1d2-166">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-166">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf1d2-167"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="bf1d2-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bf1d2-168">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf1d2-169"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="bf1d2-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bf1d2-170">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf1d2-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bf1d2-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bf1d2-172">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bf1d2-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bf1d2-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf1d2-173">See Also</span></span>

[<span data-ttu-id="bf1d2-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bf1d2-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bf1d2-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bf1d2-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bf1d2-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bf1d2-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bf1d2-177">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="bf1d2-177">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="bf1d2-178">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="bf1d2-178">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="bf1d2-179">JetStopService</span><span class="sxs-lookup"><span data-stu-id="bf1d2-179">JetStopService</span></span>](./jetstopservice-function.md)

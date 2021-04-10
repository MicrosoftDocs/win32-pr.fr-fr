---
description: 'En savoir plus sur : fonction JetGotoSecondaryIndexBookmark'
title: JetGotoSecondaryIndexBookmark fonction)
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952147"
---
# <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="96a05-103">JetGotoSecondaryIndexBookmark fonction)</span><span class="sxs-lookup"><span data-stu-id="96a05-103">JetGotoSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="96a05-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="96a05-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="96a05-105">JetGotoSecondaryIndexBookmark fonction)</span><span class="sxs-lookup"><span data-stu-id="96a05-105">JetGotoSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="96a05-106">La fonction **JetGotoSecondaryIndexBookmark** positionne un curseur sur une entrée d’index associée au signet de l’index secondaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="96a05-106">The **JetGotoSecondaryIndexBookmark** function positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="96a05-107">Le signet de l’index secondaire doit être utilisé avec le même index sur la même table que celle à partir de laquelle il a été récupéré à l’origine.</span><span class="sxs-lookup"><span data-stu-id="96a05-107">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="96a05-108">Le signet d’index secondaire d’une entrée d’index peut être récupéré à l’aide de **JetGotoSecondaryIndexBookmark**.</span><span class="sxs-lookup"><span data-stu-id="96a05-108">The secondary index bookmark for an index entry can be retrieved using **JetGotoSecondaryIndexBookmark**.</span></span>

<span data-ttu-id="96a05-109">**Windows XP :**  **JetGotoSecondaryIndexBookmark** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96a05-109">**Windows XP:**  **JetGotoSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="96a05-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96a05-110">Parameters</span></span>

<span data-ttu-id="96a05-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="96a05-111">*sesid*</span></span>

<span data-ttu-id="96a05-112">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="96a05-112">The session to use for this call.</span></span>

<span data-ttu-id="96a05-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="96a05-113">*tableid*</span></span>

<span data-ttu-id="96a05-114">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="96a05-114">The cursor to use for this call.</span></span>

<span data-ttu-id="96a05-115">*pvSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="96a05-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="96a05-116">Mémoire tampon qui contient la clé secondaire à utiliser pour positionner le curseur.</span><span class="sxs-lookup"><span data-stu-id="96a05-116">The buffer that contains the secondary key to use to position the cursor.</span></span>

<span data-ttu-id="96a05-117">*cbSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="96a05-117">*cbSecondaryKey*</span></span>

<span data-ttu-id="96a05-118">Taille de la clé secondaire dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="96a05-118">The size of the secondary key in the buffer.</span></span>

<span data-ttu-id="96a05-119">*pvPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="96a05-119">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="96a05-120">Mémoire tampon qui contient le signet de clé primaire à utiliser pour positionner le curseur.</span><span class="sxs-lookup"><span data-stu-id="96a05-120">The buffer that contains the primary key bookmark to use to position the cursor.</span></span>

<span data-ttu-id="96a05-121">*cbPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="96a05-121">*cbPrimaryBookmark*</span></span>

<span data-ttu-id="96a05-122">Taille du signet de clé primaire dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="96a05-122">The size of the primary key bookmark in the buffer.</span></span>

<span data-ttu-id="96a05-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="96a05-123">*grbit*</span></span>

<span data-ttu-id="96a05-124">Groupe de bits qui spécifie zéro, une ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="96a05-124">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96a05-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="96a05-125">Value</span></span></p></th>
<th><p><span data-ttu-id="96a05-126">Signification</span><span class="sxs-lookup"><span data-stu-id="96a05-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96a05-127">JET_bitBookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="96a05-127">JET_bitBookmarkPermitVirtualCurrency</span></span></p></td>
<td><p><span data-ttu-id="96a05-128">Dans le cas où l’entrée d’index ne peut plus être trouvée, le curseur est placé à gauche de l’emplacement où cette entrée d’index a été trouvée précédemment.</span><span class="sxs-lookup"><span data-stu-id="96a05-128">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="96a05-129">L’opération échouera toujours avec JET_errRecordDeleted ; Toutefois, il est possible de passer à l’entrée d’index suivante ou précédente relative à l’entrée d’index manquante.</span><span class="sxs-lookup"><span data-stu-id="96a05-129">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="96a05-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="96a05-130">Return Value</span></span>

<span data-ttu-id="96a05-131">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="96a05-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="96a05-132">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="96a05-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96a05-133">Code de retour</span><span class="sxs-lookup"><span data-stu-id="96a05-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="96a05-134">Description</span><span class="sxs-lookup"><span data-stu-id="96a05-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96a05-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="96a05-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="96a05-136">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="96a05-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96a05-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="96a05-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="96a05-138">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="96a05-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96a05-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="96a05-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="96a05-140">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="96a05-140">The operation cannot complete because is because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="96a05-141"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96a05-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96a05-142">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="96a05-142">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="96a05-143">Le signet de l’index secondaire fourni n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="96a05-143">The secondary index bookmark that was provided was invalid.</span></span> <span data-ttu-id="96a05-144">Cette erreur s’est peut-être produite parce que la clé secondaire est égale à zéro ou que le pointeur de la mémoire tampon de la clé secondaire a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="96a05-144">This error might have occurred because the secondary key is zero or the secondary key buffer pointer is <strong>NULL</strong>.</span></span> <span data-ttu-id="96a05-145">Cette erreur se produit car</span><span class="sxs-lookup"><span data-stu-id="96a05-145">This error occurs because</span></span></p>
<ul>
<li><p><span data-ttu-id="96a05-146">L’index secondaire actuel n’a pas de contrainte d’unicité et la taille du signet fourni est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="96a05-146">The current secondary index does not have a uniqueness constraint and the size of the provided bookmark is zero.</span></span></p></li>
<li><p><span data-ttu-id="96a05-147">Le pointeur de la mémoire tampon du signet a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="96a05-147">The bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96a05-148">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="96a05-148">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="96a05-149">Le curseur ne se trouve pas actuellement sur un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="96a05-149">The cursor is not currently on a secondary index.</span></span> <span data-ttu-id="96a05-150">Il n’est pas utile d’accéder à un signet d’index secondaire lorsque le curseur n’utilise pas actuellement un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="96a05-150">It is not meaningful to go to a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="96a05-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> doit être utilisé lorsque le curseur ne se trouve pas sur un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="96a05-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96a05-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="96a05-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="96a05-153">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="96a05-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96a05-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="96a05-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="96a05-155">L’entrée d’index associée au signet d’index secondaire est introuvable.</span><span class="sxs-lookup"><span data-stu-id="96a05-155">The index entry that is associated with the secondary index bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96a05-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="96a05-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="96a05-157">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="96a05-157">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96a05-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="96a05-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="96a05-159">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="96a05-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="96a05-160"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96a05-160"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96a05-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="96a05-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="96a05-162">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="96a05-162">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96a05-163">Si cette fonction est exécutée correctement, le curseur est positionné sur une entrée d’index associée au signet d’index secondaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="96a05-163">If this function succeeds, the cursor will be positioned at an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="96a05-164">Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée.</span><span class="sxs-lookup"><span data-stu-id="96a05-164">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="96a05-165">Si une plage d’index est en vigueur, cette plage d’index sera annulée.</span><span class="sxs-lookup"><span data-stu-id="96a05-165">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="96a05-166">Si une clé de recherche a été construite pour le curseur à utiliser, cette clé de recherche sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="96a05-166">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="96a05-167">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="96a05-167">No change to the database state will occur.</span></span>

<span data-ttu-id="96a05-168">Si cette fonction échoue, la position du curseur reste inchangée, sauf si JET_errRecordDeleted est retourné et JET_bitBookmarkPermitVirtualCurrency est spécifié.</span><span class="sxs-lookup"><span data-stu-id="96a05-168">If this function fails, the position of the cursor remains unchanged unless JET_errRecordDeleted is returned and JET_bitBookmarkPermitVirtualCurrency is specified.</span></span> <span data-ttu-id="96a05-169">Dans ce cas, le curseur est positionné à l’emplacement où l’entrée d’index associée au signet de l’index secondaire spécifié aurait été.</span><span class="sxs-lookup"><span data-stu-id="96a05-169">In that case, the cursor will be positioned where the index entry that is associated with the specified secondary index bookmark would have been.</span></span> <span data-ttu-id="96a05-170">Le curseur peut être déplacé par rapport à cette position, mais il n’est pas toujours sur une entrée d’index valide.</span><span class="sxs-lookup"><span data-stu-id="96a05-170">The cursor can be moved relative to that position, but is still not on a valid index entry.</span></span>

<span data-ttu-id="96a05-171">Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée.</span><span class="sxs-lookup"><span data-stu-id="96a05-171">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="96a05-172">Si une plage d’index est en vigueur, cette plage d’index sera annulée.</span><span class="sxs-lookup"><span data-stu-id="96a05-172">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="96a05-173">Si une clé de recherche a été construite pour le curseur à utiliser, cette clé de recherche sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="96a05-173">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="96a05-174">Dans tous les cas, aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="96a05-174">In any case, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="96a05-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96a05-175">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96a05-176"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="96a05-176"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="96a05-177">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96a05-177">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96a05-178"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="96a05-178"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="96a05-179">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="96a05-179">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96a05-180"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="96a05-180"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="96a05-181">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="96a05-181">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96a05-182"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="96a05-182"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="96a05-183">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="96a05-183">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96a05-184"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="96a05-184"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="96a05-185">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="96a05-185">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="96a05-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96a05-186">See Also</span></span>

[<span data-ttu-id="96a05-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="96a05-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="96a05-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="96a05-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="96a05-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="96a05-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="96a05-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="96a05-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="96a05-191">JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="96a05-191">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)  
[<span data-ttu-id="96a05-192">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="96a05-192">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="96a05-193">JetStopService</span><span class="sxs-lookup"><span data-stu-id="96a05-193">JetStopService</span></span>](./jetstopservice-function.md)

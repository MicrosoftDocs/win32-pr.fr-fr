---
description: 'En savoir plus sur : fonction JetGotoBookmark'
title: JetGotoBookmark fonction)
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 89dde261648b396bcfc9532911c0d4acd3c88828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529428"
---
# <a name="jetgotobookmark-function"></a><span data-ttu-id="2bea5-103">JetGotoBookmark fonction)</span><span class="sxs-lookup"><span data-stu-id="2bea5-103">JetGotoBookmark Function</span></span>


<span data-ttu-id="2bea5-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2bea5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotobookmark-function"></a><span data-ttu-id="2bea5-105">JetGotoBookmark fonction)</span><span class="sxs-lookup"><span data-stu-id="2bea5-105">JetGotoBookmark Function</span></span>

<span data-ttu-id="2bea5-106">La fonction **JetGotoBookmark** positionne un curseur sur une entrée d’index pour l’enregistrement associé au signet spécifié.</span><span class="sxs-lookup"><span data-stu-id="2bea5-106">The **JetGotoBookmark** function positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="2bea5-107">Le signet peut être utilisé avec n’importe quel index défini sur une table.</span><span class="sxs-lookup"><span data-stu-id="2bea5-107">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="2bea5-108">Le signet d’un enregistrement peut être récupéré à l’aide de [JetGetBookmark](./jetgetbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="2bea5-108">The bookmark for a record can be retrieved using [JetGetBookmark](./jetgetbookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a><span data-ttu-id="2bea5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bea5-109">Parameters</span></span>

<span data-ttu-id="2bea5-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2bea5-110">*sesid*</span></span>

<span data-ttu-id="2bea5-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="2bea5-111">The session to use for this call.</span></span>

<span data-ttu-id="2bea5-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="2bea5-112">*tableid*</span></span>

<span data-ttu-id="2bea5-113">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="2bea5-113">The cursor to use for this call.</span></span>

<span data-ttu-id="2bea5-114">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="2bea5-114">*pvBookmark*</span></span>

<span data-ttu-id="2bea5-115">Mémoire tampon qui contient le signet à utiliser pour positionner le curseur.</span><span class="sxs-lookup"><span data-stu-id="2bea5-115">The buffer that contains the bookmark to use to position the cursor.</span></span>

<span data-ttu-id="2bea5-116">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="2bea5-116">*cbBookmark*</span></span>

<span data-ttu-id="2bea5-117">Taille du signet dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2bea5-117">The size of the bookmark in the buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="2bea5-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2bea5-118">Return Value</span></span>

<span data-ttu-id="2bea5-119">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="2bea5-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2bea5-120">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2bea5-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2bea5-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2bea5-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="2bea5-122">Description</span><span class="sxs-lookup"><span data-stu-id="2bea5-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bea5-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2bea5-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2bea5-124">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="2bea5-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bea5-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2bea5-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2bea5-126">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="2bea5-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bea5-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2bea5-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2bea5-128">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="2bea5-128">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="2bea5-129"><strong>Windows XP :</strong>   Cette valeur de retour a été introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2bea5-129"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bea5-130">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="2bea5-130">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="2bea5-131">Le signet fourni n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2bea5-131">The bookmark that was provided is invalid.</span></span> <span data-ttu-id="2bea5-132">Cela peut être dû au fait que la taille du signet est égale à zéro ou que le pointeur de la mémoire tampon du signet a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="2bea5-132">This might have occurred because the size of the bookmark is zero or the bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bea5-133">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="2bea5-133">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="2bea5-134">Le curseur se trouve sur un index secondaire et aucune entrée d’index n’a été trouvée pour l’enregistrement associé au signet.</span><span class="sxs-lookup"><span data-stu-id="2bea5-134">The cursor is on a secondary index and no index entry could be found for the record that is associated with the bookmark.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bea5-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2bea5-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2bea5-136">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="2bea5-136">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bea5-137">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="2bea5-137">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="2bea5-138">L’enregistrement associé au signet est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2bea5-138">The record that is associated with the bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bea5-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2bea5-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2bea5-140">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="2bea5-140">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bea5-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="2bea5-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="2bea5-142">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="2bea5-142">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="2bea5-143"><strong>Windows XP :</strong>   Cette valeur de retour a été introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2bea5-143"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bea5-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2bea5-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2bea5-145">L’opération ne peut pas se terminer car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="2bea5-145">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2bea5-146">Si cette fonction est réussie, le curseur est positionné sur une entrée d’index pour l’enregistrement associé au signet spécifié.</span><span class="sxs-lookup"><span data-stu-id="2bea5-146">If this function succeeds, the cursor will be positioned at an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="2bea5-147">Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée.</span><span class="sxs-lookup"><span data-stu-id="2bea5-147">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="2bea5-148">Si une plage d’index est en vigueur, cette plage d’index sera annulée.</span><span class="sxs-lookup"><span data-stu-id="2bea5-148">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="2bea5-149">Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="2bea5-149">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="2bea5-150">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="2bea5-150">No change to the database state will occur.</span></span>

<span data-ttu-id="2bea5-151">Si cette fonction échoue, la position du curseur reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="2bea5-151">If this function fails, the position of the cursor will remain unchanged.</span></span> <span data-ttu-id="2bea5-152">Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée.</span><span class="sxs-lookup"><span data-stu-id="2bea5-152">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="2bea5-153">Si une plage d’index est en vigueur, cette plage d’index sera annulée.</span><span class="sxs-lookup"><span data-stu-id="2bea5-153">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="2bea5-154">Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="2bea5-154">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="2bea5-155">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="2bea5-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2bea5-156">Notes</span><span class="sxs-lookup"><span data-stu-id="2bea5-156">Remarks</span></span>

<span data-ttu-id="2bea5-157">Il existe deux façons d’utiliser un signet pour positionner un curseur sur un index.</span><span class="sxs-lookup"><span data-stu-id="2bea5-157">There are two ways to use a bookmark to position a cursor on an index.</span></span> <span data-ttu-id="2bea5-158">La première consiste à utiliser le signet pour positionner directement sur l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2bea5-158">The first is to use the bookmark to position on the record directly.</span></span> <span data-ttu-id="2bea5-159">Cela se produit lorsque l’index actuel du curseur est l’index primaire.</span><span class="sxs-lookup"><span data-stu-id="2bea5-159">This occurs when the current index of the cursor is the primary index.</span></span> <span data-ttu-id="2bea5-160">Cette technique fonctionne, car un signet ESENT est le même que la clé primaire de l’enregistrement associé.</span><span class="sxs-lookup"><span data-stu-id="2bea5-160">This technique works because an ESENT bookmark is the same as the associated record's primary key.</span></span>

<span data-ttu-id="2bea5-161">La deuxième façon d’utiliser un signet est de le positionner sur une entrée dans un index secondaire qui correspond à l’enregistrement associé à ce signet.</span><span class="sxs-lookup"><span data-stu-id="2bea5-161">The second way to use a bookmark is to position it on an entry in a secondary index that corresponds to the record that is associated with that bookmark.</span></span> <span data-ttu-id="2bea5-162">Pendant ce processus, le moteur recherche l’enregistrement réel à l’aide du signet sur l’index primaire.</span><span class="sxs-lookup"><span data-stu-id="2bea5-162">During this process, the engine looks up the actual record using the bookmark on the primary index.</span></span> <span data-ttu-id="2bea5-163">Il utilise ensuite les données d’enregistrement et la définition d’index secondaire pour calculer une clé dans l’index secondaire qui pointe vers l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2bea5-163">It then uses the record data and the secondary index definition to compute a key into the secondary index that points to the record.</span></span> <span data-ttu-id="2bea5-164">Il positionne ensuite le curseur sur l’entrée d’index pour cette clé.</span><span class="sxs-lookup"><span data-stu-id="2bea5-164">It then positions the cursor on the index entry for that key.</span></span> <span data-ttu-id="2bea5-165">Si le curseur se trouve actuellement sur un index secondaire sur une ou plusieurs colonnes clés à valeurs multiples, le curseur est positionné sur l’entrée d’index correspondant à la première valeur multiple de chacune de ces colonnes clés.</span><span class="sxs-lookup"><span data-stu-id="2bea5-165">If the cursor is currently on a secondary index over one or more multi-valued key columns, the cursor will be positioned on the index entry corresponding to the first multi-value of each of those key columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2bea5-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bea5-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bea5-167"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2bea5-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2bea5-168">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="2bea5-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bea5-169"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2bea5-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2bea5-170">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2bea5-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bea5-171"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2bea5-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2bea5-172">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2bea5-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bea5-173"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="2bea5-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2bea5-174">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2bea5-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bea5-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2bea5-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2bea5-176">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2bea5-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2bea5-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bea5-177">See Also</span></span>

[<span data-ttu-id="2bea5-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2bea5-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2bea5-179">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2bea5-179">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2bea5-180">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2bea5-180">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2bea5-181">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="2bea5-181">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

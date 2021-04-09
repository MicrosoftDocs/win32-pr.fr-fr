---
description: 'En savoir plus sur : fonction JetGetBookmark'
title: JetGetBookmark fonction)
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115846"
---
# <a name="jetgetbookmark-function"></a><span data-ttu-id="e6dc8-103">JetGetBookmark fonction)</span><span class="sxs-lookup"><span data-stu-id="e6dc8-103">JetGetBookmark Function</span></span>


<span data-ttu-id="e6dc8-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="e6dc8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetbookmark-function"></a><span data-ttu-id="e6dc8-105">JetGetBookmark fonction)</span><span class="sxs-lookup"><span data-stu-id="e6dc8-105">JetGetBookmark Function</span></span>

<span data-ttu-id="e6dc8-106">La fonction **JetGetBookmark** récupère le signet de l’enregistrement associé à l’entrée d’index à la position actuelle d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-106">The **JetGetBookmark** function retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="e6dc8-107">Ce signet peut ensuite être utilisé pour repositionner ce curseur dans le même enregistrement à l’aide de [JetGoToBookmark](./jetgotobookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="e6dc8-107">This bookmark can then be used to reposition that cursor back to the same record using [JetGoToBookmark](./jetgotobookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="e6dc8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6dc8-108">Parameters</span></span>

<span data-ttu-id="e6dc8-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e6dc8-109">*sesid*</span></span>

<span data-ttu-id="e6dc8-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-110">The session to use for this call.</span></span>

<span data-ttu-id="e6dc8-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="e6dc8-111">*tableid*</span></span>

<span data-ttu-id="e6dc8-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-112">The cursor to use for this call.</span></span>

<span data-ttu-id="e6dc8-113">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="e6dc8-113">*pvBookmark*</span></span>

<span data-ttu-id="e6dc8-114">Mémoire tampon de sortie qui reçoit le signet.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-114">The output buffer that receives the bookmark.</span></span>

<span data-ttu-id="e6dc8-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="e6dc8-115">*cbMax*</span></span>

<span data-ttu-id="e6dc8-116">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-116">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="e6dc8-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="e6dc8-117">*pcbActual*</span></span>

<span data-ttu-id="e6dc8-118">Taille réelle, en octets, du signet.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-118">The actual size, in bytes, of the bookmark.</span></span>

<span data-ttu-id="e6dc8-119">Si ce paramètre a la **valeur null** , la taille réelle du signet n’est pas retournée.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-119">If this parameter is **NULL** then the actual size of the bookmark will not be returned.</span></span>

<span data-ttu-id="e6dc8-120">Si la mémoire tampon de sortie est trop petite, la taille réelle du signet sera toujours retournée.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-120">If the output buffer is too small, the actual size of the bookmark will still be returned.</span></span> <span data-ttu-id="e6dc8-121">Cela signifie que ce nombre sera supérieur à la taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-121">That means that this number will be larger than the size of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="e6dc8-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e6dc8-122">Return Value</span></span>

<span data-ttu-id="e6dc8-123">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e6dc8-124">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e6dc8-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6dc8-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e6dc8-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="e6dc8-126">Description</span><span class="sxs-lookup"><span data-stu-id="e6dc8-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6dc8-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e6dc8-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e6dc8-128">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6dc8-129">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="e6dc8-129">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="e6dc8-130">L’opération s’est terminée correctement, mais la mémoire tampon de sortie était trop petite pour recevoir l’intégralité du signet.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-130">The operation completed successfully, but the output buffer was too small to receive the entire bookmark.</span></span> <span data-ttu-id="e6dc8-131">La mémoire tampon de sortie a été remplie avec la plus grande partie du signet.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-131">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="e6dc8-132">La taille réelle du signet a également été retournée, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-132">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6dc8-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e6dc8-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e6dc8-134">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-134">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6dc8-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e6dc8-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e6dc8-136">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-136">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="e6dc8-137"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-137"><strong>Windows XP:  </strong>This return values is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6dc8-138">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="e6dc8-138">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="e6dc8-139">Le curseur n’est pas positionné sur un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-139">The cursor is not positioned on a record.</span></span> <span data-ttu-id="e6dc8-140">Cela peut se produire pour de nombreuses raisons différentes.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-140">This can happen for many different reasons.</span></span> <span data-ttu-id="e6dc8-141">Par exemple, cela se produit si le curseur est positionné après le dernier enregistrement de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-141">For example, this will happen if the cursor is positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6dc8-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e6dc8-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e6dc8-143">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-143">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6dc8-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e6dc8-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e6dc8-145">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6dc8-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e6dc8-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e6dc8-147">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="e6dc8-148"><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6dc8-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e6dc8-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e6dc8-150">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-150">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e6dc8-151">Si cette fonction est réussie, le signet de l’enregistrement qui est associé à l’entrée d’index à la position actuelle d’un curseur est retourné dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-151">If this function succeeds, the bookmark for the record that is associated with the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="e6dc8-152">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-152">No change to the database state will occur.</span></span>

<span data-ttu-id="e6dc8-153">Si cette fonction échoue, l’état de la mémoire tampon de sortie et la taille réelle du signet ne sont pas définis, sauf si JET_errBufferTooSmall a été retourné.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-153">If this function fails, the state of the output buffer and the actual size of the bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="e6dc8-154">Dans le cas où JET_errBufferTooSmall est retourné, la mémoire tampon de sortie contiendra la plus grande partie du signet qui tient dans l’espace fourni et la taille réelle du signet sera exacte.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-154">In the event that JET_errBufferTooSmall is returned, the output buffer will contain as much of the bookmark as will fit in the space provided and the actual size of the bookmark will be accurate.</span></span> <span data-ttu-id="e6dc8-155">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e6dc8-156">Notes</span><span class="sxs-lookup"><span data-stu-id="e6dc8-156">Remarks</span></span>

<span data-ttu-id="e6dc8-157">Les signets doivent généralement être traités comme des blocs de données opaques.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-157">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="e6dc8-158">Aucune tentative n’est faite pour exploiter la structure interne de ces données.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-158">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="e6dc8-159">Toutefois, les conditions suivantes sont vraies pour tous les signets ESENT :</span><span class="sxs-lookup"><span data-stu-id="e6dc8-159">However, the following conditions are true of all ESENT bookmarks:</span></span>

  - <span data-ttu-id="e6dc8-160">Un signet identifie de façon unique un enregistrement dans une table donnée.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-160">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="e6dc8-161">Le signet d’un enregistrement ne changera pas pendant la durée de vie de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-161">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="e6dc8-162">Le signet d’un enregistrement est le même que la clé de cet enregistrement sur l’index primaire sur la table contenant cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-162">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="e6dc8-163">Si aucun index primaire n’est défini sur cette table, le moteur de base de données crée son propre signet pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-163">If no primary index is defined over that table the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="e6dc8-164">Les signets peuvent être comparés les uns aux autres à l’aide de la fonction [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) pour établir leur classement relatif dans l’index primaire sur la table des enregistrements sources.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-164">Bookmarks can be compared against each other using the [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) function to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="e6dc8-165">Si aucun index primaire n’est défini sur cette table, il n’est pas judicieux d’utiliser l’ordre relatif des signets de cette table.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-165">If no primary index is defined over that table, it is not meaningful to use the relative ordering of bookmarks from that table.</span></span>

  - <span data-ttu-id="e6dc8-166">Il est inutile de comparer les signets des enregistrements de différentes tables entre eux.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-166">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="e6dc8-167">Un signet est toujours inférieur ou égal à JET_cbBookmarkMost (256) octets en longueur, avant Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-167">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length, prior to Windows Vista.</span></span>
    
<span data-ttu-id="e6dc8-168">**Windows Vista :** Sur Windows Vista et les versions ultérieures, les signets peuvent être plus grands que JET_cbBookmarkMost (256) octets.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-168">**Windows Vista:** On Windows Vista and later releases, bookmarks can be larger than JET_cbBookmarkMost (256) bytes.</span></span> <span data-ttu-id="e6dc8-169">La taille maximale d’un signet est égale à la valeur actuelle de JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-169">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e6dc8-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6dc8-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6dc8-171"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e6dc8-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e6dc8-172">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6dc8-173"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="e6dc8-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e6dc8-174">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6dc8-175"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="e6dc8-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e6dc8-176">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6dc8-177"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="e6dc8-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e6dc8-178">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6dc8-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e6dc8-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e6dc8-180">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e6dc8-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e6dc8-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6dc8-181">See Also</span></span>

[<span data-ttu-id="e6dc8-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e6dc8-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e6dc8-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e6dc8-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e6dc8-184">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e6dc8-184">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e6dc8-185">JetGoToBookmark</span><span class="sxs-lookup"><span data-stu-id="e6dc8-185">JetGoToBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="e6dc8-186">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e6dc8-186">JetStopService</span></span>](./jetstopservice-function.md)  
<span data-ttu-id="e6dc8-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="e6dc8-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>

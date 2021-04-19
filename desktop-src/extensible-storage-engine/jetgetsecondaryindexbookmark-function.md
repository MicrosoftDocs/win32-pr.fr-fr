---
description: 'En savoir plus sur : fonction JetGetSecondaryIndexBookmark'
title: JetGetSecondaryIndexBookmark fonction)
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533921"
---
# <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="35262-103">JetGetSecondaryIndexBookmark fonction)</span><span class="sxs-lookup"><span data-stu-id="35262-103">JetGetSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="35262-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="35262-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="35262-105">JetGetSecondaryIndexBookmark fonction)</span><span class="sxs-lookup"><span data-stu-id="35262-105">JetGetSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="35262-106">La fonction **JetGetSecondaryIndexBookmark** récupère un signet spécial pour l’entrée d’index secondaire à la position actuelle d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="35262-106">The **JetGetSecondaryIndexBookmark** function retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="35262-107">Ce signet peut ensuite être utilisé pour repositionner efficacement ce curseur sur la même entrée d’index à l’aide de [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="35262-107">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span></span> <span data-ttu-id="35262-108">Cela est particulièrement utile lors du repositionnement sur un index secondaire qui contient des clés dupliquées ou qui contient plusieurs entrées d’index pour le même enregistrement.</span><span class="sxs-lookup"><span data-stu-id="35262-108">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="35262-109">**Windows XP : JetGetSecondaryIndexBookmark** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="35262-109">**Windows XP:  JetGetSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="35262-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35262-110">Parameters</span></span>

<span data-ttu-id="35262-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="35262-111">*sesid*</span></span>

<span data-ttu-id="35262-112">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="35262-112">The session to use for this call.</span></span>

<span data-ttu-id="35262-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="35262-113">*tableid*</span></span>

<span data-ttu-id="35262-114">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="35262-114">The cursor to use for this call.</span></span>

<span data-ttu-id="35262-115">*pvSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="35262-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="35262-116">Mémoire tampon de sortie qui reçoit la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="35262-116">The output buffer that receives the secondary key.</span></span>

<span data-ttu-id="35262-117">*cbSecondaryKeyMax*</span><span class="sxs-lookup"><span data-stu-id="35262-117">*cbSecondaryKeyMax*</span></span>

<span data-ttu-id="35262-118">Taille maximale, en octets, de la mémoire tampon de sortie pour la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="35262-118">The maximum size, in bytes, of the output buffer for the secondary key.</span></span>

<span data-ttu-id="35262-119">*pcbSecondaryKeyActual*</span><span class="sxs-lookup"><span data-stu-id="35262-119">*pcbSecondaryKeyActual*</span></span>

<span data-ttu-id="35262-120">Reçoit la taille réelle, en octets, de la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="35262-120">Receives the actual size in bytes of the secondary key.</span></span>

<span data-ttu-id="35262-121">Si ce paramètre a la valeur NULL, la taille réelle de la clé secondaire n’est pas retournée.</span><span class="sxs-lookup"><span data-stu-id="35262-121">If this parameter is NULL, the actual size of the secondary key will not be returned.</span></span>

<span data-ttu-id="35262-122">Si la mémoire tampon de sortie est trop petite, la taille réelle de la clé secondaire est toujours retournée.</span><span class="sxs-lookup"><span data-stu-id="35262-122">If the output buffer is too small, the actual size of the secondary key will still be returned.</span></span> <span data-ttu-id="35262-123">Cela signifie que ce nombre sera supérieur à la taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="35262-123">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="35262-124">*pvPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="35262-124">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="35262-125">Mémoire tampon de sortie qui reçoit le signet de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="35262-125">The output buffer that receives the primary key bookmark.</span></span>

<span data-ttu-id="35262-126">*cbPrimaryBookmarkMax*</span><span class="sxs-lookup"><span data-stu-id="35262-126">*cbPrimaryBookmarkMax*</span></span>

<span data-ttu-id="35262-127">Taille maximale, en octets, de la mémoire tampon de sortie pour le signet de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="35262-127">The maximum size, in bytes, of the output buffer for the primary key bookmark.</span></span>

<span data-ttu-id="35262-128">*pcbPrimaryKeyActual*</span><span class="sxs-lookup"><span data-stu-id="35262-128">*pcbPrimaryKeyActual*</span></span>

<span data-ttu-id="35262-129">Reçoit la taille réelle, en octets, du signet de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="35262-129">Receives the actual size, in bytes, of the primary key bookmark.</span></span>

<span data-ttu-id="35262-130">Si ce paramètre a la valeur NULL, la taille réelle du signet de clé primaire n’est pas retournée.</span><span class="sxs-lookup"><span data-stu-id="35262-130">If this parameter is NULL then the actual size of the primary key bookmark will not be returned.</span></span>

<span data-ttu-id="35262-131">Si la mémoire tampon de sortie est trop petite, la taille réelle du signet de clé primaire sera toujours retournée.</span><span class="sxs-lookup"><span data-stu-id="35262-131">If the output buffer is too small, the actual size of the primary key bookmark will still be returned.</span></span> <span data-ttu-id="35262-132">Cela signifie que ce nombre sera supérieur à la taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="35262-132">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="35262-133">*grbit*</span><span class="sxs-lookup"><span data-stu-id="35262-133">*grbit*</span></span>

<span data-ttu-id="35262-134">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="35262-134">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="35262-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="35262-135">Return Value</span></span>

<span data-ttu-id="35262-136">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="35262-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="35262-137">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="35262-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35262-138">Code de retour</span><span class="sxs-lookup"><span data-stu-id="35262-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="35262-139">Description</span><span class="sxs-lookup"><span data-stu-id="35262-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35262-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="35262-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="35262-141">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="35262-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35262-142">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="35262-142">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="35262-143">L’opération s’est terminée correctement, mais l’une des mémoires tampons de sortie était trop petite pour recevoir les données demandées.</span><span class="sxs-lookup"><span data-stu-id="35262-143">The operation completed successfully, but one of the output buffers was too small to receive the requested data.</span></span></p>
<p><span data-ttu-id="35262-144">La mémoire tampon de sortie a été remplie avec la plus grande partie du signet.</span><span class="sxs-lookup"><span data-stu-id="35262-144">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="35262-145">La taille réelle du signet a également été retournée, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="35262-145">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35262-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="35262-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="35262-147">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="35262-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35262-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="35262-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="35262-149">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="35262-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="35262-150">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="35262-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35262-151">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="35262-151">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="35262-152">Le curseur ne se trouve pas actuellement sur un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="35262-152">The cursor is not currently on a secondary index.</span></span></p>
<p><span data-ttu-id="35262-153">Il n’est pas utile de récupérer un signet d’index secondaire lorsque le curseur n’utilise pas actuellement un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="35262-153">It is not meaningful to retrieve a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="35262-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> doit être utilisé lorsque le curseur ne se trouve pas sur un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="35262-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35262-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="35262-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="35262-156">Le curseur n’est pas positionné sur un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="35262-156">The cursor is not positioned on a record.</span></span></p>
<p><span data-ttu-id="35262-157">Cela peut se produire pour de nombreuses raisons différentes.</span><span class="sxs-lookup"><span data-stu-id="35262-157">This can happen for many different reasons.</span></span> <span data-ttu-id="35262-158">Par exemple, cela se produit si le curseur est actuellement positionné après le dernier enregistrement de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="35262-158">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35262-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="35262-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="35262-160">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="35262-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35262-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="35262-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="35262-162">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="35262-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35262-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="35262-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="35262-164">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="35262-164">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="35262-165">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="35262-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35262-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="35262-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="35262-167">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="35262-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="35262-168">En cas de réussite, le signet d’index secondaire de l’entrée d’index à la position actuelle d’un curseur est retourné dans les tampons de sortie.</span><span class="sxs-lookup"><span data-stu-id="35262-168">On success, the secondary index bookmark for the index entry at the current position of a cursor will be returned in the output buffers.</span></span> <span data-ttu-id="35262-169">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="35262-169">No change to the database state will occur.</span></span>

<span data-ttu-id="35262-170">En cas d’échec, l’état des tampons de sortie et la taille réelle du signet de l’index secondaire ne sont pas définis, sauf si JET_errBufferTooSmall a été retourné.</span><span class="sxs-lookup"><span data-stu-id="35262-170">On failure, the state of the output buffers and the actual size of the secondary index bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="35262-171">Dans le cas où JET_errBufferTooSmall est retourné, les tampons de sortie contiendront la plus grande partie du signet d’index secondaire, comme dans l’espace fourni et la taille réelle du signet d’index secondaire sera exacte.</span><span class="sxs-lookup"><span data-stu-id="35262-171">In the event that JET_errBufferTooSmall is returned, the output buffers will contain as much of the secondary index bookmark as will fit in the space provided and the actual size of the secondary index bookmark will be accurate.</span></span> <span data-ttu-id="35262-172">Dans tous les cas, aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="35262-172">In any case, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="35262-173">Notes</span><span class="sxs-lookup"><span data-stu-id="35262-173">Remarks</span></span>

<span data-ttu-id="35262-174">Les signets doivent généralement être traités comme des blocs de données opaques.</span><span class="sxs-lookup"><span data-stu-id="35262-174">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="35262-175">Aucune tentative n’est faite pour exploiter la structure interne de ces données.</span><span class="sxs-lookup"><span data-stu-id="35262-175">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="35262-176">Toutefois, les propriétés suivantes peuvent être connues en ce qui concerne tous les signets ESENT :</span><span class="sxs-lookup"><span data-stu-id="35262-176">However, the following properties can be known about all ESENT bookmarks:</span></span>

  - <span data-ttu-id="35262-177">Un signet identifie de façon unique un enregistrement dans une table donnée.</span><span class="sxs-lookup"><span data-stu-id="35262-177">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="35262-178">Le signet d’un enregistrement ne changera pas pendant la durée de vie de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="35262-178">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="35262-179">Le signet d’un enregistrement est le même que la clé de cet enregistrement sur l’index primaire sur la table contenant cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="35262-179">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="35262-180">Si aucun index primaire n’est défini sur cette table, le moteur de base de données crée son propre signet pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="35262-180">If no primary index is defined over that table, the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="35262-181">Les signets peuvent être comparés les uns aux autres à l’aide de [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) pour établir leur ordre relatif dans l’index primaire sur la table des enregistrements sources.</span><span class="sxs-lookup"><span data-stu-id="35262-181">Bookmarks may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="35262-182">Si aucun index primaire n’est défini sur cette table, l’ordre relatif des signets de cette table n’est pas significatif.</span><span class="sxs-lookup"><span data-stu-id="35262-182">If no primary index is defined over that table, the relative ordering of bookmarks from that table is not meaningful.</span></span>

  - <span data-ttu-id="35262-183">Il est inutile de comparer les signets des enregistrements de différentes tables entre eux.</span><span class="sxs-lookup"><span data-stu-id="35262-183">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="35262-184">Un signet est toujours inférieur ou égal à JET_cbBookmarkMost (256) octets dans une longueur antérieure à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="35262-184">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="35262-185">Sur Windows Vista et les versions ultérieures, les signets peuvent être plus volumineux.</span><span class="sxs-lookup"><span data-stu-id="35262-185">On Windows Vista and later releases, bookmarks can be larger.</span></span> <span data-ttu-id="35262-186">La taille maximale d’un signet est égale à la valeur actuelle de JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="35262-186">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

<span data-ttu-id="35262-187">Les clés doivent généralement être traitées comme des blocs de données opaques.</span><span class="sxs-lookup"><span data-stu-id="35262-187">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="35262-188">Aucune tentative n’est faite pour exploiter la structure interne de ces données.</span><span class="sxs-lookup"><span data-stu-id="35262-188">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="35262-189">Toutefois, les propriétés suivantes peuvent être connues en ce qui concerne toutes les clés ESENT :</span><span class="sxs-lookup"><span data-stu-id="35262-189">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="35262-190">Les clés peuvent être comparées les unes aux autres à l’aide de [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) pour établir leur ordre relatif dans l’index d’origine sur la table des entrées d’index source.</span><span class="sxs-lookup"><span data-stu-id="35262-190">Keys may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="35262-191">Il est inutile de comparer les clés des entrées d’index de différents index.</span><span class="sxs-lookup"><span data-stu-id="35262-191">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="35262-192">Une clé est toujours inférieure ou égale à JET_cbKeyMost (255) octets dans une longueur antérieure à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="35262-192">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="35262-193">Sur Windows Vista et les versions ultérieures, les clés peuvent être plus volumineuses.</span><span class="sxs-lookup"><span data-stu-id="35262-193">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="35262-194">La taille maximale d’une clé est égale à la valeur actuelle de JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="35262-194">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="35262-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35262-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35262-196"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="35262-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="35262-197">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="35262-197">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35262-198"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="35262-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="35262-199">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="35262-199">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35262-200"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="35262-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="35262-201">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="35262-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35262-202"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="35262-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="35262-203">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="35262-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35262-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="35262-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="35262-205">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="35262-205">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="35262-206">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35262-206">See Also</span></span>

[<span data-ttu-id="35262-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="35262-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="35262-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="35262-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="35262-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="35262-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="35262-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="35262-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="35262-211">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="35262-211">JetGetBookmark</span></span>](./jetgetbookmark-function.md)  
[<span data-ttu-id="35262-212">JetGotoSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="35262-212">JetGotoSecondaryIndexBookmark</span></span>](./jetgotosecondaryindexbookmark-function.md)  
[<span data-ttu-id="35262-213">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="35262-213">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
<span data-ttu-id="35262-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="35262-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>

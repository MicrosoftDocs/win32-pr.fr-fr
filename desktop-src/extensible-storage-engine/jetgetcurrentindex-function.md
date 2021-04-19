---
description: 'En savoir plus sur : fonction JetGetCurrentIndex'
title: JetGetCurrentIndex fonction)
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518791"
---
# <a name="jetgetcurrentindex-function"></a><span data-ttu-id="c4469-103">JetGetCurrentIndex fonction)</span><span class="sxs-lookup"><span data-stu-id="c4469-103">JetGetCurrentIndex Function</span></span>


<span data-ttu-id="c4469-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c4469-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcurrentindex-function"></a><span data-ttu-id="c4469-105">JetGetCurrentIndex fonction)</span><span class="sxs-lookup"><span data-stu-id="c4469-105">JetGetCurrentIndex Function</span></span>

<span data-ttu-id="c4469-106">La fonction **JetGetCurrentIndex** détermine le nom de l’index actuel d’un curseur donné.</span><span class="sxs-lookup"><span data-stu-id="c4469-106">The **JetGetCurrentIndex** function determines the name of the current index of a given cursor.</span></span> <span data-ttu-id="c4469-107">Ce nom est également utilisé pour resélectionner ultérieurement cet index comme index actuel à l’aide de [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4469-107">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="c4469-108">Elle peut également être utilisée pour découvrir les propriétés de cet index à l’aide de [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4469-108">It can also be used to discover the properties of that index using [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="c4469-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4469-109">Parameters</span></span>

<span data-ttu-id="c4469-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c4469-110">*sesid*</span></span>

<span data-ttu-id="c4469-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="c4469-111">The session to use for this call.</span></span>

<span data-ttu-id="c4469-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c4469-112">*tableid*</span></span>

<span data-ttu-id="c4469-113">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="c4469-113">The cursor to use for this call.</span></span>

<span data-ttu-id="c4469-114">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="c4469-114">*szIndexName*</span></span>

<span data-ttu-id="c4469-115">Mémoire tampon de sortie qui reçoit le nom de l’index actuel du curseur.</span><span class="sxs-lookup"><span data-stu-id="c4469-115">The output buffer that receives the name of the current index of the cursor.</span></span>

<span data-ttu-id="c4469-116">*cchIndexName*</span><span class="sxs-lookup"><span data-stu-id="c4469-116">*cchIndexName*</span></span>

<span data-ttu-id="c4469-117">Taille maximale en caractères de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="c4469-117">The maximum size in characters of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="c4469-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c4469-118">Return Value</span></span>

<span data-ttu-id="c4469-119">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="c4469-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c4469-120">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c4469-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4469-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c4469-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="c4469-122">Description</span><span class="sxs-lookup"><span data-stu-id="c4469-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4469-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c4469-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c4469-124">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c4469-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4469-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c4469-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c4469-126">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c4469-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4469-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c4469-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c4469-128">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="c4469-128">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c4469-129">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c4469-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4469-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c4469-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c4469-131">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="c4469-131">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4469-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c4469-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c4469-133">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="c4469-133">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4469-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c4469-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c4469-135">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="c4469-135">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="c4469-136">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c4469-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4469-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c4469-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c4469-138">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="c4469-138">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4469-139">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="c4469-139">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="c4469-140">L’opération s’est terminée correctement, mais la mémoire tampon de sortie était trop petite pour recevoir l’intégralité du nom de l’index.</span><span class="sxs-lookup"><span data-stu-id="c4469-140">The operation completed successfully, but the output buffer was too small to receive the entire index name.</span></span></p>
<p><span data-ttu-id="c4469-141">La mémoire tampon de sortie a été remplie avec la plus grande partie du nom de l’index.</span><span class="sxs-lookup"><span data-stu-id="c4469-141">The output buffer has been filled with as much of the index name as would fit.</span></span> <span data-ttu-id="c4469-142">Si la mémoire tampon de sortie a au moins un caractère de longueur, la chaîne de cette mémoire tampon de sortie se termine par une valeur null.</span><span class="sxs-lookup"><span data-stu-id="c4469-142">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="c4469-143"><strong>Remarque  </strong> Cette erreur n’est pas renvoyée si cchIndexName est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c4469-143"><strong>Note  </strong>This error will not be returned if cchIndexName is zero.</span></span> <span data-ttu-id="c4469-144">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c4469-144">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c4469-145">En cas de réussite, le nom de l’index actuel du curseur donné sera retourné dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="c4469-145">On success, the name of the current index of the given cursor will be returned in the output buffer.</span></span> <span data-ttu-id="c4469-146">Si JET_wrnBufferTruncated est retourné, la mémoire tampon de sortie contiendra la plus grande partie du nom d’index, comme dans l’espace prévu à cet effet.</span><span class="sxs-lookup"><span data-stu-id="c4469-146">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the index name as will fit in the space provided.</span></span> <span data-ttu-id="c4469-147">Si la mémoire tampon de sortie a au moins un caractère de longueur, alors la chaîne retournée dans cette mémoire tampon se termine par une valeur null.</span><span class="sxs-lookup"><span data-stu-id="c4469-147">If the output buffer is at least one character in length then the string returned in that buffer will be null terminated.</span></span> <span data-ttu-id="c4469-148">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="c4469-148">No change to the database state will occur.</span></span>

<span data-ttu-id="c4469-149">En cas d’échec, l’état de la mémoire tampon de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="c4469-149">On failure, the state of the output buffer will be undefined.</span></span> <span data-ttu-id="c4469-150">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="c4469-150">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c4469-151">Notes</span><span class="sxs-lookup"><span data-stu-id="c4469-151">Remarks</span></span>

<span data-ttu-id="c4469-152">S’il n’y a pas d’index actuel pour le curseur, une chaîne vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="c4469-152">If there is no current index for the cursor then an empty string will be returned.</span></span> <span data-ttu-id="c4469-153">Cela peut se produire lorsque le curseur se trouve sur l’index cluster de la table et qu’aucun index primaire n’a été défini.</span><span class="sxs-lookup"><span data-stu-id="c4469-153">This can happen when the cursor is on the clustered index of the table and no primary index was defined.</span></span> <span data-ttu-id="c4469-154">Cet index est appelé index séquentiel de la table et n’a pas de définition.</span><span class="sxs-lookup"><span data-stu-id="c4469-154">This index is known as the sequential index of the table and has no definition.</span></span> <span data-ttu-id="c4469-155">Dans tous les cas, la définition de l’index actuel sur une chaîne vide à l’aide de [JetSetCurrentIndex](./jetsetcurrentindex-function.md) sélectionne l’index cluster, quelle que soit la présence d’une définition d’index primaire.</span><span class="sxs-lookup"><span data-stu-id="c4469-155">In any case, setting the current index to an empty string using [JetSetCurrentIndex](./jetsetcurrentindex-function.md) will select the clustered index regardless of the presence of a primary index definition.</span></span>

<span data-ttu-id="c4469-156">Il existe un bogue important dans cette fonction qui est présent dans toutes les versions.</span><span class="sxs-lookup"><span data-stu-id="c4469-156">There is an important bug in this function that is present in all releases.</span></span> <span data-ttu-id="c4469-157">Si la mémoire tampon de sortie est trop petite pour recevoir l’intégralité du nom de l’index et que la mémoire tampon de sortie a au moins un caractère de longueur, JET_wrnBufferTruncated ne sera pas retourné.</span><span class="sxs-lookup"><span data-stu-id="c4469-157">If the output buffer is too small to receive the entire index name and the output buffer is at least one character in length then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="c4469-158">JET_errSuccess est retourné à la place.</span><span class="sxs-lookup"><span data-stu-id="c4469-158">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="c4469-159">Pour éviter ce problème, la longueur de la mémoire tampon de sortie doit toujours être d’au moins JET_cbNameMost + 1 (65) caractères.</span><span class="sxs-lookup"><span data-stu-id="c4469-159">To avoid this issue, the output buffer should always be at least JET_cbNameMost + 1 (65) characters in length.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c4469-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4469-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4469-161"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c4469-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c4469-162">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="c4469-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4469-163"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="c4469-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c4469-164">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c4469-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4469-165"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="c4469-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c4469-166">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="c4469-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4469-167"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="c4469-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c4469-168">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c4469-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4469-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c4469-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c4469-170">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c4469-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4469-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c4469-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c4469-172">Implémenté en tant que <strong>JetGetCurrentIndexW</strong> (Unicode) et <strong>JetGetCurrentIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c4469-172">Implemented as <strong>JetGetCurrentIndexW</strong> (Unicode) and <strong>JetGetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c4469-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4469-173">See Also</span></span>

[<span data-ttu-id="c4469-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c4469-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c4469-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c4469-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c4469-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c4469-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c4469-177">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c4469-177">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="c4469-178">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="c4469-178">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)

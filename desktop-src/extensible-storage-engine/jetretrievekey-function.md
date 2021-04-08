---
description: 'En savoir plus sur : fonction JetRetrieveKey'
title: Fonction JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035195"
---
# <a name="jetretrievekey-function"></a><span data-ttu-id="8d1ea-103">Fonction JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="8d1ea-103">JetRetrieveKey Function</span></span>


<span data-ttu-id="8d1ea-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="8d1ea-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievekey-function"></a><span data-ttu-id="8d1ea-105">Fonction JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="8d1ea-105">JetRetrieveKey Function</span></span>

<span data-ttu-id="8d1ea-106">La fonction **JetRetrieveKey** récupère la clé de l’entrée d’index à la position actuelle d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-106">The **JetRetrieveKey** function retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="8d1ea-107">Ces clés sont construites par des appels à [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="8d1ea-107">Such keys are constructed by calls to [JetMakeKey](./jetmakekey-function.md).</span></span> <span data-ttu-id="8d1ea-108">La clé Récupérée peut ensuite être utilisée pour retourner efficacement ce curseur à la même entrée d’index par un appel à [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="8d1ea-108">The retrieved key can then be used to efficiently return that cursor to the same index entry by a call to [JetSeek](./jetseek-function.md).</span></span>

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="8d1ea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d1ea-109">Parameters</span></span>

<span data-ttu-id="8d1ea-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8d1ea-110">*sesid*</span></span>

<span data-ttu-id="8d1ea-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-111">The session to use for this call.</span></span>

<span data-ttu-id="8d1ea-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="8d1ea-112">*tableid*</span></span>

<span data-ttu-id="8d1ea-113">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-113">The cursor to use for this call.</span></span>

<span data-ttu-id="8d1ea-114">*pvData*</span><span class="sxs-lookup"><span data-stu-id="8d1ea-114">*pvData*</span></span>

<span data-ttu-id="8d1ea-115">Mémoire tampon de sortie qui recevra la clé.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-115">The output buffer that will receive the key.</span></span>

<span data-ttu-id="8d1ea-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="8d1ea-116">*cbMax*</span></span>

<span data-ttu-id="8d1ea-117">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-117">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="8d1ea-118">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="8d1ea-118">*pcbActual*</span></span>

<span data-ttu-id="8d1ea-119">Reçoit la taille réelle, en octets, de la clé.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-119">Receives the actual size in bytes of the key.</span></span>

<span data-ttu-id="8d1ea-120">Si ce paramètre a la valeur NULL, la taille réelle de la clé ne sera pas retournée.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-120">If this parameter is NULL then the actual size of the key will not be returned.</span></span>

<span data-ttu-id="8d1ea-121">Si la mémoire tampon de sortie est trop petite, la taille réelle de la clé sera toujours retournée.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-121">If the output buffer is too small, then the actual size of the key will still be returned.</span></span> <span data-ttu-id="8d1ea-122">Cela signifie que ce nombre sera supérieur à la taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-122">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="8d1ea-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="8d1ea-123">*grbit*</span></span>

<span data-ttu-id="8d1ea-124">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-124">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d1ea-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d1ea-125">Value</span></span></p></th>
<th><p><span data-ttu-id="8d1ea-126">Signification</span><span class="sxs-lookup"><span data-stu-id="8d1ea-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d1ea-127">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="8d1ea-127">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-128">Lorsqu’il est spécifié, le moteur retourne la clé de recherche pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-128">When specified, the engine will return the search key for the cursor.</span></span> <span data-ttu-id="8d1ea-129">La clé de recherche est créée à l’aide d’un ou de plusieurs appels antérieurs à <a href="gg269329(v=exchg.10).md">JetMakeKey</a> dans le cadre de la recherche de cette clé à l’aide de <a href="gg294103(v=exchg.10).md">JetSeek</a> ou de la définition d’une plage d’index à l’aide de <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-129">The search key is built up using one or more prior calls to <a href="gg269329(v=exchg.10).md">JetMakeKey</a> for the purposes of seeking to that key using <a href="gg294103(v=exchg.10).md">JetSeek</a> or setting an index range using <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8d1ea-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8d1ea-130">Return Value</span></span>

<span data-ttu-id="8d1ea-131">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8d1ea-132">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8d1ea-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d1ea-133">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8d1ea-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="8d1ea-134">Description</span><span class="sxs-lookup"><span data-stu-id="8d1ea-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d1ea-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8d1ea-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-136">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d1ea-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8d1ea-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-138">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d1ea-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8d1ea-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-140">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="8d1ea-141">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d1ea-142">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="8d1ea-142">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-143">Il n’existe pas de clé de recherche pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-143">There is no current search key for the cursor.</span></span> <span data-ttu-id="8d1ea-144">Cela se produit pour <strong>JetRetrieveKey</strong> si JET_bitRetrieveCopy est spécifié et qu’une clé de recherche n’a pas été construite pour ce curseur à l’aide d’un appel antérieur à <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-144">This will happen for <strong>JetRetrieveKey</strong> if JET_bitRetrieveCopy is specified and a search key has not been constructed for this cursor using a prior call to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span> <span data-ttu-id="8d1ea-145">La clé de recherche sera supprimée par un appel précédent à n’importe quelle API de navigation sur le curseur autre que <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-145">The search key will be deleted by a prior call to any navigational API on the cursor other than <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d1ea-146">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="8d1ea-146">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-147">Le curseur n’est pas positionné sur un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-147">The cursor is not positioned on a record.</span></span> <span data-ttu-id="8d1ea-148">Cela peut se produire pour de nombreuses raisons différentes.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-148">This can happen for many different reasons.</span></span> <span data-ttu-id="8d1ea-149">Par exemple, cela se produit si le curseur est actuellement positionné après le dernier enregistrement de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-149">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d1ea-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8d1ea-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-151">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d1ea-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8d1ea-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-153">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d1ea-154">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8d1ea-154">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-155">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-155">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="8d1ea-156">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d1ea-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8d1ea-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-158">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d1ea-159">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="8d1ea-159">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="8d1ea-160">L’opération s’est terminée correctement, mais la mémoire tampon de sortie était trop petite pour recevoir la clé entière.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-160">The operation completed successfully, but the output buffer was too small to receive the entire key.</span></span> <span data-ttu-id="8d1ea-161">Le tampon de sortie a été rempli avec autant de clé que possible.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-161">The output buffer has been filled with as much of the key as would fit.</span></span> <span data-ttu-id="8d1ea-162">La taille réelle de la clé a également été retournée, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-162">The actual size of the key has also been returned, if requested.</span></span></p>
<p><span data-ttu-id="8d1ea-163"><strong>Remarque</strong>   Cette erreur ne sera pas retournée si JET_bitRetrieveCopy est spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-163"><strong>Note</strong>   This error will not be returned if JET_bitRetrieveCopy is specified.</span></span> <span data-ttu-id="8d1ea-164">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-164">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d1ea-165">En cas de réussite, la clé de l’entrée d’index à la position actuelle d’un curseur est retournée dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-165">On success, the key for the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="8d1ea-166">Si JET_wrnBufferTruncated est retourné, la mémoire tampon de sortie contiendra la plus grande partie de la clé telle qu’elle sera contenue dans l’espace fourni et la taille réelle de la clé sera exacte.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-166">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the key as will fit in the space provided and the actual size of the key will be accurate.</span></span> <span data-ttu-id="8d1ea-167">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-167">No change to the database state will occur.</span></span>

<span data-ttu-id="8d1ea-168">En cas d’échec, l’état de la mémoire tampon de sortie et la taille réelle de la clé ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-168">On failure, the state of the output buffer and the actual size of the key will be undefined.</span></span> <span data-ttu-id="8d1ea-169">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-169">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8d1ea-170">Notes</span><span class="sxs-lookup"><span data-stu-id="8d1ea-170">Remarks</span></span>

<span data-ttu-id="8d1ea-171">Les clés doivent généralement être traitées comme des blocs de données opaques.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-171">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="8d1ea-172">Aucune tentative n’est faite pour exploiter la structure interne de ces données.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-172">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="8d1ea-173">Toutefois, les propriétés suivantes peuvent être connues en ce qui concerne toutes les clés ESENT :</span><span class="sxs-lookup"><span data-stu-id="8d1ea-173">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="8d1ea-174">Les clés peuvent être comparées les unes aux autres à l’aide de la fonction [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) pour établir leur ordre relatif dans l’index d’origine sur la table des entrées d’index source.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-174">Keys may be compared against each other using [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) function to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="8d1ea-175">Il est inutile de comparer les clés des entrées d’index de différents index.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-175">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="8d1ea-176">Une clé est toujours inférieure ou égale à JET_cbKeyMost (255) octets dans une longueur antérieure à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-176">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="8d1ea-177">Sur Windows Vista et les versions ultérieures, les clés peuvent être plus volumineuses.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-177">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="8d1ea-178">La taille maximale d’une clé est égale à la valeur actuelle de JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-178">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

<span data-ttu-id="8d1ea-179">En plus des propriétés ci-dessus des clés ESENT en général, il est important de noter qu’une clé de recherche est différente de la clé d’une entrée d’index.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-179">In addition to the above properties of ESENT keys in general, it is important to note that a search key is different from the key for an index entry.</span></span> <span data-ttu-id="8d1ea-180">Plus précisément, une clé de recherche peut être plus longue qu’une clé ordinaire.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-180">Specifically, a search key may be longer than an ordinary key.</span></span> <span data-ttu-id="8d1ea-181">Cette longueur supplémentaire se produit lorsqu’une option générique est utilisée lors de la construction de la clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-181">This extra length occurs when a wildcard option is used while constructing the search key.</span></span> <span data-ttu-id="8d1ea-182">Pour plus d’informations, consultez [JetMakeKey](./jetmakekey-function.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1ea-182">See [JetMakeKey](./jetmakekey-function.md) for more information.</span></span>

<span data-ttu-id="8d1ea-183">Il existe un bogue important dans cette API qui est présent dans toutes les versions.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-183">There is an important bug in this API that is present in all releases.</span></span> <span data-ttu-id="8d1ea-184">Si la clé de recherche est demandée à l’aide de JET_bitRetrieveCopy et que la mémoire tampon de sortie est trop petite pour recevoir la clé entière, JET_wrnBufferTruncated ne sera pas retourné.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-184">If the search key is requested using the use of JET_bitRetrieveCopy and the output buffer is too small to receive the entire key then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="8d1ea-185">JET_errSuccess est retourné à la place.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-185">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="8d1ea-186">Il est important de vérifier que la taille réelle de la clé telle qu’elle est retournée à l’aide de *pcbActual* est inférieure ou égale à la taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-186">It is important to verify that the actual size of the key as returned using *pcbActual* is less than or equal to the size of the output buffer.</span></span> <span data-ttu-id="8d1ea-187">Si la taille réelle est supérieure à la taille de la mémoire tampon de sortie, l’appelant de **JetRetrieveKey** doit réagir comme si JET_wrnBufferTruncated était retourné à la place.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-187">If the actual size is larger than the size of the output buffer, then the caller of **JetRetrieveKey** should react as if JET_wrnBufferTruncated were returned instead.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8d1ea-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d1ea-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d1ea-189"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8d1ea-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8d1ea-190">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d1ea-191"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="8d1ea-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8d1ea-192">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d1ea-193"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="8d1ea-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8d1ea-194">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d1ea-195"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="8d1ea-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8d1ea-196">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d1ea-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8d1ea-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8d1ea-198">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8d1ea-198">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8d1ea-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d1ea-199">See Also</span></span>

[<span data-ttu-id="8d1ea-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8d1ea-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8d1ea-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8d1ea-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8d1ea-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8d1ea-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8d1ea-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8d1ea-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8d1ea-204">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="8d1ea-204">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="8d1ea-205">JetSeek</span><span class="sxs-lookup"><span data-stu-id="8d1ea-205">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="8d1ea-206">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="8d1ea-206">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

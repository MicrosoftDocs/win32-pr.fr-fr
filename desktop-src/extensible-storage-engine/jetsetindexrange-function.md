---
description: 'En savoir plus sur : fonction JetSetIndexRange'
title: Fonction JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883085633bebf25180c82f0f8917f6fa31fe7304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201593"
---
# <a name="jetsetindexrange-function"></a><span data-ttu-id="1f74b-103">Fonction JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="1f74b-103">JetSetIndexRange Function</span></span>


<span data-ttu-id="1f74b-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="1f74b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetindexrange-function"></a><span data-ttu-id="1f74b-105">Fonction JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="1f74b-105">JetSetIndexRange Function</span></span>

<span data-ttu-id="1f74b-106">La fonction **JetSetIndexRange** limite temporairement l’ensemble des entrées d’index que le curseur peut parcourir à l’aide de [JetMove](./jetmove-function.md) à celles commençant à l’entrée d’index actuelle et se terminant à l’entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et les critères liés spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1f74b-106">The **JetSetIndexRange** function temporarily limits the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="1f74b-107">Une clé de recherche doit avoir été construite précédemment à l’aide de [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="1f74b-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="1f74b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f74b-108">Parameters</span></span>

<span data-ttu-id="1f74b-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1f74b-109">*sesid*</span></span>

<span data-ttu-id="1f74b-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="1f74b-110">The session to use for this call.</span></span>

<span data-ttu-id="1f74b-111">*tableidSrc*</span><span class="sxs-lookup"><span data-stu-id="1f74b-111">*tableidSrc*</span></span>

<span data-ttu-id="1f74b-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="1f74b-112">The cursor to use for this call.</span></span>

<span data-ttu-id="1f74b-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1f74b-113">*grbit*</span></span>

<span data-ttu-id="1f74b-114">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1f74b-114">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f74b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f74b-115">Value</span></span></p></th>
<th><p><span data-ttu-id="1f74b-116">Signification</span><span class="sxs-lookup"><span data-stu-id="1f74b-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-117">JET_bitRangeInclusive</span><span class="sxs-lookup"><span data-stu-id="1f74b-117">JET_bitRangeInclusive</span></span></p></td>
<td><p><span data-ttu-id="1f74b-118">Cette option indique les critères de limite de la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="1f74b-118">This presence or absence of this option indicates the boundary criteria of the index range.</span></span> <span data-ttu-id="1f74b-119">Lorsqu’elle est présente, cette option indique que la limite de la plage d’index est comprise.</span><span class="sxs-lookup"><span data-stu-id="1f74b-119">When present, this option indicates that the limit of the index range is inclusive.</span></span> <span data-ttu-id="1f74b-120">Lorsqu’elle est absente, cette option indique que la limite de la plage d’index est exclusive.</span><span class="sxs-lookup"><span data-stu-id="1f74b-120">When absent, this option indicates that the limit of the index range is exclusive.</span></span> <span data-ttu-id="1f74b-121">Lorsque la limite de la plage d’index est inclusive, toutes les entrées d’index correspondant exactement aux critères de recherche sont incluses dans la plage.</span><span class="sxs-lookup"><span data-stu-id="1f74b-121">When the limit of the index range is inclusive then any index entries exactly matching the search criteria are included in the range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f74b-122">JET_bitRangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="1f74b-122">JET_bitRangeInstantDuration</span></span></p></td>
<td><p><span data-ttu-id="1f74b-123">Cette option demande que la plage d’index soit supprimée dès qu’elle a été établie.</span><span class="sxs-lookup"><span data-stu-id="1f74b-123">This option requests that the index range be removed as soon as it has been established.</span></span> <span data-ttu-id="1f74b-124">Tous les autres aspects de l’opération restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="1f74b-124">All other aspects of the operation remain unchanged.</span></span> <span data-ttu-id="1f74b-125">Cela est utile pour tester l’existence d’entrées d’index qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="1f74b-125">This is useful for testing for the existence of index entries that match the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-126">JET_bitRangeRemove</span><span class="sxs-lookup"><span data-stu-id="1f74b-126">JET_bitRangeRemove</span></span></p></td>
<td><p><span data-ttu-id="1f74b-127">Cette option demande l’annulation d’une plage d’index existante sur le curseur.</span><span class="sxs-lookup"><span data-stu-id="1f74b-127">This option requests that an existing index range on the cursor be canceled.</span></span> <span data-ttu-id="1f74b-128">Une fois la plage d’index annulée, il est possible de se déplacer au-delà de la fin de la plage d’index à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="1f74b-128">Once the index range is canceled, it will be possible to move beyond the end of the index range using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span> <span data-ttu-id="1f74b-129">Si une plage d’index n’est pas déjà en vigueur, <strong>JetSetIndexRange</strong> échoue avec JET_errInvalidOperation.</span><span class="sxs-lookup"><span data-stu-id="1f74b-129">If an index range is not already in effect, then <strong>JetSetIndexRange</strong> will fail with JET_errInvalidOperation.</span></span></p>
<p><span data-ttu-id="1f74b-130">Quand cette option est spécifiée, toutes les autres options sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="1f74b-130">When this option is specified, all other options are ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f74b-131">JET_bitRangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="1f74b-131">JET_bitRangeUpperLimit</span></span></p></td>
<td><p><span data-ttu-id="1f74b-132">Si cette option est utilisée, la clé de recherche dans le curseur représente les critères de recherche de l’entrée d’index la plus proche de la fin de l’index qui correspond à la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="1f74b-132">If this option is used, then the search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span> <span data-ttu-id="1f74b-133">La plage d’index sera établie entre la position actuelle du curseur et cette entrée d’index afin que toutes les correspondances puissent être trouvées en progressant vers l’index à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a> avec JET_MoveNext ou un décalage positif.</span><span class="sxs-lookup"><span data-stu-id="1f74b-133">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking forward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MoveNext or a positive offset.</span></span></p>
<p><span data-ttu-id="1f74b-134">Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches du début de l’index.</span><span class="sxs-lookup"><span data-stu-id="1f74b-134">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p>
<p><span data-ttu-id="1f74b-135">Si cette option est omise, la clé de recherche dans le curseur représente les critères de recherche de l’entrée d’index la plus proche du début de l’index qui correspond à la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="1f74b-135">If this option is omitted, then the search key in the cursor represents the search criteria for the index entry closest to the start of the index that will match the index range.</span></span> <span data-ttu-id="1f74b-136">La plage d’index sera établie entre la position actuelle du curseur et cette entrée d’index afin que toutes les correspondances puissent être trouvées en parcourant l’index à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a> avec JET_MovePrevious ou un décalage négatif.</span><span class="sxs-lookup"><span data-stu-id="1f74b-136">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking backward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MovePrevious or a negative offset.</span></span></p>
<p><span data-ttu-id="1f74b-137">Il n’est pas judicieux d’omettre cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches de la fin de l’index.</span><span class="sxs-lookup"><span data-stu-id="1f74b-137">It is not meaningful to omit this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1f74b-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f74b-138">Return Value</span></span>

<span data-ttu-id="1f74b-139">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="1f74b-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1f74b-140">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1f74b-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f74b-141">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1f74b-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="1f74b-142">Description</span><span class="sxs-lookup"><span data-stu-id="1f74b-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1f74b-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1f74b-144">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="1f74b-144">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="1f74b-145">Pour <strong>JetSetIndexRange</strong>, cela signifie qu’une plage d’index existante a été annulée ou qu’il existe au moins une entrée d’index à l’intérieur de la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="1f74b-145">For <strong>JetSetIndexRange</strong>, this means that either an existing index range was canceled or that there is at least one index entry inside of the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f74b-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1f74b-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1f74b-147">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="1f74b-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1f74b-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1f74b-149">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="1f74b-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="1f74b-150">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1f74b-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f74b-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="1f74b-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="1f74b-152">Cette erreur est retournée par <strong>JetSetIndexRange</strong> lorsque JET_bitRangeRemove a été spécifié et qu’aucune plage d’index n’était en vigueur.</span><span class="sxs-lookup"><span data-stu-id="1f74b-152">This error will be returned by <strong>JetSetIndexRange</strong> when JET_bitRangeRemove was specified and no index range was in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-153">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="1f74b-153">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="1f74b-154">Il n’existe pas de clé de recherche pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="1f74b-154">There is no current search key for the cursor.</span></span> <span data-ttu-id="1f74b-155"><strong>JetSetIndexRange</strong> requiert que le curseur ait une clé de recherche valide, car il l’utilise pour les critères de recherche utilisés pour rechercher des entrées d’index.</span><span class="sxs-lookup"><span data-stu-id="1f74b-155"><strong>JetSetIndexRange</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f74b-156">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="1f74b-156">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="1f74b-157">Il n’y a pas d’index actuel pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="1f74b-157">There is no current index for the cursor.</span></span> <span data-ttu-id="1f74b-158">Cela se produit pour <strong>JetSetIndexRange</strong> si le curseur se trouve sur l’index cluster d’une table, un index primaire n’a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="1f74b-158">This will happen for <strong>JetSetIndexRange</strong> if the cursor is on the clustered index of a table, a primary index has not been defined.</span></span> <span data-ttu-id="1f74b-159">La définition d’une plage d’index sur un tel index n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1f74b-159">Setting an index range over such an index is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-160">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="1f74b-160">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="1f74b-161">Cette erreur est retournée par <strong>JetSetIndexRange</strong> pour indiquer qu’il n’y a pas d’entrées d’index à l’intérieur de la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="1f74b-161">This error will be returned by <strong>JetSetIndexRange</strong> to indicate that there are no index entries inside the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f74b-162">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1f74b-162">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1f74b-163">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="1f74b-163">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-164">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1f74b-164">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1f74b-165">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="1f74b-165">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f74b-166">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1f74b-166">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1f74b-167">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="1f74b-167">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="1f74b-168">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1f74b-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-169">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1f74b-169">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1f74b-170">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="1f74b-170">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f74b-171">En cas de réussite, si JET_bitRangeRemove est spécifié, la plage d’index actuellement en vigueur est annulée.</span><span class="sxs-lookup"><span data-stu-id="1f74b-171">On success, if JET_bitRangeRemove is specified, then the index range that is currently in effect is canceled.</span></span> <span data-ttu-id="1f74b-172">Si JET_bitRangeRemove n’est pas spécifié et que JET_bitRangeInstantDuration est spécifié, aucune plage d’index n’est en vigueur.</span><span class="sxs-lookup"><span data-stu-id="1f74b-172">If JET_bitRangeRemove is not specified and JET_bitRangeInstantDuration is specified, then no index range is in effect.</span></span> <span data-ttu-id="1f74b-173">Si ni JET_bitRangeRemove ni JET_bitRangeInstantDuration n’est spécifié, une nouvelle plage d’index est en vigueur.</span><span class="sxs-lookup"><span data-stu-id="1f74b-173">If neither JET_bitRangeRemove nor JET_bitRangeInstantDuration is specified, then a new index range is in effect.</span></span> <span data-ttu-id="1f74b-174">Cette plage d’index limite temporairement l’ensemble d’entrées d’index que le curseur peut parcourir à l’aide de [JetMove](./jetmove-function.md) à celles qui commencent à l’entrée d’index actuelle et se termine à l’entrée d’index correspondant aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="1f74b-174">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="1f74b-175">La position du curseur reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="1f74b-175">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="1f74b-176">Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="1f74b-176">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="1f74b-177">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="1f74b-177">No change to the database state will occur.</span></span>

<span data-ttu-id="1f74b-178">En cas d’échec, si JET_errNoCurrentRecord n’est pas retourné, aucune plage d’index n’est en vigueur.</span><span class="sxs-lookup"><span data-stu-id="1f74b-178">On failure, if JET_errNoCurrentRecord is not returned, then no index range is in effect.</span></span> <span data-ttu-id="1f74b-179">Si JET_errNoCurrentRecord est retourné, une nouvelle plage d’index est en vigueur.</span><span class="sxs-lookup"><span data-stu-id="1f74b-179">If JET_errNoCurrentRecord is returned, then a new index range is in effect.</span></span> <span data-ttu-id="1f74b-180">Cette plage d’index limite temporairement l’ensemble d’entrées d’index que le curseur peut parcourir à l’aide de [JetMove](./jetmove-function.md) à celles qui commencent à l’entrée d’index actuelle et se termine à l’entrée d’index correspondant aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="1f74b-180">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="1f74b-181">La position du curseur reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="1f74b-181">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="1f74b-182">Si JET_errNoCurrentRecord a été retourné et qu’une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="1f74b-182">If JET_errNoCurrentRecord was returned and a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="1f74b-183">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="1f74b-183">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1f74b-184">Notes</span><span class="sxs-lookup"><span data-stu-id="1f74b-184">Remarks</span></span>

<span data-ttu-id="1f74b-185">Une plage d’index est volatile et sera automatiquement annulée si une navigation autre que [JetMove](./jetmove-function.md) est effectuée sur le curseur.</span><span class="sxs-lookup"><span data-stu-id="1f74b-185">An index range is volatile and will automatically be canceled if any navigation other than [JetMove](./jetmove-function.md) is performed on the cursor.</span></span>

<span data-ttu-id="1f74b-186">Les plages d’index fonctionnent uniquement dans une seule direction.</span><span class="sxs-lookup"><span data-stu-id="1f74b-186">Index ranges only work in one direction.</span></span> <span data-ttu-id="1f74b-187">Si une limite supérieure est établie, seul le déplacement vers l’avant à l’aide de [JetMove](./jetmove-function.md) avec JET_MoveNext ou un décalage positif est évité une fois que la fin de la plage d’index a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="1f74b-187">If an upper limit is established then only forward motion using [JetMove](./jetmove-function.md) with JET_MoveNext or a positive offset will be prevented once the end of the index range has been reached.</span></span> <span data-ttu-id="1f74b-188">Dans ce cas, il est toujours possible de conserver la plage d’index à l’aide de [JetMove](./jetmove-function.md) avec JET_MovePrevious ou un décalage négatif.</span><span class="sxs-lookup"><span data-stu-id="1f74b-188">It is still possible to leave the index range in this case using [JetMove](./jetmove-function.md) with JET_MovePrevious or a negative offset.</span></span> <span data-ttu-id="1f74b-189">Une situation analogue se produit pour une limite inférieure.</span><span class="sxs-lookup"><span data-stu-id="1f74b-189">An analogous situation occurs for a lower limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1f74b-190">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f74b-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-191"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1f74b-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1f74b-192">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="1f74b-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f74b-193"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="1f74b-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1f74b-194">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1f74b-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-195"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="1f74b-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1f74b-196">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="1f74b-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f74b-197"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="1f74b-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1f74b-198">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1f74b-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f74b-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1f74b-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1f74b-200">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1f74b-200">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1f74b-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f74b-201">See Also</span></span>

[<span data-ttu-id="1f74b-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1f74b-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1f74b-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1f74b-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1f74b-204">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1f74b-204">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1f74b-205">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1f74b-205">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1f74b-206">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="1f74b-206">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="1f74b-207">JetMove</span><span class="sxs-lookup"><span data-stu-id="1f74b-207">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="1f74b-208">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="1f74b-208">JetSetIndexRange</span></span>]()  
[<span data-ttu-id="1f74b-209">JetStopService</span><span class="sxs-lookup"><span data-stu-id="1f74b-209">JetStopService</span></span>](./jetstopservice-function.md)

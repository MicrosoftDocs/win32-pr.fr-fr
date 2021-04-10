---
description: 'En savoir plus sur : fonction JetMove'
title: Fonction JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201221"
---
# <a name="jetmove-function"></a><span data-ttu-id="e1218-103">Fonction JetMove</span><span class="sxs-lookup"><span data-stu-id="e1218-103">JetMove Function</span></span>


<span data-ttu-id="e1218-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="e1218-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetmove-function"></a><span data-ttu-id="e1218-105">Fonction JetMove</span><span class="sxs-lookup"><span data-stu-id="e1218-105">JetMove Function</span></span>

<span data-ttu-id="e1218-106">La fonction **JetMove** positionne un curseur au début ou à la fin d’un index et parcourt les entrées de cet index vers l’avant ou vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="e1218-106">The **JetMove** function positions a cursor at the start or end of an index and traverses the entries in that index either forward or backward.</span></span> <span data-ttu-id="e1218-107">Il est également possible de déplacer le curseur vers l’avant ou vers l’arrière sur l’index actuel en fonction d’un nombre spécifié d’entrées d’index.</span><span class="sxs-lookup"><span data-stu-id="e1218-107">It is also possible to move the cursor forward or backward on the current index by a specified number of index entries.</span></span> <span data-ttu-id="e1218-108">Une autre approche consiste à limiter artificiellement les entrées d’index qui peuvent être énumérées à l’aide de **JetMove** en définissant une plage d’index sur le curseur à l’aide de [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="e1218-108">Another approach is to artificially limit the index entries that can be enumerated using **JetMove** by setting up an index range on the cursor using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e1218-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1218-109">Parameters</span></span>

<span data-ttu-id="e1218-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e1218-110">*sesid*</span></span>

<span data-ttu-id="e1218-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="e1218-111">The session to use for this call.</span></span>

<span data-ttu-id="e1218-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="e1218-112">*tableid*</span></span>

<span data-ttu-id="e1218-113">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="e1218-113">The cursor to use for this call.</span></span>

<span data-ttu-id="e1218-114">*Vol*</span><span class="sxs-lookup"><span data-stu-id="e1218-114">*cRow*</span></span>

<span data-ttu-id="e1218-115">Décalage arbitraire qui indique le déplacement souhaité du curseur sur l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="e1218-115">An arbitrary offset that indicates the desired movement of the cursor on the current index.</span></span>

<span data-ttu-id="e1218-116">En plus des décalages standard, ce paramètre peut également être défini avec l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1218-116">In addition to standard offsets, this parameter can also be set with one of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1218-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1218-117">Value</span></span></p></th>
<th><p><span data-ttu-id="e1218-118">Signification</span><span class="sxs-lookup"><span data-stu-id="e1218-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1218-119">JET_MoveFirst</span><span class="sxs-lookup"><span data-stu-id="e1218-119">JET_MoveFirst</span></span></p></td>
<td><p><span data-ttu-id="e1218-120">Déplace le curseur vers la première entrée d’index dans l’index (s’il en existe un).</span><span class="sxs-lookup"><span data-stu-id="e1218-120">Moves the cursor to the first index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="e1218-121"><strong>Remarque</strong>   La valeur littérale de-2147483648 est utilisée pour désigner cette option.</span><span class="sxs-lookup"><span data-stu-id="e1218-121"><strong>Note</strong>   The literal value of -2147483648 is used to denote this option.</span></span> <span data-ttu-id="e1218-122">N’utilisez pas cette valeur comme un décalage ordinaire ou un comportement inattendu peut se produire.</span><span class="sxs-lookup"><span data-stu-id="e1218-122">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1218-123">JET_MoveLast</span><span class="sxs-lookup"><span data-stu-id="e1218-123">JET_MoveLast</span></span></p></td>
<td><p><span data-ttu-id="e1218-124">Déplace le curseur vers la dernière entrée d’index de l’index (s’il en existe un).</span><span class="sxs-lookup"><span data-stu-id="e1218-124">Moves the cursor to the last index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="e1218-125"><strong>Remarque</strong>   La valeur littérale de 2147483647 est utilisée pour désigner cette option.</span><span class="sxs-lookup"><span data-stu-id="e1218-125"><strong>Note</strong>   The literal value of 2147483647 is used to denote this option.</span></span> <span data-ttu-id="e1218-126">N’utilisez pas cette valeur comme un décalage ordinaire ou un comportement inattendu peut se produire.</span><span class="sxs-lookup"><span data-stu-id="e1218-126">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1218-127">JET_MoveNext</span><span class="sxs-lookup"><span data-stu-id="e1218-127">JET_MoveNext</span></span></p></td>
<td><p><span data-ttu-id="e1218-128">Déplace le curseur à l’entrée d’index suivante dans l’index (s’il en existe un).</span><span class="sxs-lookup"><span data-stu-id="e1218-128">Moves the cursor to the next index entry in the index (if one exists).</span></span> <span data-ttu-id="e1218-129">Cette valeur est exactement égale à un décalage ordinaire de + 1.</span><span class="sxs-lookup"><span data-stu-id="e1218-129">This value is exactly equal to an ordinary offset of +1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1218-130">JET_MovePrevious</span><span class="sxs-lookup"><span data-stu-id="e1218-130">JET_MovePrevious</span></span></p></td>
<td><p><span data-ttu-id="e1218-131">Déplace le curseur à l’entrée d’index précédente dans l’index (s’il en existe un).</span><span class="sxs-lookup"><span data-stu-id="e1218-131">Moves the cursor to the previous index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="e1218-132">Cette valeur est exactement égale à un décalage ordinaire de-1, ou 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="e1218-132">This value is exactly equal to an ordinary offset of -1, or 0 (Zero).</span></span></p>
<p><span data-ttu-id="e1218-133">Le curseur reste à la position logique actuelle et l’existence de l’entrée d’index correspondant à cette position logique sera testée.</span><span class="sxs-lookup"><span data-stu-id="e1218-133">The cursor remains at the current logical position and the existence of the index entry that corresponds to that logical position will be tested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e1218-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e1218-134">*grbit*</span></span>

<span data-ttu-id="e1218-135">Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1218-135">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1218-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1218-136">Value</span></span></p></th>
<th><p><span data-ttu-id="e1218-137">Signification</span><span class="sxs-lookup"><span data-stu-id="e1218-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1218-138">JET_bitMoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="e1218-138">JET_bitMoveKeyNE</span></span></p></td>
<td><p><span data-ttu-id="e1218-139">Déplace le curseur vers l’avant ou vers l’arrière selon le nombre d’entrées d’index requises pour ignorer le nombre demandé de valeurs de clé d’index rencontrées dans l’index.</span><span class="sxs-lookup"><span data-stu-id="e1218-139">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="e1218-140">Cela a pour effet de réduire les entrées d’index avec des valeurs de clé en double dans une entrée d’index unique.</span><span class="sxs-lookup"><span data-stu-id="e1218-140">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span> <span data-ttu-id="e1218-141">En règle générale, un décalage déplace le curseur en fonction du nombre d’entrées d’index spécifié, indépendamment de leurs valeurs de clés.</span><span class="sxs-lookup"><span data-stu-id="e1218-141">Ordinarily, an offset will move the cursor by the specified number of index entries regardless of their key values.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e1218-142">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e1218-142">Return Value</span></span>

<span data-ttu-id="e1218-143">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="e1218-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e1218-144">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e1218-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1218-145">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e1218-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="e1218-146">Description</span><span class="sxs-lookup"><span data-stu-id="e1218-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1218-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e1218-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e1218-148">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e1218-148">The operation completed successfully.</span></span> <span data-ttu-id="e1218-149">Pour <strong>JetMove</strong>, cela signifie qu’une entrée d’index a été trouvée à l’emplacement ou au décalage demandé sur l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="e1218-149">For <strong>JetMove</strong>, this means that an index entry was found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1218-150">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e1218-150">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e1218-151">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e1218-151">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1218-152">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e1218-152">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e1218-153">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="e1218-153">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="e1218-154"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e1218-154"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1218-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="e1218-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="e1218-156">Le curseur n’est pas positionné sur une entrée d’index.</span><span class="sxs-lookup"><span data-stu-id="e1218-156">The cursor is not currently positioned on an index entry.</span></span> <span data-ttu-id="e1218-157">Pour <strong>JetMove</strong>, cela signifie qu’une entrée d’index est introuvable à l’emplacement ou au décalage demandé sur l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="e1218-157">For <strong>JetMove</strong>, this means that an index entry was not found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1218-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e1218-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e1218-159">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="e1218-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1218-160">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="e1218-160">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="e1218-161">Le curseur est actuellement positionné logiquement sur une entrée d’index qui correspond à un enregistrement qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="e1218-161">The cursor is currently logically positioned on an index entry that corresponds to a record that has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1218-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e1218-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e1218-163">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="e1218-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1218-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e1218-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e1218-165">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="e1218-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="e1218-166"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e1218-166"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1218-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e1218-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e1218-168">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e1218-168">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e1218-169">Si cette fonction est réussie, le curseur est positionné sur une entrée d’index qui correspond à l’emplacement ou au décalage demandé.</span><span class="sxs-lookup"><span data-stu-id="e1218-169">If this function succeeds, the cursor will be positioned at an index entry that matches the requested location or offset.</span></span> <span data-ttu-id="e1218-170">Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée.</span><span class="sxs-lookup"><span data-stu-id="e1218-170">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="e1218-171">Si une plage d’index est en vigueur et JET_MoveFirst ou JET_MoveLast a été spécifié, cette plage d’index sera annulée.</span><span class="sxs-lookup"><span data-stu-id="e1218-171">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="e1218-172">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="e1218-172">No change to the database state will occur.</span></span>

<span data-ttu-id="e1218-173">Si cette fonction échoue, la position du curseur reste inchangée, à moins que JET_errNoCurrentRecord ne soit retourné.</span><span class="sxs-lookup"><span data-stu-id="e1218-173">If this function fails, the position of the cursor will remain unchanged unless JET_errNoCurrentRecord was returned.</span></span> <span data-ttu-id="e1218-174">Dans ce cas, le curseur est positionné à l’emplacement où l’entrée d’index qui correspond à l’emplacement ou au décalage demandé aurait été.</span><span class="sxs-lookup"><span data-stu-id="e1218-174">In that case, the cursor will be positioned where the index entry that matches the requested location or offset would have been.</span></span> <span data-ttu-id="e1218-175">Le curseur peut être déplacé par rapport à cette position, mais il n’est pas toujours sur une entrée d’index valide.</span><span class="sxs-lookup"><span data-stu-id="e1218-175">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="e1218-176">Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée.</span><span class="sxs-lookup"><span data-stu-id="e1218-176">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="e1218-177">Si une plage d’index est en vigueur et JET_MoveFirst ou JET_MoveLast a été spécifié, cette plage d’index sera annulée.</span><span class="sxs-lookup"><span data-stu-id="e1218-177">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="e1218-178">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="e1218-178">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e1218-179">Notes</span><span class="sxs-lookup"><span data-stu-id="e1218-179">Remarks</span></span>

<span data-ttu-id="e1218-180">Un curseur peut être déplacé vers deux positions spéciales à l’aide de **JetMove**, avant le premier et après le dernier.</span><span class="sxs-lookup"><span data-stu-id="e1218-180">A cursor can be moved to two special positions using **JetMove**, Before First and After Last.</span></span> <span data-ttu-id="e1218-181">Si le curseur se trouve sur la première entrée d’index de la table et que **JetMove** est appelé avec JET_MovePrevious, l’appel échoue avec JET_errNoCurrentRecord et le curseur est positionné logiquement avant la première entrée de l’index.</span><span class="sxs-lookup"><span data-stu-id="e1218-181">If the cursor is on the first index entry in the table and **JetMove** is called with JET_MovePrevious, the call will fail with JET_errNoCurrentRecord and the cursor will be logically positioned before the first entry in the index.</span></span> <span data-ttu-id="e1218-182">Cette position logique est conservée même si une autre entrée d’index est insérée avant la première entrée de l’index.</span><span class="sxs-lookup"><span data-stu-id="e1218-182">This logical position is maintained even if another index entry is inserted prior to the first entry in the index.</span></span> <span data-ttu-id="e1218-183">Une situation analogue se produit pour la dernière fois par rapport à la fin de l’index.</span><span class="sxs-lookup"><span data-stu-id="e1218-183">An analogous situation occurs for After Last relative to the end of the index.</span></span> <span data-ttu-id="e1218-184">Avant le premier et après dernier sont particulièrement utiles lors de la configuration d’une plage d’entrées d’index à itérer à l’aide de **JetMove**, à l’aide d’un modèle d’itérateur qui s’attend à toujours passer à l’élément suivant (ou précédent) avant d’utiliser cet élément.</span><span class="sxs-lookup"><span data-stu-id="e1218-184">Before First and After Last are most useful when setting up a range of index entries to be iterated using **JetMove**, using an iterator model that expects to always move to the next (or previous) element prior to using that element.</span></span>

<span data-ttu-id="e1218-185">L’ensemble d’entrées d’index qui peut être visité par **JetMove** peut être limité en définissant une plage d’index sur le curseur.</span><span class="sxs-lookup"><span data-stu-id="e1218-185">The set of index entries that can be visited by **JetMove** can be limited by setting up an index range on the cursor.</span></span> <span data-ttu-id="e1218-186">Cela est utile pour les applications qui énumèrent un ensemble d’entrées d’index qui correspondent à des critères simples qui peuvent être exprimés à l’aide d’une paire de clés de recherche générées pour cet index.</span><span class="sxs-lookup"><span data-stu-id="e1218-186">This is useful for applications that enumerate a set of index entries that match simple criteria that can be expressed through a pair of search keys built for that index.</span></span> <span data-ttu-id="e1218-187">Pour plus d’informations, consultez [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="e1218-187">For more information, see [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="e1218-188">Dans les versions antérieures à Windows Server 2003 SP1, un problème survient dans **JetMove** dans certains cas spécifiques, ce qui affecte la mise en œuvre correcte d’une plage d’index telle qu’elle est définie par la fonction [JetSetIndexRange](./jetsetindexrange-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e1218-188">On releases prior to Windows Server 2003 SP1, there is a problem in **JetMove** that occurs in some specific cases, that affects the correct enforcement of an index range as set up by the [JetSetIndexRange](./jetsetindexrange-function.md) function.</span></span> <span data-ttu-id="e1218-189">Si le curseur se trouve actuellement avant la première entrée d’index et qu’une plage d’index est définie avec une limite supérieure inférieure à la première entrée d’index, l’appel suivant à **JetMove** passera par erreur à cette entrée d’index au lieu d’échouer avec JET_errNoCurrentRecord, comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e1218-189">If the cursor is currently before the first index entry and an index range is set with an upper limit that is less than the first index entry, the next call to **JetMove** will erroneously go to that index entry instead of failing with JET_errNoCurrentRecord, as expected.</span></span> <span data-ttu-id="e1218-190">La même erreur se produit pour la situation analogue à partir de la fin de l’index.</span><span class="sxs-lookup"><span data-stu-id="e1218-190">The same error will happen for the analogous situation starting from the end of the index.</span></span> <span data-ttu-id="e1218-191">Cette situation peut se produire dans une application qui configure une plage d’index et la parcourt à l’aide d’un itérateur qui s’attend à démarrer avant la première entrée d’index qui est membre du jeu d’entrées à énumérer, au lieu de démarrer sur la première entrée d’index de ce jeu.</span><span class="sxs-lookup"><span data-stu-id="e1218-191">This situation can occur in an application that sets up an index range and navigates it using an iterator that expects to start before the first index entry that is a member of the set of entries to enumerate, rather than starting on the first index entry of that set.</span></span> <span data-ttu-id="e1218-192">Cette situation se produit également dans le cas analogue à partir de la fin de l’index.</span><span class="sxs-lookup"><span data-stu-id="e1218-192">This situation also occurs on the analogous case starting from the end of the index.</span></span> <span data-ttu-id="e1218-193">La solution de contournement consiste à ce que l’application vérifie manuellement que l’entrée d’index acquise se trouve à l’intérieur de la plage d’index en comparant la clé de l’entrée d’index actuelle (Récupérée à l’aide de [JetRetrieveKey](./jetretrievekey-function.md)) avec la clé représentant la fin de la plage d’index actuelle (Récupérée à l’aide de [JetRetrieveKey](./jetretrievekey-function.md) à l’aide de JET_bitRetrieveCopy).</span><span class="sxs-lookup"><span data-stu-id="e1218-193">The workaround is for the application to manually verify that the index entry acquired is inside the index range by comparing the key for the current index entry (retrieved using [JetRetrieveKey](./jetretrievekey-function.md)) with the key representing the end of the current index range (retrieved using [JetRetrieveKey](./jetretrievekey-function.md) using JET_bitRetrieveCopy).</span></span>

<span data-ttu-id="e1218-194">Il est important d’être prudent lors du passage de décalages calculés à **JetMove**.</span><span class="sxs-lookup"><span data-stu-id="e1218-194">It is important to be careful when passing computed offsets to **JetMove**.</span></span> <span data-ttu-id="e1218-195">Si le décalage calculé est inférieur ou égal à JET_MoveFirst, cet offset doit être divisé en plusieurs parties, chacune d’elles étant passée à **JetMove** séparément, mais dans une transaction unique pour obtenir l’effet souhaité.</span><span class="sxs-lookup"><span data-stu-id="e1218-195">If the computed offset is less than or equal to JET_MoveFirst, that offset must be broken up into multiple pieces, each of which is passed to **JetMove** separately but within a single transaction to get the desired effect.</span></span> <span data-ttu-id="e1218-196">Il en va de même pour les décalages supérieurs ou égaux à JET_MoveNext.</span><span class="sxs-lookup"><span data-stu-id="e1218-196">The same is true for offsets greater than or equal to JET_MoveNext.</span></span> <span data-ttu-id="e1218-197">Il est peu probable qu’une application subisse cette situation dans le monde réel, mais il est judicieux d’avoir une protection contre ce cas en raison de la sémantique très différente de JET_MoveFirst et de JET_MoveLast à partir d’un décalage ordinaire.</span><span class="sxs-lookup"><span data-stu-id="e1218-197">It is unlikely that an application would undergo this in the real world, but it is good to have a defense against this case given the very different semantics of JET_MoveFirst and JET_MoveLast from an ordinary offset.</span></span>

<span data-ttu-id="e1218-198">Quand **JetMove** est appelé avec un décalage très important, par exemple lorsque le paramètre cRow a la valeur 1000, **JetMove** parcourt toutes les entrées d’index de 1000 pour atteindre la position finale.</span><span class="sxs-lookup"><span data-stu-id="e1218-198">When **JetMove** is called with a very large offset, such as when the cRow parameter is set to 1000, **JetMove** traverses all 1000 index entries to reach the final position.</span></span> <span data-ttu-id="e1218-199">Actuellement, l’API ESE ne fournit pas de méthode efficace pour passer directement à une entrée d’index donnée par décalage sans traverser chaque entrée d’index.</span><span class="sxs-lookup"><span data-stu-id="e1218-199">Currently, the ESE API does not provide an efficient way to move directly to a given index entry by offset without traversing each index entry.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e1218-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1218-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1218-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e1218-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e1218-202">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="e1218-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1218-203"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="e1218-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e1218-204">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e1218-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1218-205"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="e1218-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e1218-206">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="e1218-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1218-207"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="e1218-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e1218-208">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e1218-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1218-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e1218-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e1218-210">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e1218-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e1218-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1218-211">See Also</span></span>

[<span data-ttu-id="e1218-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e1218-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e1218-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e1218-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e1218-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e1218-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e1218-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e1218-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e1218-216">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="e1218-216">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="e1218-217">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="e1218-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

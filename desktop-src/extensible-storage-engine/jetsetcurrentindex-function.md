---
description: 'En savoir plus sur : fonction JetSetCurrentIndex'
title: Fonction JetSetCurrentIndex
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7698a12f470fadd5c43dc2afe23f95f8e51bdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514401"
---
# <a name="jetsetcurrentindex-function"></a><span data-ttu-id="620b4-103">Fonction JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="620b4-103">JetSetCurrentIndex Function</span></span>


<span data-ttu-id="620b4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="620b4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex-function"></a><span data-ttu-id="620b4-105">Fonction JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="620b4-105">JetSetCurrentIndex Function</span></span>

<span data-ttu-id="620b4-106">La fonction **JetSetCurrentIndex** peut être utilisée pour définir l’index actuel d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="620b4-106">The **JetSetCurrentIndex** function can be used to set the current index of a cursor.</span></span> <span data-ttu-id="620b4-107">L’index actuel d’un curseur définit les enregistrements d’une table qui sont visibles pour ce curseur et l’ordre dans lequel ils apparaissent en sélectionnant l’ensemble d’entrées d’index à utiliser pour exposer ces enregistrements.</span><span class="sxs-lookup"><span data-stu-id="620b4-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="620b4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="620b4-108">Parameters</span></span>

<span data-ttu-id="620b4-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="620b4-109">*sesid*</span></span>

<span data-ttu-id="620b4-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="620b4-110">The session to use for this call.</span></span>

<span data-ttu-id="620b4-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="620b4-111">*tableid*</span></span>

<span data-ttu-id="620b4-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="620b4-112">The cursor to use for this call.</span></span>

<span data-ttu-id="620b4-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="620b4-113">*szIndexName*</span></span>

<span data-ttu-id="620b4-114">Nom de l’index à sélectionner pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="620b4-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="620b4-115">Si ce paramètre a la valeur NULL ou est une chaîne vide, l’index cluster est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="620b4-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="620b4-116">Si un index primaire est défini pour la table, cet index est sélectionné, car il est identique à l’index cluster.</span><span class="sxs-lookup"><span data-stu-id="620b4-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="620b4-117">Si aucun index primaire n’est défini pour la table, l’index séquentiel est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="620b4-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="620b4-118">L’index séquentiel n’a pas de définition d’index.</span><span class="sxs-lookup"><span data-stu-id="620b4-118">The sequential index has no index definition.</span></span> <span data-ttu-id="620b4-119">Pour plus d’informations, consultez [JetCreateIndex](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="620b4-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="620b4-120">Si *pIndexID* n’a pas la valeur null, le nom de l’index sera ignoré et l’index sera sélectionné par son ID d’index.</span><span class="sxs-lookup"><span data-stu-id="620b4-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

### <a name="return-value"></a><span data-ttu-id="620b4-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="620b4-121">Return Value</span></span>

<span data-ttu-id="620b4-122">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="620b4-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="620b4-123">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="620b4-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="620b4-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="620b4-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="620b4-125">Description</span><span class="sxs-lookup"><span data-stu-id="620b4-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="620b4-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="620b4-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="620b4-127">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="620b4-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="620b4-128">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="620b4-128">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="620b4-129">Un index secondaire est sélectionné avec l’option JET_bitNoMove et il n’y a aucune valeur pour la première colonne clé à valeurs multiples dans la définition de la nouvelle index qui correspond au numéro de séquence spécifié.</span><span class="sxs-lookup"><span data-stu-id="620b4-129">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="620b4-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="620b4-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="620b4-131">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="620b4-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="620b4-132">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="620b4-132">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="620b4-133">Le contenu de l’ID d’index n’était pas valide ou a expiré et doit être actualisé.</span><span class="sxs-lookup"><span data-stu-id="620b4-133">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="620b4-134">Cela peut se produire pour <strong>JetSetCurrentIndex</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="620b4-134">This can happen for <strong>JetSetCurrentIndex</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="620b4-135">pIndexID- &gt; cbStruct n’est pas de la taille attendue (Windows Server 2003 et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="620b4-135">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="620b4-136">Le moteur a été arrêté depuis que l’ID d’index a été extrait.</span><span class="sxs-lookup"><span data-stu-id="620b4-136">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="620b4-137">Tous les curseurs faisant référence à la table contenant l’index correspondant à l’ID d’index ont été fermés et le moteur a supprimé la définition de cet index du cache de schéma.</span><span class="sxs-lookup"><span data-stu-id="620b4-137">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted that index's definition from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="620b4-138">L’ID d’index est utilisé avec un curseur ouvert sur une table incorrecte.</span><span class="sxs-lookup"><span data-stu-id="620b4-138">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="620b4-139">L’index a été supprimé ou n’est pas encore visible dans la session.</span><span class="sxs-lookup"><span data-stu-id="620b4-139">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="620b4-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="620b4-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="620b4-141">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="620b4-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="620b4-142">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="620b4-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="620b4-143">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="620b4-143">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="620b4-144">L’un des noms d’objets spécifiés n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="620b4-144">One of the specified object names was invalid.</span></span> <span data-ttu-id="620b4-145">Tous les noms d’objets doivent être conformes au même ensemble de règles.</span><span class="sxs-lookup"><span data-stu-id="620b4-145">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="620b4-146">Ces règles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="620b4-146">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="620b4-147">Les noms d’objets doivent être composés de caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="620b4-147">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="620b4-148">Les noms d’objets doivent comporter au moins un caractère.</span><span class="sxs-lookup"><span data-stu-id="620b4-148">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="620b4-149">Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</span><span class="sxs-lookup"><span data-stu-id="620b4-149">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="620b4-150">Les noms d’objets ne peuvent pas commencer par un espace.</span><span class="sxs-lookup"><span data-stu-id="620b4-150">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="620b4-151">Les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</span><span class="sxs-lookup"><span data-stu-id="620b4-151">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="620b4-152">Les noms d’objets ne peuvent pas contenir de point d’exclamation ( !), de point (.), de crochet gauche ([) ou de crochet droit (]).</span><span class="sxs-lookup"><span data-stu-id="620b4-152">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="620b4-153">Une fois validée, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="620b4-153">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="620b4-154">Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</span><span class="sxs-lookup"><span data-stu-id="620b4-154">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="620b4-155">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="620b4-155">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="620b4-156">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="620b4-156">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="620b4-157">Cela peut se produire pour <strong>JetSetCurrentIndex</strong> lorsque <em>pIndexID</em> n’a pas la valeur null et que pIndexID- &gt; cbStruct n’est pas de la taille attendue (Windows XP et versions antérieures).</span><span class="sxs-lookup"><span data-stu-id="620b4-157">This can happen for <strong>JetSetCurrentIndex</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="620b4-158">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="620b4-158">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="620b4-159">Un index secondaire est sélectionné avec l’option JET_bitNoMove et il n’existe aucune entrée d’index dans le nouvel index qui correspond à l’enregistrement associé à l’entrée d’index à la position actuelle du curseur sur l’ancien index.</span><span class="sxs-lookup"><span data-stu-id="620b4-159">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="620b4-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="620b4-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="620b4-161">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="620b4-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="620b4-162">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="620b4-162">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="620b4-163">Le moteur a épuisé son pool de ressources utilisé pour ouvrir les curseurs.</span><span class="sxs-lookup"><span data-stu-id="620b4-163">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="620b4-164">Le nombre maximal de curseurs pouvant être ouverts à un moment donné est contrôlé à l’aide de <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="620b4-164">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="620b4-165">Pour plus d’informations, consultez <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> .</span><span class="sxs-lookup"><span data-stu-id="620b4-165">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="620b4-166">Cela peut se produire pour <strong>JetSetCurrentIndex</strong> lorsqu’un index secondaire a été sélectionné et que le moteur ne peut pas ouvrir un curseur interne pour utiliser cet index.</span><span class="sxs-lookup"><span data-stu-id="620b4-166">This can happen for <strong>JetSetCurrentIndex</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="620b4-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="620b4-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="620b4-168">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="620b4-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="620b4-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="620b4-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="620b4-170">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="620b4-170">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="620b4-171">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="620b4-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="620b4-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="620b4-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="620b4-173">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="620b4-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="620b4-174">En cas de réussite, l’index actuel du curseur est défini sur l’index demandé.</span><span class="sxs-lookup"><span data-stu-id="620b4-174">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="620b4-175">Les entrées d’index peuvent désormais être recherchées à l’aide de [JetSeek](./jetseek-function.md) en fonction de la définition d’index de l’index demandé.</span><span class="sxs-lookup"><span data-stu-id="620b4-175">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="620b4-176">Les entrées d’index peuvent également être énumérées à l’aide de [JetMove](./jetmove-function.md) dans l’ordre spécifié par cette définition d’index.</span><span class="sxs-lookup"><span data-stu-id="620b4-176">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="620b4-177">La position actuelle du curseur est définie sur la première entrée d’index de l’index (JET_bitMoveFirst) ou sur une entrée d’index spécifique qui est associée à la position actuelle du curseur sur l’ancien index (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="620b4-177">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="620b4-178">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="620b4-178">No change to the database state will occur.</span></span>

<span data-ttu-id="620b4-179">En cas d’échec, l’index actuel et la position actuelle du curseur sont dans un État indéfini.</span><span class="sxs-lookup"><span data-stu-id="620b4-179">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="620b4-180">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="620b4-180">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="620b4-181">Notes</span><span class="sxs-lookup"><span data-stu-id="620b4-181">Remarks</span></span>

<span data-ttu-id="620b4-182">Si l’indicateur d’ID d’index est obsolète, l’API échoue simplement.</span><span class="sxs-lookup"><span data-stu-id="620b4-182">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="620b4-183">Il n’existe pas de secours pour le nom de texte de l’index dans ce cas, car il peut s’agir d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="620b4-183">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="620b4-184">Ce secours doit être effectué manuellement par l’appelant de l’API.</span><span class="sxs-lookup"><span data-stu-id="620b4-184">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="620b4-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="620b4-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="620b4-186"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="620b4-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="620b4-187">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="620b4-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="620b4-188"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="620b4-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="620b4-189">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="620b4-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="620b4-190"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="620b4-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="620b4-191">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="620b4-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="620b4-192"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="620b4-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="620b4-193">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="620b4-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="620b4-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="620b4-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="620b4-195">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="620b4-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="620b4-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="620b4-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="620b4-197">Implémenté en tant que <strong>JetSetCurrentIndexW</strong> (Unicode) et <strong>JetSetCurrentIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="620b4-197">Implemented as <strong>JetSetCurrentIndexW</strong> (Unicode) and <strong>JetSetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="620b4-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="620b4-198">See Also</span></span>

[<span data-ttu-id="620b4-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="620b4-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="620b4-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="620b4-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="620b4-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="620b4-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="620b4-202">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="620b4-202">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="620b4-203">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="620b4-203">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="620b4-204">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="620b4-204">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="620b4-205">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="620b4-205">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="620b4-206">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="620b4-206">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="620b4-207">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="620b4-207">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="620b4-208">JetMove</span><span class="sxs-lookup"><span data-stu-id="620b4-208">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="620b4-209">JetSeek</span><span class="sxs-lookup"><span data-stu-id="620b4-209">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="620b4-210">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="620b4-210">JetSetCurrentIndex</span></span>]()  
[<span data-ttu-id="620b4-211">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="620b4-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="620b4-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="620b4-212">JetStopService</span></span>](./jetstopservice-function.md)

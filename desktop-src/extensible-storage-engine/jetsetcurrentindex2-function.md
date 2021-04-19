---
description: 'En savoir plus sur : fonction JetSetCurrentIndex2'
title: Fonction JetSetCurrentIndex2
TOCTitle: JetSetCurrentIndex2 Function
ms:assetid: da94465e-bd35-45c2-9ccc-1d2e8c34aa9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294110(v=EXCHG.10)
ms:contentKeyID: 32765725
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex2W
- JetSetCurrentIndex2A
- JetSetCurrentIndex2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c95e665b549fff82e0beaaca9682329217ebb0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514976"
---
# <a name="jetsetcurrentindex2-function"></a><span data-ttu-id="eaa9e-103">Fonction JetSetCurrentIndex2</span><span class="sxs-lookup"><span data-stu-id="eaa9e-103">JetSetCurrentIndex2 Function</span></span>


<span data-ttu-id="eaa9e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="eaa9e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex2-function"></a><span data-ttu-id="eaa9e-105">Fonction JetSetCurrentIndex2</span><span class="sxs-lookup"><span data-stu-id="eaa9e-105">JetSetCurrentIndex2 Function</span></span>

<span data-ttu-id="eaa9e-106">La fonction **JetSetCurrentIndex2** définit l’index actuel d’un curseur qui définit les enregistrements d’une table qui sont visibles par ce curseur et l’ordre dans lequel ils apparaissent en sélectionnant l’ensemble d’entrées d’index à utiliser pour exposer ces enregistrements.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-106">The **JetSetCurrentIndex2** function sets the current index of a cursor that defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="eaa9e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eaa9e-107">Parameters</span></span>

<span data-ttu-id="eaa9e-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="eaa9e-108">*sesid*</span></span>

<span data-ttu-id="eaa9e-109">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-109">The session to use for this call.</span></span>

<span data-ttu-id="eaa9e-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="eaa9e-110">*tableid*</span></span>

<span data-ttu-id="eaa9e-111">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-111">The cursor to use for this call.</span></span>

<span data-ttu-id="eaa9e-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="eaa9e-112">*szIndexName*</span></span>

<span data-ttu-id="eaa9e-113">Nom de l’index à sélectionner pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-113">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="eaa9e-114">Si ce paramètre a la valeur NULL ou est une chaîne vide, l’index cluster est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-114">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="eaa9e-115">Si un index primaire est défini pour la table, cet index est sélectionné, car il est identique à l’index cluster.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-115">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="eaa9e-116">Si aucun index primaire n’est défini pour la table, l’index séquentiel est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-116">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="eaa9e-117">L’index séquentiel n’a pas de définition d’index.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-117">The sequential index has no index definition.</span></span> <span data-ttu-id="eaa9e-118">Pour plus d’informations, consultez [JetCreateIndex](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="eaa9e-118">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="eaa9e-119">Si *pIndexID* n’a pas la valeur null, le nom de l’index sera ignoré et l’index sera sélectionné par son ID d’index.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-119">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="eaa9e-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="eaa9e-120">*grbit*</span></span>

<span data-ttu-id="eaa9e-121">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-121">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eaa9e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaa9e-122">Value</span></span></p></th>
<th><p><span data-ttu-id="eaa9e-123">Signification</span><span class="sxs-lookup"><span data-stu-id="eaa9e-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-124">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="eaa9e-124">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-125">Cette option indique que le curseur doit être positionné sur la première entrée de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-125">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="eaa9e-126">Si l’index cluster est en cours de sélection (index primaire ou index séquentiel) et si l’index actuel est un index secondaire, JET_bitMoveFirst est supposé.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-126">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="eaa9e-127">Si l’index actuel est sélectionné, cette option est ignorée et aucune modification n’est apportée à la position du curseur.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-127">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaa9e-128">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="eaa9e-128">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-129">Cette option indique que le curseur doit être positionné sur l’entrée d’index du nouvel index qui correspond à l’enregistrement associé à l’entrée d’index à la position actuelle du curseur sur l’ancien index.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-129">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="eaa9e-130">Si la définition du nouvel index contient au moins une colonne clé à valeurs multiples, l’entrée d’index de destination est ambiguë.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-130">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="eaa9e-131">Dans ce cas, le <em>itagSequence</em> spécifié est utilisé pour sélectionner la valeur à plusieurs valeurs de la colonne clé à valeurs multiples la plus significative qui est utilisée pour positionner le curseur.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-131">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="eaa9e-132">Il est seulement nécessaire de passer un seul <em>itagSequence</em> même dans le cas de plusieurs colonnes clés à valeurs multiples, car le moteur étend uniquement toutes les valeurs de la colonne clé à valeurs multiples la plus significative.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-132">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="eaa9e-133">Pour plus d’informations, consultez <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> .</span><span class="sxs-lookup"><span data-stu-id="eaa9e-133">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="eaa9e-134">Si JET_bitMoveFirst est spécifié, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-134">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="eaa9e-135">Si l’index actuel est sélectionné, cette option est ignorée et aucune modification n’est apportée à la position du curseur.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-135">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="eaa9e-136">Quand ce paramètre n’est pas présent, sa valeur est supposée être JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-136">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="eaa9e-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eaa9e-137">Return Value</span></span>

<span data-ttu-id="eaa9e-138">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="eaa9e-139">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eaa9e-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eaa9e-140">Code de retour</span><span class="sxs-lookup"><span data-stu-id="eaa9e-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="eaa9e-141">Description</span><span class="sxs-lookup"><span data-stu-id="eaa9e-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="eaa9e-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-143">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaa9e-144">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="eaa9e-144">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-145">Un index secondaire est sélectionné avec l’option JET_bitNoMove et il n’y a aucune valeur pour la première colonne clé à valeurs multiples dans la nouvelle définition pour l’index qui correspond au numéro de séquence spécifié.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-145">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new definition for the index that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="eaa9e-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-147">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaa9e-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="eaa9e-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-149">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="eaa9e-150">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-151">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="eaa9e-151">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-152">Le contenu de l’ID d’index n’était pas valide ou a expiré et doit être actualisé.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-152">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="eaa9e-153">Cela peut se produire pour <strong>JetSetCurrentIndex2</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="eaa9e-153">This can happen for <strong>JetSetCurrentIndex2</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="eaa9e-154">pIndexID- &gt; cbStruct n’est pas de la taille attendue (Windows Server 2003 et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="eaa9e-154">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="eaa9e-155">Le moteur a été arrêté depuis que l’ID d’index a été extrait.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-155">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="eaa9e-156">Tous les curseurs faisant référence à la table contenant l’index correspondant à l’ID d’index ont été fermés et le moteur a supprimé la définition de l’index du cache de schéma.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-156">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted the definition for the index from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="eaa9e-157">L’ID d’index est utilisé avec un curseur ouvert sur une table incorrecte.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-157">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="eaa9e-158">L’index a été supprimé ou n’est pas encore visible dans la session.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-158">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaa9e-159">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="eaa9e-159">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-160">L’un des noms d’objets spécifiés n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-160">One of the specified object names was invalid.</span></span> <span data-ttu-id="eaa9e-161">Tous les noms d’objets doivent être conformes au même ensemble de règles.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-161">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="eaa9e-162">Ces règles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="eaa9e-162">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="eaa9e-163">Les noms d’objets doivent être composés de caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-163">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="eaa9e-164">Les noms d’objets doivent comporter au moins un caractère.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-164">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="eaa9e-165">Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-165">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="eaa9e-166">Les noms d’objets ne peuvent pas commencer par un espace.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-166">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="eaa9e-167">Les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</span><span class="sxs-lookup"><span data-stu-id="eaa9e-167">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="eaa9e-168">Les noms d’objets ne peuvent pas contenir de point d’exclamation ( !), de point (.), de crochet gauche ([) ou de crochet droit (]).</span><span class="sxs-lookup"><span data-stu-id="eaa9e-168">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="eaa9e-169">Une fois validée, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-169">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="eaa9e-170">Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-170">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-171">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="eaa9e-171">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-172">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-172">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="eaa9e-173">Cela peut se produire pour <strong>JetSetCurrentIndex2</strong> lorsque <em>pIndexID</em> n’a pas la valeur null et que pIndexID- &gt; cbStruct n’est pas de la taille attendue (Windows XP et versions antérieures).</span><span class="sxs-lookup"><span data-stu-id="eaa9e-173">This can happen for <strong>JetSetCurrentIndex2</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaa9e-174">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="eaa9e-174">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-175">Un index secondaire est sélectionné avec l’option JET_bitNoMove et il n’existe aucune entrée d’index dans le nouvel index qui correspond à l’enregistrement associé à l’entrée d’index à la position actuelle du curseur sur l’ancien index.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-175">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-176">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="eaa9e-176">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-177">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-177">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaa9e-178">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="eaa9e-178">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-179">Le moteur a épuisé son pool de ressources utilisé pour ouvrir les curseurs.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-179">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="eaa9e-180">Le nombre maximal de curseurs pouvant être ouverts à un moment donné est contrôlé à l’aide de <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-180">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="eaa9e-181">Pour plus d’informations, consultez <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> .</span><span class="sxs-lookup"><span data-stu-id="eaa9e-181">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="eaa9e-182">Cela peut se produire pour <strong>JetSetCurrentIndex2</strong> lorsqu’un index secondaire a été sélectionné et que le moteur ne peut pas ouvrir un curseur interne pour utiliser cet index.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-182">This can happen for <strong>JetSetCurrentIndex2</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-183">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="eaa9e-183">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-184">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-184">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaa9e-185">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="eaa9e-185">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-186">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-186">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="eaa9e-187">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-187">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-188">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="eaa9e-188">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="eaa9e-189">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-189">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eaa9e-190">En cas de réussite, l’index actuel du curseur est défini sur l’index demandé.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-190">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="eaa9e-191">Les entrées d’index peuvent désormais être recherchées à l’aide de [JetSeek](./jetseek-function.md) en fonction de la définition d’index de l’index demandé.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-191">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="eaa9e-192">Les entrées d’index peuvent également être énumérées à l’aide de [JetMove](./jetmove-function.md) dans l’ordre spécifié par cette définition d’index.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-192">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="eaa9e-193">La position actuelle du curseur est définie sur la première entrée d’index de l’index (JET_bitMoveFirst) ou sur une entrée d’index spécifique qui est associée à la position actuelle du curseur sur l’ancien index (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="eaa9e-193">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="eaa9e-194">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-194">No change to the database state will occur.</span></span>

<span data-ttu-id="eaa9e-195">En cas d’échec, l’index actuel et la position actuelle du curseur sont dans un État indéfini.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-195">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="eaa9e-196">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-196">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="eaa9e-197">Notes</span><span class="sxs-lookup"><span data-stu-id="eaa9e-197">Remarks</span></span>

<span data-ttu-id="eaa9e-198">Si l’indicateur d’ID d’index est obsolète, l’API échoue simplement.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-198">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="eaa9e-199">Il n’existe pas de secours pour le nom de texte de l’index dans ce cas, car il peut s’agir d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-199">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="eaa9e-200">Ce secours doit être effectué manuellement par l’appelant de l’API.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-200">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="eaa9e-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaa9e-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="eaa9e-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="eaa9e-203">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaa9e-204"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="eaa9e-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="eaa9e-205">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-206"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="eaa9e-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="eaa9e-207">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaa9e-208"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="eaa9e-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="eaa9e-209">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaa9e-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="eaa9e-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="eaa9e-211">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="eaa9e-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaa9e-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="eaa9e-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="eaa9e-213">Implémenté en tant que <strong>JetSetCurrentIndex2W</strong> (Unicode) et <strong>JetSetCurrentIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="eaa9e-213">Implemented as <strong>JetSetCurrentIndex2W</strong> (Unicode) and <strong>JetSetCurrentIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="eaa9e-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaa9e-214">See Also</span></span>

[<span data-ttu-id="eaa9e-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="eaa9e-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="eaa9e-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="eaa9e-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="eaa9e-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="eaa9e-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="eaa9e-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="eaa9e-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="eaa9e-219">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="eaa9e-219">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="eaa9e-220">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="eaa9e-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="eaa9e-221">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="eaa9e-221">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="eaa9e-222">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="eaa9e-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="eaa9e-223">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="eaa9e-223">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="eaa9e-224">JetMove</span><span class="sxs-lookup"><span data-stu-id="eaa9e-224">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="eaa9e-225">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="eaa9e-225">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="eaa9e-226">JetSeek</span><span class="sxs-lookup"><span data-stu-id="eaa9e-226">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="eaa9e-227">JetStopService</span><span class="sxs-lookup"><span data-stu-id="eaa9e-227">JetStopService</span></span>](./jetstopservice-function.md)

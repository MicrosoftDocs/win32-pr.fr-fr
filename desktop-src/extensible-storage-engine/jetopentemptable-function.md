---
description: 'En savoir plus sur : fonction JetOpenTempTable'
title: Fonction JetOpenTempTable
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66c58abc5cff433bb4d944e39c283ba712d7cebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543650"
---
# <a name="jetopentemptable-function"></a><span data-ttu-id="4b668-103">Fonction JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="4b668-103">JetOpenTempTable Function</span></span>


<span data-ttu-id="4b668-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="4b668-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable-function"></a><span data-ttu-id="4b668-105">Fonction JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="4b668-105">JetOpenTempTable Function</span></span>

<span data-ttu-id="4b668-106">La fonction **JetOpenTempTable** crée une table temporaire avec un index unique.</span><span class="sxs-lookup"><span data-stu-id="4b668-106">The **JetOpenTempTable** function creates a temporary table with a single index.</span></span> <span data-ttu-id="4b668-107">Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="4b668-107">A temporary table stores and retrieves records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="4b668-108">Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile.</span><span class="sxs-lookup"><span data-stu-id="4b668-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="4b668-109">Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.</span><span class="sxs-lookup"><span data-stu-id="4b668-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="4b668-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b668-110">Parameters</span></span>

<span data-ttu-id="4b668-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4b668-111">*sesid*</span></span>

<span data-ttu-id="4b668-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4b668-112">The session to use.</span></span>

<span data-ttu-id="4b668-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="4b668-113">*prgcolumndef*</span></span>

<span data-ttu-id="4b668-114">Définitions de colonne pour les colonnes créées dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="4b668-115">Il existe des limitations **importantes** pour les options de définition de colonne utilisées avec une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-115">**Important**   limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="4b668-116">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4b668-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="4b668-117">Outre les options de définition de colonne habituelles, aucune ou plusieurs des options suivantes peuvent également être spécifiées qui ne sont pertinentes que dans le contexte d’une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b668-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b668-118">Value</span></span></p></th>
<th><p><span data-ttu-id="4b668-119">Signification</span><span class="sxs-lookup"><span data-stu-id="4b668-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b668-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="4b668-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="4b668-121">L’ordre de tri de la colonne clé pour la table temporaire doit être décroissant plutôt que croissant.</span><span class="sxs-lookup"><span data-stu-id="4b668-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="4b668-122">Si cette option est spécifiée sans JET_bitColumnTTKey, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="4b668-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="4b668-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="4b668-124">La colonne est une colonne clé pour la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="4b668-125">L’ordre des définitions de colonne avec cette option spécifiée dans le tableau d’entrée détermine la précédence de chaque colonne clé pour la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="4b668-126">La première définition de colonne dans le tableau qui a cette option est définie sur la colonne clé la plus significative, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="4b668-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="4b668-127">Si le moteur de base de données demande plus de colonnes clés que ce qui peut être pris en charge par le moteur de base de données, cette option est ignorée pour les colonnes clés non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4b668-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4b668-128">*ccolumn*</span><span class="sxs-lookup"><span data-stu-id="4b668-128">*ccolumn*</span></span>

<span data-ttu-id="4b668-129">Consultez *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="4b668-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="4b668-130">*grbit*</span><span class="sxs-lookup"><span data-stu-id="4b668-130">*grbit*</span></span>

<span data-ttu-id="4b668-131">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b668-131">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b668-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b668-132">Value</span></span></p></th>
<th><p><span data-ttu-id="4b668-133">Signification</span><span class="sxs-lookup"><span data-stu-id="4b668-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b668-134">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="4b668-134">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="4b668-135">Toute tentative d’insertion d’un enregistrement avec la même clé d’index qu’un enregistrement précédemment inséré échouera immédiatement avec JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="4b668-135">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="4b668-136">Si cette option n’est pas demandée, un doublon est détecté immédiatement et échoue, ou est supprimé en mode silencieux ultérieurement, en fonction de la stratégie choisie par le moteur de base de données pour implémenter la table temporaire, en fonction de la fonctionnalité demandée.</span><span class="sxs-lookup"><span data-stu-id="4b668-136">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="4b668-137">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="4b668-137">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="4b668-138">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="4b668-138">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-139">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="4b668-139">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="4b668-140">Force le gestionnaire de tables temporaires à abandonner la recherche de la meilleure stratégie pour utiliser la gestion de la table temporaire qui entraîne des performances améliorées.</span><span class="sxs-lookup"><span data-stu-id="4b668-140">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-141">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="4b668-141">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="4b668-142">La table temporaire est créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation qui est optimisée pour les résultats de requête intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="4b668-142">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="4b668-143">Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="4b668-143">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="4b668-144">L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées.</span><span class="sxs-lookup"><span data-stu-id="4b668-144">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="4b668-145">Pour plus d’informations, consultez JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="4b668-145">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="4b668-146">Cette option est disponible uniquement sur Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4b668-146">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-147">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="4b668-147">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="4b668-148">Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’utilisation de <a href="gg294103(v=exchg.10).md">JetSeek</a> pour rechercher des enregistrements par clé d’index.</span><span class="sxs-lookup"><span data-stu-id="4b668-148">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="4b668-149">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="4b668-149">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="4b668-150">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="4b668-150">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-151">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="4b668-151">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="4b668-152">Demande que les enregistrements avec des clés d’index dupliquées soient supprimés du jeu final d’enregistrements dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-152">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="4b668-153">Avant Windows Server 2003, le moteur de base de données supposait toujours que cette option était appliquée en raison du fait que tous les index cluster doivent également être une clé primaire et doivent donc être uniques.</span><span class="sxs-lookup"><span data-stu-id="4b668-153">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="4b668-154">À compter de Windows Server 2003, il est désormais possible de créer une table temporaire qui ne supprime pas les doublons lorsque l’option JET_bitTTForwardOnly est également spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4b668-154">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="4b668-155">Il n’est pas possible de savoir quel doublon va être effectué et quels doublons seront ignorés, en général.</span><span class="sxs-lookup"><span data-stu-id="4b668-155">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="4b668-156">Toutefois, lorsque l’option JET_bitTTErrorOnDuplicateInsertion est demandée, le premier enregistrement avec une clé d’index donnée à insérer dans la table temporaire sera toujours correctement effectué.</span><span class="sxs-lookup"><span data-stu-id="4b668-156">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-157">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="4b668-157">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="4b668-158">Demande que la table temporaire soit suffisamment flexible pour permettre la modification ultérieure des enregistrements qui ont été insérés précédemment.</span><span class="sxs-lookup"><span data-stu-id="4b668-158">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="4b668-159">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="4b668-159">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="4b668-160">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="4b668-160">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-161">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="4b668-161">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="4b668-162">Demande que la table temporaire soit suffisamment flexible pour permettre l’analyse des enregistrements dans un ordre et une direction arbitraires à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="4b668-162">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="4b668-163">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="4b668-163">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="4b668-164">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="4b668-164">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-165">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="4b668-165">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="4b668-166">Demande que les valeurs de colonne clé NULL soient plus proches de la fin de l’index que les valeurs de colonne clé non NULL.</span><span class="sxs-lookup"><span data-stu-id="4b668-166">Requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-167">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="4b668-167">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="4b668-168">Demande d’autoriser uniquement les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="4b668-168">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="4b668-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4b668-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4b668-170">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="4b668-170">*ptableid*</span></span>

<span data-ttu-id="4b668-171">Mémoire tampon de sortie qui reçoit le nouveau curseur ouvert sur la table temporaire nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="4b668-171">The output buffer that receives the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="4b668-172">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="4b668-172">*prgcolumnid*</span></span>

<span data-ttu-id="4b668-173">Mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés au cours de la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-173">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="4b668-174">Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="4b668-174">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="4b668-175">Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4b668-175">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="4b668-176">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4b668-176">Return Value</span></span>

<span data-ttu-id="4b668-177">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="4b668-177">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4b668-178">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4b668-178">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b668-179">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4b668-179">Return code</span></span></p></th>
<th><p><span data-ttu-id="4b668-180">Description</span><span class="sxs-lookup"><span data-stu-id="4b668-180">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b668-181">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4b668-181">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4b668-182">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="4b668-182">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-183">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="4b668-183">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="4b668-184"><strong>JetOpenTempTable</strong> a échoué parce que JET_bitTTForwardOnly a été spécifié et que la table temporaire spécifiée n’a pas pu être créée à l’aide de l’optimisation avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="4b668-184"><strong>JetOpenTempTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="4b668-185">Cette erreur est renvoyée uniquement par Windows Server 2003 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4b668-185">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-186">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4b668-186">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4b668-187">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="4b668-187">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-188">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="4b668-188">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="4b668-189">Impossible de créer l’index, car une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4b668-189">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="4b668-190"><strong>JetOpenTempTable</strong> renvoie cette erreur dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="4b668-190"><strong>JetOpenTempTable</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b668-191">Les paramètres régionaux de langue neutre sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="4b668-191">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="4b668-192">Un ensemble non valide d’indicateurs de normalisation est spécifié.</span><span class="sxs-lookup"><span data-stu-id="4b668-192">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="4b668-193">Cette erreur est renvoyée uniquement par Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4b668-193">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4b668-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4b668-195">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="4b668-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="4b668-196">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4b668-196">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-197">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="4b668-197">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="4b668-198">Le champ CP de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur une page de codes valide.</span><span class="sxs-lookup"><span data-stu-id="4b668-198">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="4b668-199">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="4b668-199">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="4b668-200">La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="4b668-200">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-201">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="4b668-201">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="4b668-202">Le champ <em>coltyp</em> de l' <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur un type de colonne valide.</span><span class="sxs-lookup"><span data-stu-id="4b668-202">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="4b668-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="4b668-204">Impossible de créer l’index, car une tentative d’utilisation d’un ID de paramètres régionaux non valide a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="4b668-204">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="4b668-205">L’ID de paramètres régionaux peut être entièrement non valide ou le module linguistique associé n’est peut-être pas installé.</span><span class="sxs-lookup"><span data-stu-id="4b668-205">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-206">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="4b668-206">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="4b668-207">Impossible de créer l’index, car une tentative d’utilisation d’un ensemble non valide d’indicateurs de normalisation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="4b668-207">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="4b668-208">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4b668-208">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="4b668-209">Sur Windows 2000, les indicateurs de normalisation non valides génèrent JET_errIndexInvalidDef à la place.</span><span class="sxs-lookup"><span data-stu-id="4b668-209">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-210">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="4b668-210">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="4b668-211">Le descripteur de session n’est pas valide ou fait référence à une session fermée.</span><span class="sxs-lookup"><span data-stu-id="4b668-211">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="4b668-212"><strong>Remarque</strong>  Cette erreur n’est pas retournée dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="4b668-212"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="4b668-213">Les handles ne sont validés qu’à titre d’effort optimal.</span><span class="sxs-lookup"><span data-stu-id="4b668-213">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-214">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4b668-214">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4b668-215">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="4b668-215">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-216">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="4b668-216">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="4b668-217">L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour ouvrir un nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="4b668-217">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="4b668-218">Les ressources de curseur sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="4b668-218">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-219">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="4b668-219">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="4b668-220">L’opération a échoué, car la mémoire peut être allouée pour être terminée.</span><span class="sxs-lookup"><span data-stu-id="4b668-220">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="4b668-221"><strong>JetOpenTempTable</strong> peut retourner JET_errOutOfMemory si l’espace d’adressage du processus hôte est trop fragmenté.</span><span class="sxs-lookup"><span data-stu-id="4b668-221"><strong>JetOpenTempTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="4b668-222">Le gestionnaire de tables temporaire allouera toujours un segment d’espace d’adressage de 1 Mo pour chaque table temporaire créée, quelle que soit la quantité de données à stocker.</span><span class="sxs-lookup"><span data-stu-id="4b668-222">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-223">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4b668-223">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4b668-224">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="4b668-224">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-225">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4b668-225">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4b668-226">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="4b668-226">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="4b668-227">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4b668-227">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-228">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4b668-228">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4b668-229">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4b668-229">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-230">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="4b668-230">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="4b668-231">Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="4b668-231">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="4b668-232">Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</span><span class="sxs-lookup"><span data-stu-id="4b668-232">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-233">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="4b668-233">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="4b668-234">L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache les index de la table.</span><span class="sxs-lookup"><span data-stu-id="4b668-234">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="4b668-235">Le nombre d’index dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="4b668-235">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-236">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="4b668-236">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="4b668-237">L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache le schéma de la table.</span><span class="sxs-lookup"><span data-stu-id="4b668-237">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="4b668-238">Le nombre de tables dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="4b668-238">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-239">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="4b668-239">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="4b668-240">L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour créer une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-240">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="4b668-241">Les ressources de table temporaire sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="4b668-241">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4b668-242">En cas de réussite, un curseur ouvert sur la table temporaire nouvellement créée est retourné.</span><span class="sxs-lookup"><span data-stu-id="4b668-242">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="4b668-243">L’état de la base de données temporaire sera préparé à contenir la nouvelle table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-243">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="4b668-244">L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="4b668-244">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="4b668-245">En cas d’échec, la table temporaire n’est pas créée et un curseur n’est pas renvoyé.</span><span class="sxs-lookup"><span data-stu-id="4b668-245">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="4b668-246">L’état de la base de données temporaire peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="4b668-246">The state of the temporary database may be changed.</span></span> <span data-ttu-id="4b668-247">L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="4b668-247">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4b668-248">Notes</span><span class="sxs-lookup"><span data-stu-id="4b668-248">Remarks</span></span>

<span data-ttu-id="4b668-249">Les tables temporaires ne prennent pas en charge le complément complet des options de définition de colonne généralement prises en charge par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="4b668-249">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="4b668-250">En fait, seuls les JET_bitColumnFixed et les JET_bitColumnTagged sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4b668-250">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="4b668-251">Cela signifie qu’il n’est pas possible de créer une colonne à incrémentation automatique, une version ou une colonne à plusieurs valeurs dans une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-251">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="4b668-252">Enfin, les colonnes de mise à jour de tiers de confiance ne sont pas prises en charge car elles ne sont pas utiles dans une table temporaire, car elles ne peuvent être utilisées que par une seule session à la fois.</span><span class="sxs-lookup"><span data-stu-id="4b668-252">Finally, escrow update columns are not supported because they are not useful in a temporary table since they can only be used by one session at a time.</span></span> <span data-ttu-id="4b668-253">Si l’une de ces options est demandée, elles seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="4b668-253">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="4b668-254">Les tables temporaires ne prennent pas en charge les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="4b668-254">Temporary tables do not support default values.</span></span> <span data-ttu-id="4b668-255">Si une définition de colonne est fournie et contient une spécification de valeur par défaut, cette spécification sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="4b668-255">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="4b668-256">Les tables temporaires sont retournées à l’appelant à la suite de nombreuses fonctions ESE différentes.</span><span class="sxs-lookup"><span data-stu-id="4b668-256">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="4b668-257">Par exemple, [JetGetIndexInfo](./jetgetindexinfo-function.md) avec l’option JET_IdxInfo définie dans le paramètre *InfoLevel* retourne une table temporaire contenant une liste de toutes les colonnes clés d’un index donné.</span><span class="sxs-lookup"><span data-stu-id="4b668-257">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set in the *InfoLevel* parameter will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="4b668-258">Les tables temporaires suivent les mêmes règles de cycle de vie que les tables temporaires ordinaires, comme décrit ici.</span><span class="sxs-lookup"><span data-stu-id="4b668-258">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="4b668-259">Les tables temporaires sont également utilisées en interne par le moteur de base de données pour de nombreuses tâches.</span><span class="sxs-lookup"><span data-stu-id="4b668-259">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="4b668-260">La plus importante de ces tâches est la création d’un index sur une table existante.</span><span class="sxs-lookup"><span data-stu-id="4b668-260">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="4b668-261">Une table temporaire sera utilisée pour trier les clés d’index utilisées pour construire cet index.</span><span class="sxs-lookup"><span data-stu-id="4b668-261">A temporary table will be used to sort the index keys used to construct that index.</span></span>

<span data-ttu-id="4b668-262">Toutes les tables temporaires sont stockées dans la base de données temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-262">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="4b668-263">La base de données temporaire est un fichier de base de données spécial qui est conservé pendant la durée de vie d’une instance ESE et qui est supprimé lorsque cette instance est arrêtée ou redémarrée.</span><span class="sxs-lookup"><span data-stu-id="4b668-263">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="4b668-264">L’emplacement de la base de données temporaire peut être configuré à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4b668-264">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="4b668-265">Le placement de la base de données temporaire sur le disque par rapport à vos fichiers journaux de transactions et vos fichiers de base de données peut être important si votre application utilise intensivement des tables temporaires ou crée fréquemment des index.</span><span class="sxs-lookup"><span data-stu-id="4b668-265">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="4b668-266">Le cycle de vie d’une table temporaire est lié aux curseurs qui la référencent.</span><span class="sxs-lookup"><span data-stu-id="4b668-266">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="4b668-267">Si tous les curseurs qui font référence à une table temporaire sont fermés, de manière implicite ou explicite, la table temporaire est supprimée.</span><span class="sxs-lookup"><span data-stu-id="4b668-267">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="4b668-268">Si une table temporaire est créée à l’intérieur d’une transaction et que la transaction est ensuite restaurée, la table temporaire est supprimée, car tous les curseurs qui y font référence sont implicitement fermés.</span><span class="sxs-lookup"><span data-stu-id="4b668-268">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="4b668-269">Les nouveaux curseurs peuvent référencer une table temporaire uniquement par le biais de l’utilisation de [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="4b668-269">New cursors may reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="4b668-270">Dans ce cas, les nouveaux curseurs sont positionnés sur la première entrée d’index de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-270">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="4b668-271">[JetDupCursor](./jetdupcursor-function.md) ne fonctionnera que pendant certaines phases d’utilisation de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-271">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="4b668-272">Pour plus d’informations, consultez les notes relatives aux fonctionnalités de curseur de table temporaires.</span><span class="sxs-lookup"><span data-stu-id="4b668-272">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="4b668-273">Il n’est pas possible de référencer une table temporaire à partir de plusieurs sessions à la fois.</span><span class="sxs-lookup"><span data-stu-id="4b668-273">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="4b668-274">Il existe un problème important dans [JetDupCursor](./jetdupcursor-function.md) qui affecte les tables temporaires.</span><span class="sxs-lookup"><span data-stu-id="4b668-274">There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="4b668-275">Si une tentative est faite pour dupliquer une table temporaire en mode avant uniquement, le curseur résultant ne sera pas créé correctement et fonctionnera correctement.</span><span class="sxs-lookup"><span data-stu-id="4b668-275">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="4b668-276">Il est toujours possible de dupliquer un curseur sur une table temporaire matérialisée.</span><span class="sxs-lookup"><span data-stu-id="4b668-276">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="4b668-277">Le gestionnaire de tables temporaire peut choisir d’implémenter une table temporaire de trois manières.</span><span class="sxs-lookup"><span data-stu-id="4b668-277">The temporary table manager may choose to implement a temporary table in three ways.</span></span> <span data-ttu-id="4b668-278">La première méthode consiste à conserver une table en mémoire.</span><span class="sxs-lookup"><span data-stu-id="4b668-278">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="4b668-279">Cette stratégie est la plus rapide, mais elle ne peut être utilisée que pour les petites tables temporaires simples.</span><span class="sxs-lookup"><span data-stu-id="4b668-279">This strategy is the fastest but can only be used for small, simple temporary tables.</span></span> <span data-ttu-id="4b668-280">La deuxième méthode consiste à créer un tri sur disque qui peut être piloté à l’aide d’un itérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="4b668-280">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="4b668-281">Cette stratégie ne peut être utilisée que dans certaines circonstances et est le moyen le plus rapide pour trier et supprimer les doublons d’un jeu de données très volumineux.</span><span class="sxs-lookup"><span data-stu-id="4b668-281">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="4b668-282">La troisième méthode consiste à créer une arborescence B + dans la base de données temporaire pour contenir la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-282">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="4b668-283">Cette stratégie est la plus lente, mais la plus polyvalente, appelée « table temporaire matérialisée ».</span><span class="sxs-lookup"><span data-stu-id="4b668-283">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="4b668-284">Ces stratégies peuvent être utilisées en association pour atteindre en fin de fonction la fonctionnalité demandée par la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-284">These strategies may be used in combination to ultimately achieve the functionality requested of the temporary table.</span></span>

<span data-ttu-id="4b668-285">Lorsque la table temporaire n’est pas matérialisée, elle est utilisée principalement en deux phases principales.</span><span class="sxs-lookup"><span data-stu-id="4b668-285">When the temporary table is not materialized then it is used in primarily two major phases.</span></span> <span data-ttu-id="4b668-286">La première phase correspond à la phase d’insertion où la table est remplie avec son jeu de données initial.</span><span class="sxs-lookup"><span data-stu-id="4b668-286">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="4b668-287">Pendant cette phase, seule l’insertion de données est autorisée.</span><span class="sxs-lookup"><span data-stu-id="4b668-287">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="4b668-288">Cette phase se termine lorsqu’une tentative est effectuée pour déplacer le curseur à l’aide de [JetMove](./jetmove-function.md) ou [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="4b668-288">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="4b668-289">La deuxième phase est la phase d’extraction des données.</span><span class="sxs-lookup"><span data-stu-id="4b668-289">The second phase is the data extraction phase.</span></span> <span data-ttu-id="4b668-290">Au cours de cette phase, les données stockées dans la table temporaire peuvent être extraites en fonction des capacités requises lors de la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="4b668-290">During this phase, the data stored in the temporary table may be extracted according to the capabilities requested when the temporary table was created.</span></span>

<span data-ttu-id="4b668-291">**Fonctionnalités de curseur de table temporaires**</span><span class="sxs-lookup"><span data-stu-id="4b668-291">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="4b668-292">Lorsque la table temporaire est matérialisée, le curseur a les fonctionnalités suivantes, mais peut être limité par les options demandées :</span><span class="sxs-lookup"><span data-stu-id="4b668-292">When the temporary table is materialized, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="4b668-293">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="4b668-293">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="4b668-294">JetDelete</span><span class="sxs-lookup"><span data-stu-id="4b668-294">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="4b668-295">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="4b668-295">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="4b668-296">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="4b668-296">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="4b668-297">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="4b668-297">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="4b668-298">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="4b668-298">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="4b668-299">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="4b668-299">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="4b668-300">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="4b668-300">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="4b668-301">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="4b668-301">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="4b668-302">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="4b668-302">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="4b668-303">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="4b668-303">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="4b668-304">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="4b668-304">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="4b668-305">JetMove</span><span class="sxs-lookup"><span data-stu-id="4b668-305">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="4b668-306">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="4b668-306">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="4b668-307">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="4b668-307">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="4b668-308">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="4b668-308">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="4b668-309">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="4b668-309">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="4b668-310">JetSeek</span><span class="sxs-lookup"><span data-stu-id="4b668-310">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="4b668-311">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="4b668-311">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="4b668-312">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="4b668-312">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="4b668-313">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="4b668-313">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="4b668-314">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="4b668-314">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="4b668-315">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="4b668-315">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="4b668-316">Lorsque la table temporaire n’est pas matérialisée et qu’elle est dans la phase d’insertion, le curseur a les fonctionnalités suivantes, mais peut être limité par les options demandées :</span><span class="sxs-lookup"><span data-stu-id="4b668-316">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="4b668-317">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="4b668-317">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="4b668-318">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="4b668-318">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="4b668-319">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="4b668-319">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="4b668-320">JetMove</span><span class="sxs-lookup"><span data-stu-id="4b668-320">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="4b668-321">**Remarque**  Provoque la transition vers la phase d’extraction.</span><span class="sxs-lookup"><span data-stu-id="4b668-321">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="4b668-322">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="4b668-322">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="4b668-323">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="4b668-323">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="4b668-324">JetSeek</span><span class="sxs-lookup"><span data-stu-id="4b668-324">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="4b668-325">**Remarque**  Provoque la transition vers la phase d’extraction.</span><span class="sxs-lookup"><span data-stu-id="4b668-325">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="4b668-326">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="4b668-326">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="4b668-327">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="4b668-327">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="4b668-328">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="4b668-328">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="4b668-329">Lorsque la table temporaire n’est pas matérialisée et qu’elle est dans la phase d’extraction, le curseur a les fonctionnalités suivantes, mais peut être limité par les options demandées :</span><span class="sxs-lookup"><span data-stu-id="4b668-329">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="4b668-330">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="4b668-330">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="4b668-331">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="4b668-331">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="4b668-332">**Remarque**  Si une tentative est faite pour dupliquer une table temporaire en mode avant uniquement, le curseur résultant ne sera pas créé correctement et fonctionnera correctement.</span><span class="sxs-lookup"><span data-stu-id="4b668-332">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="4b668-333">Il est toujours possible de dupliquer un curseur sur une table temporaire matérialisée.</span><span class="sxs-lookup"><span data-stu-id="4b668-333">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="4b668-334">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="4b668-334">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="4b668-335">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="4b668-335">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="4b668-336">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="4b668-336">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="4b668-337">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="4b668-337">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="4b668-338">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="4b668-338">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="4b668-339">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="4b668-339">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="4b668-340">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="4b668-340">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="4b668-341">JetMove</span><span class="sxs-lookup"><span data-stu-id="4b668-341">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="4b668-342">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="4b668-342">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="4b668-343">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="4b668-343">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="4b668-344">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="4b668-344">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="4b668-345">JetSeek</span><span class="sxs-lookup"><span data-stu-id="4b668-345">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="4b668-346">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="4b668-346">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="4b668-347">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="4b668-347">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="4b668-348">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b668-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b668-349"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="4b668-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4b668-350">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="4b668-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-351"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="4b668-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4b668-352">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4b668-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-353"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="4b668-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4b668-354">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="4b668-354">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b668-355"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="4b668-355"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4b668-356">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4b668-356">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b668-357"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4b668-357"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4b668-358">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4b668-358">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4b668-359">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b668-359">See Also</span></span>

[<span data-ttu-id="4b668-360">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="4b668-360">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="4b668-361">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="4b668-361">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="4b668-362">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4b668-362">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4b668-363">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4b668-363">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4b668-364">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4b668-364">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4b668-365">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4b668-365">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4b668-366">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="4b668-366">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="4b668-367">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="4b668-367">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="4b668-368">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="4b668-368">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="4b668-369">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="4b668-369">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="4b668-370">JetMove</span><span class="sxs-lookup"><span data-stu-id="4b668-370">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="4b668-371">JetRollback</span><span class="sxs-lookup"><span data-stu-id="4b668-371">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="4b668-372">JetSeek</span><span class="sxs-lookup"><span data-stu-id="4b668-372">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="4b668-373">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="4b668-373">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="4b668-374">Paramètres de base de données temporaires</span><span class="sxs-lookup"><span data-stu-id="4b668-374">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)

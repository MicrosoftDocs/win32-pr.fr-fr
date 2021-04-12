---
description: 'En savoir plus sur : structure JET_OPENTEMPORARYTABLE'
title: Structure JET_OPENTEMPORARYTABLE
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319318"
---
# <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="e0cca-103">Structure JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="e0cca-103">JET_OPENTEMPORARYTABLE Structure</span></span>


<span data-ttu-id="e0cca-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="e0cca-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="e0cca-105">Structure JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="e0cca-105">JET_OPENTEMPORARYTABLE Structure</span></span>

<span data-ttu-id="e0cca-106">La structure **JET_OPENTEMPORARYTABLE** contient une collection de paramètres facilement extensible pour la fonction **JET_OPENTEMPORARYTABLE** .</span><span class="sxs-lookup"><span data-stu-id="e0cca-106">The **JET_OPENTEMPORARYTABLE** structure contains an easily extensible collection of parameters for the **JET_OPENTEMPORARYTABLE** function.</span></span> <span data-ttu-id="e0cca-107">Cette structure est l’équivalent de la table temporaire de la structure [JET_TABLECREATE](./jet-tablecreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="e0cca-107">This structure is the temporary table equivalent of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure.</span></span>

<span data-ttu-id="e0cca-108">**Windows Vista :** La structure **JET_OPENTEMPORARYTABLE** est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0cca-108">**Windows Vista:** The **JET_OPENTEMPORARYTABLE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a><span data-ttu-id="e0cca-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e0cca-109">Members</span></span>

<span data-ttu-id="e0cca-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="e0cca-110">**cbStruct**</span></span>

<span data-ttu-id="e0cca-111">Taille de cette structure en octets (pour une extension future).</span><span class="sxs-lookup"><span data-stu-id="e0cca-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="e0cca-112">Elle doit être définie sur sizeof (JET_TABLECREATE) en octets.</span><span class="sxs-lookup"><span data-stu-id="e0cca-112">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="e0cca-113">**prgcolumndef**</span><span class="sxs-lookup"><span data-stu-id="e0cca-113">**prgcolumndef**</span></span>

<span data-ttu-id="e0cca-114">Définitions de colonne pour les colonnes créées dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="e0cca-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="e0cca-115">Il existe des limitations **importantes** pour les options de définition de colonne utilisées avec une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="e0cca-115">**Important** limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="e0cca-116">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="e0cca-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="e0cca-117">Outre les options de définition de colonne habituelles, aucune ou plusieurs des options suivantes peuvent également être spécifiées qui ne sont pertinentes que dans le contexte d’une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="e0cca-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0cca-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0cca-118">Value</span></span></p></th>
<th><p><span data-ttu-id="e0cca-119">Signification</span><span class="sxs-lookup"><span data-stu-id="e0cca-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0cca-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="e0cca-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="e0cca-121">L’ordre de tri de la colonne clé pour la table temporaire doit être décroissant plutôt que croissant.</span><span class="sxs-lookup"><span data-stu-id="e0cca-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="e0cca-122">Si cette option est spécifiée sans JET_bitColumnTTKey, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="e0cca-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0cca-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="e0cca-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="e0cca-124">La colonne est une colonne clé pour la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="e0cca-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="e0cca-125">L’ordre des définitions de colonne avec cette option spécifiée dans le tableau d’entrée détermine la précédence de chaque colonne clé pour la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="e0cca-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="e0cca-126">La première définition de colonne dans le tableau qui a cette option est définie sur la colonne clé la plus significative, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e0cca-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="e0cca-127">Si le moteur de base de données demande plus de colonnes clés que ce qui peut être pris en charge par le moteur de base de données, cette option est ignorée pour les colonnes clés non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e0cca-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e0cca-128">**ccolumn**</span><span class="sxs-lookup"><span data-stu-id="e0cca-128">**ccolumn**</span></span>

<span data-ttu-id="e0cca-129">Consultez *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="e0cca-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="e0cca-130">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="e0cca-130">**pidxunicode**</span></span>

<span data-ttu-id="e0cca-131">Indicateurs de normalisation et d’ID de paramètres régionaux à utiliser pour comparer des données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="e0cca-131">The locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="e0cca-132">Lorsque ce paramètre n’est pas présent et que le paramètre *LCID* n’est pas présent, le LCID par défaut est utilisé pour comparer les colonnes clés Unicode de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="e0cca-132">When this parameter is not present and when the *lcid* parameter is not present, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="e0cca-133">Le LCID par défaut est le paramètre régional anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="e0cca-133">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="e0cca-134">Lorsque ce paramètre n’est pas présent, les indicateurs de normalisation par défaut sont utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="e0cca-134">When this parameter is not present, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="e0cca-135">Les indicateurs de normalisation par défaut sont les suivants : NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="e0cca-135">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="e0cca-136">**grbit**</span><span class="sxs-lookup"><span data-stu-id="e0cca-136">**grbit**</span></span>

<span data-ttu-id="e0cca-137">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="e0cca-137">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0cca-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0cca-138">Value</span></span></p></th>
<th><p><span data-ttu-id="e0cca-139">Signification</span><span class="sxs-lookup"><span data-stu-id="e0cca-139">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0cca-140">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="e0cca-140">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="e0cca-141">Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’utilisation de <a href="gg294103(v=exchg.10).md">JetSeek</a> pour rechercher des enregistrements par clé d’index.</span><span class="sxs-lookup"><span data-stu-id="e0cca-141">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="e0cca-142">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="e0cca-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="e0cca-143">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="e0cca-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0cca-144">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="e0cca-144">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="e0cca-145">Demande que les enregistrements avec des clés d’index dupliquées soient supprimés du jeu final d’enregistrements dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="e0cca-145">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="e0cca-146">Avant Windows Server 2003, le moteur de base de données supposait toujours que cette option était appliquée en raison du fait que tous les index cluster doivent également être une clé primaire et doivent donc être uniques.</span><span class="sxs-lookup"><span data-stu-id="e0cca-146">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="e0cca-147">À compter de Windows Server 2003, il est désormais possible de créer une table temporaire qui ne supprime pas les doublons lorsque l’option JET_bitTTForwardOnly est également spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e0cca-147">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="e0cca-148">Il n’est pas possible de savoir quel doublon va être effectué et quels doublons seront ignorés, en général.</span><span class="sxs-lookup"><span data-stu-id="e0cca-148">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="e0cca-149">Toutefois, lorsque l’option JET_bitTTErrorOnDuplicateInsertion est demandée, le premier enregistrement avec une clé d’index donnée à insérer dans la table temporaire sera toujours correctement effectué.</span><span class="sxs-lookup"><span data-stu-id="e0cca-149">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0cca-150">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="e0cca-150">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="e0cca-151">Demande que la table temporaire soit suffisamment flexible pour permettre la modification ultérieure des enregistrements qui ont été insérés précédemment.</span><span class="sxs-lookup"><span data-stu-id="e0cca-151">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="e0cca-152">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="e0cca-152">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="e0cca-153">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="e0cca-153">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0cca-154">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="e0cca-154">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="e0cca-155">Demande que la table temporaire soit suffisamment flexible pour permettre l’analyse des enregistrements dans un ordre et une direction arbitraires à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="e0cca-155">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="e0cca-156">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="e0cca-156">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="e0cca-157">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="e0cca-157">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0cca-158">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="e0cca-158">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="e0cca-159">Demande que les valeurs de colonne clé <strong>null</strong> soient plus proches de la fin de l’index que les valeurs de colonne clé non null.</span><span class="sxs-lookup"><span data-stu-id="e0cca-159">Requests that <strong>NULL</strong> key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0cca-160">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="e0cca-160">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="e0cca-161">Force le gestionnaire de tables temporaires à abandonner la recherche de la meilleure stratégie pour utiliser la gestion de la table temporaire qui entraîne des performances améliorées.</span><span class="sxs-lookup"><span data-stu-id="e0cca-161">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0cca-162">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="e0cca-162">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="e0cca-163">Toute tentative d’insertion d’un enregistrement avec la même clé d’index qu’un enregistrement précédemment inséré échouera immédiatement avec JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="e0cca-163">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="e0cca-164">Si cette option n’est pas demandée, un doublon est détecté immédiatement et échoue, ou est supprimé en mode silencieux ultérieurement, en fonction de la stratégie choisie par le moteur de base de données pour implémenter la table temporaire, en fonction de la fonctionnalité demandée.</span><span class="sxs-lookup"><span data-stu-id="e0cca-164">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="e0cca-165">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="e0cca-165">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="e0cca-166">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="e0cca-166">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0cca-167">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="e0cca-167">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="e0cca-168">La table temporaire est créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation qui est optimisée pour les résultats de requête intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="e0cca-168">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="e0cca-169">Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="e0cca-169">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="e0cca-170">L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées.</span><span class="sxs-lookup"><span data-stu-id="e0cca-170">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="e0cca-171">Pour plus d’informations, consultez JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="e0cca-171">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="e0cca-172"><strong>Windows Server 2003 :  </strong> Cette option est disponible uniquement sur Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e0cca-172"><strong>Windows Server 2003:  </strong>This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e0cca-173">**prgcolumnid**</span><span class="sxs-lookup"><span data-stu-id="e0cca-173">**prgcolumnid**</span></span>

<span data-ttu-id="e0cca-174">Mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés au cours de la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="e0cca-174">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="e0cca-175">Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="e0cca-175">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="e0cca-176">Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e0cca-176">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

<span data-ttu-id="e0cca-177">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="e0cca-177">**cbKeyMost**</span></span>

<span data-ttu-id="e0cca-178">Taille maximale d’une clé représentant une ligne donnée.</span><span class="sxs-lookup"><span data-stu-id="e0cca-178">The maximum size for a key representing a given row.</span></span>

<span data-ttu-id="e0cca-179">La taille de clé maximale peut être définie pour contrôler la façon dont les clés sont tronquées.</span><span class="sxs-lookup"><span data-stu-id="e0cca-179">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="e0cca-180">La troncation de clé est importante, car elle peut affecter le moment où les lignes sont considérées comme distinctes.</span><span class="sxs-lookup"><span data-stu-id="e0cca-180">Key truncation is important because it can affect when rows are considered to be distinct.</span></span>

<span data-ttu-id="e0cca-181">Si ce paramètre a la valeur 0 ou JET_cbKeyMostMin (255), la taille maximale de la clé et sa sémantique restent identiques à la taille de clé maximale prise en charge par Windows Server 2003 et les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="e0cca-181">If this parameter is set to 0 or JET_cbKeyMostMin (255) then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003 and previous releases.</span></span> <span data-ttu-id="e0cca-182">Ce paramètre peut également être défini sur une valeur supérieure en fonction de la taille de page de la base de données de l’instance (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="e0cca-182">This parameter may also be set to a larger value as a function of the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="e0cca-183">Pour plus d’informations, consultez JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="e0cca-183">See JET_paramKeyMost for more information.</span></span>

<span data-ttu-id="e0cca-184">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="e0cca-184">**cbVarSegMac**</span></span>

<span data-ttu-id="e0cca-185">Quantité maximale de données qui seront utilisées à partir d’une colonne de longueur variable pour construire une clé pour une ligne donnée.</span><span class="sxs-lookup"><span data-stu-id="e0cca-185">The maximum amount of data that will be used from any variable length column to construct a key for a given row.</span></span>

<span data-ttu-id="e0cca-186">Ce paramètre peut être utilisé pour contrôler la quantité d’espace clé consommée par une colonne clé donnée.</span><span class="sxs-lookup"><span data-stu-id="e0cca-186">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="e0cca-187">Cette limite est en octets.</span><span class="sxs-lookup"><span data-stu-id="e0cca-187">This limit is in bytes.</span></span> <span data-ttu-id="e0cca-188">Si ce paramètre est égal à zéro ou est identique au paramètre *cbKeyMost* , aucune limite n’est appliquée.</span><span class="sxs-lookup"><span data-stu-id="e0cca-188">If this parameter is zero or is the same as the *cbKeyMost* parameter then no limit is in effect.</span></span>

<span data-ttu-id="e0cca-189">**TableID**</span><span class="sxs-lookup"><span data-stu-id="e0cca-189">**tableid**</span></span>

<span data-ttu-id="e0cca-190">Descripteur de table pour la table temporaire créée à la suite d’un appel réussi à [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="e0cca-190">The table handle for the temporary table created as a result of a successful call to [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="e0cca-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0cca-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0cca-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e0cca-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e0cca-193">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0cca-193">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0cca-194"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="e0cca-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e0cca-195">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e0cca-195">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0cca-196"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="e0cca-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e0cca-197">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="e0cca-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e0cca-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0cca-198">See Also</span></span>

[<span data-ttu-id="e0cca-199">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="e0cca-199">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="e0cca-200">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="e0cca-200">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="e0cca-201">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="e0cca-201">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="e0cca-202">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e0cca-202">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e0cca-203">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e0cca-203">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="e0cca-204">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e0cca-204">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e0cca-205">JetOpenTemporaryTable</span><span class="sxs-lookup"><span data-stu-id="e0cca-205">JetOpenTemporaryTable</span></span>](./jetopentemporarytable-function.md)  
[<span data-ttu-id="e0cca-206">Paramètres système du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="e0cca-206">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

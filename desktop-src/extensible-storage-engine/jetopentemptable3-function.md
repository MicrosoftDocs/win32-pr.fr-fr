---
description: 'En savoir plus sur : fonction JetOpenTempTable3'
title: Fonction JetOpenTempTable3
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7820f90ef0192c1f700759835bf1572b187cf3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514570"
---
# <a name="jetopentemptable3-function"></a><span data-ttu-id="1475e-103">Fonction JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="1475e-103">JetOpenTempTable3 Function</span></span>


<span data-ttu-id="1475e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="1475e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable3-function"></a><span data-ttu-id="1475e-105">Fonction JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="1475e-105">JetOpenTempTable3 Function</span></span>

<span data-ttu-id="1475e-106">La fonction **JetOpenTempTable3** crée une table temporaire avec un index unique qui peut être utilisé pour stocker et récupérer des enregistrements comme une table ordinaire créée à l’aide de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="1475e-106">The **JetOpenTempTable3** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="1475e-107">Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile.</span><span class="sxs-lookup"><span data-stu-id="1475e-107">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="1475e-108">Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.</span><span class="sxs-lookup"><span data-stu-id="1475e-108">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="1475e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1475e-109">Parameters</span></span>

<span data-ttu-id="1475e-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1475e-110">*sesid*</span></span>

<span data-ttu-id="1475e-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="1475e-111">The session to use for this call.</span></span>

<span data-ttu-id="1475e-112">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="1475e-112">*prgcolumndef*</span></span>

<span data-ttu-id="1475e-113">Identifie les définitions de colonne des colonnes à créer dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-113">Identifies the column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="1475e-114">Il existe des limitations importantes pour les options de définition de colonne qui peuvent être utilisées avec une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-114">Important limitations exist to the column definition options that may be used with a temporary table.</span></span> <span data-ttu-id="1475e-115">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1475e-115">See the Remarks section for more information.</span></span>

<span data-ttu-id="1475e-116">Outre les options de définition de colonne habituelles, aucune ou plusieurs des options suivantes peuvent également être spécifiées qui ne sont pertinentes que dans le contexte d’une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-116">In addition to the usual column definition options, zero or more of the following options may also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1475e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1475e-117">Value</span></span></p></th>
<th><p><span data-ttu-id="1475e-118">Signification</span><span class="sxs-lookup"><span data-stu-id="1475e-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1475e-119">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="1475e-119">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="1475e-120">Cette option indique que l’ordre de tri de la colonne clé pour la table temporaire doit être décroissant plutôt que croissant.</span><span class="sxs-lookup"><span data-stu-id="1475e-120">This option indicates that the sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="1475e-121">Si cette option est spécifiée sans JET_bitColumnTTKey, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="1475e-121">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-122">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="1475e-122">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="1475e-123">Cette option indique que la colonne sera une colonne clé pour la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-123">This option indicates that the column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="1475e-124">L’ordre des définitions de colonne avec cette option spécifiée dans le tableau d’entrée détermine la précédence de chaque colonne clé pour la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-124">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="1475e-125">La première définition de colonne dans le tableau avec cette option est définie sur la colonne clé la plus significative, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="1475e-125">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="1475e-126">Si le moteur de base de données demande plus de colonnes clés que ce qui peut être pris en charge par le moteur de base de données, cette option est ignorée pour les colonnes clés non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1475e-126">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1475e-127">*ccolumn*</span><span class="sxs-lookup"><span data-stu-id="1475e-127">*ccolumn*</span></span>

<span data-ttu-id="1475e-128">Consultez *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="1475e-128">See *prgcolumndef*.</span></span>

<span data-ttu-id="1475e-129">*pidxunicode*</span><span class="sxs-lookup"><span data-stu-id="1475e-129">*pidxunicode*</span></span>

<span data-ttu-id="1475e-130">ID de paramètres régionaux et indicateurs de normalisation qui seront utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-130">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="1475e-131">Lorsque ce paramètre n’est pas présent, le LCID par défaut est utilisé pour comparer les colonnes clés Unicode de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-131">When this parameter is not present then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="1475e-132">Le LCID par défaut est le paramètre régional anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="1475e-132">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="1475e-133">Lorsque ce paramètre n’est pas présent, les indicateurs de normalisation par défaut sont utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-133">When this parameter is not present then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="1475e-134">Les indicateurs de normalisation par défaut sont les suivants : NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="1475e-134">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="1475e-135">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1475e-135">*grbit*</span></span>

<span data-ttu-id="1475e-136">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="1475e-136">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1475e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="1475e-137">Value</span></span></p></th>
<th><p><span data-ttu-id="1475e-138">Signification</span><span class="sxs-lookup"><span data-stu-id="1475e-138">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1475e-139">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="1475e-139">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="1475e-140">Cette option demande que toute tentative d’insertion d’un enregistrement avec la même clé d’index qu’un enregistrement précédemment inséré échoue avec JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="1475e-140">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="1475e-141">Si cette option n’est pas demandée, un doublon peut être détecté immédiatement et échouer ou peut être supprimé en mode silencieux ultérieurement selon la stratégie choisie par le moteur de base de données pour implémenter la table temporaire en fonction de la fonctionnalité demandée.</span><span class="sxs-lookup"><span data-stu-id="1475e-141">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="1475e-142">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="1475e-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="1475e-143">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="1475e-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-144">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="1475e-144">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="1475e-145">Cette option force le gestionnaire de tables temporaires à abandonner toute tentative de choix d’une stratégie astucieuse pour la gestion de la table temporaire qui entraîne des performances améliorées.</span><span class="sxs-lookup"><span data-stu-id="1475e-145">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-146">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="1475e-146">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="1475e-147">Cette option demande que la table temporaire soit créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation optimisée pour les résultats de requête intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="1475e-147">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="1475e-148">Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="1475e-148">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="1475e-149">L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées.</span><span class="sxs-lookup"><span data-stu-id="1475e-149">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="1475e-150">Pour plus d’informations, consultez JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="1475e-150">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="1475e-151">Cette option est disponible uniquement sur Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1475e-151">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-152">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="1475e-152">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="1475e-153">Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’utilisation de <a href="gg294103(v=exchg.10).md">JetSeek</a> pour rechercher des enregistrements par clé d’index.</span><span class="sxs-lookup"><span data-stu-id="1475e-153">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="1475e-154">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="1475e-154">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="1475e-155">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="1475e-155">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-156">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="1475e-156">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="1475e-157">Cette option demande que les enregistrements avec des clés d’index dupliquées soient supprimés du jeu final d’enregistrements dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-157">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="1475e-158">Avant Windows Server 2003, le moteur de base de données supposait toujours que cette option était appliquée en raison du fait que tous les index cluster doivent également être une clé primaire et doivent donc être uniques.</span><span class="sxs-lookup"><span data-stu-id="1475e-158">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="1475e-159">À compter de Windows Server 2003, il est désormais possible de créer une table temporaire qui ne supprime pas les doublons lorsque l’option JET_bitTTForwardOnly est également spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1475e-159">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="1475e-160">Il n’est pas possible de savoir quels doublons seront remportés et quels doublons seront ignorés en général.</span><span class="sxs-lookup"><span data-stu-id="1475e-160">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="1475e-161">Toutefois, lorsque l’option JET_bitTTErrorOnDuplicateInsertion est demandée, alors le premier enregistrement avec une clé d’index donnée à insérer dans la table temporaire est toujours gagnant.</span><span class="sxs-lookup"><span data-stu-id="1475e-161">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-162">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="1475e-162">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="1475e-163">Cette option demande que la table temporaire soit suffisamment flexible pour permettre la modification ultérieure des enregistrements qui ont été insérés précédemment.</span><span class="sxs-lookup"><span data-stu-id="1475e-163">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="1475e-164">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="1475e-164">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="1475e-165">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="1475e-165">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-166">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="1475e-166">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="1475e-167">Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’analyse des enregistrements dans un ordre et une direction arbitraires à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="1475e-167">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="1475e-168">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="1475e-168">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="1475e-169">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="1475e-169">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-170">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="1475e-170">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="1475e-171">Cette option demande que les valeurs de colonne clé NULL soient triées plus près de la fin de l’index que les valeurs de colonne clé non NULL.</span><span class="sxs-lookup"><span data-stu-id="1475e-171">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-172">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="1475e-172">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="1475e-173">Demande d’autoriser uniquement les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="1475e-173">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="1475e-174"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1475e-174"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1475e-175">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="1475e-175">*ptableid*</span></span>

<span data-ttu-id="1475e-176">Mémoire tampon de sortie qui recevra le nouveau curseur ouvert sur la table temporaire nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="1475e-176">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="1475e-177">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="1475e-177">*prgcolumnid*</span></span>

<span data-ttu-id="1475e-178">Mémoire tampon de sortie qui recevra le tableau d’ID de colonne générés au cours de la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-178">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="1475e-179">Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="1475e-179">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="1475e-180">Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1475e-180">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="1475e-181">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1475e-181">Return Value</span></span>

<span data-ttu-id="1475e-182">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="1475e-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1475e-183">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1475e-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1475e-184">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1475e-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="1475e-185">Description</span><span class="sxs-lookup"><span data-stu-id="1475e-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1475e-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1475e-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1475e-187">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="1475e-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-188">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="1475e-188">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="1475e-189"><strong>JetOpenTempTable3</strong> a échoué parce que JET_bitTTForwardOnly a été spécifié et que la table temporaire spécifiée n’a pas pu être créée à l’aide de l’optimisation avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="1475e-189"><strong>JetOpenTempTable3</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="1475e-190">Cette erreur est renvoyée uniquement par Windows Server 2003 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1475e-190">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1475e-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1475e-192">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="1475e-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-193">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="1475e-193">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="1475e-194">Impossible de créer l’index, car une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1475e-194">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="1475e-195"><strong>JetOpenTempTable3</strong> renvoie cette erreur dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="1475e-195"><strong>JetOpenTempTable3</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="1475e-196">Les paramètres régionaux de langue neutre sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1475e-196">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="1475e-197">Un ensemble non valide d’indicateurs de normalisation est spécifié.</span><span class="sxs-lookup"><span data-stu-id="1475e-197">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="1475e-198">Cette erreur est renvoyée uniquement par Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1475e-198">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-199">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1475e-199">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1475e-200">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="1475e-200">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="1475e-201">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1475e-201">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-202">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="1475e-202">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="1475e-203">Le membre <strong>CP</strong> de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur une page de codes valide.</span><span class="sxs-lookup"><span data-stu-id="1475e-203">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="1475e-204">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="1475e-204">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="1475e-205">La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="1475e-205">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-206">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="1475e-206">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="1475e-207">Le membre <strong>coltyp</strong> de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur un type de colonne valide.</span><span class="sxs-lookup"><span data-stu-id="1475e-207">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-208">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="1475e-208">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="1475e-209">Impossible de créer l’index, car une tentative d’utilisation d’un ID de paramètres régionaux non valide a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="1475e-209">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="1475e-210">L’ID de paramètres régionaux peut être entièrement non valide ou le module linguistique associé n’est peut-être pas installé.</span><span class="sxs-lookup"><span data-stu-id="1475e-210">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-211">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="1475e-211">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="1475e-212">Impossible de créer l’index, car une tentative d’utilisation d’un ensemble non valide d’indicateurs de normalisation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="1475e-212">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="1475e-213">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1475e-213">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="1475e-214">Sur Windows 2000, les indicateurs de normalisation non valides génèrent JET_errIndexInvalidDef à la place.</span><span class="sxs-lookup"><span data-stu-id="1475e-214">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-215">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="1475e-215">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="1475e-216">Le descripteur de session n’est pas valide ou fait référence à une session fermée.</span><span class="sxs-lookup"><span data-stu-id="1475e-216">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="1475e-217">Cette erreur n’est pas retournée dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="1475e-217">This error is not returned under all circumstances.</span></span> <span data-ttu-id="1475e-218">Les handles ne sont validés qu’à titre d’effort optimal.</span><span class="sxs-lookup"><span data-stu-id="1475e-218">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-219">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1475e-219">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1475e-220">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="1475e-220">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-221">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="1475e-221">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="1475e-222">L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour ouvrir un nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="1475e-222">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="1475e-223">Les ressources de curseur sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="1475e-223">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-224">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1475e-224">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="1475e-225">L’opération a échoué, car la mémoire peut être allouée pour être terminée.</span><span class="sxs-lookup"><span data-stu-id="1475e-225">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="1475e-226"><strong>JetOpenTempTable3</strong> peut retourner JET_errOutOfMemory si l’espace d’adressage du processus hôte est trop fragmenté.</span><span class="sxs-lookup"><span data-stu-id="1475e-226"><strong>JetOpenTempTable3</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="1475e-227">Le gestionnaire de tables temporaire allouera toujours un segment d’espace d’adressage de 1 Mo pour chaque table temporaire créée, quelle que soit la quantité de données à stocker.</span><span class="sxs-lookup"><span data-stu-id="1475e-227">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1475e-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1475e-229">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="1475e-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1475e-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1475e-231">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="1475e-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="1475e-232">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1475e-232">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1475e-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1475e-234">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="1475e-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-235">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="1475e-235">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="1475e-236">Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="1475e-236">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="1475e-237">Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</span><span class="sxs-lookup"><span data-stu-id="1475e-237">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-238">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="1475e-238">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="1475e-239">L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache les index de la table.</span><span class="sxs-lookup"><span data-stu-id="1475e-239">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="1475e-240">Le nombre d’index dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="1475e-240">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-241">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="1475e-241">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="1475e-242">L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache le schéma de la table.</span><span class="sxs-lookup"><span data-stu-id="1475e-242">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="1475e-243">Le nombre de tables dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="1475e-243">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-244">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="1475e-244">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="1475e-245">L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour créer une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-245">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="1475e-246">Les ressources de table temporaire sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="1475e-246">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1475e-247">En cas de réussite, un curseur ouvert sur la table temporaire nouvellement créée est retourné.</span><span class="sxs-lookup"><span data-stu-id="1475e-247">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="1475e-248">L’état de la base de données temporaire sera préparé à contenir la nouvelle table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1475e-248">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="1475e-249">L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="1475e-249">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="1475e-250">En cas d’échec, la table temporaire n’est pas créée et un curseur n’est pas renvoyé.</span><span class="sxs-lookup"><span data-stu-id="1475e-250">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="1475e-251">L’état de la base de données temporaire peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="1475e-251">The state of the temporary database may be changed.</span></span> <span data-ttu-id="1475e-252">L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="1475e-252">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1475e-253">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1475e-253">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1475e-254"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1475e-254"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1475e-255">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="1475e-255">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-256"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="1475e-256"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1475e-257">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1475e-257">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-258"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="1475e-258"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1475e-259">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="1475e-259">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1475e-260"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="1475e-260"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1475e-261">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1475e-261">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1475e-262"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1475e-262"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1475e-263">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1475e-263">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1475e-264">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1475e-264">See Also</span></span>

[<span data-ttu-id="1475e-265">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="1475e-265">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="1475e-266">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="1475e-266">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="1475e-267">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="1475e-267">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="1475e-268">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="1475e-268">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="1475e-269">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1475e-269">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1475e-270">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1475e-270">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1475e-271">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1475e-271">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1475e-272">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1475e-272">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1475e-273">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="1475e-273">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="1475e-274">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="1475e-274">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="1475e-275">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="1475e-275">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="1475e-276">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="1475e-276">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="1475e-277">JetMove</span><span class="sxs-lookup"><span data-stu-id="1475e-277">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="1475e-278">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="1475e-278">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="1475e-279">JetRollback</span><span class="sxs-lookup"><span data-stu-id="1475e-279">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="1475e-280">JetSeek</span><span class="sxs-lookup"><span data-stu-id="1475e-280">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="1475e-281">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="1475e-281">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="1475e-282">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="1475e-282">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

---
description: 'En savoir plus sur : fonction JetOpenTempTable2'
title: Fonction JetOpenTempTable2
TOCTitle: JetOpenTempTable2 Function
ms:assetid: 788ec4f9-b0c3-409b-850c-7567dec47024
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269302(v=EXCHG.10)
ms:contentKeyID: 32765594
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 324bcde75c0ba9376c8ad9f5e98df585b1d341e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534019"
---
# <a name="jetopentemptable2-function"></a><span data-ttu-id="36bfa-103">Fonction JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="36bfa-103">JetOpenTempTable2 Function</span></span>


<span data-ttu-id="36bfa-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="36bfa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable2-function"></a><span data-ttu-id="36bfa-105">Fonction JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="36bfa-105">JetOpenTempTable2 Function</span></span>

<span data-ttu-id="36bfa-106">La fonction **JetOpenTempTable2** crée une table temporaire avec un index unique qui peut être utilisé pour stocker et récupérer des enregistrements comme une table ordinaire créée à l’aide de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="36bfa-106">The **JetOpenTempTable2** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="36bfa-107">Cette fonction a également un ID de paramètres régionaux qui peut être utilisé pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-107">This function also has a Locale ID that can be used to compare Unicode key column data in the temporary table.</span></span> <span data-ttu-id="36bfa-108">Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile.</span><span class="sxs-lookup"><span data-stu-id="36bfa-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="36bfa-109">Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.</span><span class="sxs-lookup"><span data-stu-id="36bfa-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable2(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          unsigned long lcid,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="36bfa-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36bfa-110">Parameters</span></span>

<span data-ttu-id="36bfa-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="36bfa-111">*sesid*</span></span>

<span data-ttu-id="36bfa-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="36bfa-112">The session to use.</span></span>

<span data-ttu-id="36bfa-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="36bfa-113">*prgcolumndef*</span></span>

<span data-ttu-id="36bfa-114">Définitions de colonne des colonnes à créer dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-114">The column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="36bfa-115">Il existe des limitations importantes pour les options de définition de colonne utilisées avec une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-115">Important limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="36bfa-116">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="36bfa-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="36bfa-117">Outre les options de définition de colonne habituelles, aucune ou plusieurs des options suivantes peuvent également être spécifiées qui ne sont pertinentes que dans le contexte d’une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36bfa-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="36bfa-118">Value</span></span></p></th>
<th><p><span data-ttu-id="36bfa-119">Signification</span><span class="sxs-lookup"><span data-stu-id="36bfa-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="36bfa-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="36bfa-121">L’ordre de tri de la colonne clé pour la table temporaire doit être décroissant plutôt que croissant.</span><span class="sxs-lookup"><span data-stu-id="36bfa-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="36bfa-122">Si cette option est spécifiée sans JET_bitColumnTTKey, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="36bfa-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="36bfa-124">La colonne est une colonne clé pour la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="36bfa-125">L’ordre des définitions de colonne avec cette option spécifiée dans le tableau d’entrée détermine la précédence de chaque colonne clé pour la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="36bfa-126">La première définition de colonne dans le tableau avec cette option est définie sur la colonne clé la plus significative, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="36bfa-126">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="36bfa-127">Si le moteur de base de données demande plus de colonnes clés que ce qui peut être pris en charge par le moteur de base de données, cette option est ignorée pour les colonnes clés non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="36bfa-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="36bfa-128">*ccolumn*</span><span class="sxs-lookup"><span data-stu-id="36bfa-128">*ccolumn*</span></span>

<span data-ttu-id="36bfa-129">Consultez *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="36bfa-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="36bfa-130">*lcid*</span><span class="sxs-lookup"><span data-stu-id="36bfa-130">*lcid*</span></span>

<span data-ttu-id="36bfa-131">ID de paramètres régionaux à utiliser pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-131">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="36bfa-132">Les paramètres régionaux peuvent être utilisés tant que le module linguistique approprié a été installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36bfa-132">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="36bfa-133">La seule exception est que les paramètres régionaux de langue neutre (LCID de zéro) ne sont pas conformes.</span><span class="sxs-lookup"><span data-stu-id="36bfa-133">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="36bfa-134">Sur Windows Server 2003 et versions ultérieures, si les paramètres régionaux de langue neutre sont spécifiés pour ce paramètre, l’ID de paramètres régionaux par défaut (anglais des États-Unis) sera utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="36bfa-134">On Windows Server 2003 and later, if the Language Neutral locale is specified for this parameter then the default locale ID (U.S. English) will be used instead.</span></span> <span data-ttu-id="36bfa-135">Cela permet d’autoriser une valeur de zéro pour signifier la valeur par défaut plutôt qu’une valeur non conforme.</span><span class="sxs-lookup"><span data-stu-id="36bfa-135">This is to allow a value of zero to signify the default rather than an illegal value.</span></span>

<span data-ttu-id="36bfa-136">Lorsque ce paramètre n’est pas présent et que le paramètre *pidxunicode* n’est pas présent, le LCID par défaut est utilisé pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-136">When this parameter is not present and when the *pidxunicode* parameter is not present, then the default LCID will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="36bfa-137">Le LCID par défaut est le paramètre régional anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="36bfa-137">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="36bfa-138">*grbit*</span><span class="sxs-lookup"><span data-stu-id="36bfa-138">*grbit*</span></span>

<span data-ttu-id="36bfa-139">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="36bfa-139">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36bfa-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="36bfa-140">Value</span></span></p></th>
<th><p><span data-ttu-id="36bfa-141">Signification</span><span class="sxs-lookup"><span data-stu-id="36bfa-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-142">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="36bfa-142">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="36bfa-143">Cette option demande que toute tentative d’insertion d’un enregistrement avec la même clé d’index qu’un enregistrement précédemment inséré échoue avec JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="36bfa-143">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="36bfa-144">Si cette option n’est pas demandée, un doublon peut être détecté immédiatement et échouer ou peut être supprimé en mode silencieux ultérieurement selon la stratégie choisie par le moteur de base de données pour implémenter la table temporaire en fonction de la fonctionnalité demandée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-144">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="36bfa-145">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="36bfa-145">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="36bfa-146">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="36bfa-146">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-147">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="36bfa-147">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="36bfa-148">Cette option force le gestionnaire de tables temporaires à abandonner toute tentative de choix d’une stratégie astucieuse pour la gestion de la table temporaire qui entraîne des performances améliorées.</span><span class="sxs-lookup"><span data-stu-id="36bfa-148">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-149">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="36bfa-149">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="36bfa-150">Cette option demande que la table temporaire soit créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation optimisée pour les résultats de requête intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="36bfa-150">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="36bfa-151">Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="36bfa-151">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="36bfa-152">L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées.</span><span class="sxs-lookup"><span data-stu-id="36bfa-152">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="36bfa-153">Pour plus d’informations, consultez JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="36bfa-153">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="36bfa-154">Cette option est disponible uniquement sur Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="36bfa-154">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-155">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="36bfa-155">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="36bfa-156">Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’utilisation de <a href="gg294103(v=exchg.10).md">JetSeek</a> pour rechercher des enregistrements par clé d’index.</span><span class="sxs-lookup"><span data-stu-id="36bfa-156">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="36bfa-157">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="36bfa-157">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="36bfa-158">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="36bfa-158">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-159">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="36bfa-159">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="36bfa-160">Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’analyse des enregistrements dans un ordre et une direction arbitraires à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="36bfa-160">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="36bfa-161">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="36bfa-161">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="36bfa-162">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="36bfa-162">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-163">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="36bfa-163">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="36bfa-164">Cette option demande que les valeurs de colonne clé NULL soient triées plus près de la fin de l’index que les valeurs de colonne clé non NULL.</span><span class="sxs-lookup"><span data-stu-id="36bfa-164">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-165">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="36bfa-165">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="36bfa-166">Cette option demande que les enregistrements avec des clés d’index dupliquées soient supprimés du jeu final d’enregistrements dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-166">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="36bfa-167">Avant Windows Server 2003, le moteur de base de données supposait toujours que cette option était appliquée en raison du fait que tous les index cluster doivent également être une clé primaire et doivent donc être uniques.</span><span class="sxs-lookup"><span data-stu-id="36bfa-167">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="36bfa-168">À compter de Windows Server 2003, il est désormais possible de créer une table temporaire qui ne supprime pas les doublons lorsque l’option JET_bitTTForwardOnly est également spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-168">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="36bfa-169">Il n’est pas possible de savoir quels doublons seront remportés et quels doublons seront ignorés en général.</span><span class="sxs-lookup"><span data-stu-id="36bfa-169">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="36bfa-170">Toutefois, lorsque l’option JET_bitTTErrorOnDuplicateInsertion est demandée, alors le premier enregistrement avec une clé d’index donnée à insérer dans la table temporaire est toujours gagnant.</span><span class="sxs-lookup"><span data-stu-id="36bfa-170">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-171">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="36bfa-171">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="36bfa-172">Cette option demande que la table temporaire soit suffisamment flexible pour permettre la modification ultérieure des enregistrements qui ont été insérés précédemment.</span><span class="sxs-lookup"><span data-stu-id="36bfa-172">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="36bfa-173">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="36bfa-173">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="36bfa-174">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="36bfa-174">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-175">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="36bfa-175">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="36bfa-176">Demande d’autoriser uniquement les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="36bfa-176">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="36bfa-177"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="36bfa-177"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="36bfa-178">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="36bfa-178">*ptableid*</span></span>

<span data-ttu-id="36bfa-179">Mémoire tampon de sortie qui recevra le nouveau curseur ouvert sur la table temporaire nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-179">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="36bfa-180">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="36bfa-180">*prgcolumnid*</span></span>

<span data-ttu-id="36bfa-181">Mémoire tampon de sortie qui recevra le tableau d’ID de colonne générés au cours de la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-181">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="36bfa-182">Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="36bfa-182">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="36bfa-183">Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-183">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="36bfa-184">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="36bfa-184">Return Value</span></span>

<span data-ttu-id="36bfa-185">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="36bfa-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="36bfa-186">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="36bfa-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36bfa-187">Code de retour</span><span class="sxs-lookup"><span data-stu-id="36bfa-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="36bfa-188">Description</span><span class="sxs-lookup"><span data-stu-id="36bfa-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="36bfa-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="36bfa-190">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="36bfa-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-191">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="36bfa-191">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="36bfa-192"><strong>JetOpenTempTable2</strong> a échoué parce que JET_bitTTForwardOnly a été spécifié et que la table temporaire spécifiée n’a pas pu être créée à l’aide de l’optimisation avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="36bfa-192"><strong>JetOpenTempTable2</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="36bfa-193">Cette erreur est renvoyée uniquement par Windows Server 2003 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="36bfa-193">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-194">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="36bfa-194">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="36bfa-195">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="36bfa-195">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-196">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="36bfa-196">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="36bfa-197">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="36bfa-197">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="36bfa-198">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="36bfa-198">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-199">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="36bfa-199">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="36bfa-200">Le champ CP de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur une page de codes valide.</span><span class="sxs-lookup"><span data-stu-id="36bfa-200">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="36bfa-201">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="36bfa-201">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="36bfa-202">La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="36bfa-202">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-203">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="36bfa-203">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="36bfa-204">Le champ <em>coltyp</em> de l' <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur un type de colonne valide.</span><span class="sxs-lookup"><span data-stu-id="36bfa-204">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-205">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="36bfa-205">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="36bfa-206">Impossible de créer l’index, car une définition d’index non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-206">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="36bfa-207"><strong>JetOpenTempTable2</strong> renvoie cette erreur dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="36bfa-207"><strong>JetOpenTempTable2</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="36bfa-208">Les paramètres régionaux de langue neutre sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="36bfa-208">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="36bfa-209">Un ensemble non valide d’indicateurs de normalisation est spécifié.</span><span class="sxs-lookup"><span data-stu-id="36bfa-209">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="36bfa-210">Cette erreur est renvoyée uniquement par Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="36bfa-210">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-211">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="36bfa-211">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="36bfa-212">Impossible de créer l’index, car une tentative d’utilisation d’un ID de paramètres régionaux non valide a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-212">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="36bfa-213">L’ID de paramètres régionaux peut être entièrement non valide ou le module linguistique associé n’est peut-être pas installé.</span><span class="sxs-lookup"><span data-stu-id="36bfa-213">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-214">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="36bfa-214">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="36bfa-215">Impossible de créer l’index, car une tentative d’utilisation d’un ensemble non valide d’indicateurs de normalisation a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-215">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="36bfa-216">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="36bfa-216">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="36bfa-217">Sur Windows 2000, les indicateurs de normalisation non valides génèrent JET_errIndexInvalidDef à la place.</span><span class="sxs-lookup"><span data-stu-id="36bfa-217">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-218">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="36bfa-218">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="36bfa-219">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-219">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-220">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="36bfa-220">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="36bfa-221">L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour ouvrir un nouveau curseur.</span><span class="sxs-lookup"><span data-stu-id="36bfa-221">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="36bfa-222">Les ressources de curseur sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="36bfa-222">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-223">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="36bfa-223">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="36bfa-224">L’opération a échoué, car la mémoire peut être allouée pour être terminée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-224">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="36bfa-225"><strong>JetOpenTempTable2</strong> peut retourner JET_errOutOfMemory si l’espace d’adressage du processus hôte est trop fragmenté.</span><span class="sxs-lookup"><span data-stu-id="36bfa-225"><strong>JetOpenTempTable2</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="36bfa-226">Le gestionnaire de tables temporaire allouera toujours un segment d’espace d’adressage de 1 Mo pour chaque table temporaire créée, quelle que soit la quantité de données à stocker.</span><span class="sxs-lookup"><span data-stu-id="36bfa-226">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-227">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="36bfa-227">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="36bfa-228">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="36bfa-228">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-229">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="36bfa-229">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="36bfa-230">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="36bfa-230">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="36bfa-231">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="36bfa-231">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-232">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="36bfa-232">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="36bfa-233">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="36bfa-233">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-234">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="36bfa-234">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="36bfa-235">Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="36bfa-235">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="36bfa-236">Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</span><span class="sxs-lookup"><span data-stu-id="36bfa-236">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-237">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="36bfa-237">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="36bfa-238">L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache les index de la table.</span><span class="sxs-lookup"><span data-stu-id="36bfa-238">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="36bfa-239">Le nombre d’index dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="36bfa-239">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-240">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="36bfa-240">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="36bfa-241">L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache le schéma de la table.</span><span class="sxs-lookup"><span data-stu-id="36bfa-241">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="36bfa-242">Le nombre de tables dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="36bfa-242">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-243">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="36bfa-243">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="36bfa-244">L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour créer une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-244">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="36bfa-245">Les ressources de table temporaire sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="36bfa-245">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="36bfa-246">En cas de réussite, un curseur ouvert sur la table temporaire nouvellement créée est retourné.</span><span class="sxs-lookup"><span data-stu-id="36bfa-246">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="36bfa-247">L’état de la base de données temporaire sera préparé à contenir la nouvelle table temporaire.</span><span class="sxs-lookup"><span data-stu-id="36bfa-247">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="36bfa-248">L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="36bfa-248">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="36bfa-249">En cas d’échec, la table temporaire n’est pas créée et un curseur n’est pas renvoyé.</span><span class="sxs-lookup"><span data-stu-id="36bfa-249">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="36bfa-250">L’état de la base de données temporaire peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="36bfa-250">The state of the temporary database may be changed.</span></span> <span data-ttu-id="36bfa-251">L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="36bfa-251">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="36bfa-252">Notes</span><span class="sxs-lookup"><span data-stu-id="36bfa-252">Remarks</span></span>

<span data-ttu-id="36bfa-253">Consultez [JetOpenTempTable](./jetopentemptable-function.md).</span><span class="sxs-lookup"><span data-stu-id="36bfa-253">See [JetOpenTempTable](./jetopentemptable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="36bfa-254">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36bfa-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-255"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="36bfa-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="36bfa-256">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="36bfa-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-257"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="36bfa-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="36bfa-258">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="36bfa-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-259"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="36bfa-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="36bfa-260">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="36bfa-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36bfa-261"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="36bfa-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="36bfa-262">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="36bfa-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36bfa-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="36bfa-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="36bfa-264">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="36bfa-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="36bfa-265">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36bfa-265">See Also</span></span>

[<span data-ttu-id="36bfa-266">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="36bfa-266">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="36bfa-267">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="36bfa-267">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="36bfa-268">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="36bfa-268">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="36bfa-269">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="36bfa-269">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="36bfa-270">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="36bfa-270">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="36bfa-271">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="36bfa-271">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="36bfa-272">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="36bfa-272">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="36bfa-273">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="36bfa-273">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="36bfa-274">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="36bfa-274">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="36bfa-275">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="36bfa-275">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="36bfa-276">JetMove</span><span class="sxs-lookup"><span data-stu-id="36bfa-276">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="36bfa-277">JetRollback</span><span class="sxs-lookup"><span data-stu-id="36bfa-277">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="36bfa-278">JetSeek</span><span class="sxs-lookup"><span data-stu-id="36bfa-278">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="36bfa-279">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="36bfa-279">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="36bfa-280">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="36bfa-280">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

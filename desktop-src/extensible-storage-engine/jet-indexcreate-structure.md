---
description: 'En savoir plus sur : structure JET_INDEXCREATE'
title: Structure JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c465d81dce628497b1b9210fb08b37a3003e2e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757936"
---
# <a name="jet_indexcreate-structure"></a><span data-ttu-id="9246b-103">Structure JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="9246b-103">JET_INDEXCREATE Structure</span></span>


<span data-ttu-id="9246b-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="9246b-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="9246b-105">La structure **JET_INDEXCREATE** contient les informations nécessaires à la création d’un index sur des données dans une base de données ESE (Extensible Storage Engine).</span><span class="sxs-lookup"><span data-stu-id="9246b-105">The **JET_INDEXCREATE** structure contains the information needed to create an index over data in an Extensible Storage Engine (ESE) database.</span></span> <span data-ttu-id="9246b-106">La structure est utilisée par des fonctions telles que [JetCreateIndex2](./jetcreateindex2-function.md)et dans des structures telles que [JET_TABLECREATE](./jet-tablecreate-structure.md) et [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span><span class="sxs-lookup"><span data-stu-id="9246b-106">The structure is used by functions such as [JetCreateIndex2](./jetcreateindex2-function.md), and in structures such as [JET_TABLECREATE](./jet-tablecreate-structure.md) and [JET_TABLECREATE2](./jet-tablecreate2-structure.md).</span></span>

``` c++
typedef struct tagJET_INDEXCREATE {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
  unsigned long cbKeyMost;
} JET_INDEXCREATE;
```

### <a name="members"></a><span data-ttu-id="9246b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9246b-107">Members</span></span>

<span data-ttu-id="9246b-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="9246b-108">**cbStruct**</span></span>

<span data-ttu-id="9246b-109">Taille, en octets, de cette structure.</span><span class="sxs-lookup"><span data-stu-id="9246b-109">The size, in bytes, of this structure.</span></span> <span data-ttu-id="9246b-110">Affectez à ce membre la valeur sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="9246b-110">Set this member to sizeof( JET_INDEXCREATE ).</span></span>

<span data-ttu-id="9246b-111">**szIndexName**</span><span class="sxs-lookup"><span data-stu-id="9246b-111">**szIndexName**</span></span>

<span data-ttu-id="9246b-112">Nom de l’index à créer.</span><span class="sxs-lookup"><span data-stu-id="9246b-112">The name of the index to create.</span></span>

<span data-ttu-id="9246b-113">Le nom de l’index doit respecter les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="9246b-113">The name of the index must meet the following conditions:</span></span>

  - <span data-ttu-id="9246b-114">Elle doit être inférieure à JET_cbNameMost, à l’exclusion de la valeur null de fin.</span><span class="sxs-lookup"><span data-stu-id="9246b-114">It must be less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="9246b-115">Il doit comporter les caractères suivants : 0 (zéro) à 9, A à Z, a à z et toutes les autres signes de ponctuation, à l’exception de « \! »</span><span class="sxs-lookup"><span data-stu-id="9246b-115">It must consist of the following characters: 0 (zero) through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="9246b-116">(point d’exclamation), « , » (virgule), « \[ » (crochet ouvrant) et « \] » (crochet fermant), c’est-à-dire les caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c, 0x5d à 0x7F.</span><span class="sxs-lookup"><span data-stu-id="9246b-116">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="9246b-117">Il ne doit pas commencer par un espace.</span><span class="sxs-lookup"><span data-stu-id="9246b-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="9246b-118">Il doit comporter au moins un caractère autre qu’un espace.</span><span class="sxs-lookup"><span data-stu-id="9246b-118">It must consist of at least one nonspace character.</span></span>

<span data-ttu-id="9246b-119">**szKey**</span><span class="sxs-lookup"><span data-stu-id="9246b-119">**szKey**</span></span>

<span data-ttu-id="9246b-120">Pointeur vers une chaîne se terminant par un caractère null et des jetons délimités par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="9246b-120">A pointer to a double-null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="9246b-121">Chaque jeton se présente sous la forme « \<direction-specifier\> \<column-name\> », où direction-Specification est « + » ou « - ».</span><span class="sxs-lookup"><span data-stu-id="9246b-121">Each token is of the form "\<direction-specifier\>\<column-name\>", where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="9246b-122">Par exemple, un **szKey** de « + ABC \\ 0-Def \\ 0 + GHI \\ 0 » sera indexé sur les trois colonnes « ABC » (dans l’ordre croissant), « def » (dans l’ordre décroissant) et « GHI » (dans l’ordre croissant).</span><span class="sxs-lookup"><span data-stu-id="9246b-122">For example, a **szKey** of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span> <span data-ttu-id="9246b-123">Dans le langage C, les littéraux de chaîne ont un terminateur **null** implicite ; par conséquent, la chaîne ci-dessus se termine par une valeur double NULL.</span><span class="sxs-lookup"><span data-stu-id="9246b-123">In the C language, string literals have an implied **NULL** terminator; therefore, the above string will be terminated by a double-NULL.</span></span>

<span data-ttu-id="9246b-124">Le nombre de colonnes spécifié dans **szKey** ne peut pas dépasser la valeur de **JET_ccolKeyMost** (une constante dépendante de la version).</span><span class="sxs-lookup"><span data-stu-id="9246b-124">The number of columns specified in **szKey** may not exceed the value of **JET_ccolKeyMost** (a version-dependent constant).</span></span>

<span data-ttu-id="9246b-125">Au moins une colonne doit être nommée dans **szKey**.</span><span class="sxs-lookup"><span data-stu-id="9246b-125">At least one column must be named in **szKey**.</span></span>

<span data-ttu-id="9246b-126">Comportement obsolète : après le terminateur double-NULL, il est possible de spécifier un ID de langue (un mot qui est passé dans MAKELCID (langid, SORT_DEFAULT)) pour spécifier le LCID de l’index.</span><span class="sxs-lookup"><span data-stu-id="9246b-126">Obsolete behavior: After the double-NULL terminator, it is possible to specify a language ID (a WORD which gets passed into MAKELCID( langid, SORT_DEFAULT ) ) as a way to specify the LCID for the index.</span></span> <span data-ttu-id="9246b-127">Il n’est pas conforme de spécifier à la fois un ID de langue dans **szKey** et un LCID dans [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (en définissant JET_bitIndexUnicode dans *Grbit*).</span><span class="sxs-lookup"><span data-stu-id="9246b-127">It is illegal to specify both a language ID in **szKey** and an LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (by setting JET_bitIndexUnicode in *grbit*).</span></span>

<span data-ttu-id="9246b-128">Déconseillé : après l’ID de langue, il est possible de passer **cbVarSegMac** comme UShort.</span><span class="sxs-lookup"><span data-stu-id="9246b-128">Deprecated: After the language ID, it is possible to pass **cbVarSegMac** as a USHORT.</span></span> <span data-ttu-id="9246b-129">Le comportement n’est pas défini si le USHORT est défini à la fois dans **szKey** et si **cbVarSegMac** est défini dans la structure.</span><span class="sxs-lookup"><span data-stu-id="9246b-129">The behavior is undefined if the USHORT is set both in **szKey** and if **cbVarSegMac** is set in the structure.</span></span>

<span data-ttu-id="9246b-130">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="9246b-130">**cbKey**</span></span>

<span data-ttu-id="9246b-131">Longueur, en octets, de **szKey** , y compris les deux valeurs null de fin.</span><span class="sxs-lookup"><span data-stu-id="9246b-131">The length, in bytes, of **szKey** including the two terminating nulls.</span></span>

<span data-ttu-id="9246b-132">**grbit**</span><span class="sxs-lookup"><span data-stu-id="9246b-132">**grbit**</span></span>

<span data-ttu-id="9246b-133">Groupe de bits qui comprend zéro, une ou plusieurs des valeurs énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9246b-133">A group of bits that includes zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9246b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="9246b-134">Value</span></span></p></th>
<th><p><span data-ttu-id="9246b-135">Signification</span><span class="sxs-lookup"><span data-stu-id="9246b-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9246b-136">JET_bitIndexUnique</span><span class="sxs-lookup"><span data-stu-id="9246b-136">JET_bitIndexUnique</span></span></p></td>
<td><p><span data-ttu-id="9246b-137">Les entrées d’index en double (clés) ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="9246b-137">Duplicate index entries (keys) are not allowed.</span></span> <span data-ttu-id="9246b-138">Cette méthode est appliquée quand <a href="gg269288(v=exchg.10).md">JetUpdate</a> est appelé, et non lorsque <a href="gg294137(v=exchg.10).md">JetSetColumn</a> est appelé.</span><span class="sxs-lookup"><span data-stu-id="9246b-138">This is enforced when <a href="gg269288(v=exchg.10).md">JetUpdate</a> is called, not when <a href="gg294137(v=exchg.10).md">JetSetColumn</a> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-139">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="9246b-139">JET_bitIndexPrimary</span></span></p></td>
<td><p><span data-ttu-id="9246b-140">L’index est un index principal (cluster).</span><span class="sxs-lookup"><span data-stu-id="9246b-140">The index is a primary (clustered) index.</span></span> <span data-ttu-id="9246b-141">Chaque table doit avoir un seul index primaire.</span><span class="sxs-lookup"><span data-stu-id="9246b-141">Every table must have exactly one primary index.</span></span> <span data-ttu-id="9246b-142">Si aucun index primaire n’est défini explicitement sur une table, le moteur de base de données crée son propre index primaire.</span><span class="sxs-lookup"><span data-stu-id="9246b-142">If no primary index is explicitly defined over a table, the database engine will create its own primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9246b-143">JET_bitIndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="9246b-143">JET_bitIndexDisallowNull</span></span></p></td>
<td><p><span data-ttu-id="9246b-144">Aucune des colonnes sur lesquelles l’index est créé ne peut contenir une valeur <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="9246b-144">None of the columns over which the index is created can contain a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-145">JET_bitIndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="9246b-145">JET_bitIndexIgnoreNull</span></span></p></td>
<td><p><span data-ttu-id="9246b-146">N’ajoutez pas d’entrée d’index pour une ligne si toutes les colonnes indexées ont la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="9246b-146">Do not add an index entry for a row if all of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9246b-147">JET_bitIndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="9246b-147">JET_bitIndexIgnoreAnyNull</span></span></p></td>
<td><p><span data-ttu-id="9246b-148">N’ajoutez pas d’entrée d’index pour une ligne si l’une des colonnes indexées a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="9246b-148">Do not add an index entry for a row if any of the columns being indexed are <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-149">JET_bitIndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="9246b-149">JET_bitIndexIgnoreFirstNull</span></span></p></td>
<td><p><span data-ttu-id="9246b-150">N’ajoutez pas d’entrée d’index pour une ligne si la première colonne indexée a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="9246b-150">Do not add an index entry for a row if the first column being indexed is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9246b-151">JET_bitIndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="9246b-151">JET_bitIndexLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="9246b-152">Les opérations d’index seront journalisées tardivement.</span><span class="sxs-lookup"><span data-stu-id="9246b-152">Index operations will be logged lazily.</span></span></p>
<p><span data-ttu-id="9246b-153">JET_bitIndexLazyFlush n’affecte pas le paresse des mises à jour de données.</span><span class="sxs-lookup"><span data-stu-id="9246b-153">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="9246b-154">Si l’opération d’indexation est interrompue par un arrêt de processus, la récupération logicielle peut toujours être en mesure d’obtenir la base de données à un état cohérent, mais l’index peut ne pas être présent.</span><span class="sxs-lookup"><span data-stu-id="9246b-154">If the indexing operation is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index might not be present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-155">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="9246b-155">JET_bitIndexEmpty</span></span></p></td>
<td><p><span data-ttu-id="9246b-156">N’essayez pas de créer l’index, car toutes les entrées ont la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="9246b-156">Do not attempt to build the index, because all entries would evaluate to <strong>NULL</strong>.</span></span> <span data-ttu-id="9246b-157"><strong>Grbit</strong> doit également spécifier JET_bitIgnoreAnyNull lorsque JET_bitIndexEmpty est passé.</span><span class="sxs-lookup"><span data-stu-id="9246b-157"><strong>grbit</strong> must also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="9246b-158">Il s’agit d’une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="9246b-158">This is a performance enhancement.</span></span> <span data-ttu-id="9246b-159">Par exemple, si une nouvelle colonne est ajoutée à une table, un index est créé sur cette colonne nouvellement ajoutée, et tous les enregistrements de la table sont analysés même s’ils ne sont pas ajoutés à l’index.</span><span class="sxs-lookup"><span data-stu-id="9246b-159">For example, if a new column is added to a table, an index is created over this newly added column, and all the records in the table are scanned even though they are not added to the index.</span></span> <span data-ttu-id="9246b-160">La spécification de JET_bitIndexEmpty ignore l’analyse de la table, ce qui peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="9246b-160">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9246b-161">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="9246b-161">JET_bitIndexUnversioned</span></span></p></td>
<td><p><span data-ttu-id="9246b-162">Rend la création d’index visible pour les autres transactions.</span><span class="sxs-lookup"><span data-stu-id="9246b-162">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="9246b-163">En général, une session dans une transaction ne peut pas voir une opération de création d’index dans une autre session.</span><span class="sxs-lookup"><span data-stu-id="9246b-163">Typically a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="9246b-164">Cet indicateur peut être utile si une autre transaction est susceptible de créer le même index.</span><span class="sxs-lookup"><span data-stu-id="9246b-164">This flag can be useful if another transaction is likely to create the same index.</span></span> <span data-ttu-id="9246b-165">Le second index-Create échoue au lieu de provoquer potentiellement des opérations de base de données inutiles.</span><span class="sxs-lookup"><span data-stu-id="9246b-165">The second index-create will fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="9246b-166">La deuxième transaction peut ne pas être en mesure d’utiliser l’index immédiatement.</span><span class="sxs-lookup"><span data-stu-id="9246b-166">The second transaction might not be able to use the index immediately.</span></span> <span data-ttu-id="9246b-167">L’opération de création d’index doit être terminée pour pouvoir être utilisée.</span><span class="sxs-lookup"><span data-stu-id="9246b-167">The index creation operation has to complete before it is usable.</span></span> <span data-ttu-id="9246b-168">La session ne doit pas être actuellement dans une transaction pour créer un index sans informations de version.</span><span class="sxs-lookup"><span data-stu-id="9246b-168">The session must not currently be in a transaction to create an index without version information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-169">JET_bitIndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="9246b-169">JET_bitIndexSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="9246b-170">Si vous spécifiez cet indicateur, les valeurs <strong>null</strong> sont triées après les données de toutes les colonnes de l’index.</span><span class="sxs-lookup"><span data-stu-id="9246b-170">Specifying this flag causes <strong>NULL</strong> values to be sorted after data for all columns in the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9246b-171">JET_bitIndexUnicode</span><span class="sxs-lookup"><span data-stu-id="9246b-171">JET_bitIndexUnicode</span></span></p></td>
<td><p><span data-ttu-id="9246b-172">La spécification de cet indicateur affecte l’interprétation du champ LCID/pidxunicde Union dans la structure.</span><span class="sxs-lookup"><span data-stu-id="9246b-172">Specifying this flag affects the interpretation of the lcid/pidxunicde union field in the structure.</span></span> <span data-ttu-id="9246b-173">La définition du bit signifie que le champ <strong>pidxunicode</strong> pointe en fait vers une structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> .</span><span class="sxs-lookup"><span data-stu-id="9246b-173">Setting the bit means that the <strong>pidxunicode</strong> field actually points to a <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure.</span></span> <span data-ttu-id="9246b-174">JET_bitIndexUnicode n’est pas nécessaire pour indexer les données Unicode.</span><span class="sxs-lookup"><span data-stu-id="9246b-174">JET_bitIndexUnicode is not required in order to index Unicode data.</span></span> <span data-ttu-id="9246b-175">Elle est utilisée uniquement pour personnaliser la normalisation des données Unicode.</span><span class="sxs-lookup"><span data-stu-id="9246b-175">It is only used to customize the normalization of Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-176">JET_bitIndexTuples</span><span class="sxs-lookup"><span data-stu-id="9246b-176">JET_bitIndexTuples</span></span></p></td>
<td><p><span data-ttu-id="9246b-177">Spécifie que l’index est un index de Tuple.</span><span class="sxs-lookup"><span data-stu-id="9246b-177">Specifies that the index is a tuple index.</span></span> <span data-ttu-id="9246b-178">Pour obtenir une description d’un index de tuple, consultez <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="9246b-178">See <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> for a description of a tuple index.</span></span></p>
<p><span data-ttu-id="9246b-179">JET_bitIndexTuples a été introduite dans le système d’exploitation Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9246b-179">JET_bitIndexTuples was introduced in the Windows XP operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9246b-180">JET_bitIndexTupleLimits</span><span class="sxs-lookup"><span data-stu-id="9246b-180">JET_bitIndexTupleLimits</span></span></p></td>
<td><p><span data-ttu-id="9246b-181">La spécification de cet indicateur affecte l’interprétation du champ <strong>cbVarSegMac/ptuplelimits</strong> Union dans la structure.</span><span class="sxs-lookup"><span data-stu-id="9246b-181">Specifying this flag affects the interpretation of the <strong>cbVarSegMac/ptuplelimits</strong> union field in the structure.</span></span> <span data-ttu-id="9246b-182">Le fait de définir ce bit signifie que le champ <strong>ptuplelimits</strong> pointe vers une structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> pour autoriser les limites d’index de tuple personnalisées (implique JET_bitIndexTuples).</span><span class="sxs-lookup"><span data-stu-id="9246b-182">Setting this bit means that the <strong>ptuplelimits</strong> field actually points to a <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure to allow custom tuple index limits (implies JET_bitIndexTuples).</span></span></p>
<p><span data-ttu-id="9246b-183">JET_bitIndexTupleLimits a été introduite dans le système d’exploitation Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9246b-183">JET_bitIndexTupleLimits was introduced in the Windows Server 2003 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-184">JET_bitIndexCrossProduct 0x00004000</span><span class="sxs-lookup"><span data-stu-id="9246b-184">JET_bitIndexCrossProduct 0x00004000</span></span></p></td>
<td><p><span data-ttu-id="9246b-185">La spécification de cet indicateur pour un index qui a plusieurs colonnes clés qui est une colonne à valeurs multiples entraîne la création d’une entrée d’index pour chaque résultat d’un produit croisé de toutes les valeurs dans ces colonnes clés.</span><span class="sxs-lookup"><span data-stu-id="9246b-185">Specifying this flag for an index that has more than one key column that is a multivalued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="9246b-186">Dans le cas contraire, l’index comporterait une seule entrée pour chaque valeur multivaleur dans la colonne clé la plus significative qui est une colonne à valeurs multiples et chacune de ces entrées d’index utiliserait la première valeur multivaleur de toutes les autres colonnes clés qui sont des colonnes à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="9246b-186">Otherwise, the index would only have one entry for each multivalue in the most significant key column that is a multivalued column and each of those index entries would use the first multivalue from any other key columns that are multivalued columns.</span></span></p>
<p><span data-ttu-id="9246b-187">Par exemple, si vous avez spécifié cet indicateur pour un index sur la colonne a qui a les valeurs &quot; rouge &quot; et &quot; bleu &quot; et sur la colonne B qui a les valeurs &quot; 1 &quot; et &quot; 2, &quot; les entrées d’index suivantes sont créées : &quot; rouge &quot; , &quot; 1 &quot; ; &quot; rouge &quot; , &quot; 2 &quot; ; &quot; bleu &quot; , &quot; 1 &quot; ; &quot; bleu &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9246b-187">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="9246b-188">Dans le cas contraire, les entrées d’index suivantes sont créées : &quot; rouge &quot; , &quot; 1 &quot; ; &quot; bleu &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9246b-188">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></p>
<p><span data-ttu-id="9246b-189">JET_bitIndexCrossProduct a été introduite dans le système d’exploitation Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9246b-189">JET_bitIndexCrossProduct was introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9246b-190">JET_bitIndexKeyMost 0x00008000</span><span class="sxs-lookup"><span data-stu-id="9246b-190">JET_bitIndexKeyMost 0x00008000</span></span></p></td>
<td><p><span data-ttu-id="9246b-191">La spécification de cet indicateur entraîne l’utilisation par l’index de la taille de clé maximale spécifiée dans le champ <strong>cbKeyMost</strong> de la structure.</span><span class="sxs-lookup"><span data-stu-id="9246b-191">Specifying this flag will cause the index to use the maximum key size specified in the <strong>cbKeyMost</strong> field in the structure.</span></span> <span data-ttu-id="9246b-192">Dans le cas contraire, l’index utilise JET_cbKeyMost (255) comme taille de clé maximale.</span><span class="sxs-lookup"><span data-stu-id="9246b-192">Otherwise, the index will use JET_cbKeyMost (255) as its maximum key size.</span></span></p>
<p><span data-ttu-id="9246b-193">JET_bitIndexKeyMost a été introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9246b-193">JET_bitIndexKeyMost was introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-194">JET_bitIndexDisallowTruncation 0x00010000</span><span class="sxs-lookup"><span data-stu-id="9246b-194">JET_bitIndexDisallowTruncation 0x00010000</span></span></p></td>
<td><p><span data-ttu-id="9246b-195">Si vous spécifiez cet indicateur, toute mise à jour de l’index entraînant l’échec d’une clé tronquée avec JET_errKeyTruncated.</span><span class="sxs-lookup"><span data-stu-id="9246b-195">Specifying this flag will cause any update to the index that would result in a truncated key to fail with JET_errKeyTruncated.</span></span> <span data-ttu-id="9246b-196">Dans le cas contraire, les clés sont tronquées en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="9246b-196">Otherwise, keys will be silently truncated.</span></span> <span data-ttu-id="9246b-197">Pour plus d’informations sur la troncation de clé, consultez la fonction <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</span><span class="sxs-lookup"><span data-stu-id="9246b-197">For more information on key truncation, see the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p>
<p><span data-ttu-id="9246b-198"><strong>Windows Vista : JET_bitIndexDisallowTruncation</strong> est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9246b-198"><strong>Windows Vista:  JET_bitIndexDisallowTruncation</strong> is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9246b-199">JET_bitIndexNestedTable 0x00020000</span><span class="sxs-lookup"><span data-stu-id="9246b-199">JET_bitIndexNestedTable 0x00020000</span></span></p></td>
<td><p><span data-ttu-id="9246b-200">La spécification de cet indicateur entraîne la mise à jour de l’index sur plusieurs colonnes à valeurs multiples, mais uniquement avec les valeurs du même <strong>itagSequence</strong>.</span><span class="sxs-lookup"><span data-stu-id="9246b-200">Specifying this flag will cause update the index over multiple multivalued columns but only with values of same <strong>itagSequence</strong>.</span></span></p>
<p><span data-ttu-id="9246b-201">JET_bitIndexNestedTable a été introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9246b-201">JET_bitIndexNestedTable was introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9246b-202">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="9246b-202">**ulDensity**</span></span>

<span data-ttu-id="9246b-203">Densité de pourcentage de l’index initial B +.</span><span class="sxs-lookup"><span data-stu-id="9246b-203">The percentage density of the initial index B+ tree.</span></span> <span data-ttu-id="9246b-204">La spécification d’un nombre inférieur à 100 utilise plus d’espace pour créer initialement l’index, mais permet la croissance future de l’index, évitant ainsi la fragmentation interne.</span><span class="sxs-lookup"><span data-stu-id="9246b-204">Specifying a number less than 100 uses up more space to create the index initially, but allows future growth of the index to be in place, thus avoiding internal fragmentation.</span></span>

<span data-ttu-id="9246b-205">**lcid**</span><span class="sxs-lookup"><span data-stu-id="9246b-205">**lcid**</span></span>

<span data-ttu-id="9246b-206">Identificateur de paramètres régionaux (LCID) à utiliser lors de la normalisation des données lorsque la valeur JET_bitIndexUnicode n’est pas spécifiée dans le paramètre *Grbit* .</span><span class="sxs-lookup"><span data-stu-id="9246b-206">The locale identifier (LCID) to use when normalizing the data when the JET_bitIndexUnicode value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="9246b-207">Le LCID affecte la normalisation si l’index se trouve sur des colonnes Unicode.</span><span class="sxs-lookup"><span data-stu-id="9246b-207">The LCID affects the normalization if the index is over Unicode columns.</span></span>

<span data-ttu-id="9246b-208">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="9246b-208">**pidxunicode**</span></span>

<span data-ttu-id="9246b-209">Pointeur vers une structure [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) si la valeur JET_bitIndexUnicode est spécifiée dans le paramètre *Grbit* .</span><span class="sxs-lookup"><span data-stu-id="9246b-209">A pointer to a [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) structure if the JET_bitIndexUnicode value is specified in the *grbit* parameter.</span></span> <span data-ttu-id="9246b-210">Cela permet à l’utilisateur de spécifier des indicateurs personnalisés qui sont passés à la fonction [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) pendant la normalisation Unicode.</span><span class="sxs-lookup"><span data-stu-id="9246b-210">This allows the user to specify custom flags that get passed to the [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) function during Unicode normalization.</span></span>

<span data-ttu-id="9246b-211">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="9246b-211">**cbVarSegMac**</span></span>

<span data-ttu-id="9246b-212">Longueur maximale, en octets, de chaque colonne à stocker dans l’index lorsque la valeur de JET_bitIndexTupleLimits n’est pas spécifiée dans le paramètre *Grbit* .</span><span class="sxs-lookup"><span data-stu-id="9246b-212">The maximum length, in bytes, of each column to store in the index when the JET_bitIndexTupleLimits value is not specified in the *grbit* parameter.</span></span>

<span data-ttu-id="9246b-213">Si vous spécifiez la valeur 0 (zéro) pour ce champ, cela équivaut à :</span><span class="sxs-lookup"><span data-stu-id="9246b-213">Specifying a value of 0 (zero) for this field is equivalent to:</span></span>

  - <span data-ttu-id="9246b-214">Spécification de JET_cbPrimaryKeyMost pour un index primaire.</span><span class="sxs-lookup"><span data-stu-id="9246b-214">Specifying JET_cbPrimaryKeyMost for a primary index.</span></span>

  - <span data-ttu-id="9246b-215">Spécification de JET_cbSecondaryKeyMost pour un index secondaire.</span><span class="sxs-lookup"><span data-stu-id="9246b-215">Specifying JET_cbSecondaryKeyMost for a secondary index.</span></span>

<span data-ttu-id="9246b-216">**ptuplelimits**</span><span class="sxs-lookup"><span data-stu-id="9246b-216">**ptuplelimits**</span></span>

<span data-ttu-id="9246b-217">Pointeur vers une structure [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) si la valeur JET_bitIndexTupleLimits est spécifiée dans le paramètre *Grbit* .</span><span class="sxs-lookup"><span data-stu-id="9246b-217">A pointer to a [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure if the JET_bitIndexTupleLimits value is specified in the *grbit* parameter.</span></span>

<span data-ttu-id="9246b-218">ptuplelimits a été introduit dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9246b-218">ptuplelimits was introduced in Windows Server 2003.</span></span>

<span data-ttu-id="9246b-219">**rgconditionalcolumn**</span><span class="sxs-lookup"><span data-stu-id="9246b-219">**rgconditionalcolumn**</span></span>

<span data-ttu-id="9246b-220">Paramètre facultatif d’un tableau de structures de [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , qui sont utilisées pour spécifier les colonnes conditionnelles dans l’index.</span><span class="sxs-lookup"><span data-stu-id="9246b-220">An optional parameter to an array of [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) structures, which are used to specify the conditional columns in the index.</span></span>

<span data-ttu-id="9246b-221">**cConditionalColumn**</span><span class="sxs-lookup"><span data-stu-id="9246b-221">**cConditionalColumn**</span></span>

<span data-ttu-id="9246b-222">Nombre de structures dans le tableau **rgconditionalcolumn** .</span><span class="sxs-lookup"><span data-stu-id="9246b-222">The count of structures in the **rgconditionalcolumn** array.</span></span>

<span data-ttu-id="9246b-223">**Raise**</span><span class="sxs-lookup"><span data-stu-id="9246b-223">**err**</span></span>

<span data-ttu-id="9246b-224">Contient le code de retour pour la création de cet index.</span><span class="sxs-lookup"><span data-stu-id="9246b-224">Contains the return code for creating this index.</span></span>

<span data-ttu-id="9246b-225">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="9246b-225">**cbKeyMost**</span></span>

<span data-ttu-id="9246b-226">Spécifie la taille maximale autorisée, en octets, pour les clés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="9246b-226">Specifies the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="9246b-227">Ce paramètre est ignoré si la valeur JET_bitIndexKeyMost n’est pas spécifiée dans le paramètre *Grbit* .</span><span class="sxs-lookup"><span data-stu-id="9246b-227">This parameter is ignored if the JET_bitIndexKeyMost value is not specified in the *grbit* parameter.</span></span> <span data-ttu-id="9246b-228">Si ce paramètre a la valeur zéro et que JET_bitIndexKeyMost est spécifié dans le paramètre *Grbit* , la fonction appelante échoue avec JET_err_InvalidDef.</span><span class="sxs-lookup"><span data-stu-id="9246b-228">If this parameter is set to zero, and JET_bitIndexKeyMost is specified in the *grbit* parameter, the calling function will fail with JET_err_InvalidDef.</span></span>

<span data-ttu-id="9246b-229">La taille de clé maximale prise en charge minimale est JET_cbKeyMostMin (255), qui est la taille de clé maximale héritée.</span><span class="sxs-lookup"><span data-stu-id="9246b-229">The minimum supported maximum key size is JET_cbKeyMostMin (255), which is the legacy maximum key size.</span></span>

<span data-ttu-id="9246b-230">La taille de clé maximale dépend de la taille de page de la base de données (JET_paramDatabasePageSize), comme suit :</span><span class="sxs-lookup"><span data-stu-id="9246b-230">The maximum key size is dependent on the database page size (JET_paramDatabasePageSize), as follows:</span></span>

  - <span data-ttu-id="9246b-231">Si JET_paramDatabasePageSize = 2048, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)</span><span class="sxs-lookup"><span data-stu-id="9246b-231">If JET_paramDatabasePageSize = 2048 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost2KBytePage (500)</span></span>

  - <span data-ttu-id="9246b-232">Si JET_paramDatabasePageSize = 4096, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)</span><span class="sxs-lookup"><span data-stu-id="9246b-232">If JET_paramDatabasePageSize = 4096 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost4KBytePage (1000)</span></span>

  - <span data-ttu-id="9246b-233">Si JET_paramDatabasePageSize = 8192, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)</span><span class="sxs-lookup"><span data-stu-id="9246b-233">If JET_paramDatabasePageSize = 8192 then JET_cbKeyMostMin (255) \<= **cbKeyMost** \<= JET_cbKeyMost8KBytePage (2000)</span></span>

<span data-ttu-id="9246b-234">La taille de clé maximale prise en charge pour l’instance peut également être lue à partir du paramètre système JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="9246b-234">The maximum supported key size for the instance can also be read from the JET_paramKeyMost system parameter.</span></span>

<span data-ttu-id="9246b-235">**cbKeyMost** a été introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9246b-235">**cbKeyMost** was introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="9246b-236">Notes</span><span class="sxs-lookup"><span data-stu-id="9246b-236">Remarks</span></span>

<span data-ttu-id="9246b-237">Le moteur ESE prend en charge l’indexation sur des colonnes clés contenant plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="9246b-237">ESE supports indexing over key columns containing multiple values.</span></span> <span data-ttu-id="9246b-238">Pour utiliser cette fonctionnalité, la colonne doit être un type de colonne avec balises (JET_bitColumnTagged), et elle doit être marquée pour que ses multiples valeurs soient indexées avec JET_bitColumnMultiValued.</span><span class="sxs-lookup"><span data-stu-id="9246b-238">To use this feature, the column must be a tagged column type (JET_bitColumnTagged), and it must be flagged to have its multiple values indexed with JET_bitColumnMultiValued.</span></span> <span data-ttu-id="9246b-239">Dans les versions de Windows antérieures à Windows Vista, seule la première colonne clé à valeurs multiples de l’index aura ses valeurs développées dans l’index.</span><span class="sxs-lookup"><span data-stu-id="9246b-239">In versions of Windows earlier than Windows Vista, only the first multivalued key column in the index will have its values expanded in the index.</span></span> <span data-ttu-id="9246b-240">Toutes les autres colonnes à valeurs multiples et balises auront uniquement leurs premières valeurs développées dans l’index.</span><span class="sxs-lookup"><span data-stu-id="9246b-240">All other multivalued and tagged columns will only have their first values expanded in the index.</span></span>

<span data-ttu-id="9246b-241">En supposant que les lignes suivantes existent dans une table (la colonne alpha n’est pas à valeurs multiples, tandis que les colonnes Beta, gamma et Delta sont à valeurs multiples) et qu’un index est créé en tant que « + alpha \\ 0 + bêta \\ 0 + gamma \\ 0 + Delta \\ 0 \\ 0 » :</span><span class="sxs-lookup"><span data-stu-id="9246b-241">Assuming the following rows exist in a table (column Alpha is not multivalued, while columns Beta, Gamma, and Delta are multivalued), and an index is created as "+Alpha\\0+Beta\\0+Gamma\\0+Delta\\0\\0":</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9246b-242">Alpha</span><span class="sxs-lookup"><span data-stu-id="9246b-242">Alpha</span></span></p></th>
<th><p><span data-ttu-id="9246b-243">Bêta</span><span class="sxs-lookup"><span data-stu-id="9246b-243">Beta</span></span></p></th>
<th><p><span data-ttu-id="9246b-244">Gamma</span><span class="sxs-lookup"><span data-stu-id="9246b-244">Gamma</span></span></p></th>
<th><p><span data-ttu-id="9246b-245">Delta</span><span class="sxs-lookup"><span data-stu-id="9246b-245">Delta</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9246b-246">1</span><span class="sxs-lookup"><span data-stu-id="9246b-246">1</span></span></p></td>
<td><p><span data-ttu-id="9246b-247">ABC</span><span class="sxs-lookup"><span data-stu-id="9246b-247">ABC</span></span><br />
<span data-ttu-id="9246b-248">GHI</span><span class="sxs-lookup"><span data-stu-id="9246b-248">GHI</span></span><br />
<span data-ttu-id="9246b-249">JKL</span><span class="sxs-lookup"><span data-stu-id="9246b-249">JKL</span></span></p></td>
<td><p><span data-ttu-id="9246b-250">MNO</span><span class="sxs-lookup"><span data-stu-id="9246b-250">MNO</span></span><br />
<span data-ttu-id="9246b-251">PQR</span><span class="sxs-lookup"><span data-stu-id="9246b-251">PQR</span></span><br />
<span data-ttu-id="9246b-252">TT2</span><span class="sxs-lookup"><span data-stu-id="9246b-252">STU</span></span></p></td>
<td><p><span data-ttu-id="9246b-253">VWX</span><span class="sxs-lookup"><span data-stu-id="9246b-253">VWX</span></span><br />
<span data-ttu-id="9246b-254">YZ</span><span class="sxs-lookup"><span data-stu-id="9246b-254">YZ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-255">2</span><span class="sxs-lookup"><span data-stu-id="9246b-255">2</span></span></p></td>
<td><p><span data-ttu-id="9246b-256">LA</span><span class="sxs-lookup"><span data-stu-id="9246b-256">THE</span></span></p></td>
<td><p><span data-ttu-id="9246b-257">PLUIE</span><span class="sxs-lookup"><span data-stu-id="9246b-257">RAIN</span></span><br />
<span data-ttu-id="9246b-258">Espagne</span><span class="sxs-lookup"><span data-stu-id="9246b-258">SPAIN</span></span></p></td>
<td><p><span data-ttu-id="9246b-259">IN</span><span class="sxs-lookup"><span data-stu-id="9246b-259">IN</span></span><br />
<span data-ttu-id="9246b-260">FAIT</span><span class="sxs-lookup"><span data-stu-id="9246b-260">FALLS</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9246b-261">La chute des tuples d’index sera stockée :</span><span class="sxs-lookup"><span data-stu-id="9246b-261">The falling index-tuples will be stored:</span></span>

<span data-ttu-id="9246b-262">{1, ABC, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="9246b-262">{1,ABC,MNO,VWX}</span></span>  
<span data-ttu-id="9246b-263">{1, GHI, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="9246b-263">{1,GHI,MNO,VWX}</span></span>  
<span data-ttu-id="9246b-264">{1, JKL, MNO, VWX}</span><span class="sxs-lookup"><span data-stu-id="9246b-264">{1,JKL,MNO,VWX}</span></span>  
<span data-ttu-id="9246b-265">{2, THE, PLUIE, IN}</span><span class="sxs-lookup"><span data-stu-id="9246b-265">{2,THE,RAIN,IN}</span></span>

<span data-ttu-id="9246b-266">Notez que {2, l’Espagne, IN} n’est pas stocké, même si la colonne alpha de la deuxième ligne contient une seule valeur multivaleur.</span><span class="sxs-lookup"><span data-stu-id="9246b-266">Note that {2,THE,SPAIN,IN} is not stored, even though the Alpha column in the second row happens to have a single multivalue.</span></span>

<span data-ttu-id="9246b-267">Dans les versions de Windows à partir de Windows Vista, toutes les colonnes à valeurs multiples peuvent être développées dans l’index en spécifiant JET_bitIndexCrossProduct.</span><span class="sxs-lookup"><span data-stu-id="9246b-267">In versions of Windows starting with Windows Vista, all multivalued columns can be expanded in the index by specifying JET_bitIndexCrossProduct.</span></span>

### <a name="requirements"></a><span data-ttu-id="9246b-268">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9246b-268">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9246b-269"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9246b-269"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9246b-270">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="9246b-270">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-271"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="9246b-271"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9246b-272">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9246b-272">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9246b-273"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="9246b-273"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9246b-274">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="9246b-274">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9246b-275"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9246b-275"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9246b-276">Implémenté comme <strong>JET_ INDEXCREATE_W</strong> (Unicode) et <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9246b-276">Implemented as <strong>JET_ INDEXCREATE_W</strong> (Unicode) and <strong>JET_ INDEXCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9246b-277">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9246b-277">See also</span></span>

[<span data-ttu-id="9246b-278">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="9246b-278">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="9246b-279">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="9246b-279">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="9246b-280">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9246b-280">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9246b-281">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9246b-281">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9246b-282">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="9246b-282">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="9246b-283">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="9246b-283">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="9246b-284">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="9246b-284">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="9246b-285">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="9246b-285">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="9246b-286">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="9246b-286">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="9246b-287">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="9246b-287">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="9246b-288">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="9246b-288">JetUpdate</span></span>](./jetupdate-function.md)

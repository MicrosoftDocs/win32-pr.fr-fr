---
description: 'En savoir plus sur : structure JET_TABLECREATE'
title: Structure JET_TABLECREATE
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112067"
---
# <a name="jet_tablecreate-structure"></a><span data-ttu-id="8a316-103">Structure JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="8a316-103">JET_TABLECREATE Structure</span></span>


<span data-ttu-id="8a316-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="8a316-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate-structure"></a><span data-ttu-id="8a316-105">Structure JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="8a316-105">JET_TABLECREATE Structure</span></span>

<span data-ttu-id="8a316-106">La structure **JET_TABLECREATE** contient les informations nécessaires à la création d’une table remplie avec des colonnes et des index dans une base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="8a316-106">The **JET_TABLECREATE** structure contains the information that is necessary to create a table populated with columns and indexes in an ESE database.</span></span> <span data-ttu-id="8a316-107">La structure **JET_TABLECREATE** est utilisée par [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)</span><span class="sxs-lookup"><span data-stu-id="8a316-107">The **JET_TABLECREATE** structure is used by [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)</span></span>

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a><span data-ttu-id="8a316-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8a316-108">Members</span></span>

<span data-ttu-id="8a316-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="8a316-109">**cbStruct**</span></span>

<span data-ttu-id="8a316-110">Taille de cette structure en octets (pour une extension future).</span><span class="sxs-lookup"><span data-stu-id="8a316-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="8a316-111">Elle doit être définie sur sizeof (JET_TABLECREATE) en octets.</span><span class="sxs-lookup"><span data-stu-id="8a316-111">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="8a316-112">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="8a316-112">**szTableName**</span></span>

<span data-ttu-id="8a316-113">Nom de la table à créer.</span><span class="sxs-lookup"><span data-stu-id="8a316-113">The name of the table to create.</span></span>

<span data-ttu-id="8a316-114">Le nom doit être utilisé pour remplir les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a316-114">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="8a316-115">A une valeur inférieure à JET_cbNameMost, à l’exclusion de la valeur NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="8a316-115">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="8a316-116">Se compose du jeu de caractères suivant : de 0 à 9, de A à Z, de a à z et de toute autre ponctuation, à l’exception du point d’exclamation ( \! ), de la virgule (,), du crochet ouvrant ( \[ ) et du crochet fermant ( \] ), c’est-À-dire des caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c et 0x5d à 0x7F.</span><span class="sxs-lookup"><span data-stu-id="8a316-116">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="8a316-117">Ne commence pas par un espace.</span><span class="sxs-lookup"><span data-stu-id="8a316-117">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="8a316-118">Se compose d’au moins un caractère autre qu’un espace.</span><span class="sxs-lookup"><span data-stu-id="8a316-118">Consist of at least one non-space character.</span></span>

<span data-ttu-id="8a316-119">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="8a316-119">**szTemplateTableName**</span></span>

<span data-ttu-id="8a316-120">Nom d’une table déjà existante à partir de laquelle hériter le DDL de base (langage de définition de données).</span><span class="sxs-lookup"><span data-stu-id="8a316-120">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="8a316-121">L’utilisation d’une table de modèle permet de créer facilement de nombreuses tables avec des colonnes et des index identiques.</span><span class="sxs-lookup"><span data-stu-id="8a316-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="8a316-122">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="8a316-122">**ulPages**</span></span>

<span data-ttu-id="8a316-123">Nombre initial de pages de base de données à allouer pour la table.</span><span class="sxs-lookup"><span data-stu-id="8a316-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="8a316-124">La spécification d’un nombre supérieur à un peut réduire la fragmentation si de nombreuses lignes sont insérées dans cette table.</span><span class="sxs-lookup"><span data-stu-id="8a316-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="8a316-125">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="8a316-125">**ulDensity**</span></span>

<span data-ttu-id="8a316-126">Densité de la table, en points de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="8a316-126">The table density, in percentage points.</span></span> <span data-ttu-id="8a316-127">Le nombre doit être égal à 0 ou compris entre 20 et 100.</span><span class="sxs-lookup"><span data-stu-id="8a316-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="8a316-128">Le passage de 0 signifie que la valeur par défaut doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="8a316-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="8a316-129">La valeur par défaut est 80.</span><span class="sxs-lookup"><span data-stu-id="8a316-129">The default is 80.</span></span>

<span data-ttu-id="8a316-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="8a316-130">**rgcolumncreate**</span></span>

<span data-ttu-id="8a316-131">Tableau de structures de [JET_COLUMNCREATE](./jet-columncreate-structure.md) , chacune d’elles correspondant à une colonne à créer dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="8a316-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="8a316-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="8a316-132">**cColumns**</span></span>

<span data-ttu-id="8a316-133">Nombre d’éléments [JET_COLUMNCREATE](./jet-columncreate-structure.md) dans **rgcolumncreate**.</span><span class="sxs-lookup"><span data-stu-id="8a316-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="8a316-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="8a316-134">**rgindexcreate**</span></span>

<span data-ttu-id="8a316-135">Tableau de structures de [JET_INDEXCREATE](./jet-indexcreate-structure.md) , chacune d’elles correspondant à un index à créer dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="8a316-135">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="8a316-136">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="8a316-136">**cIndexes**</span></span>

<span data-ttu-id="8a316-137">Nombre d’éléments [JET_INDEXCREATE](./jet-indexcreate-structure.md) dans **rgindexcreate**.</span><span class="sxs-lookup"><span data-stu-id="8a316-137">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="8a316-138">**grbit**</span><span class="sxs-lookup"><span data-stu-id="8a316-138">**grbit**</span></span>

<span data-ttu-id="8a316-139">Groupe de bits qui contiennent les options pour cet appel, qui incluent zéro, une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a316-139">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a316-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a316-140">Value</span></span></p></th>
<th><p><span data-ttu-id="8a316-141">Signification</span><span class="sxs-lookup"><span data-stu-id="8a316-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a316-142">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="8a316-142">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="8a316-143">La définition de JET_bitTableCreateFixedDDL empêche les opérations DDL sur la table (telles que l’ajout ou la suppression de colonnes).</span><span class="sxs-lookup"><span data-stu-id="8a316-143">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a316-144">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="8a316-144">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="8a316-145">La définition de JET_bitTableCreateTemplateTable fait que la table est une table de modèle.</span><span class="sxs-lookup"><span data-stu-id="8a316-145">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="8a316-146">Les nouvelles tables peuvent ensuite spécifier le nom de cette table comme table de modèle.</span><span class="sxs-lookup"><span data-stu-id="8a316-146">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="8a316-147">La définition de JET_bitTableCreateTemplateTable implique JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="8a316-147">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a316-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="8a316-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="8a316-149">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="8a316-149">Deprecated.</span></span> <span data-ttu-id="8a316-150">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="8a316-150">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8a316-151">**TableID**</span><span class="sxs-lookup"><span data-stu-id="8a316-151">**tableid**</span></span>

<span data-ttu-id="8a316-152">Champ de sortie qui contient le [JET_TABLEID](./jet-tableid.md) de la nouvelle table si l’appel d’API a échoué.</span><span class="sxs-lookup"><span data-stu-id="8a316-152">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="8a316-153">Si l’appel d’API échoue, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="8a316-153">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="8a316-154">**Encore**</span><span class="sxs-lookup"><span data-stu-id="8a316-154">**cCreated**</span></span>

<span data-ttu-id="8a316-155">Champ de sortie qui contient le nombre d’objets créés si l’appel d’API a échoué.</span><span class="sxs-lookup"><span data-stu-id="8a316-155">An output field that contains the count of objects created if the API call succeeds.</span></span> <span data-ttu-id="8a316-156">Si l’appel d’API échoue, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="8a316-156">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="8a316-157">Le nombre d’objets créés est égal à la somme des colonnes, des tables et des index qui ont été créés avec succès.</span><span class="sxs-lookup"><span data-stu-id="8a316-157">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="8a316-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a316-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a316-159"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8a316-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8a316-160">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="8a316-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a316-161"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="8a316-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8a316-162">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8a316-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a316-163"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="8a316-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8a316-164">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="8a316-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a316-165"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8a316-165"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8a316-166">Implémenté comme <strong>JET_TABLECREATE_W</strong> (Unicode) et <strong>JET_TABLECREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8a316-166">Implemented as <strong>JET_TABLECREATE_W</strong> (Unicode) and <strong>JET_TABLECREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8a316-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a316-167">See Also</span></span>

[<span data-ttu-id="8a316-168">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="8a316-168">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="8a316-169">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="8a316-169">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="8a316-170">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8a316-170">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="8a316-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8a316-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8a316-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8a316-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8a316-173">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8a316-173">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8a316-174">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="8a316-174">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="8a316-175">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="8a316-175">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="8a316-176">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="8a316-176">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="8a316-177">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="8a316-177">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)

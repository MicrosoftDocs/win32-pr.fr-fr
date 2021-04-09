---
description: 'En savoir plus sur : structure JET_TABLECREATE2'
title: Structure JET_TABLECREATE2
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
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
ms.openlocfilehash: d7ce983d393954c0d82f0d4e43108ff845d31571
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869137"
---
# <a name="jet_tablecreate2-structure"></a><span data-ttu-id="c5fe8-103">Structure JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="c5fe8-103">JET_TABLECREATE2 Structure</span></span>


<span data-ttu-id="c5fe8-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c5fe8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate2-structure"></a><span data-ttu-id="c5fe8-105">Structure JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="c5fe8-105">JET_TABLECREATE2 Structure</span></span>

<span data-ttu-id="c5fe8-106">La structure **JET_TABLECREATE2** contient les informations nécessaires pour créer une table remplie avec des colonnes et des index dans une base de données ESE, et qui désigne une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-106">The **JET_TABLECREATE2** structure contains the information that is needed to create a table populated with columns and indexes in an ESE database, and that designates a callback function.</span></span> <span data-ttu-id="c5fe8-107">La structure **JET_TABLECREATE2** est utilisée par [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-107">The **JET_TABLECREATE2** structure is used by [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span>

<span data-ttu-id="c5fe8-108">**Windows XP :** La structure **JET_TABLECREATE2** est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-108">**Windows XP:** The **JET_TABLECREATE2** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a><span data-ttu-id="c5fe8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c5fe8-109">Members</span></span>

<span data-ttu-id="c5fe8-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-110">**cbStruct**</span></span>

<span data-ttu-id="c5fe8-111">Taille de cette structure en octets (pour une extension future).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="c5fe8-112">Elle doit être définie sur sizeof (JET_TABLECREATE2) en octets.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-112">It must be set to sizeof( JET_TABLECREATE2 ) in bytes.</span></span>

<span data-ttu-id="c5fe8-113">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-113">**szTableName**</span></span>

<span data-ttu-id="c5fe8-114">Nom de la table à créer.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-114">The name of table to create.</span></span>

<span data-ttu-id="c5fe8-115">Le nom doit être utilisé pour remplir les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c5fe8-115">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="c5fe8-116">A une valeur inférieure à JET_cbNameMost, à l’exclusion de la valeur NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-116">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5fe8-117">Se compose du jeu de caractères suivant : de 0 à 9, de A à Z, de a à z et de toute autre ponctuation, à l’exception du point d’exclamation ( \! ), de la virgule (,), du crochet ouvrant ( \[ ) et du crochet fermant ( \] ), c’est-À-dire des caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c et 0x5d à 0x7F.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-117">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5fe8-118">Ne commence pas par un espace.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-118">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5fe8-119">Se compose d’au moins un caractère autre qu’un espace.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-119">Consist of at least one non-space character.</span></span>

<span data-ttu-id="c5fe8-120">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-120">**szTemplateTableName**</span></span>

<span data-ttu-id="c5fe8-121">Nom d’une table déjà existante à partir de laquelle hériter le DDL de base (langage de définition de données).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-121">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="c5fe8-122">L’utilisation d’une table de modèle permet de créer facilement de nombreuses tables avec des colonnes et des index identiques.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-122">Using a template table allows easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="c5fe8-123">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-123">**ulPages**</span></span>

<span data-ttu-id="c5fe8-124">Nombre initial de pages de base de données à allouer pour la table.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-124">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="c5fe8-125">La spécification d’un nombre supérieur à un peut réduire la fragmentation si de nombreuses lignes sont insérées dans cette table.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-125">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="c5fe8-126">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-126">**ulDensity**</span></span>

<span data-ttu-id="c5fe8-127">Densité de la table, en points de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-127">The table density, in percentage points.</span></span> <span data-ttu-id="c5fe8-128">Le nombre doit être égal à 0 ou compris entre 20 et 100.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-128">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="c5fe8-129">Le passage de 0 signifie que la valeur par défaut doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-129">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="c5fe8-130">La valeur par défaut est 80.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-130">The default is 80.</span></span>

<span data-ttu-id="c5fe8-131">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-131">**rgcolumncreate**</span></span>

<span data-ttu-id="c5fe8-132">Tableau de structures de [JET_COLUMNCREATE](./jet-columncreate-structure.md) , chacune d’elles correspondant à une colonne à créer dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-132">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="c5fe8-133">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-133">**cColumns**</span></span>

<span data-ttu-id="c5fe8-134">nombre d’éléments [JET_COLUMNCREATE](./jet-columncreate-structure.md) dans **rgcolumncreate**.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-134">the number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="c5fe8-135">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-135">**rgindexcreate**</span></span>

<span data-ttu-id="c5fe8-136">Tableau de structures de [JET_INDEXCREATE](./jet-indexcreate-structure.md) , chacune d’elles correspondant à un index à créer dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-136">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="c5fe8-137">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-137">**cIndexes**</span></span>

<span data-ttu-id="c5fe8-138">Nombre d’éléments [JET_INDEXCREATE](./jet-indexcreate-structure.md) dans **rgindexcreate**.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-138">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="c5fe8-139">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-139">**szCallback**</span></span>

<span data-ttu-id="c5fe8-140">Fonction qui est appelée pendant certains événements.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-140">The function that gets called during certain events.</span></span> <span data-ttu-id="c5fe8-141">**cbtyp** détermine le moment où la fonction de rappel sera appelée.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-141">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="c5fe8-142">Le format de **szCallback** doit être « fonction de module \! », par exemple, « alpha \! bêta » fait référence à la fonction bêta dans le module nommé « alpha ».</span><span class="sxs-lookup"><span data-stu-id="c5fe8-142">The format of **szCallback** must be "module\!function"—for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span> <span data-ttu-id="c5fe8-143">Le prototype de la fonction doit correspondre à [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-143">The prototype of the function must match [JET_CALLBACK](./jet-callback-callback-function.md).</span></span> <span data-ttu-id="c5fe8-144">Pour plus d’informations, consultez [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-144">For more information, see [JET_CALLBACK](./jet-callback-callback-function.md).</span></span>

<span data-ttu-id="c5fe8-145">**cbtyp**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-145">**cbtyp**</span></span>

<span data-ttu-id="c5fe8-146">Décrit le type de fonction de rappel désigné par **szCallback**.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-146">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="c5fe8-147">Pour plus d’informations, consultez [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-147">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span> <span data-ttu-id="c5fe8-148">Ce champ de bits est composé d’un ou plusieurs des bits suivants.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-148">This bitfield is composed of one or more of the following bits.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5fe8-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5fe8-149">Value</span></span></p></th>
<th><p><span data-ttu-id="c5fe8-150">Signification</span><span class="sxs-lookup"><span data-stu-id="c5fe8-150">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5fe8-151">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="c5fe8-151">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-152">La fonction de rappel est appelée lorsqu’une colonne qui peut être finalisée est passée à zéro.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-152">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5fe8-153">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="c5fe8-153">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-154">La fonction de rappel sera appelée avant l’insertion de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-154">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5fe8-155">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="c5fe8-155">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-156">La fonction de rappel est appelée une fois que le moteur de base de données a terminé l’insertion d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-156">The callback function will be called once the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5fe8-157">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="c5fe8-157">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-158">La fonction de rappel sera appelée avant la modification d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-158">The callback function will be called prior to modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5fe8-159">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="c5fe8-159">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-160">La fonction de rappel sera appelée à la fin de la modification d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-160">The callback function will be called after finishing modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5fe8-161">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="c5fe8-161">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-162">La fonction de rappel sera appelée avant la suppression d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-162">The callback function will be called prior to deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5fe8-163">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="c5fe8-163">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-164">La fonction de rappel est appelée après la suppression d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-164">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5fe8-165">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="c5fe8-165">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-166">La fonction de rappel sera appelée pour calculer une valeur par défaut définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-166">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5fe8-167">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="c5fe8-167">JET_cbtypOnlineDefragCompleted</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-168">La fonction de rappel est appelée après l’exécution d’un appel à <a href="gg294095(v=exchg.10).md">JetDefragment2</a> .</span><span class="sxs-lookup"><span data-stu-id="c5fe8-168">The callback function will be called after a call to <a href="gg294095(v=exchg.10).md">JetDefragment2</a> has completed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5fe8-169">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="c5fe8-169">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-170">La fonction de rappel sera appelée lorsque le stockage local qui est associé à un curseur doit être libéré.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-170">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5fe8-171">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="c5fe8-171">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-172">La fonction de rappel sera appelée lorsque le stockage local qui est associé à une table doit être libéré.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-172">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5fe8-173">**grbit**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-173">**grbit**</span></span>

<span data-ttu-id="c5fe8-174">Groupe de bits qui contiennent les options pour cet appel, qui incluent zéro, une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-174">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5fe8-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5fe8-175">Value</span></span></p></th>
<th><p><span data-ttu-id="c5fe8-176">Signification</span><span class="sxs-lookup"><span data-stu-id="c5fe8-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5fe8-177">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="c5fe8-177">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-178">La définition de JET_bitTableCreateFixedDDL empêche les opérations DDL sur la table (telles que l’ajout ou la suppression de colonnes).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-178">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5fe8-179">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="c5fe8-179">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-180">La définition de JET_bitTableCreateTemplateTable fait que la table est une table de modèle.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-180">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="c5fe8-181">Les nouvelles tables peuvent ensuite spécifier le nom de cette table comme table de modèle.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-181">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="c5fe8-182">La définition de JET_bitTableCreateTemplateTable implique JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-182">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5fe8-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="c5fe8-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="c5fe8-184">Doit être utilisé conjointement avec JET_bitTableCreateTemplateTable.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-184">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="c5fe8-185">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-185">Deprecated.</span></span> <span data-ttu-id="c5fe8-186">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-186">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5fe8-187">**TableID**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-187">**tableid**</span></span>

<span data-ttu-id="c5fe8-188">Champ de sortie qui contient le [JET_TABLEID](./jet-tableid.md) de la nouvelle table si l’appel d’API a échoué.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-188">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="c5fe8-189">Si l’appel d’API échoue, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-189">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="c5fe8-190">**Encore**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-190">**cCreated**</span></span>

<span data-ttu-id="c5fe8-191">Champ de sortie qui contient le nombre d’objets qui sont créés si l’appel d’API a échoué.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-191">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="c5fe8-192">Si l’appel d’API échoue, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-192">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="c5fe8-193">Le nombre d’objets créés est égal à la somme des colonnes, des tables et des index qui ont été créés avec succès.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-193">The count of objects that is created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="c5fe8-194">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5fe8-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5fe8-195"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c5fe8-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c5fe8-196">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-196">Requires Windows  Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5fe8-197"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="c5fe8-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c5fe8-198">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-198">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5fe8-199"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="c5fe8-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c5fe8-200">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5fe8-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c5fe8-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c5fe8-202">Implémenté comme <strong>JET_TABLECREATE2_W</strong> (Unicode) et <strong>JET_TABLECREATE2_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-202">Implemented as <strong>JET_TABLECREATE2_W</strong> (Unicode) and <strong>JET_TABLECREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c5fe8-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5fe8-203">See Also</span></span>

[<span data-ttu-id="c5fe8-204">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="c5fe8-204">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="c5fe8-205">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="c5fe8-205">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="c5fe8-206">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="c5fe8-206">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="c5fe8-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c5fe8-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c5fe8-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c5fe8-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c5fe8-209">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="c5fe8-209">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="c5fe8-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c5fe8-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c5fe8-211">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="c5fe8-211">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="c5fe8-212">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="c5fe8-212">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="c5fe8-213">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="c5fe8-213">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="c5fe8-214">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="c5fe8-214">JetDefragment2</span></span>](./jetdefragment2-function.md)

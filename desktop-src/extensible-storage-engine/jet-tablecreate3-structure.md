---
description: 'En savoir plus sur : structure JET_TABLECREATE3'
title: Structure JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
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
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516824"
---
# <a name="jet_tablecreate3-structure"></a><span data-ttu-id="efab7-103">Structure JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="efab7-103">JET_TABLECREATE3 Structure</span></span>


<span data-ttu-id="efab7-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="efab7-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="efab7-105">La structure **JET_TABLECREATE3** contient les informations nécessaires pour créer une table remplie avec des colonnes et des index dans une base de données ESE (Extensible Storage Engine) et qui désigne une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="efab7-105">The **JET_TABLECREATE3** structure contains the information that is needed to create a table populated with columns and indexes in an Extensible Storage Engine (ESE) database, and that designates a callback function.</span></span> <span data-ttu-id="efab7-106">La structure **JET_TABLECREATE3** est utilisée par la fonction [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) .</span><span class="sxs-lookup"><span data-stu-id="efab7-106">The **JET_TABLECREATE3** structure is used by the [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) function.</span></span>

<span data-ttu-id="efab7-107">La structure **JET_TABLECREATE3** a été introduite dans le système d’exploitation Windows 7.</span><span class="sxs-lookup"><span data-stu-id="efab7-107">The **JET_TABLECREATE3** structure was introduced in the Windows 7 operating system.</span></span>

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a><span data-ttu-id="efab7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="efab7-108">Members</span></span>

<span data-ttu-id="efab7-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="efab7-109">**cbStruct**</span></span>

<span data-ttu-id="efab7-110">Taille de cette structure en octets (pour une extension future).</span><span class="sxs-lookup"><span data-stu-id="efab7-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="efab7-111">Elle doit être définie sur sizeof (JET_TABLECREATE3) en octets.</span><span class="sxs-lookup"><span data-stu-id="efab7-111">It must be set to sizeof( JET_TABLECREATE3 ) in bytes.</span></span>

<span data-ttu-id="efab7-112">**szTableName**</span><span class="sxs-lookup"><span data-stu-id="efab7-112">**szTableName**</span></span>

<span data-ttu-id="efab7-113">Nom de la table à créer.</span><span class="sxs-lookup"><span data-stu-id="efab7-113">The name of the table to create.</span></span>

<span data-ttu-id="efab7-114">Le nom doit remplir les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="efab7-114">The name must meet the following conditions:</span></span>

  - <span data-ttu-id="efab7-115">Elle doit avoir une valeur inférieure à JET_cbNameMost, à l’exclusion de la valeur null de fin.</span><span class="sxs-lookup"><span data-stu-id="efab7-115">It must have a value that is less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="efab7-116">Il doit se composer du jeu de caractères suivant : de 0 à 9, de A à Z, de a à z et de toute autre ponctuation, à l’exception du point d’exclamation ( \! ), de la virgule (,), du crochet ouvrant ( \[ ) et du crochet fermant ( \] ), c’est-À-dire des caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c et 0x5d à 0x7F</span><span class="sxs-lookup"><span data-stu-id="efab7-116">It must consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]); that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="efab7-117">Il ne doit pas commencer par un espace.</span><span class="sxs-lookup"><span data-stu-id="efab7-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="efab7-118">Il doit comporter au moins un caractère autre qu’un espace.</span><span class="sxs-lookup"><span data-stu-id="efab7-118">It must consist of at least one non-space character.</span></span>

<span data-ttu-id="efab7-119">**szTemplateTableName**</span><span class="sxs-lookup"><span data-stu-id="efab7-119">**szTemplateTableName**</span></span>

<span data-ttu-id="efab7-120">Nom d’une table existante à partir de laquelle hériter le langage de définition de données (DDL) de base.</span><span class="sxs-lookup"><span data-stu-id="efab7-120">The name of an existing table from which to inherit the base data definition language (DDL).</span></span> <span data-ttu-id="efab7-121">L’utilisation d’une table de modèle permet de créer facilement de nombreuses tables avec des colonnes et des index identiques.</span><span class="sxs-lookup"><span data-stu-id="efab7-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="efab7-122">**ulPages**</span><span class="sxs-lookup"><span data-stu-id="efab7-122">**ulPages**</span></span>

<span data-ttu-id="efab7-123">Nombre initial de pages de base de données à allouer pour la table.</span><span class="sxs-lookup"><span data-stu-id="efab7-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="efab7-124">La spécification d’un nombre supérieur à un peut réduire la fragmentation si de nombreuses lignes sont insérées dans cette table.</span><span class="sxs-lookup"><span data-stu-id="efab7-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="efab7-125">**ulDensity**</span><span class="sxs-lookup"><span data-stu-id="efab7-125">**ulDensity**</span></span>

<span data-ttu-id="efab7-126">Densité de la table, en points de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="efab7-126">The table density, in percentage points.</span></span> <span data-ttu-id="efab7-127">Le nombre doit être égal à 0 ou compris entre 20 et 100.</span><span class="sxs-lookup"><span data-stu-id="efab7-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="efab7-128">Le passage de 0 signifie que la valeur par défaut doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="efab7-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="efab7-129">La valeur par défaut est 80.</span><span class="sxs-lookup"><span data-stu-id="efab7-129">The default value is 80.</span></span>

<span data-ttu-id="efab7-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="efab7-130">**rgcolumncreate**</span></span>

<span data-ttu-id="efab7-131">Tableau de structures de [JET_COLUMNCREATE](./jet-columncreate-structure.md) , chacune d’elles correspondant à une colonne à créer dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="efab7-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="efab7-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="efab7-132">**cColumns**</span></span>

<span data-ttu-id="efab7-133">Nombre d’éléments [JET_COLUMNCREATE](./jet-columncreate-structure.md) dans le paramètre *rgcolumncreate* .</span><span class="sxs-lookup"><span data-stu-id="efab7-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in the *rgcolumncreate* parameter.</span></span>

<span data-ttu-id="efab7-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="efab7-134">**rgindexcreate**</span></span>

<span data-ttu-id="efab7-135">Tableau de structures de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , chacune d’elles correspondant à un index à créer dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="efab7-135">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="efab7-136">**cIndexes**</span><span class="sxs-lookup"><span data-stu-id="efab7-136">**cIndexes**</span></span>

<span data-ttu-id="efab7-137">Nombre d’éléments [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) dans le paramètre *rgindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="efab7-137">The number of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) elements in the *rgindexcreate* parameter.</span></span>

<span data-ttu-id="efab7-138">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="efab7-138">**szCallback**</span></span>

<span data-ttu-id="efab7-139">Fonction qui est appelée pendant certains événements.</span><span class="sxs-lookup"><span data-stu-id="efab7-139">The function that gets called during certain events.</span></span> <span data-ttu-id="efab7-140">**cbtyp** détermine le moment où la fonction de rappel sera appelée.</span><span class="sxs-lookup"><span data-stu-id="efab7-140">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="efab7-141">Le format de **szCallback** doit être « fonction de module \! », par exemple, « alpha \! bêta » fait référence à la fonction bêta dans le module nommé « alpha ».</span><span class="sxs-lookup"><span data-stu-id="efab7-141">The format of **szCallback** must be "module\!function" — for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span>

<span data-ttu-id="efab7-142">Le prototype de la fonction doit correspondre à la fonction de rappel [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="efab7-142">The prototype of the function must match the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span>

<span data-ttu-id="efab7-143">**cbtyp**</span><span class="sxs-lookup"><span data-stu-id="efab7-143">**cbtyp**</span></span>

<span data-ttu-id="efab7-144">Décrit le type de fonction de rappel désigné par **szCallback**.</span><span class="sxs-lookup"><span data-stu-id="efab7-144">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="efab7-145">Pour plus d’informations, consultez [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="efab7-145">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span>

<span data-ttu-id="efab7-146">Ce champ de bits est composé d’une ou plusieurs des valeurs de bit listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="efab7-146">This bitfield is composed of one or more of the bit values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="efab7-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="efab7-147">Value</span></span></p></th>
<th><p><span data-ttu-id="efab7-148">Signification</span><span class="sxs-lookup"><span data-stu-id="efab7-148">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efab7-149">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="efab7-149">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="efab7-150">La fonction de rappel est appelée lorsqu’une colonne qui peut être finalisée est passée à zéro.</span><span class="sxs-lookup"><span data-stu-id="efab7-150">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efab7-151">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="efab7-151">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="efab7-152">La fonction de rappel sera appelée avant l’insertion de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="efab7-152">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efab7-153">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="efab7-153">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="efab7-154">La fonction de rappel est appelée une fois que le moteur de base de données a terminé l’insertion d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="efab7-154">The callback function will be called after the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efab7-155">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="efab7-155">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="efab7-156">La fonction de rappel sera appelée avant la modification d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="efab7-156">The callback function will be called prior to the modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efab7-157">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="efab7-157">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="efab7-158">La fonction de rappel est appelée après la fin de la modification d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="efab7-158">The callback function will be called after finishing the modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efab7-159">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="efab7-159">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="efab7-160">La fonction de rappel sera appelée avant la suppression d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="efab7-160">The callback function will be called prior to the deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efab7-161">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="efab7-161">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="efab7-162">La fonction de rappel est appelée après la suppression d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="efab7-162">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efab7-163">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="efab7-163">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="efab7-164">La fonction de rappel sera appelée pour calculer une valeur par défaut définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="efab7-164">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efab7-165">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="efab7-165">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="efab7-166">La fonction de rappel sera appelée lorsque le stockage local qui est associé à un curseur doit être libéré.</span><span class="sxs-lookup"><span data-stu-id="efab7-166">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efab7-167">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="efab7-167">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="efab7-168">La fonction de rappel sera appelée lorsque le stockage local qui est associé à une table doit être libéré.</span><span class="sxs-lookup"><span data-stu-id="efab7-168">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="efab7-169">**grbit**</span><span class="sxs-lookup"><span data-stu-id="efab7-169">**grbit**</span></span>

<span data-ttu-id="efab7-170">Groupe de bits qui contient zéro, une ou plusieurs des valeurs d’option d’appel énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="efab7-170">A group of bits that contains zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="efab7-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="efab7-171">Value</span></span></p></th>
<th><p><span data-ttu-id="efab7-172">Signification</span><span class="sxs-lookup"><span data-stu-id="efab7-172">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efab7-173">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="efab7-173">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="efab7-174">Empêche les opérations DDL sur la table (telles que l’ajout ou la suppression de colonnes).</span><span class="sxs-lookup"><span data-stu-id="efab7-174">Prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efab7-175">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="efab7-175">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="efab7-176">Indique que la table est une table de modèles.</span><span class="sxs-lookup"><span data-stu-id="efab7-176">Causes the table to be a template table.</span></span> <span data-ttu-id="efab7-177">Les nouvelles tables peuvent ensuite spécifier le nom de cette table comme table de modèle.</span><span class="sxs-lookup"><span data-stu-id="efab7-177">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="efab7-178">La définition de JET_bitTableCreateTemplateTable implique JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="efab7-178">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efab7-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="efab7-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="efab7-180">Doit être utilisé conjointement avec JET_bitTableCreateTemplateTable.</span><span class="sxs-lookup"><span data-stu-id="efab7-180">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="efab7-181">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="efab7-181">Deprecated.</span></span> <span data-ttu-id="efab7-182">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="efab7-182">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="efab7-183">**pSeqSpacehints**</span><span class="sxs-lookup"><span data-stu-id="efab7-183">**pSeqSpacehints**</span></span>

<span data-ttu-id="efab7-184">Pointeur vers une structure [JET_SPACEHINTS](./jet-spacehints-structure.md) pour l’index séquentiel par défaut.</span><span class="sxs-lookup"><span data-stu-id="efab7-184">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for default sequential index.</span></span>

<span data-ttu-id="efab7-185">**pSeqSpacehints** a été introduit dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="efab7-185">**pSeqSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="efab7-186">**pLVSpacehints**</span><span class="sxs-lookup"><span data-stu-id="efab7-186">**pLVSpacehints**</span></span>

<span data-ttu-id="efab7-187">Pointeur vers une structure [JET_SPACEHINTS](./jet-spacehints-structure.md) pour une arborescence de valeurs longues séparée.</span><span class="sxs-lookup"><span data-stu-id="efab7-187">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for a Separated Long Value tree.</span></span>

<span data-ttu-id="efab7-188">**pLVSpacehints** a été introduit dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="efab7-188">**pLVSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="efab7-189">**cbSeparateLV**</span><span class="sxs-lookup"><span data-stu-id="efab7-189">**cbSeparateLV**</span></span>

<span data-ttu-id="efab7-190">Taille à laquelle séparer un LV intrinsèque de l’enregistrement principal.</span><span class="sxs-lookup"><span data-stu-id="efab7-190">The size to separate an intrinsic LV from the primary record.</span></span> <span data-ttu-id="efab7-191">Toute structure c à valeurs longues pour une arborescence LV séparée.</span><span class="sxs-lookup"><span data-stu-id="efab7-191">Any long-value c structure for a Separated LV tree.</span></span> <span data-ttu-id="efab7-192">Pour plus d’informations, consultez ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span><span class="sxs-lookup"><span data-stu-id="efab7-192">For more information, see ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span></span> <span data-ttu-id="efab7-193">Les colonnes de valeur longue inférieures à cette valeur peuvent être séparées si l’enregistrement devient trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="efab7-193">Long-value columns smaller than this value may be separated if the record becomes too large.</span></span>

<span data-ttu-id="efab7-194">**cbSeparateLV** a été introduit dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="efab7-194">**cbSeparateLV** was introduced in Windows 7.</span></span>

<span data-ttu-id="efab7-195">**TableID**</span><span class="sxs-lookup"><span data-stu-id="efab7-195">**tableid**</span></span>

<span data-ttu-id="efab7-196">Champ de sortie qui contient le [JET_TABLEID](./jet-tableid.md) de la nouvelle table si l’appel d’API a échoué.</span><span class="sxs-lookup"><span data-stu-id="efab7-196">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="efab7-197">Si l’appel d’API échoue, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="efab7-197">If the API call fails, the value is undefined.</span></span> <span data-ttu-id="efab7-198">Cette table est ouverte exclusivement.</span><span class="sxs-lookup"><span data-stu-id="efab7-198">This table is opened exclusively.</span></span>

<span data-ttu-id="efab7-199">**Encore**</span><span class="sxs-lookup"><span data-stu-id="efab7-199">**cCreated**</span></span>

<span data-ttu-id="efab7-200">Champ de sortie qui contient le nombre d’objets qui sont créés si l’appel d’API a échoué.</span><span class="sxs-lookup"><span data-stu-id="efab7-200">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="efab7-201">Si l’appel d’API échoue, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="efab7-201">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="efab7-202">Le nombre d’objets créés est égal à la somme des colonnes, des tables et des index qui ont été créés avec succès.</span><span class="sxs-lookup"><span data-stu-id="efab7-202">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="efab7-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efab7-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efab7-204"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="efab7-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="efab7-205">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="efab7-205">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efab7-206"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="efab7-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="efab7-207">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="efab7-207">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efab7-208"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="efab7-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="efab7-209">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="efab7-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efab7-210"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="efab7-210"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="efab7-211">Implémenté comme <strong>JET_TABLECREATE3_W</strong> (Unicode) et <strong>JET_TABLECREATE3_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="efab7-211">Implemented as <strong>JET_TABLECREATE3_W</strong> (Unicode) and <strong>JET_TABLECREATE3_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="efab7-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efab7-212">See also</span></span>

[<span data-ttu-id="efab7-213">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="efab7-213">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="efab7-214">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="efab7-214">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="efab7-215">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="efab7-215">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="efab7-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="efab7-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="efab7-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="efab7-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="efab7-218">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="efab7-218">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="efab7-219">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="efab7-219">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="efab7-220">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="efab7-220">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="efab7-221">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="efab7-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="efab7-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="efab7-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="efab7-223">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="efab7-223">JetDefragment2</span></span>](./jetdefragment2-function.md)

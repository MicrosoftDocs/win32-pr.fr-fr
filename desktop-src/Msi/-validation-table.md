---
description: La \_ table de validation est une table système qui contient les noms de colonne et les valeurs de colonne pour toutes les tables de la base de données.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: Table _Validation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864542"
---
# <a name="_validation-table"></a><span data-ttu-id="99a9b-103">\_Tableau de validation</span><span class="sxs-lookup"><span data-stu-id="99a9b-103">\_Validation Table</span></span>

<span data-ttu-id="99a9b-104">La \_ table de validation est une table système qui contient les noms de colonne et les valeurs de colonne pour toutes les tables de la base de données.</span><span class="sxs-lookup"><span data-stu-id="99a9b-104">The \_Validation table is a system table that contains the column names and the column values for all of the tables in the database.</span></span> <span data-ttu-id="99a9b-105">Il est utilisé pendant le processus de validation de la base de données pour s’assurer que toutes les colonnes sont comptabilisées et ont les valeurs correctes.</span><span class="sxs-lookup"><span data-stu-id="99a9b-105">It is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="99a9b-106">Cette table n’est pas fournie avec la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="99a9b-106">This table is not shipped with the installer database.</span></span>

<span data-ttu-id="99a9b-107">La \_ table de validation contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="99a9b-107">The \_Validation table has the following columns.</span></span>



| <span data-ttu-id="99a9b-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="99a9b-108">Column</span></span>      | <span data-ttu-id="99a9b-109">Type</span><span class="sxs-lookup"><span data-stu-id="99a9b-109">Type</span></span>                               | <span data-ttu-id="99a9b-110">Clé</span><span class="sxs-lookup"><span data-stu-id="99a9b-110">Key</span></span> | <span data-ttu-id="99a9b-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="99a9b-111">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="99a9b-112">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="99a9b-112">Table</span></span>       | [<span data-ttu-id="99a9b-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="99a9b-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="99a9b-114">O</span><span class="sxs-lookup"><span data-stu-id="99a9b-114">Y</span></span>   | <span data-ttu-id="99a9b-115">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-115">N</span></span>        |
| <span data-ttu-id="99a9b-116">Colonne</span><span class="sxs-lookup"><span data-stu-id="99a9b-116">Column</span></span>      | [<span data-ttu-id="99a9b-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="99a9b-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="99a9b-118">O</span><span class="sxs-lookup"><span data-stu-id="99a9b-118">Y</span></span>   | <span data-ttu-id="99a9b-119">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-119">N</span></span>        |
| <span data-ttu-id="99a9b-120">Nullable</span><span class="sxs-lookup"><span data-stu-id="99a9b-120">Nullable</span></span>    | [<span data-ttu-id="99a9b-121">Text</span><span class="sxs-lookup"><span data-stu-id="99a9b-121">Text</span></span>](text.md)                   | <span data-ttu-id="99a9b-122">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-122">N</span></span>   | <span data-ttu-id="99a9b-123">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-123">N</span></span>        |
| <span data-ttu-id="99a9b-124">MinValue</span><span class="sxs-lookup"><span data-stu-id="99a9b-124">MinValue</span></span>    | [<span data-ttu-id="99a9b-125">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="99a9b-125">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="99a9b-126">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-126">N</span></span>   | <span data-ttu-id="99a9b-127">O</span><span class="sxs-lookup"><span data-stu-id="99a9b-127">Y</span></span>        |
| <span data-ttu-id="99a9b-128">MaxValue</span><span class="sxs-lookup"><span data-stu-id="99a9b-128">MaxValue</span></span>    | [<span data-ttu-id="99a9b-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="99a9b-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="99a9b-130">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-130">N</span></span>   | <span data-ttu-id="99a9b-131">O</span><span class="sxs-lookup"><span data-stu-id="99a9b-131">Y</span></span>        |
| <span data-ttu-id="99a9b-132">Keytable</span><span class="sxs-lookup"><span data-stu-id="99a9b-132">KeyTable</span></span>    | [<span data-ttu-id="99a9b-133">Identificateur</span><span class="sxs-lookup"><span data-stu-id="99a9b-133">Identifier</span></span>](identifier.md)       | <span data-ttu-id="99a9b-134">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-134">N</span></span>   | <span data-ttu-id="99a9b-135">O</span><span class="sxs-lookup"><span data-stu-id="99a9b-135">Y</span></span>        |
| <span data-ttu-id="99a9b-136">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="99a9b-136">KeyColumn</span></span>   | [<span data-ttu-id="99a9b-137">Integer</span><span class="sxs-lookup"><span data-stu-id="99a9b-137">Integer</span></span>](integer.md)             | <span data-ttu-id="99a9b-138">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-138">N</span></span>   | <span data-ttu-id="99a9b-139">O</span><span class="sxs-lookup"><span data-stu-id="99a9b-139">Y</span></span>        |
| <span data-ttu-id="99a9b-140">Category</span><span class="sxs-lookup"><span data-stu-id="99a9b-140">Category</span></span>    | [<span data-ttu-id="99a9b-141">Text</span><span class="sxs-lookup"><span data-stu-id="99a9b-141">Text</span></span>](text.md)                   | <span data-ttu-id="99a9b-142">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-142">N</span></span>   | <span data-ttu-id="99a9b-143">O</span><span class="sxs-lookup"><span data-stu-id="99a9b-143">Y</span></span>        |
| <span data-ttu-id="99a9b-144">Définissez</span><span class="sxs-lookup"><span data-stu-id="99a9b-144">Set</span></span>         | [<span data-ttu-id="99a9b-145">Text</span><span class="sxs-lookup"><span data-stu-id="99a9b-145">Text</span></span>](text.md)                   | <span data-ttu-id="99a9b-146">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-146">N</span></span>   | <span data-ttu-id="99a9b-147">O</span><span class="sxs-lookup"><span data-stu-id="99a9b-147">Y</span></span>        |
| <span data-ttu-id="99a9b-148">Description</span><span class="sxs-lookup"><span data-stu-id="99a9b-148">Description</span></span> | [<span data-ttu-id="99a9b-149">Text</span><span class="sxs-lookup"><span data-stu-id="99a9b-149">Text</span></span>](text.md)                   | <span data-ttu-id="99a9b-150">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-150">N</span></span>   | <span data-ttu-id="99a9b-151">O</span><span class="sxs-lookup"><span data-stu-id="99a9b-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="99a9b-152">Colonnes</span><span class="sxs-lookup"><span data-stu-id="99a9b-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="99a9b-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau</span><span class="sxs-lookup"><span data-stu-id="99a9b-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="99a9b-154">Utilisé pour identifier une table particulière.</span><span class="sxs-lookup"><span data-stu-id="99a9b-154">Used to identify a particular table.</span></span> <span data-ttu-id="99a9b-155">Cette clé et la clé de colonne forment la clé primaire de la \_ table de validation.</span><span class="sxs-lookup"><span data-stu-id="99a9b-155">This key and the Column key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="99a9b-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Chronique</span><span class="sxs-lookup"><span data-stu-id="99a9b-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="99a9b-157">Utilisé pour identifier une colonne particulière de la table.</span><span class="sxs-lookup"><span data-stu-id="99a9b-157">Used to identify a particular column of the table.</span></span> <span data-ttu-id="99a9b-158">Cette clé et la clé de table forment la clé primaire de la \_ table de validation.</span><span class="sxs-lookup"><span data-stu-id="99a9b-158">This key and the Table key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="99a9b-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable</span><span class="sxs-lookup"><span data-stu-id="99a9b-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable</span></span>
</dt> <dd>

<span data-ttu-id="99a9b-160">Indique si la colonne peut contenir une valeur null.</span><span class="sxs-lookup"><span data-stu-id="99a9b-160">Identifies whether the column may contain a Null value.</span></span>

<span data-ttu-id="99a9b-161">Cette colonne peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="99a9b-161">This column may have one of the following values.</span></span>



| <span data-ttu-id="99a9b-162">String</span><span class="sxs-lookup"><span data-stu-id="99a9b-162">String</span></span> | <span data-ttu-id="99a9b-163">Signification</span><span class="sxs-lookup"><span data-stu-id="99a9b-163">Meaning</span></span>                                   |
|--------|-------------------------------------------|
| <span data-ttu-id="99a9b-164">O</span><span class="sxs-lookup"><span data-stu-id="99a9b-164">Y</span></span>      | <span data-ttu-id="99a9b-165">Oui, la colonne peut avoir une valeur null.</span><span class="sxs-lookup"><span data-stu-id="99a9b-165">Yes, the column may have a Null value.</span></span>    |
| <span data-ttu-id="99a9b-166">N</span><span class="sxs-lookup"><span data-stu-id="99a9b-166">N</span></span>      | <span data-ttu-id="99a9b-167">Non, la colonne ne peut pas avoir de valeur null.</span><span class="sxs-lookup"><span data-stu-id="99a9b-167">No, the column may not have a Null value.</span></span> |



 

</dd> <dt>

<span data-ttu-id="99a9b-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span><span class="sxs-lookup"><span data-stu-id="99a9b-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span></span>
</dt> <dd>

<span data-ttu-id="99a9b-169">Ce champ s’applique aux colonnes ayant une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="99a9b-169">This field applies to columns having numeric value.</span></span> <span data-ttu-id="99a9b-170">Le champ contient la valeur minimale autorisée.</span><span class="sxs-lookup"><span data-stu-id="99a9b-170">The field contains the minimum permissible value.</span></span> <span data-ttu-id="99a9b-171">Il peut s’agir de la valeur minimale pour un entier ou de la valeur minimale pour une chaîne de date ou de version.</span><span class="sxs-lookup"><span data-stu-id="99a9b-171">This can be the minimum value for an integer or the minimum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="99a9b-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span><span class="sxs-lookup"><span data-stu-id="99a9b-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span></span>
</dt> <dd>

<span data-ttu-id="99a9b-173">Ce champ s’applique aux colonnes ayant une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="99a9b-173">This field applies to columns having numeric value.</span></span> <span data-ttu-id="99a9b-174">Le champ est la valeur maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="99a9b-174">The field is the maximum permissible value.</span></span> <span data-ttu-id="99a9b-175">Il peut s’agir de la valeur maximale d’un entier ou de la valeur maximale d’une chaîne de date ou de version.</span><span class="sxs-lookup"><span data-stu-id="99a9b-175">This may be the maximum value for an integer or the maximum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="99a9b-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>Keytable</span><span class="sxs-lookup"><span data-stu-id="99a9b-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span></span>
</dt> <dd>

<span data-ttu-id="99a9b-177">Ce champ s’applique aux colonnes qui sont des clés externes.</span><span class="sxs-lookup"><span data-stu-id="99a9b-177">This field applies to columns that are external keys.</span></span> <span data-ttu-id="99a9b-178">Le champ identifié dans la colonne doit être lié au numéro de colonne spécifié par KeyColumn dans la table nommée dans keytable.</span><span class="sxs-lookup"><span data-stu-id="99a9b-178">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="99a9b-179">Il peut s’agir d’une liste de tables séparées par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="99a9b-179">This can be a list of tables separated by semicolons.</span></span>

</dd> <dt>

<span data-ttu-id="99a9b-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span><span class="sxs-lookup"><span data-stu-id="99a9b-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span></span>
</dt> <dd>

<span data-ttu-id="99a9b-181">Ce champ s’applique aux colonnes de table qui sont des clés externes.</span><span class="sxs-lookup"><span data-stu-id="99a9b-181">This field applies to table columns that are external keys.</span></span> <span data-ttu-id="99a9b-182">Le champ identifié dans la colonne doit être lié au numéro de colonne spécifié par KeyColumn dans la table nommée dans keytable.</span><span class="sxs-lookup"><span data-stu-id="99a9b-182">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="99a9b-183">La plage autorisée du champ KeyColumn est 1-32.</span><span class="sxs-lookup"><span data-stu-id="99a9b-183">The permissible range of the KeyColumn field is 1-32.</span></span>

</dd> <dt>

<span data-ttu-id="99a9b-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Catégorie</span><span class="sxs-lookup"><span data-stu-id="99a9b-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="99a9b-185">Il s’agit du type de données contenues dans le champ de base de données spécifié par les colonnes de table et de colonne de la \_ table de validation.</span><span class="sxs-lookup"><span data-stu-id="99a9b-185">This is the type of data contained by the database field specified by the Table and Column columns of the \_Validation table.</span></span> <span data-ttu-id="99a9b-186">S’il s’agit d’un type ayant une valeur numérique, par exemple [entier](integer.md), [DoubleInteger](doubleinteger.md) ou [heure/date](time-date.md), entrez null dans ce champ et spécifiez la plage de valeurs à l’aide des colonnes MinValue et MaxValue.</span><span class="sxs-lookup"><span data-stu-id="99a9b-186">If this is a type having a numeric value, such as [Integer](integer.md), [DoubleInteger](doubleinteger.md) or [Time/Date](time-date.md), then enter null into this field and specify the value's range using the MinValue and MaxValue columns.</span></span> <span data-ttu-id="99a9b-187">Utilisez la colonne catégorie pour spécifier les types de données non numériques décrits dans [types de données de colonne](column-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="99a9b-187">Use the Category column to specify the non-numeric data types described in [Column Data Types](column-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="99a9b-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Définie</span><span class="sxs-lookup"><span data-stu-id="99a9b-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Set</span></span>
</dt> <dd>

<span data-ttu-id="99a9b-189">Il s’agit d’une liste de valeurs autorisées pour ce champ, séparées par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="99a9b-189">This is a list of permissible values for this field separated by semicolons.</span></span> <span data-ttu-id="99a9b-190">Ce champ est généralement utilisé pour les énumérations.</span><span class="sxs-lookup"><span data-stu-id="99a9b-190">This field is usually used for enumerations.</span></span>

</dd> <dt>

<span data-ttu-id="99a9b-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="99a9b-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="99a9b-192">Description des données stockées dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="99a9b-192">A description of the data that is stored in the column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="99a9b-193">Validation</span><span class="sxs-lookup"><span data-stu-id="99a9b-193">Validation</span></span>

<dl>

[<span data-ttu-id="99a9b-194">ICE03</span><span class="sxs-lookup"><span data-stu-id="99a9b-194">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="99a9b-195">ICE06</span><span class="sxs-lookup"><span data-stu-id="99a9b-195">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="99a9b-196">ICE32</span><span class="sxs-lookup"><span data-stu-id="99a9b-196">ICE32</span></span>](ice32.md)  
</dl>

## <a name="remarks"></a><span data-ttu-id="99a9b-197">Notes</span><span class="sxs-lookup"><span data-stu-id="99a9b-197">Remarks</span></span>

<span data-ttu-id="99a9b-198">Le champ de catégorie de ce tableau s’applique uniquement aux données de chaîne.</span><span class="sxs-lookup"><span data-stu-id="99a9b-198">The Category field of this table only applies to string data.</span></span> <span data-ttu-id="99a9b-199">Si le champ de colonne fait référence à une colonne avec des données binaires, le type de données binaire doit être spécifié dans le champ catégorie.</span><span class="sxs-lookup"><span data-stu-id="99a9b-199">If the Column field refers to a column with binary data, the binary data type must be specified in the Category field.</span></span> <span data-ttu-id="99a9b-200">Les types de colonne de données Integer ignorent le champ Category pendant la validation.</span><span class="sxs-lookup"><span data-stu-id="99a9b-200">Integer data Column types ignore the Category field during validation.</span></span>

 

 




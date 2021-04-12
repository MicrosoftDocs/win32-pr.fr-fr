---
description: MsiViewGetColumnInfo et la propriété ColumnInfo de l’objet View utilisent le format suivant pour décrire les définitions de colonne de base de données.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Format de définition de colonne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203219"
---
# <a name="column-definition-format"></a><span data-ttu-id="7f0fa-103">Format de définition de colonne</span><span class="sxs-lookup"><span data-stu-id="7f0fa-103">Column Definition Format</span></span>

<span data-ttu-id="7f0fa-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) et la [**propriété COLUMNINFO**](view-columninfo.md) de l’objet [**View**](view-object.md) utilisent le format suivant pour décrire les définitions de colonne de base de données.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) and the [**ColumnInfo Property**](view-columninfo.md) of the [**View**](view-object.md) object use the following format to describe database column definitions.</span></span> <span data-ttu-id="7f0fa-105">Chaque colonne est décrite par une chaîne dans le champ d’enregistrement correspondant retourné par la fonction ou la propriété.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-105">Each column is described by a string in the corresponding record field returned by the function or property.</span></span> <span data-ttu-id="7f0fa-106">La chaîne de définition se compose d’une seule lettre représentant le type de données suivi de la largeur de la colonne (en caractères, le cas échéant, octets).</span><span class="sxs-lookup"><span data-stu-id="7f0fa-106">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, bytes otherwise).</span></span> <span data-ttu-id="7f0fa-107">Une largeur de zéro désigne une largeur illimitée (par exemple, des champs de texte longs et des flux).</span><span class="sxs-lookup"><span data-stu-id="7f0fa-107">A width of zero designates an unbounded width (for example, long text fields and streams).</span></span> <span data-ttu-id="7f0fa-108">Une lettre majuscule indique que les valeurs NULL sont autorisées dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-108">An uppercase letter indicates that null values are allowed in the column.</span></span>



| <span data-ttu-id="7f0fa-109">Descripteur de colonne</span><span class="sxs-lookup"><span data-stu-id="7f0fa-109">Column descriptor</span></span> | <span data-ttu-id="7f0fa-110">Chaîne de définition</span><span class="sxs-lookup"><span data-stu-id="7f0fa-110">Definition string</span></span>                 |
|-------------------|-----------------------------------|
| <span data-ttu-id="7f0fa-111">x?</span><span class="sxs-lookup"><span data-stu-id="7f0fa-111">s?</span></span>                | <span data-ttu-id="7f0fa-112">Chaîne, longueur de variable ( ? = 1-255)</span><span class="sxs-lookup"><span data-stu-id="7f0fa-112">String, variable length (?=1-255)</span></span> |
| <span data-ttu-id="7f0fa-113">consommation</span><span class="sxs-lookup"><span data-stu-id="7f0fa-113">s0</span></span>                | <span data-ttu-id="7f0fa-114">Chaîne, longueur de variable</span><span class="sxs-lookup"><span data-stu-id="7f0fa-114">String, variable length</span></span>           |
| <span data-ttu-id="7f0fa-115">i2</span><span class="sxs-lookup"><span data-stu-id="7f0fa-115">i2</span></span>                | <span data-ttu-id="7f0fa-116">Entier Short</span><span class="sxs-lookup"><span data-stu-id="7f0fa-116">Short integer</span></span>                     |
| <span data-ttu-id="7f0fa-117">i4</span><span class="sxs-lookup"><span data-stu-id="7f0fa-117">i4</span></span>                | <span data-ttu-id="7f0fa-118">Entier long</span><span class="sxs-lookup"><span data-stu-id="7f0fa-118">Long integer</span></span>                      |
| <span data-ttu-id="7f0fa-119">v0</span><span class="sxs-lookup"><span data-stu-id="7f0fa-119">v0</span></span>                | <span data-ttu-id="7f0fa-120">Flux binaire</span><span class="sxs-lookup"><span data-stu-id="7f0fa-120">Binary Stream</span></span>                     |
| <span data-ttu-id="7f0fa-121">activée?</span><span class="sxs-lookup"><span data-stu-id="7f0fa-121">g?</span></span>                | <span data-ttu-id="7f0fa-122">Chaîne temporaire ( ? = 0-255)</span><span class="sxs-lookup"><span data-stu-id="7f0fa-122">Temporary string (?=0-255)</span></span>        |
| <span data-ttu-id="7f0fa-123">j?</span><span class="sxs-lookup"><span data-stu-id="7f0fa-123">j?</span></span>                | <span data-ttu-id="7f0fa-124">Entier temporaire ( ? = 0, 1, 2, 4)</span><span class="sxs-lookup"><span data-stu-id="7f0fa-124">Temporary integer (?=0,1,2,4)</span></span>     |
| <span data-ttu-id="7f0fa-125">O0</span><span class="sxs-lookup"><span data-stu-id="7f0fa-125">O0</span></span>                | <span data-ttu-id="7f0fa-126">Objet temporaire</span><span class="sxs-lookup"><span data-stu-id="7f0fa-126">Temporary object</span></span>                  |



 

<span data-ttu-id="7f0fa-127">Les chaînes utilisées pour décrire les colonnes ont la relation suivante avec les chaînes de requête SQL utilisées par CREATe et ALTER.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-127">The strings used to describe columns have the following relationship to the SQL query strings used by CREATE and ALTER.</span></span> <span data-ttu-id="7f0fa-128">Pour plus d’informations, consultez [syntaxe SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="7f0fa-128">For more information, see [SQL Syntax](sql-syntax.md).</span></span>



| <span data-ttu-id="7f0fa-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7f0fa-129">Returned value</span></span> | <span data-ttu-id="7f0fa-130">Syntaxe SQL</span><span class="sxs-lookup"><span data-stu-id="7f0fa-130">SQL syntax</span></span>                |
|----------------|---------------------------|
| <span data-ttu-id="7f0fa-131">consommation</span><span class="sxs-lookup"><span data-stu-id="7f0fa-131">s0</span></span>             | <span data-ttu-id="7f0fa-132">LONGCHAR</span><span class="sxs-lookup"><span data-stu-id="7f0fa-132">LONGCHAR</span></span>                  |
| <span data-ttu-id="7f0fa-133">fusion</span><span class="sxs-lookup"><span data-stu-id="7f0fa-133">l0</span></span>             | <span data-ttu-id="7f0fa-134">LONGCHAR LOCALISABLE</span><span class="sxs-lookup"><span data-stu-id="7f0fa-134">LONGCHAR LOCALIZABLE</span></span>      |
| <span data-ttu-id="7f0fa-135">x \#</span><span class="sxs-lookup"><span data-stu-id="7f0fa-135">s \#</span></span>           | <span data-ttu-id="7f0fa-136">CHAR ( \# )</span><span class="sxs-lookup"><span data-stu-id="7f0fa-136">CHAR(\#)</span></span>                  |
| <span data-ttu-id="7f0fa-137">x \#</span><span class="sxs-lookup"><span data-stu-id="7f0fa-137">s \#</span></span>           | <span data-ttu-id="7f0fa-138">CARACTÈRE ( \# )</span><span class="sxs-lookup"><span data-stu-id="7f0fa-138">CHARACTER(\#)</span></span>             |
| <span data-ttu-id="7f0fa-139">budget \#</span><span class="sxs-lookup"><span data-stu-id="7f0fa-139">l \#</span></span>           | <span data-ttu-id="7f0fa-140">CHAR ( \# ) localisable</span><span class="sxs-lookup"><span data-stu-id="7f0fa-140">CHAR(\#) LOCALIZABLE</span></span>      |
| <span data-ttu-id="7f0fa-141">budget \#</span><span class="sxs-lookup"><span data-stu-id="7f0fa-141">l \#</span></span>           | <span data-ttu-id="7f0fa-142">CARACTÈRE ( \# ) localisable</span><span class="sxs-lookup"><span data-stu-id="7f0fa-142">CHARACTER(\#) LOCALIZABLE</span></span> |
| <span data-ttu-id="7f0fa-143">i2</span><span class="sxs-lookup"><span data-stu-id="7f0fa-143">i2</span></span>             | <span data-ttu-id="7f0fa-144">SHORT</span><span class="sxs-lookup"><span data-stu-id="7f0fa-144">SHORT</span></span>                     |
| <span data-ttu-id="7f0fa-145">i2</span><span class="sxs-lookup"><span data-stu-id="7f0fa-145">i2</span></span>             | <span data-ttu-id="7f0fa-146">INT</span><span class="sxs-lookup"><span data-stu-id="7f0fa-146">INT</span></span>                       |
| <span data-ttu-id="7f0fa-147">i2</span><span class="sxs-lookup"><span data-stu-id="7f0fa-147">i2</span></span>             | <span data-ttu-id="7f0fa-148">INTEGER</span><span class="sxs-lookup"><span data-stu-id="7f0fa-148">INTEGER</span></span>                   |
| <span data-ttu-id="7f0fa-149">i4</span><span class="sxs-lookup"><span data-stu-id="7f0fa-149">i4</span></span>             | <span data-ttu-id="7f0fa-150">LONG</span><span class="sxs-lookup"><span data-stu-id="7f0fa-150">LONG</span></span>                      |
| <span data-ttu-id="7f0fa-151">v0</span><span class="sxs-lookup"><span data-stu-id="7f0fa-151">v0</span></span>             | <span data-ttu-id="7f0fa-152">OBJECT</span><span class="sxs-lookup"><span data-stu-id="7f0fa-152">OBJECT</span></span>                    |



 

<span data-ttu-id="7f0fa-153">Si la lettre n’est pas en majuscule, l’instruction SQL doit être ajoutée avec NOT NULL.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-153">If the letter is not capitalized, the SQL statement should be appended with NOT NULL.</span></span>



| <span data-ttu-id="7f0fa-154">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7f0fa-154">Returned value</span></span> | <span data-ttu-id="7f0fa-155">Syntaxe SQL</span><span class="sxs-lookup"><span data-stu-id="7f0fa-155">SQL syntax</span></span>        |
|----------------|-------------------|
| <span data-ttu-id="7f0fa-156">consommation</span><span class="sxs-lookup"><span data-stu-id="7f0fa-156">s0</span></span>             | <span data-ttu-id="7f0fa-157">LONGCHAR NON NULL</span><span class="sxs-lookup"><span data-stu-id="7f0fa-157">LONGCHAR NOT NULL</span></span> |



 

<span data-ttu-id="7f0fa-158">Le programme d’installation ne limite pas en interne la longueur des colonnes à la valeur spécifiée par le format de définition de colonne.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-158">The installer does not internally limit the length of columns to the value specified by the column definition format.</span></span> <span data-ttu-id="7f0fa-159">Si les données entrées dans un champ dépassent la longueur de colonne spécifiée, le package ne réussit pas la [validation du package](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="7f0fa-159">If the data entered into a field exceeds the specified column length, the package fails to pass [package validation](package-validation.md).</span></span> <span data-ttu-id="7f0fa-160">Pour passer la validation dans ce cas, les données ou le schéma de base de données doivent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-160">To pass validation in this case, either the data or the database schema must be changed.</span></span> <span data-ttu-id="7f0fa-161">La seule méthode pour modifier la longueur de colonne d’une table standard consiste à exporter la table à l’aide de [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), à modifier le fichier. IDT exporté, puis à importer la table à l’aide de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="7f0fa-161">The only means to change the column length of a standard table is by exporting the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editing the exported .idt file, and then importing the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="7f0fa-162">Les auteurs ne peuvent pas modifier les types de données de colonne, les valeurs null ou les attributs de localisation des colonnes dans les tables standard.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-162">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="7f0fa-163">Les auteurs peuvent créer des tables personnalisées avec des colonnes ayant des attributs de colonne.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-163">Authors can create custom tables with columns having any column attributes.</span></span>

<span data-ttu-id="7f0fa-164">Lorsque vous utilisez [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) pour fusionner une base de données de référence dans une base de données cible, les noms de colonnes, le nombre de clés primaires et les types de données de colonne doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-164">When using [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to merge a reference database into a target database, the column names, number of primary keys, and column data types must match.</span></span> <span data-ttu-id="7f0fa-165">**MsiDatabaseMerge** ignore les attributs de localisation et de longueur de colonne.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-165">**MsiDatabaseMerge** ignores the localization and column length attributes.</span></span> <span data-ttu-id="7f0fa-166">Si une colonne de la base de données de référence a une longueur supérieure ou égale à la longueur de la colonne dans la base de données cible, **MsiDatabaseMerge** augmente la longueur de colonne dans la base de données cible à la longueur de la base de données de référence.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-166">If a column in the reference database has a length that is 0 or greater than the that column's length in the target database, **MsiDatabaseMerge** increases the column length in the target database to the length in the reference database.</span></span>

<span data-ttu-id="7f0fa-167">Lors de l’utilisation de Mergmod.dll version 2,0, l’application d’un module de fusion à un fichier. msi ne modifie jamais la longueur des colonnes ou les types de colonnes d’une table de base de données existante.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-167">When using Mergmod.dll version 2.0, the application of a merge module to a .msi file never changes the length of columns or the column types of an existing database table.</span></span> <span data-ttu-id="7f0fa-168">L’application d’un module de fusion peut toutefois modifier le schéma d’une table de base de données existante si le module ajoute de nouvelles colonnes à une table pour laquelle il est valide pour ajouter des colonnes.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-168">The application of a merge module can however change the schema of an existing database table if the module adds new columns to a table for which it is valid to add columns.</span></span> <span data-ttu-id="7f0fa-169">Lors de l’utilisation d’une version Mergemod.dll antérieure à la version 2,0, l’application d’un module de fusion ne modifie jamais la longueur des colonnes et ne modifie jamais le schéma de la base de données cible.</span><span class="sxs-lookup"><span data-stu-id="7f0fa-169">When using a Mergemod.dll version less than version 2.0, the application of a merge module never changes the length of columns and never changes the schema of the target database.</span></span>

 

 




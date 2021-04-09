---
description: La table IniFile contient les informations. ini que l’application doit définir dans un fichier. ini.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Table IniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034396"
---
# <a name="inifile-table"></a><span data-ttu-id="e1b19-103">Table IniFile</span><span class="sxs-lookup"><span data-stu-id="e1b19-103">IniFile Table</span></span>

<span data-ttu-id="e1b19-104">La table IniFile contient les informations. ini que l’application doit définir dans un fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="e1b19-104">The IniFile table contains the .ini information that the application needs to set in an .ini file.</span></span>

<span data-ttu-id="e1b19-105">La table IniFile contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1b19-105">The IniFile table has the following columns.</span></span>



| <span data-ttu-id="e1b19-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="e1b19-106">Column</span></span>      | <span data-ttu-id="e1b19-107">Type</span><span class="sxs-lookup"><span data-stu-id="e1b19-107">Type</span></span>                         | <span data-ttu-id="e1b19-108">Clé</span><span class="sxs-lookup"><span data-stu-id="e1b19-108">Key</span></span> | <span data-ttu-id="e1b19-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="e1b19-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="e1b19-110">IniFile</span><span class="sxs-lookup"><span data-stu-id="e1b19-110">IniFile</span></span>     | [<span data-ttu-id="e1b19-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="e1b19-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="e1b19-112">O</span><span class="sxs-lookup"><span data-stu-id="e1b19-112">Y</span></span>   | <span data-ttu-id="e1b19-113">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-113">N</span></span>        |
| <span data-ttu-id="e1b19-114">FileName</span><span class="sxs-lookup"><span data-stu-id="e1b19-114">FileName</span></span>    | [<span data-ttu-id="e1b19-115">FileName</span><span class="sxs-lookup"><span data-stu-id="e1b19-115">FileName</span></span>](text.md)         | <span data-ttu-id="e1b19-116">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-116">N</span></span>   | <span data-ttu-id="e1b19-117">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-117">N</span></span>        |
| <span data-ttu-id="e1b19-118">DirProperty</span><span class="sxs-lookup"><span data-stu-id="e1b19-118">DirProperty</span></span> | [<span data-ttu-id="e1b19-119">Identificateur</span><span class="sxs-lookup"><span data-stu-id="e1b19-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="e1b19-120">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-120">N</span></span>   | <span data-ttu-id="e1b19-121">O</span><span class="sxs-lookup"><span data-stu-id="e1b19-121">Y</span></span>        |
| <span data-ttu-id="e1b19-122">Section</span><span class="sxs-lookup"><span data-stu-id="e1b19-122">Section</span></span>     | [<span data-ttu-id="e1b19-123">Correct</span><span class="sxs-lookup"><span data-stu-id="e1b19-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e1b19-124">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-124">N</span></span>   | <span data-ttu-id="e1b19-125">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-125">N</span></span>        |
| <span data-ttu-id="e1b19-126">Clé</span><span class="sxs-lookup"><span data-stu-id="e1b19-126">Key</span></span>         | [<span data-ttu-id="e1b19-127">Correct</span><span class="sxs-lookup"><span data-stu-id="e1b19-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e1b19-128">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-128">N</span></span>   | <span data-ttu-id="e1b19-129">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-129">N</span></span>        |
| <span data-ttu-id="e1b19-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b19-130">Value</span></span>       | [<span data-ttu-id="e1b19-131">Correct</span><span class="sxs-lookup"><span data-stu-id="e1b19-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e1b19-132">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-132">N</span></span>   | <span data-ttu-id="e1b19-133">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-133">N</span></span>        |
| <span data-ttu-id="e1b19-134">Action</span><span class="sxs-lookup"><span data-stu-id="e1b19-134">Action</span></span>      | [<span data-ttu-id="e1b19-135">Integer</span><span class="sxs-lookup"><span data-stu-id="e1b19-135">Integer</span></span>](integer.md)       | <span data-ttu-id="e1b19-136">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-136">N</span></span>   | <span data-ttu-id="e1b19-137">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-137">N</span></span>        |
| <span data-ttu-id="e1b19-138">-\_</span><span class="sxs-lookup"><span data-stu-id="e1b19-138">Component\_</span></span> | [<span data-ttu-id="e1b19-139">Identificateur</span><span class="sxs-lookup"><span data-stu-id="e1b19-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="e1b19-140">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-140">N</span></span>   | <span data-ttu-id="e1b19-141">N</span><span class="sxs-lookup"><span data-stu-id="e1b19-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e1b19-142">Colonnes</span><span class="sxs-lookup"><span data-stu-id="e1b19-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e1b19-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span><span class="sxs-lookup"><span data-stu-id="e1b19-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span></span>
</dt> <dd>

<span data-ttu-id="e1b19-144">Clé de cette table.</span><span class="sxs-lookup"><span data-stu-id="e1b19-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension</span><span class="sxs-lookup"><span data-stu-id="e1b19-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="e1b19-146">Nom localisable du fichier. ini dans lequel les informations doivent être écrites.</span><span class="sxs-lookup"><span data-stu-id="e1b19-146">The localizable name of the .ini file in which to write the information.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="e1b19-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="e1b19-148">Nom d’une propriété ayant une valeur qui correspond au chemin d’accès complet du dossier contenant le fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="e1b19-148">Name of a property having a value that resolves to the full path of the folder containing the .ini file.</span></span> <span data-ttu-id="e1b19-149">La propriété peut être le nom d’un répertoire dans la [table de répertoires](directory-table.md), une propriété définie par la [table AppSearch](appsearch-table.md), ou toute autre propriété qui représente un chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="e1b19-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span> <span data-ttu-id="e1b19-150">Si ce champ est laissé vide, le fichier. ini est créé dans le dossier avec le chemin d’accès complet spécifié par la propriété [**WindowsFolder**](windowsfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="e1b19-150">If this field is left blank, the .ini file is created in the folder having the full path specified by the [**WindowsFolder**](windowsfolder.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span><span class="sxs-lookup"><span data-stu-id="e1b19-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="e1b19-152">Section du fichier. ini localisable.</span><span class="sxs-lookup"><span data-stu-id="e1b19-152">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel</span><span class="sxs-lookup"><span data-stu-id="e1b19-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="e1b19-154">Clé du fichier. ini localisable dans la section.</span><span class="sxs-lookup"><span data-stu-id="e1b19-154">The localizable .ini file key within the section.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="e1b19-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="e1b19-156">Valeur localisable à écrire.</span><span class="sxs-lookup"><span data-stu-id="e1b19-156">The localizable value to be written.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="e1b19-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="e1b19-158">Type de modification à effectuer.</span><span class="sxs-lookup"><span data-stu-id="e1b19-158">The type of modification to be made.</span></span>



| <span data-ttu-id="e1b19-159">Constante</span><span class="sxs-lookup"><span data-stu-id="e1b19-159">Constant</span></span>                         | <span data-ttu-id="e1b19-160">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="e1b19-160">Hexadecimal</span></span> | <span data-ttu-id="e1b19-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="e1b19-161">Decimal</span></span> | <span data-ttu-id="e1b19-162">Modification</span><span class="sxs-lookup"><span data-stu-id="e1b19-162">Modification</span></span>                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1b19-163">**msidbIniFileActionAddLine**</span><span class="sxs-lookup"><span data-stu-id="e1b19-163">**msidbIniFileActionAddLine**</span></span>    | <span data-ttu-id="e1b19-164">0x000</span><span class="sxs-lookup"><span data-stu-id="e1b19-164">0x000</span></span>       | <span data-ttu-id="e1b19-165">0</span><span class="sxs-lookup"><span data-stu-id="e1b19-165">0</span></span>       | <span data-ttu-id="e1b19-166">Crée ou met à jour une entrée. ini.</span><span class="sxs-lookup"><span data-stu-id="e1b19-166">Creates or updates a .ini entry.</span></span>                                                 |
| <span data-ttu-id="e1b19-167">**msidbIniFileActionCreateLine**</span><span class="sxs-lookup"><span data-stu-id="e1b19-167">**msidbIniFileActionCreateLine**</span></span> | <span data-ttu-id="e1b19-168">0x001</span><span class="sxs-lookup"><span data-stu-id="e1b19-168">0x001</span></span>       | <span data-ttu-id="e1b19-169">1</span><span class="sxs-lookup"><span data-stu-id="e1b19-169">1</span></span>       | <span data-ttu-id="e1b19-170">Crée une entrée. ini uniquement si l’entrée n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="e1b19-170">Creates a .ini entry only if the entry does not already exist.</span></span>                   |
| <span data-ttu-id="e1b19-171">**msidbIniFileActionAddTag**</span><span class="sxs-lookup"><span data-stu-id="e1b19-171">**msidbIniFileActionAddTag**</span></span>     | <span data-ttu-id="e1b19-172">0x003</span><span class="sxs-lookup"><span data-stu-id="e1b19-172">0x003</span></span>       | <span data-ttu-id="e1b19-173">3</span><span class="sxs-lookup"><span data-stu-id="e1b19-173">3</span></span>       | <span data-ttu-id="e1b19-174">Crée une entrée ou ajoute une nouvelle valeur séparée par des virgules à une entrée existante.</span><span class="sxs-lookup"><span data-stu-id="e1b19-174">Creates a new entry or appends a new comma-separated value to an existing entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e1b19-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="e1b19-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="e1b19-176">Clé externe dans la première colonne de la [table de composants](component-table.md) référençant le composant qui contrôle l’installation de la valeur. ini.</span><span class="sxs-lookup"><span data-stu-id="e1b19-176">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1b19-177">Notes</span><span class="sxs-lookup"><span data-stu-id="e1b19-177">Remarks</span></span>

<span data-ttu-id="e1b19-178">Les informations du fichier. ini sont écrites lorsque le composant correspondant a été sélectionné pour être installé en local ou exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="e1b19-178">The .ini file information is written out when the corresponding component has been selected to be installed as local or run from source.</span></span>

<span data-ttu-id="e1b19-179">Cette table est référencée lorsque l' [action WriteIniValues](writeinivalues-action.md) ou l' [action RemoveIniValues](removeinivalues-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="e1b19-179">This table is referred to when the [WriteIniValues action](writeinivalues-action.md) or the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="e1b19-180">Validation</span><span class="sxs-lookup"><span data-stu-id="e1b19-180">Validation</span></span>

<dl>

[<span data-ttu-id="e1b19-181">ICE03</span><span class="sxs-lookup"><span data-stu-id="e1b19-181">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e1b19-182">ICE06</span><span class="sxs-lookup"><span data-stu-id="e1b19-182">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e1b19-183">ICE32</span><span class="sxs-lookup"><span data-stu-id="e1b19-183">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e1b19-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="e1b19-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="e1b19-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="e1b19-185">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="e1b19-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="e1b19-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="e1b19-187">ICE91</span><span class="sxs-lookup"><span data-stu-id="e1b19-187">ICE91</span></span>](ice91.md)  
</dl>

 

 




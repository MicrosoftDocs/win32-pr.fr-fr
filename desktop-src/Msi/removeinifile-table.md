---
description: La table RemoveIniFile contient les informations qu’une application doit supprimer d’un fichier. ini.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Table RemoveIniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542013"
---
# <a name="removeinifile-table"></a><span data-ttu-id="b7c29-103">Table RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="b7c29-103">RemoveIniFile Table</span></span>

<span data-ttu-id="b7c29-104">La table RemoveIniFile contient les informations qu’une application doit supprimer d’un fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="b7c29-104">The RemoveIniFile table contains the information an application needs to delete from a .ini file.</span></span>

<span data-ttu-id="b7c29-105">La table RemoveIniFile contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7c29-105">The RemoveIniFile table has the following columns.</span></span>



| <span data-ttu-id="b7c29-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="b7c29-106">Column</span></span>        | <span data-ttu-id="b7c29-107">Type</span><span class="sxs-lookup"><span data-stu-id="b7c29-107">Type</span></span>                         | <span data-ttu-id="b7c29-108">Clé</span><span class="sxs-lookup"><span data-stu-id="b7c29-108">Key</span></span> | <span data-ttu-id="b7c29-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="b7c29-109">Nullable</span></span> |
|---------------|------------------------------|-----|----------|
| <span data-ttu-id="b7c29-110">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="b7c29-110">RemoveIniFile</span></span> | [<span data-ttu-id="b7c29-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b7c29-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="b7c29-112">O</span><span class="sxs-lookup"><span data-stu-id="b7c29-112">Y</span></span>   | <span data-ttu-id="b7c29-113">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-113">N</span></span>        |
| <span data-ttu-id="b7c29-114">FileName</span><span class="sxs-lookup"><span data-stu-id="b7c29-114">FileName</span></span>      | [<span data-ttu-id="b7c29-115">FileName</span><span class="sxs-lookup"><span data-stu-id="b7c29-115">FileName</span></span>](text.md)         | <span data-ttu-id="b7c29-116">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-116">N</span></span>   | <span data-ttu-id="b7c29-117">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-117">N</span></span>        |
| <span data-ttu-id="b7c29-118">DirProperty</span><span class="sxs-lookup"><span data-stu-id="b7c29-118">DirProperty</span></span>   | [<span data-ttu-id="b7c29-119">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b7c29-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="b7c29-120">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-120">N</span></span>   | <span data-ttu-id="b7c29-121">O</span><span class="sxs-lookup"><span data-stu-id="b7c29-121">Y</span></span>        |
| <span data-ttu-id="b7c29-122">Section</span><span class="sxs-lookup"><span data-stu-id="b7c29-122">Section</span></span>       | [<span data-ttu-id="b7c29-123">Correct</span><span class="sxs-lookup"><span data-stu-id="b7c29-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b7c29-124">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-124">N</span></span>   | <span data-ttu-id="b7c29-125">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-125">N</span></span>        |
| <span data-ttu-id="b7c29-126">Clé</span><span class="sxs-lookup"><span data-stu-id="b7c29-126">Key</span></span>           | [<span data-ttu-id="b7c29-127">Correct</span><span class="sxs-lookup"><span data-stu-id="b7c29-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b7c29-128">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-128">N</span></span>   | <span data-ttu-id="b7c29-129">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-129">N</span></span>        |
| <span data-ttu-id="b7c29-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7c29-130">Value</span></span>         | [<span data-ttu-id="b7c29-131">Correct</span><span class="sxs-lookup"><span data-stu-id="b7c29-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b7c29-132">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-132">N</span></span>   | <span data-ttu-id="b7c29-133">O</span><span class="sxs-lookup"><span data-stu-id="b7c29-133">Y</span></span>        |
| <span data-ttu-id="b7c29-134">Action</span><span class="sxs-lookup"><span data-stu-id="b7c29-134">Action</span></span>        | [<span data-ttu-id="b7c29-135">Integer</span><span class="sxs-lookup"><span data-stu-id="b7c29-135">Integer</span></span>](integer.md)       | <span data-ttu-id="b7c29-136">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-136">N</span></span>   | <span data-ttu-id="b7c29-137">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-137">N</span></span>        |
| <span data-ttu-id="b7c29-138">-\_</span><span class="sxs-lookup"><span data-stu-id="b7c29-138">Component\_</span></span>   | [<span data-ttu-id="b7c29-139">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b7c29-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="b7c29-140">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-140">N</span></span>   | <span data-ttu-id="b7c29-141">N</span><span class="sxs-lookup"><span data-stu-id="b7c29-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b7c29-142">Colonnes</span><span class="sxs-lookup"><span data-stu-id="b7c29-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b7c29-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="b7c29-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span></span>
</dt> <dd>

<span data-ttu-id="b7c29-144">Clé de cette table.</span><span class="sxs-lookup"><span data-stu-id="b7c29-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="b7c29-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension</span><span class="sxs-lookup"><span data-stu-id="b7c29-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="b7c29-146">Nom du fichier. ini dans lequel supprimer les informations.</span><span class="sxs-lookup"><span data-stu-id="b7c29-146">The .ini file name in which to delete the information.</span></span>

</dd> <dt>

<span data-ttu-id="b7c29-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="b7c29-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="b7c29-148">Nom d’une propriété dont la valeur est supposée correspondre au chemin d’accès complet au dossier du fichier. ini à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b7c29-148">Name of a property whose value is assumed to resolve to the full path to the folder of the .ini file to be removed.</span></span> <span data-ttu-id="b7c29-149">La propriété peut être le nom d’un répertoire dans la [table de répertoires](directory-table.md), une propriété définie par la [table AppSearch](appsearch-table.md), ou toute autre propriété qui représente un chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="b7c29-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="b7c29-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span><span class="sxs-lookup"><span data-stu-id="b7c29-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="b7c29-151">Section du fichier. ini localisable.</span><span class="sxs-lookup"><span data-stu-id="b7c29-151">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="b7c29-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel</span><span class="sxs-lookup"><span data-stu-id="b7c29-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="b7c29-153">La clé du fichier. ini localisable sous la section.</span><span class="sxs-lookup"><span data-stu-id="b7c29-153">The localizable .ini file key below the section.</span></span>

</dd> <dt>

<span data-ttu-id="b7c29-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="b7c29-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="b7c29-155">Valeur localisable à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b7c29-155">The localizable value to be deleted.</span></span> <span data-ttu-id="b7c29-156">La valeur est obligatoire lorsque action a la valeur 4.</span><span class="sxs-lookup"><span data-stu-id="b7c29-156">The value is required when Action is 4.</span></span>

</dd> <dt>

<span data-ttu-id="b7c29-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="b7c29-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="b7c29-158">Type de modification à effectuer.</span><span class="sxs-lookup"><span data-stu-id="b7c29-158">The type of modification to be made.</span></span>



| <span data-ttu-id="b7c29-159">Constante</span><span class="sxs-lookup"><span data-stu-id="b7c29-159">Constant</span></span>                         | <span data-ttu-id="b7c29-160">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="b7c29-160">Hexadecimal</span></span> | <span data-ttu-id="b7c29-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="b7c29-161">Decimal</span></span> | <span data-ttu-id="b7c29-162">Signification</span><span class="sxs-lookup"><span data-stu-id="b7c29-162">Meaning</span></span>                          |
|----------------------------------|-------------|---------|----------------------------------|
| <span data-ttu-id="b7c29-163">**msidbIniFileActionRemoveLine**</span><span class="sxs-lookup"><span data-stu-id="b7c29-163">**msidbIniFileActionRemoveLine**</span></span> | <span data-ttu-id="b7c29-164">0x002</span><span class="sxs-lookup"><span data-stu-id="b7c29-164">0x002</span></span>       | <span data-ttu-id="b7c29-165">2</span><span class="sxs-lookup"><span data-stu-id="b7c29-165">2</span></span>       | <span data-ttu-id="b7c29-166">Supprime l’entrée. ini.</span><span class="sxs-lookup"><span data-stu-id="b7c29-166">Deletes .ini entry.</span></span>              |
| <span data-ttu-id="b7c29-167">**msidbIniFileActionRemoveTag**</span><span class="sxs-lookup"><span data-stu-id="b7c29-167">**msidbIniFileActionRemoveTag**</span></span>  | <span data-ttu-id="b7c29-168">0x004</span><span class="sxs-lookup"><span data-stu-id="b7c29-168">0x004</span></span>       | <span data-ttu-id="b7c29-169">4</span><span class="sxs-lookup"><span data-stu-id="b7c29-169">4</span></span>       | <span data-ttu-id="b7c29-170">Supprime une balise d’une entrée. ini.</span><span class="sxs-lookup"><span data-stu-id="b7c29-170">Deletes a tag from a .ini entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b7c29-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="b7c29-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="b7c29-172">Clé externe dans la première colonne de la [table de composants](component-table.md) référençant le composant qui contrôle la suppression de la valeur. ini.</span><span class="sxs-lookup"><span data-stu-id="b7c29-172">External key into first column of the [Component table](component-table.md) referencing the component that controls the deletion of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7c29-173">Notes</span><span class="sxs-lookup"><span data-stu-id="b7c29-173">Remarks</span></span>

<span data-ttu-id="b7c29-174">Les informations du fichier. ini sont supprimées lorsque le composant correspondant a été sélectionné pour être installé, localement ou exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="b7c29-174">The .ini file information is deleted when the corresponding Component has been selected to be installed, either locally or run from source.</span></span>

<span data-ttu-id="b7c29-175">Cette table est référencée lorsque l' [action RemoveIniValues](removeinivalues-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="b7c29-175">This table is referred to when the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

<span data-ttu-id="b7c29-176">Si la colonne de répertoire \_ est spécifiée comme étant null, l’emplacement du fichier ini est l’emplacement du fichier ini Windows standard qui est le répertoire Windows par défaut.</span><span class="sxs-lookup"><span data-stu-id="b7c29-176">If the Directory\_ column is specified as null, the ini file location is the standard Windows ini location which is the Windows directory by default.</span></span>

<span data-ttu-id="b7c29-177">La suppression de la dernière valeur d’une section supprime cette section.</span><span class="sxs-lookup"><span data-stu-id="b7c29-177">Removing the last value from a section deletes that section.</span></span> <span data-ttu-id="b7c29-178">Il n’existe aucune autre façon de supprimer toute une section autre que la suppression de toutes ses valeurs.</span><span class="sxs-lookup"><span data-stu-id="b7c29-178">There is no other way to delete an entire section other than removing all its values.</span></span>

## <a name="validation"></a><span data-ttu-id="b7c29-179">Validation</span><span class="sxs-lookup"><span data-stu-id="b7c29-179">Validation</span></span>

<dl>

[<span data-ttu-id="b7c29-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="b7c29-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b7c29-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="b7c29-181">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b7c29-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="b7c29-182">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b7c29-183">ICE40</span><span class="sxs-lookup"><span data-stu-id="b7c29-183">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="b7c29-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="b7c29-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="b7c29-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="b7c29-185">ICE69</span></span>](ice69.md)  
</dl>

 

 




---
description: Cette table contient la liste des fichiers à déplacer ou à copier à partir d’un répertoire source spécifié vers un répertoire de destination spécifié.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: Table MoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2340626e745627c3c6146998c851a076d21ab81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760167"
---
# <a name="movefile-table"></a><span data-ttu-id="114d0-103">Table MoveFile</span><span class="sxs-lookup"><span data-stu-id="114d0-103">MoveFile Table</span></span>

<span data-ttu-id="114d0-104">Cette table contient la liste des fichiers à déplacer ou à copier à partir d’un répertoire source spécifié vers un répertoire de destination spécifié.</span><span class="sxs-lookup"><span data-stu-id="114d0-104">This table contains a list of files to be moved or copied from a specified source directory to a specified destination directory.</span></span>

<span data-ttu-id="114d0-105">La table MoveFile contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="114d0-105">The MoveFile table has the following columns.</span></span>



| <span data-ttu-id="114d0-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="114d0-106">Column</span></span>       | <span data-ttu-id="114d0-107">Type</span><span class="sxs-lookup"><span data-stu-id="114d0-107">Type</span></span>                         | <span data-ttu-id="114d0-108">Clé</span><span class="sxs-lookup"><span data-stu-id="114d0-108">Key</span></span> | <span data-ttu-id="114d0-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="114d0-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="114d0-110">FileKey</span><span class="sxs-lookup"><span data-stu-id="114d0-110">FileKey</span></span>      | [<span data-ttu-id="114d0-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="114d0-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="114d0-112">O</span><span class="sxs-lookup"><span data-stu-id="114d0-112">Y</span></span>   | <span data-ttu-id="114d0-113">N</span><span class="sxs-lookup"><span data-stu-id="114d0-113">N</span></span>        |
| <span data-ttu-id="114d0-114">-\_</span><span class="sxs-lookup"><span data-stu-id="114d0-114">Component\_</span></span>  | [<span data-ttu-id="114d0-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="114d0-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="114d0-116">N</span><span class="sxs-lookup"><span data-stu-id="114d0-116">N</span></span>   | <span data-ttu-id="114d0-117">N</span><span class="sxs-lookup"><span data-stu-id="114d0-117">N</span></span>        |
| <span data-ttu-id="114d0-118">SourceName</span><span class="sxs-lookup"><span data-stu-id="114d0-118">SourceName</span></span>   | [<span data-ttu-id="114d0-119">Text</span><span class="sxs-lookup"><span data-stu-id="114d0-119">Text</span></span>](text.md)             | <span data-ttu-id="114d0-120">N</span><span class="sxs-lookup"><span data-stu-id="114d0-120">N</span></span>   | <span data-ttu-id="114d0-121">O</span><span class="sxs-lookup"><span data-stu-id="114d0-121">Y</span></span>        |
| <span data-ttu-id="114d0-122">DestName</span><span class="sxs-lookup"><span data-stu-id="114d0-122">DestName</span></span>     | [<span data-ttu-id="114d0-123">Nom du fichier</span><span class="sxs-lookup"><span data-stu-id="114d0-123">Filename</span></span>](filename.md)     | <span data-ttu-id="114d0-124">N</span><span class="sxs-lookup"><span data-stu-id="114d0-124">N</span></span>   | <span data-ttu-id="114d0-125">O</span><span class="sxs-lookup"><span data-stu-id="114d0-125">Y</span></span>        |
| <span data-ttu-id="114d0-126">SourceFolder</span><span class="sxs-lookup"><span data-stu-id="114d0-126">SourceFolder</span></span> | [<span data-ttu-id="114d0-127">Identificateur</span><span class="sxs-lookup"><span data-stu-id="114d0-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="114d0-128">N</span><span class="sxs-lookup"><span data-stu-id="114d0-128">N</span></span>   | <span data-ttu-id="114d0-129">O</span><span class="sxs-lookup"><span data-stu-id="114d0-129">Y</span></span>        |
| <span data-ttu-id="114d0-130">DestFolder</span><span class="sxs-lookup"><span data-stu-id="114d0-130">DestFolder</span></span>   | [<span data-ttu-id="114d0-131">Identificateur</span><span class="sxs-lookup"><span data-stu-id="114d0-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="114d0-132">N</span><span class="sxs-lookup"><span data-stu-id="114d0-132">N</span></span>   | <span data-ttu-id="114d0-133">N</span><span class="sxs-lookup"><span data-stu-id="114d0-133">N</span></span>        |
| <span data-ttu-id="114d0-134">Options</span><span class="sxs-lookup"><span data-stu-id="114d0-134">Options</span></span>      | [<span data-ttu-id="114d0-135">Integer</span><span class="sxs-lookup"><span data-stu-id="114d0-135">Integer</span></span>](integer.md)       | <span data-ttu-id="114d0-136">N</span><span class="sxs-lookup"><span data-stu-id="114d0-136">N</span></span>   | <span data-ttu-id="114d0-137">N</span><span class="sxs-lookup"><span data-stu-id="114d0-137">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="114d0-138">Colonnes</span><span class="sxs-lookup"><span data-stu-id="114d0-138">Columns</span></span>

<dl> <dt>

<span data-ttu-id="114d0-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="114d0-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="114d0-140">Clé primaire qui identifie de façon unique un enregistrement MoveFile particulier.</span><span class="sxs-lookup"><span data-stu-id="114d0-140">Primary key that uniquely identifies a particular MoveFile record.</span></span>

</dd> <dt>

<span data-ttu-id="114d0-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="114d0-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="114d0-142">Clé externe dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="114d0-142">External key into the [Component table](component-table.md).</span></span> <span data-ttu-id="114d0-143">Si le composant référencé par cette clé n’est pas sélectionné pour l’installation ou la suppression, aucune action n’est effectuée sur cette entrée MoveFile.</span><span class="sxs-lookup"><span data-stu-id="114d0-143">If the component referenced by this key is not selected for installation or removal, then no action is taken on this MoveFile entry.</span></span>

</dd> <dt>

<span data-ttu-id="114d0-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span><span class="sxs-lookup"><span data-stu-id="114d0-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span></span>
</dt> <dd>

<span data-ttu-id="114d0-145">Cette colonne contient le nom localisable des fichiers sources à déplacer ou copier.</span><span class="sxs-lookup"><span data-stu-id="114d0-145">This column contains the localizable name of the source files to be moved or copied.</span></span> <span data-ttu-id="114d0-146">Cette colonne peut être laissée vide.</span><span class="sxs-lookup"><span data-stu-id="114d0-146">This column may be left blank.</span></span> <span data-ttu-id="114d0-147">Consultez la description de la colonne SourceFolder.</span><span class="sxs-lookup"><span data-stu-id="114d0-147">See the description of the SourceFolder column.</span></span> <span data-ttu-id="114d0-148">Ce champ doit contenir un nom de fichier long et peut contenir des caractères génériques ( \* et ?).</span><span class="sxs-lookup"><span data-stu-id="114d0-148">This field must contain a long file name and may contain wildcard characters (\* and ?).</span></span>

</dd> <dt>

<span data-ttu-id="114d0-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span><span class="sxs-lookup"><span data-stu-id="114d0-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="114d0-150">Cette colonne contient le nom localisable à attribuer au fichier d’origine après qu’il a été déplacé ou copié.</span><span class="sxs-lookup"><span data-stu-id="114d0-150">This column contains the localizable name to be given to the original file after it is moved or copied.</span></span> <span data-ttu-id="114d0-151">Si ce champ est vide, le nom du fichier de destination est le même que celui du fichier source.</span><span class="sxs-lookup"><span data-stu-id="114d0-151">If this field is blank, then the destination file is given the same name as the source file.</span></span>

</dd> <dt>

<span data-ttu-id="114d0-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span><span class="sxs-lookup"><span data-stu-id="114d0-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span></span>
</dt> <dd>

<span data-ttu-id="114d0-153">Cette colonne contient le nom d’une propriété ayant une valeur qui correspond au chemin d’accès complet au répertoire source.</span><span class="sxs-lookup"><span data-stu-id="114d0-153">This column contains the name of a property having a value that resolves to the full path to the source directory.</span></span> <span data-ttu-id="114d0-154">Si la colonne SourceName est laissée vide, la propriété nommée dans la colonne SourceFolder est supposée contenir le chemin d’accès complet au fichier source lui-même (y compris le nom du fichier).</span><span class="sxs-lookup"><span data-stu-id="114d0-154">If the SourceName column is left blank, then the property named in the SourceFolder column is assumed to contain the full path to the source file itself (including the file name).</span></span>

</dd> <dt>

<span data-ttu-id="114d0-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="114d0-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="114d0-156">Nom d’une propriété dont la valeur correspond au chemin d’accès complet au répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="114d0-156">The name of a property whose value resolves to the full path to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="114d0-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span><span class="sxs-lookup"><span data-stu-id="114d0-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="114d0-158">Valeur entière spécifiant le mode d’opération.</span><span class="sxs-lookup"><span data-stu-id="114d0-158">Integer value specifying the operating mode.</span></span>



| <span data-ttu-id="114d0-159">Constante</span><span class="sxs-lookup"><span data-stu-id="114d0-159">Constant</span></span>                     | <span data-ttu-id="114d0-160">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="114d0-160">Hexadecimal</span></span> | <span data-ttu-id="114d0-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="114d0-161">Decimal</span></span> | <span data-ttu-id="114d0-162">Signification</span><span class="sxs-lookup"><span data-stu-id="114d0-162">Meaning</span></span>               |
|------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="114d0-163">(aucun)</span><span class="sxs-lookup"><span data-stu-id="114d0-163">(none)</span></span>                       | <span data-ttu-id="114d0-164">0x000</span><span class="sxs-lookup"><span data-stu-id="114d0-164">0x000</span></span>       | <span data-ttu-id="114d0-165">0</span><span class="sxs-lookup"><span data-stu-id="114d0-165">0</span></span>       | <span data-ttu-id="114d0-166">Copiez le fichier source.</span><span class="sxs-lookup"><span data-stu-id="114d0-166">Copy the source file.</span></span> |
| <span data-ttu-id="114d0-167">**msidbMoveFileOptionsMove**</span><span class="sxs-lookup"><span data-stu-id="114d0-167">**msidbMoveFileOptionsMove**</span></span> | <span data-ttu-id="114d0-168">0x001</span><span class="sxs-lookup"><span data-stu-id="114d0-168">0x001</span></span>       | <span data-ttu-id="114d0-169">1</span><span class="sxs-lookup"><span data-stu-id="114d0-169">1</span></span>       | <span data-ttu-id="114d0-170">Déplacez le fichier source.</span><span class="sxs-lookup"><span data-stu-id="114d0-170">Move the source file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="114d0-171">Notes</span><span class="sxs-lookup"><span data-stu-id="114d0-171">Remarks</span></span>

<span data-ttu-id="114d0-172">Si un \* caractère générique «» est entré dans la colonne SourceName de la table MoveFile et qu’un nom de fichier de destination est spécifié dans la colonne DestName, tous les fichiers déplacés ou copiés conservent les noms dans les sources.</span><span class="sxs-lookup"><span data-stu-id="114d0-172">If a "\*" wildcard is entered in the SourceName column of the MoveFile table and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="114d0-173">Cette table est traitée par l' [action MoveFiles](movefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="114d0-173">This table is processed by the [MoveFiles action](movefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="114d0-174">Validation</span><span class="sxs-lookup"><span data-stu-id="114d0-174">Validation</span></span>

<dl>

[<span data-ttu-id="114d0-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="114d0-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="114d0-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="114d0-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="114d0-177">ICE18</span><span class="sxs-lookup"><span data-stu-id="114d0-177">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="114d0-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="114d0-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="114d0-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="114d0-179">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="114d0-180">ICE85</span><span class="sxs-lookup"><span data-stu-id="114d0-180">ICE85</span></span>](ice85.md)  
</dl>

 

 




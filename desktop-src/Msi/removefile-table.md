---
description: La table RemoveFile contient une liste de fichiers à supprimer par l’action RemoveFiles. L’affectation de la valeur null à la colonne FileName de cette table prend en charge la suppression des dossiers vides.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Table RemoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723e42582821d79842686678c5b310e95cd1e944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866714"
---
# <a name="removefile-table"></a><span data-ttu-id="bcd7a-104">Table RemoveFile</span><span class="sxs-lookup"><span data-stu-id="bcd7a-104">RemoveFile Table</span></span>

<span data-ttu-id="bcd7a-105">La table RemoveFile contient une liste de fichiers à supprimer par l' [action RemoveFiles](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="bcd7a-105">The RemoveFile table contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span> <span data-ttu-id="bcd7a-106">L’affectation de la valeur null à la colonne FileName de cette table prend en charge la suppression des dossiers vides.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-106">Setting the FileName column of this table to Null supports the removal of empty folders.</span></span>

<span data-ttu-id="bcd7a-107">La table RemoveFile contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-107">The RemoveFile table has the following columns.</span></span>



| <span data-ttu-id="bcd7a-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="bcd7a-108">Column</span></span>      | <span data-ttu-id="bcd7a-109">Type</span><span class="sxs-lookup"><span data-stu-id="bcd7a-109">Type</span></span>                                     | <span data-ttu-id="bcd7a-110">Clé</span><span class="sxs-lookup"><span data-stu-id="bcd7a-110">Key</span></span> | <span data-ttu-id="bcd7a-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="bcd7a-111">Nullable</span></span> |
|-------------|------------------------------------------|-----|----------|
| <span data-ttu-id="bcd7a-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="bcd7a-112">FileKey</span></span>     | [<span data-ttu-id="bcd7a-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="bcd7a-113">Identifier</span></span>](identifier.md)             | <span data-ttu-id="bcd7a-114">O</span><span class="sxs-lookup"><span data-stu-id="bcd7a-114">Y</span></span>   | <span data-ttu-id="bcd7a-115">N</span><span class="sxs-lookup"><span data-stu-id="bcd7a-115">N</span></span>        |
| <span data-ttu-id="bcd7a-116">-\_</span><span class="sxs-lookup"><span data-stu-id="bcd7a-116">Component\_</span></span> | [<span data-ttu-id="bcd7a-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="bcd7a-117">Identifier</span></span>](identifier.md)             | <span data-ttu-id="bcd7a-118">N</span><span class="sxs-lookup"><span data-stu-id="bcd7a-118">N</span></span>   | <span data-ttu-id="bcd7a-119">N</span><span class="sxs-lookup"><span data-stu-id="bcd7a-119">N</span></span>        |
| <span data-ttu-id="bcd7a-120">FileName</span><span class="sxs-lookup"><span data-stu-id="bcd7a-120">FileName</span></span>    | [<span data-ttu-id="bcd7a-121">WildCardFilename</span><span class="sxs-lookup"><span data-stu-id="bcd7a-121">WildCardFilename</span></span>](wildcardfilename.md) | <span data-ttu-id="bcd7a-122">N</span><span class="sxs-lookup"><span data-stu-id="bcd7a-122">N</span></span>   | <span data-ttu-id="bcd7a-123">O</span><span class="sxs-lookup"><span data-stu-id="bcd7a-123">Y</span></span>        |
| <span data-ttu-id="bcd7a-124">DirProperty</span><span class="sxs-lookup"><span data-stu-id="bcd7a-124">DirProperty</span></span> | [<span data-ttu-id="bcd7a-125">Identificateur</span><span class="sxs-lookup"><span data-stu-id="bcd7a-125">Identifier</span></span>](identifier.md)             | <span data-ttu-id="bcd7a-126">N</span><span class="sxs-lookup"><span data-stu-id="bcd7a-126">N</span></span>   | <span data-ttu-id="bcd7a-127">N</span><span class="sxs-lookup"><span data-stu-id="bcd7a-127">N</span></span>        |
| <span data-ttu-id="bcd7a-128">InstallMode</span><span class="sxs-lookup"><span data-stu-id="bcd7a-128">InstallMode</span></span> | [<span data-ttu-id="bcd7a-129">Integer</span><span class="sxs-lookup"><span data-stu-id="bcd7a-129">Integer</span></span>](integer.md)                   | <span data-ttu-id="bcd7a-130">N</span><span class="sxs-lookup"><span data-stu-id="bcd7a-130">N</span></span>   | <span data-ttu-id="bcd7a-131">N</span><span class="sxs-lookup"><span data-stu-id="bcd7a-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="bcd7a-132">Colonnes</span><span class="sxs-lookup"><span data-stu-id="bcd7a-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="bcd7a-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="bcd7a-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="bcd7a-134">Clé primaire utilisée pour identifier cette entrée de table particulière.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-134">Primary key used to identify this particular table entry.</span></span>

</dd> <dt>

<span data-ttu-id="bcd7a-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="bcd7a-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="bcd7a-136">Clé externe première colonne de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="bcd7a-136">External key the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="bcd7a-137">Ce champ fait référence au composant qui contrôle le fichier à supprimer.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-137">This field references the component that controls the file to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="bcd7a-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension</span><span class="sxs-lookup"><span data-stu-id="bcd7a-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="bcd7a-139">Cette colonne contient le nom localisable du fichier à supprimer.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-139">This column contains the localizable name of the file to be removed.</span></span> <span data-ttu-id="bcd7a-140">Si cette colonne est null, le dossier spécifié est supprimé s’il est vide.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-140">If this column is null, then the specified folder will be removed if it is empty.</span></span> <span data-ttu-id="bcd7a-141">Tous les fichiers qui correspondent au caractère générique seront supprimés du répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-141">All of the files that match the wildcard will be removed from the specified directory.</span></span>

</dd> <dt>

<span data-ttu-id="bcd7a-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="bcd7a-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="bcd7a-143">Nom d’une propriété dont la valeur est supposée correspondre au chemin d’accès complet au dossier du fichier à supprimer.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-143">Name of a property whose value is assumed to resolve to the full path to the folder of the file to be removed.</span></span> <span data-ttu-id="bcd7a-144">La propriété peut être le nom d’un répertoire dans la [table de répertoires](directory-table.md), une propriété définie par la [table AppSearch](appsearch-table.md), ou toute autre propriété qui représente un chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-144">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="bcd7a-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span><span class="sxs-lookup"><span data-stu-id="bcd7a-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span></span>
</dt> <dd>

<span data-ttu-id="bcd7a-146">Doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-146">Must be one of the following values.</span></span>



| <span data-ttu-id="bcd7a-147">Constante</span><span class="sxs-lookup"><span data-stu-id="bcd7a-147">Constant</span></span>                                | <span data-ttu-id="bcd7a-148">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="bcd7a-148">Hexadecimal</span></span> | <span data-ttu-id="bcd7a-149">Decimal</span><span class="sxs-lookup"><span data-stu-id="bcd7a-149">Decimal</span></span> | <span data-ttu-id="bcd7a-150">Description</span><span class="sxs-lookup"><span data-stu-id="bcd7a-150">Description</span></span>                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd7a-151">**msidbRemoveFileInstallModeOnInstall**</span><span class="sxs-lookup"><span data-stu-id="bcd7a-151">**msidbRemoveFileInstallModeOnInstall**</span></span> | <span data-ttu-id="bcd7a-152">0x001</span><span class="sxs-lookup"><span data-stu-id="bcd7a-152">0x001</span></span>       | <span data-ttu-id="bcd7a-153">1</span><span class="sxs-lookup"><span data-stu-id="bcd7a-153">1</span></span>       | <span data-ttu-id="bcd7a-154">Supprimer uniquement lorsque le composant associé est en cours d’installation (msiInstallStateLocal ou msiInstallStateSource).</span><span class="sxs-lookup"><span data-stu-id="bcd7a-154">Remove only when the associated component is being installed (msiInstallStateLocal or msiInstallStateSource).</span></span> |
| <span data-ttu-id="bcd7a-155">**msidbRemoveFileInstallModeOnRemove**</span><span class="sxs-lookup"><span data-stu-id="bcd7a-155">**msidbRemoveFileInstallModeOnRemove**</span></span>  | <span data-ttu-id="bcd7a-156">0x002</span><span class="sxs-lookup"><span data-stu-id="bcd7a-156">0x002</span></span>       | <span data-ttu-id="bcd7a-157">2</span><span class="sxs-lookup"><span data-stu-id="bcd7a-157">2</span></span>       | <span data-ttu-id="bcd7a-158">Supprimer uniquement lorsque le composant associé est en cours de suppression (msiInstallStateAbsent).</span><span class="sxs-lookup"><span data-stu-id="bcd7a-158">Remove only when the associated component is being removed (msiInstallStateAbsent).</span></span>                           |
| <span data-ttu-id="bcd7a-159">**msidbRemoveFileInstallModeOnBoth**</span><span class="sxs-lookup"><span data-stu-id="bcd7a-159">**msidbRemoveFileInstallModeOnBoth**</span></span>    | <span data-ttu-id="bcd7a-160">0x003</span><span class="sxs-lookup"><span data-stu-id="bcd7a-160">0x003</span></span>       | <span data-ttu-id="bcd7a-161">3</span><span class="sxs-lookup"><span data-stu-id="bcd7a-161">3</span></span>       | <span data-ttu-id="bcd7a-162">Supprimez dans l’un des cas ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="bcd7a-162">Remove in either of the above cases.</span></span>                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcd7a-163">Notes</span><span class="sxs-lookup"><span data-stu-id="bcd7a-163">Remarks</span></span>

<span data-ttu-id="bcd7a-164">Les références de fichier de cette table sont traitées par l' [action RemoveFiles](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="bcd7a-164">The file references in this table are processed by the [RemoveFiles action](removefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="bcd7a-165">Validation</span><span class="sxs-lookup"><span data-stu-id="bcd7a-165">Validation</span></span>

<dl>

[<span data-ttu-id="bcd7a-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="bcd7a-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="bcd7a-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="bcd7a-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="bcd7a-168">ICE18</span><span class="sxs-lookup"><span data-stu-id="bcd7a-168">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="bcd7a-169">ICE32</span><span class="sxs-lookup"><span data-stu-id="bcd7a-169">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="bcd7a-170">ICE45</span><span class="sxs-lookup"><span data-stu-id="bcd7a-170">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="bcd7a-171">ICE64</span><span class="sxs-lookup"><span data-stu-id="bcd7a-171">ICE64</span></span>](ice64.md)  
</dl>

 

 




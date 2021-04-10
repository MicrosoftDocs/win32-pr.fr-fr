---
description: La table Directory spécifie la disposition des répertoires pour le produit. Chaque ligne de la table indique un répertoire à la fois au niveau de la source et de la cible.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Table de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952306"
---
# <a name="directory-table"></a><span data-ttu-id="b88a1-104">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="b88a1-104">Directory Table</span></span>

<span data-ttu-id="b88a1-105">La table Directory spécifie la disposition des répertoires pour le produit.</span><span class="sxs-lookup"><span data-stu-id="b88a1-105">The Directory table specifies the directory layout for the product.</span></span> <span data-ttu-id="b88a1-106">Chaque ligne de la table indique un répertoire à la fois au niveau de la source et de la cible.</span><span class="sxs-lookup"><span data-stu-id="b88a1-106">Each row of the table indicates a directory both at the source and the target.</span></span>

<span data-ttu-id="b88a1-107">La table Directory contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b88a1-107">The Directory table has the following columns.</span></span>



| <span data-ttu-id="b88a1-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="b88a1-108">Column</span></span>            | <span data-ttu-id="b88a1-109">Type</span><span class="sxs-lookup"><span data-stu-id="b88a1-109">Type</span></span>                         | <span data-ttu-id="b88a1-110">Clé</span><span class="sxs-lookup"><span data-stu-id="b88a1-110">Key</span></span> | <span data-ttu-id="b88a1-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="b88a1-111">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="b88a1-112">Répertoire</span><span class="sxs-lookup"><span data-stu-id="b88a1-112">Directory</span></span>         | [<span data-ttu-id="b88a1-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b88a1-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="b88a1-114">O</span><span class="sxs-lookup"><span data-stu-id="b88a1-114">Y</span></span>   | <span data-ttu-id="b88a1-115">N</span><span class="sxs-lookup"><span data-stu-id="b88a1-115">N</span></span>        |
| <span data-ttu-id="b88a1-116">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="b88a1-116">Directory\_Parent</span></span> | [<span data-ttu-id="b88a1-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b88a1-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="b88a1-118">N</span><span class="sxs-lookup"><span data-stu-id="b88a1-118">N</span></span>   | <span data-ttu-id="b88a1-119">O</span><span class="sxs-lookup"><span data-stu-id="b88a1-119">Y</span></span>        |
| <span data-ttu-id="b88a1-120">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="b88a1-120">DefaultDir</span></span>        | [<span data-ttu-id="b88a1-121">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="b88a1-121">DefaultDir</span></span>](defaultdir.md) | <span data-ttu-id="b88a1-122">N</span><span class="sxs-lookup"><span data-stu-id="b88a1-122">N</span></span>   | <span data-ttu-id="b88a1-123">N</span><span class="sxs-lookup"><span data-stu-id="b88a1-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b88a1-124">Colonnes</span><span class="sxs-lookup"><span data-stu-id="b88a1-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b88a1-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory</span><span class="sxs-lookup"><span data-stu-id="b88a1-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory</span></span>
</dt> <dd>

<span data-ttu-id="b88a1-126">La colonne Directory contient un identificateur unique pour un chemin d’accès de répertoire ou de répertoire.</span><span class="sxs-lookup"><span data-stu-id="b88a1-126">The Directory column contains a unique identifier for a directory or directory path.</span></span> <span data-ttu-id="b88a1-127">Cette colonne peut contenir le nom d’une propriété qui est définie sur le chemin d’accès complet d’un répertoire cible.</span><span class="sxs-lookup"><span data-stu-id="b88a1-127">This column can contain the name of a property that is set to the full path of a target directory.</span></span> <span data-ttu-id="b88a1-128">Si cette colonne contient une propriété, le répertoire cible prend le nom spécifié dans la colonne DefaultDir et prend le répertoire parent spécifié dans la \_ colonne parente du répertoire.</span><span class="sxs-lookup"><span data-stu-id="b88a1-128">If this column contains a property, the target directory takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="b88a1-129">Le répertoire source prend toujours le nom spécifié dans la colonne DefaultDir et prend le répertoire parent spécifié dans la \_ colonne parente du répertoire.</span><span class="sxs-lookup"><span data-stu-id="b88a1-129">The source directory always takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="b88a1-130">Si la \_ colonne parente Directory est null ou égale à la valeur de la colonne Directory, la colonne Directory représente un répertoire cible racine.</span><span class="sxs-lookup"><span data-stu-id="b88a1-130">If the Directory\_Parent column is either null or equal to the value of the Directory column, the Directory column represents a root target directory.</span></span> <span data-ttu-id="b88a1-131">Un seul répertoire racine peut être spécifié dans la table de répertoires.</span><span class="sxs-lookup"><span data-stu-id="b88a1-131">Only one root directory may be specified in the Directory table.</span></span>

</dd> <dt>

<span data-ttu-id="b88a1-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="b88a1-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Directory\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="b88a1-133">Cette colonne est une référence au répertoire parent du répertoire.</span><span class="sxs-lookup"><span data-stu-id="b88a1-133">This column is a reference to the directory's parent directory.</span></span> <span data-ttu-id="b88a1-134">Un enregistrement qui a une \_ colonne parente de répertoire égale à null ou égal à la colonne de répertoire représente un répertoire racine.</span><span class="sxs-lookup"><span data-stu-id="b88a1-134">A record that has a Directory\_Parent column equal to null or equal to the Directory column represents a root directory.</span></span> <span data-ttu-id="b88a1-135">Le chemin d’accès complet du répertoire parent est résolu par référence dans la \_ colonne parente du répertoire est une clé externe dans la colonne Directory.</span><span class="sxs-lookup"><span data-stu-id="b88a1-135">The full path of the parent directory is resolved by reference in the Directory\_Parent column is an external key into the Directory column.</span></span> <span data-ttu-id="b88a1-136">Par exemple, si un dossier a un répertoire parent nommé PDIR, le répertoire parent de PDIR est indiqué dans la \_ colonne parente Directory de la ligne avec PDIR dans la colonne Directory.</span><span class="sxs-lookup"><span data-stu-id="b88a1-136">For example, if a folder has a parent directory named PDIR, the parent directory of PDIR is given in the Directory\_Parent column of the row with PDIR in the Directory column.</span></span>

</dd> <dt>

<span data-ttu-id="b88a1-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span><span class="sxs-lookup"><span data-stu-id="b88a1-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span></span>
</dt> <dd>

<span data-ttu-id="b88a1-138">La colonne DefaultDir contient le nom du répertoire (localisable) sous le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="b88a1-138">The DefaultDir column contains the directory's name (localizable)under the parent directory.</span></span> <span data-ttu-id="b88a1-139">Par défaut, il s’agit du nom des répertoires cible et source.</span><span class="sxs-lookup"><span data-stu-id="b88a1-139">By default, this is the name of both the target and source directories.</span></span> <span data-ttu-id="b88a1-140">Pour spécifier des noms de répertoires source et cible différents, séparez les noms de source et de source par le signe deux-points comme suit : \[ TargetName \] : \[ SourceName \] .</span><span class="sxs-lookup"><span data-stu-id="b88a1-140">To specify different source and target directory names, separate the target and source names with a colon as follows: \[targetname\]:\[sourcename\].</span></span>

<span data-ttu-id="b88a1-141">Si la valeur de la \_ colonne parente Directory est null ou est égale à la colonne Directory, la colonne DefaultDir spécifie le nom d’un répertoire source racine.</span><span class="sxs-lookup"><span data-stu-id="b88a1-141">If the value of the Directory\_Parent column is null or is equal to the Directory column, the DefaultDir column specifies the name of a root source directory.</span></span>

<span data-ttu-id="b88a1-142">Dans le cas d’un répertoire source non racine, un point (.) entré dans la colonne DefaultDir pour le nom du répertoire source ou le nom du répertoire cible indique que le répertoire doit se trouver dans son répertoire parent sans un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="b88a1-142">For a non-root source directory, a period (.) entered in the DefaultDir column for the source directory name or the target directory name indicates the directory should be located in its parent directory without a subdirectory.</span></span>

<span data-ttu-id="b88a1-143">Les noms de répertoires de cette colonne peuvent être formatés en tant que paires de noms de fichiers \| longs.</span><span class="sxs-lookup"><span data-stu-id="b88a1-143">The directory names in this column may be formatted as short filename \| long filename pairs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b88a1-144">Notes</span><span class="sxs-lookup"><span data-stu-id="b88a1-144">Remarks</span></span>

<span data-ttu-id="b88a1-145">Chaque enregistrement de la table représente un répertoire dans les images source et de destination.</span><span class="sxs-lookup"><span data-stu-id="b88a1-145">Each record in the table represents a directory in both the source and the destination images.</span></span> <span data-ttu-id="b88a1-146">La table de répertoire doit spécifier un répertoire racine unique avec une valeur de colonne de répertoire égale à la propriété [**targetDir**](targetdir.md) .</span><span class="sxs-lookup"><span data-stu-id="b88a1-146">The Directory table must specify a single root directory with a Directory column value equal to the [**TARGETDIR**](targetdir.md) property.</span></span>

<span data-ttu-id="b88a1-147">Pour une [installation administrative](administrative-installation.md), installez l’image administrative dans le répertoire racine nommé TARGETDIR et utilisez les noms des répertoires sources pour résoudre les répertoires cibles.</span><span class="sxs-lookup"><span data-stu-id="b88a1-147">For an [administrative installation](administrative-installation.md), install the administrative image into the root directory named TARGETDIR and use the source directory names to resolve the target directories.</span></span>

<span data-ttu-id="b88a1-148">Remarque Le programme d’installation définit un certain nombre de [Propriétés](properties.md) standard pour les chemins d’accès de dossier système.</span><span class="sxs-lookup"><span data-stu-id="b88a1-148">Note the installer sets a number of standard [properties](properties.md) to system folder paths.</span></span> <span data-ttu-id="b88a1-149">Consultez la [référence](property-reference.md) de la propriété pour obtenir la liste des propriétés définies sur les dossiers système.</span><span class="sxs-lookup"><span data-stu-id="b88a1-149">See the [Property Reference](property-reference.md) for a list of the properties that are set to system folders.</span></span>

<span data-ttu-id="b88a1-150">La résolution d’annuaire est effectuée pendant l' [action CostFinalize](costfinalize-action.md) et est effectuée comme suit :</span><span class="sxs-lookup"><span data-stu-id="b88a1-150">Directory resolution is performed during the [CostFinalize action](costfinalize-action.md) and is done as follows:</span></span>

### <a name="root-destination-directory"></a><span data-ttu-id="b88a1-151">Répertoire de destination racine</span><span class="sxs-lookup"><span data-stu-id="b88a1-151">Root Destination Directory</span></span>

<span data-ttu-id="b88a1-152">Il ne peut y avoir qu’un seul répertoire de destination racine.</span><span class="sxs-lookup"><span data-stu-id="b88a1-152">There may only be a single root destination directory.</span></span> <span data-ttu-id="b88a1-153">Pour spécifier le répertoire de destination racine, définissez la colonne Directory sur la propriété [**targetDir**](targetdir.md) et la colonne DefaultDir sur la propriété [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="b88a1-153">To specify the root destination directory, set the Directory column to the [**TARGETDIR**](targetdir.md) property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="b88a1-154">Si la propriété **targetDir** est définie, le répertoire de destination est résolu à la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="b88a1-154">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="b88a1-155">Si la propriété **targetDir** n’est pas définie, la propriété [**ROOTDRIVE**](rootdrive.md) est utilisée pour résoudre le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="b88a1-155">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span>

### <a name="root-source-directory"></a><span data-ttu-id="b88a1-156">Répertoire source racine</span><span class="sxs-lookup"><span data-stu-id="b88a1-156">Root Source Directory</span></span>

<span data-ttu-id="b88a1-157">La valeur de la colonne DefaultDir de l’entrée de répertoire racine doit être définie sur la propriété [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="b88a1-157">The value of the DefaultDir column for the root directory entry must be set to the [**SourceDir**](sourcedir.md) property.</span></span>

### <a name="non-root-destination-directories"></a><span data-ttu-id="b88a1-158">Répertoires de destination non racine</span><span class="sxs-lookup"><span data-stu-id="b88a1-158">Non-root Destination Directories</span></span>

<span data-ttu-id="b88a1-159">La valeur de répertoire pour un répertoire non racine est également interprétée comme le nom d’une propriété définissant l’emplacement de la destination.</span><span class="sxs-lookup"><span data-stu-id="b88a1-159">The Directory value for a non-root directory is also interpreted as the name of a property defining the location of the destination.</span></span> <span data-ttu-id="b88a1-160">Si la propriété est définie, le répertoire de destination est résolu à la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="b88a1-160">If the property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="b88a1-161">Si la propriété n’est pas définie, le répertoire de destination est résolu en un sous-répertoire sous le répertoire de destination résolu pour l' \_ entrée parente de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="b88a1-161">If the property is not defined, the destination directory is resolved to a subdirectory beneath the resolved destination directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="b88a1-162">La valeur DefaultDir définit le nom du sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="b88a1-162">The DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="non-root-source-directories"></a><span data-ttu-id="b88a1-163">Répertoires sources non racines</span><span class="sxs-lookup"><span data-stu-id="b88a1-163">Non-root Source Directories</span></span>

<span data-ttu-id="b88a1-164">Le répertoire source d’un répertoire non racine est résolu dans un sous-répertoire du répertoire source résolu pour l' \_ entrée parente de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="b88a1-164">The source directory for a non-root directory is resolved to a subdirectory of the resolved source directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="b88a1-165">Là encore, la valeur DefaultDir définit le nom du sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="b88a1-165">Again, the DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="short-or-long-file-names"></a><span data-ttu-id="b88a1-166">Noms de fichier courts ou longs</span><span class="sxs-lookup"><span data-stu-id="b88a1-166">Short or Long File Names</span></span>

<span data-ttu-id="b88a1-167">Lors de la résolution des répertoires de destination, les noms de fichiers courts spécifiés dans la colonne DefaultDir sont utilisés si la propriété [**SHORTFILENAMES**](shortfilenames.md) est définie ou si le volume dans lequel se trouve le répertoire ne prend pas en charge les noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="b88a1-167">When resolving destination directories, the short file names specified in the DefaultDir column are used if either the [**SHORTFILENAMES**](shortfilenames.md) property is set or the volume the directory is located on does not support long file names.</span></span> <span data-ttu-id="b88a1-168">Dans le cas contraire, le nom de fichier long est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b88a1-168">Otherwise, the long file name is used.</span></span>

<span data-ttu-id="b88a1-169">Notez que lorsque les répertoires sont résolus au cours de l’action CostFinalize, les clés de la table Directory deviennent des [Propriétés](properties.md) définies sur des chemins d’accès aux répertoires.</span><span class="sxs-lookup"><span data-stu-id="b88a1-169">Note that when the directories are resolved during the CostFinalize action, the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span>

[<span data-ttu-id="b88a1-170">Table CreateFolder</span><span class="sxs-lookup"><span data-stu-id="b88a1-170">CreateFolder Table</span></span>](createfolder-table.md)

<span data-ttu-id="b88a1-171">Pour créer des dossiers vides pendant une installation, consultez la [table CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="b88a1-171">For creating empty folders during an installation, see [CreateFolder Table](createfolder-table.md).</span></span>

[<span data-ttu-id="b88a1-172">Utilisation de la table Directory</span><span class="sxs-lookup"><span data-stu-id="b88a1-172">Using the Directory Table</span></span>](using-the-directory-table.md)

<span data-ttu-id="b88a1-173">Pour plus d’informations sur la table de répertoires, y compris des exemples, consultez [utilisation de la table de répertoires](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="b88a1-173">For more information about the Directory table, including samples, see [Using the Directory Table](using-the-directory-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="b88a1-174">Validation</span><span class="sxs-lookup"><span data-stu-id="b88a1-174">Validation</span></span>

<dl>

[<span data-ttu-id="b88a1-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="b88a1-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b88a1-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="b88a1-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b88a1-177">ICE07</span><span class="sxs-lookup"><span data-stu-id="b88a1-177">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="b88a1-178">ICE30</span><span class="sxs-lookup"><span data-stu-id="b88a1-178">ICE30</span></span>](ice30.md)  
[<span data-ttu-id="b88a1-179">ICE32</span><span class="sxs-lookup"><span data-stu-id="b88a1-179">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b88a1-180">ICE38</span><span class="sxs-lookup"><span data-stu-id="b88a1-180">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="b88a1-181">ICE46</span><span class="sxs-lookup"><span data-stu-id="b88a1-181">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="b88a1-182">ICE48</span><span class="sxs-lookup"><span data-stu-id="b88a1-182">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="b88a1-183">ICE56</span><span class="sxs-lookup"><span data-stu-id="b88a1-183">ICE56</span></span>](ice56.md)  
[<span data-ttu-id="b88a1-184">ICE57</span><span class="sxs-lookup"><span data-stu-id="b88a1-184">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="b88a1-185">ICE64</span><span class="sxs-lookup"><span data-stu-id="b88a1-185">ICE64</span></span>](ice64.md)  
[<span data-ttu-id="b88a1-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="b88a1-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="b88a1-187">ICE90</span><span class="sxs-lookup"><span data-stu-id="b88a1-187">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="b88a1-188">ICE91</span><span class="sxs-lookup"><span data-stu-id="b88a1-188">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="b88a1-189">ICE99</span><span class="sxs-lookup"><span data-stu-id="b88a1-189">ICE99</span></span>](ice99.md)  
</dl>

 

 




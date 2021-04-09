---
description: La table TargetImages contient des informations sur les images cibles du produit. Un package de correctifs Windows Installer met à jour une image cible en une image mise à niveau.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Table TargetImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868450"
---
# <a name="targetimages-table-patchwizdll"></a><span data-ttu-id="0ca6b-104">Table TargetImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="0ca6b-104">TargetImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="0ca6b-105">La table TargetImages contient des informations sur les images cibles du produit.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-105">The TargetImages table contains information about the target images of the product.</span></span> <span data-ttu-id="0ca6b-106">Un package de correctifs Windows Installer met à jour une image cible en une image mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span>

<span data-ttu-id="0ca6b-107">Une table TargetImages contenant au moins un enregistrement est requise dans chaque base de données de création de correctif (fichier. PCP).</span><span class="sxs-lookup"><span data-stu-id="0ca6b-107">A TargetImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="0ca6b-108">Cette table est utilisée par la fonction [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="0ca6b-108">This table is used by the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="0ca6b-109">La table TargetImages contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-109">The TargetImages table has the following columns.</span></span>



| <span data-ttu-id="0ca6b-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="0ca6b-110">Column</span></span>                | <span data-ttu-id="0ca6b-111">Type</span><span class="sxs-lookup"><span data-stu-id="0ca6b-111">Type</span></span>    | <span data-ttu-id="0ca6b-112">Clé</span><span class="sxs-lookup"><span data-stu-id="0ca6b-112">Key</span></span> | <span data-ttu-id="0ca6b-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="0ca6b-113">Nullable</span></span> |
|-----------------------|---------|-----|----------|
| <span data-ttu-id="0ca6b-114">Cible</span><span class="sxs-lookup"><span data-stu-id="0ca6b-114">Target</span></span>                | <span data-ttu-id="0ca6b-115">text</span><span class="sxs-lookup"><span data-stu-id="0ca6b-115">text</span></span>    | <span data-ttu-id="0ca6b-116">O</span><span class="sxs-lookup"><span data-stu-id="0ca6b-116">Y</span></span>   | <span data-ttu-id="0ca6b-117">N</span><span class="sxs-lookup"><span data-stu-id="0ca6b-117">N</span></span>        |
| <span data-ttu-id="0ca6b-118">MsiPath</span><span class="sxs-lookup"><span data-stu-id="0ca6b-118">MsiPath</span></span>               | <span data-ttu-id="0ca6b-119">text</span><span class="sxs-lookup"><span data-stu-id="0ca6b-119">text</span></span>    |     | <span data-ttu-id="0ca6b-120">N</span><span class="sxs-lookup"><span data-stu-id="0ca6b-120">N</span></span>        |
| <span data-ttu-id="0ca6b-121">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="0ca6b-121">SymbolPaths</span></span>           | <span data-ttu-id="0ca6b-122">text</span><span class="sxs-lookup"><span data-stu-id="0ca6b-122">text</span></span>    |     | <span data-ttu-id="0ca6b-123">O</span><span class="sxs-lookup"><span data-stu-id="0ca6b-123">Y</span></span>        |
| <span data-ttu-id="0ca6b-124">Upgraded</span><span class="sxs-lookup"><span data-stu-id="0ca6b-124">Upgraded</span></span>              | <span data-ttu-id="0ca6b-125">text</span><span class="sxs-lookup"><span data-stu-id="0ca6b-125">text</span></span>    |     | <span data-ttu-id="0ca6b-126">N</span><span class="sxs-lookup"><span data-stu-id="0ca6b-126">N</span></span>        |
| <span data-ttu-id="0ca6b-127">Commande</span><span class="sxs-lookup"><span data-stu-id="0ca6b-127">Order</span></span>                 | <span data-ttu-id="0ca6b-128">entier</span><span class="sxs-lookup"><span data-stu-id="0ca6b-128">integer</span></span> |     | <span data-ttu-id="0ca6b-129">N</span><span class="sxs-lookup"><span data-stu-id="0ca6b-129">N</span></span>        |
| <span data-ttu-id="0ca6b-130">ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="0ca6b-130">ProductValidateFlags</span></span>  | <span data-ttu-id="0ca6b-131">text</span><span class="sxs-lookup"><span data-stu-id="0ca6b-131">text</span></span>    |     | <span data-ttu-id="0ca6b-132">O</span><span class="sxs-lookup"><span data-stu-id="0ca6b-132">Y</span></span>        |
| <span data-ttu-id="0ca6b-133">IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="0ca6b-133">IgnoreMissingSrcFiles</span></span> | <span data-ttu-id="0ca6b-134">entier</span><span class="sxs-lookup"><span data-stu-id="0ca6b-134">integer</span></span> |     | <span data-ttu-id="0ca6b-135">N</span><span class="sxs-lookup"><span data-stu-id="0ca6b-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0ca6b-136">Colonnes</span><span class="sxs-lookup"><span data-stu-id="0ca6b-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0ca6b-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Indicatif</span><span class="sxs-lookup"><span data-stu-id="0ca6b-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="0ca6b-138">Identificateur d’une image cible.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-138">Identifier for a target image.</span></span> <span data-ttu-id="0ca6b-139">Le package de correctifs met à jour l’image cible spécifiée dans cette colonne avec l’image mise à niveau spécifiée dans la colonne mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-139">The patch package updates the target image specified in this column to the upgraded image specified in the Upgraded column.</span></span> <span data-ttu-id="0ca6b-140">Il existe une ou plusieurs images cibles pour chaque image mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-140">There are one or more target images for each upgraded image.</span></span> <span data-ttu-id="0ca6b-141">L’image cible doit être une image d’installation entièrement décompressée du produit, telle qu’une image administrative ou une image d’installation non compressée sur un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-141">The target image must be a fully uncompressed setup image of the product, such as an administrative image or an uncompressed setup image on a CD-ROM.</span></span> <span data-ttu-id="0ca6b-142">Notez que la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) ne génère pas de correctifs binaires pour les fichiers dans les armoires.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-142">Note that the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function does not generate binary patches for files in cabinets.</span></span> <span data-ttu-id="0ca6b-143">La valeur de ce champ est utilisée avec la valeur dans le champ mis à niveau pour générer les noms des transformations que le programme d’installation ajoute au package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-143">The value in this field is used with the value in the Upgraded field to generate the names of the transforms that the installer adds to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="0ca6b-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span><span class="sxs-lookup"><span data-stu-id="0ca6b-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="0ca6b-145">Ce champ spécifie le chemin d’accès complet, y compris le nom de fichier, à l’emplacement du fichier. msi de l’image cible.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-145">This field specifies the full path, including the file name, to the location of the .msi file for the target image.</span></span> <span data-ttu-id="0ca6b-146">Il s’agit de l’emplacement des fichiers sources de l’image cible.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-146">This is the location of the source files for the target image.</span></span>

</dd> <dt>

<span data-ttu-id="0ca6b-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="0ca6b-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="0ca6b-148">Liste délimitée par des points-virgules des dossiers dans lesquels rechercher les fichiers de symboles qui peuvent être utilisés pour optimiser la génération du correctif binaire.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-148">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="0ca6b-149">Notez que les sous-répertoires des dossiers spécifiés dans ce champ ne sont pas recherchés.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-149">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="0ca6b-150">Un correctif binaire optimisé peut être plus petit.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-150">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="0ca6b-151">Microsoft Visual C++ doit être installé sur l’ordinateur générant le correctif et utilisé pour créer les fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-151">Microsoft Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="0ca6b-152">Ce champ est facultatif et le programme d’installation crée un correctif binaire même si aucun fichier de symboles n’est spécifié ou si les fichiers de symboles ne sont pas disponibles pour Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-152">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="0ca6b-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Mis à niveau</span><span class="sxs-lookup"><span data-stu-id="0ca6b-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="0ca6b-154">Clé étrangère vers la colonne mise à niveau de la [table UpgradedImages](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="0ca6b-154">Foreign key to the Upgraded column of the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="0ca6b-155">La fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) ignore toutes les images mises à niveau qui ne sont pas référencées par au moins un enregistrement de la table TargetImages.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-155">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function ignores any upgraded image that is not referenced by at least one record of the TargetImages table.</span></span>

</dd> <dt>

<span data-ttu-id="0ca6b-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordre</span><span class="sxs-lookup"><span data-stu-id="0ca6b-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="0ca6b-157">Ordre relatif de l’image cible.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-157">Relative order of the target image.</span></span> <span data-ttu-id="0ca6b-158">Étant donné que plusieurs cibles peuvent être corrigées vers une image mise à niveau, le champ order fournit un moyen de séquencer les transformations dans la liste des transformations de correctifs.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-158">Because multiple targets can be patched to an upgraded image, the Order field provides a means to sequence the transforms in the patch transforms list.</span></span> <span data-ttu-id="0ca6b-159">En règle générale, l’ordre passe de l’image la plus ancienne à la plus récente.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-159">Commonly, the order is from oldest to newest image.</span></span>

</dd> <dt>

<span data-ttu-id="0ca6b-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="0ca6b-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span></span>
</dt> <dd>

<span data-ttu-id="0ca6b-161">Le champ ProductValidateFlags est utilisé pour spécifier la vérification du produit afin d’éviter d’appliquer des transformations non pertinentes.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-161">The ProductValidateFlags field is used to specify product checking to avoid applying irrelevant transforms.</span></span> <span data-ttu-id="0ca6b-162">La valeur entrée dans ce champ doit être un entier hexadécimal à 8 chiffres et l’une des valeurs valides pour le paramètre *iValidation* de la fonction [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) .</span><span class="sxs-lookup"><span data-stu-id="0ca6b-162">The value entered in this field must be an 8-digit hex integer and one of the valid values for the *iValidation* parameter of the [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) function.</span></span> <span data-ttu-id="0ca6b-163">La valeur par défaut est 0x00000922, ce qui équivaut à **MSITRANSFORM \_ Validate \_ UPDATEVERSION**  +  **MSITRANSFORM \_ Validate \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ Validate \_ UPGRADECODE**  +  **MSITRANSFORM \_ Validate \_ Product**.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-163">The default value is 0x00000922 which equals **MSITRANSFORM\_VALIDATE\_UPDATEVERSION** + **MSITRANSFORM\_VALIDATE\_NEWEQUALBASEVERSION** + **MSITRANSFORM\_VALIDATE\_UPGRADECODE** + **MSITRANSFORM\_VALIDATE\_PRODUCT**.</span></span>

</dd> <dt>

<span data-ttu-id="0ca6b-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="0ca6b-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span></span>
</dt> <dd>

<span data-ttu-id="0ca6b-165">Si ce champ est défini sur une valeur différente de zéro, les fichiers absents de l’image cible sont ignorés par le programme d’installation et restent inchangés lors de la mise à jour corrective.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-165">If this field is set to a nonzero value, files missing from the target image are ignored by the installer and left unchanged during patching.</span></span> <span data-ttu-id="0ca6b-166">Cela permet d’effectuer des correctifs sans avoir besoin de l’intégralité de l’image. Seuls les fichiers modifiés du produit et le fichier. msi sont requis.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-166">This enables patches to be made without requiring the entire image; only the changed files of the product and the .msi file are required.</span></span> <span data-ttu-id="0ca6b-167">Cela peut réduire le temps nécessaire pour générer le correctif.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-167">This may reduce the time required to generate the patch.</span></span>

> [!Note]  
> <span data-ttu-id="0ca6b-168">N’utilisez pas la valeur IgnoreMissingSrcFiles avec TrustMsi défini sur 1 dans le [tableau des propriétés](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="0ca6b-168">Do not use the IgnoreMissingSrcFiles value with TrustMsi set to 1 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ca6b-169">Notes</span><span class="sxs-lookup"><span data-stu-id="0ca6b-169">Remarks</span></span>

<span data-ttu-id="0ca6b-170">Cette table accepte les variables d’environnement en tant que chemins d’accès commençant par la version 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="0ca6b-170">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 




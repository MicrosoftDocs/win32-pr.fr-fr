---
description: La table ExternalFiles contient des informations sur des fichiers spécifiques qui ne font pas partie d’une image cible normale.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Table ExternalFiles (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528197"
---
# <a name="externalfiles-table-patchwizdll"></a><span data-ttu-id="838bf-103">Table ExternalFiles (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="838bf-103">ExternalFiles Table (Patchwiz.dll)</span></span>

<span data-ttu-id="838bf-104">La table ExternalFiles contient des informations sur des fichiers spécifiques qui ne font pas partie d’une image cible normale.</span><span class="sxs-lookup"><span data-stu-id="838bf-104">The ExternalFiles table contains information about specific files that are not part of a regular target image.</span></span> <span data-ttu-id="838bf-105">Ces fichiers peuvent exister dans des produits qui ont été mis à jour par un autre produit, une mise à niveau ou un correctif.</span><span class="sxs-lookup"><span data-stu-id="838bf-105">These files may exist in products that have been updated by another product, upgrade, or patch.</span></span> <span data-ttu-id="838bf-106">Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="838bf-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="838bf-107">La table ExternalFiles contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="838bf-107">The ExternalFiles table has the following columns.</span></span>



| <span data-ttu-id="838bf-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="838bf-108">Column</span></span>        | <span data-ttu-id="838bf-109">Type</span><span class="sxs-lookup"><span data-stu-id="838bf-109">Type</span></span>    | <span data-ttu-id="838bf-110">Clé</span><span class="sxs-lookup"><span data-stu-id="838bf-110">Key</span></span> | <span data-ttu-id="838bf-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="838bf-111">Nullable</span></span> |
|---------------|---------|-----|----------|
| <span data-ttu-id="838bf-112">Famille</span><span class="sxs-lookup"><span data-stu-id="838bf-112">Family</span></span>        | <span data-ttu-id="838bf-113">text</span><span class="sxs-lookup"><span data-stu-id="838bf-113">text</span></span>    | <span data-ttu-id="838bf-114">O</span><span class="sxs-lookup"><span data-stu-id="838bf-114">Y</span></span>   | <span data-ttu-id="838bf-115">N</span><span class="sxs-lookup"><span data-stu-id="838bf-115">N</span></span>        |
| <span data-ttu-id="838bf-116">TCTI</span><span class="sxs-lookup"><span data-stu-id="838bf-116">FTK</span></span>           | <span data-ttu-id="838bf-117">text</span><span class="sxs-lookup"><span data-stu-id="838bf-117">text</span></span>    | <span data-ttu-id="838bf-118">O</span><span class="sxs-lookup"><span data-stu-id="838bf-118">Y</span></span>   | <span data-ttu-id="838bf-119">N</span><span class="sxs-lookup"><span data-stu-id="838bf-119">N</span></span>        |
| <span data-ttu-id="838bf-120">FilePath</span><span class="sxs-lookup"><span data-stu-id="838bf-120">FilePath</span></span>      | <span data-ttu-id="838bf-121">text</span><span class="sxs-lookup"><span data-stu-id="838bf-121">text</span></span>    | <span data-ttu-id="838bf-122">O</span><span class="sxs-lookup"><span data-stu-id="838bf-122">Y</span></span>   | <span data-ttu-id="838bf-123">N</span><span class="sxs-lookup"><span data-stu-id="838bf-123">N</span></span>        |
| <span data-ttu-id="838bf-124">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="838bf-124">SymbolPaths</span></span>   | <span data-ttu-id="838bf-125">text</span><span class="sxs-lookup"><span data-stu-id="838bf-125">text</span></span>    |     | <span data-ttu-id="838bf-126">O</span><span class="sxs-lookup"><span data-stu-id="838bf-126">Y</span></span>        |
| <span data-ttu-id="838bf-127">IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="838bf-127">IgnoreOffsets</span></span> | <span data-ttu-id="838bf-128">text</span><span class="sxs-lookup"><span data-stu-id="838bf-128">text</span></span>    |     | <span data-ttu-id="838bf-129">O</span><span class="sxs-lookup"><span data-stu-id="838bf-129">Y</span></span>        |
| <span data-ttu-id="838bf-130">IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="838bf-130">IgnoreLengths</span></span> | <span data-ttu-id="838bf-131">text</span><span class="sxs-lookup"><span data-stu-id="838bf-131">text</span></span>    |     | <span data-ttu-id="838bf-132">O</span><span class="sxs-lookup"><span data-stu-id="838bf-132">Y</span></span>        |
| <span data-ttu-id="838bf-133">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="838bf-133">RetainOffsets</span></span> | <span data-ttu-id="838bf-134">text</span><span class="sxs-lookup"><span data-stu-id="838bf-134">text</span></span>    |     | <span data-ttu-id="838bf-135">N</span><span class="sxs-lookup"><span data-stu-id="838bf-135">N</span></span>        |
| <span data-ttu-id="838bf-136">Commande</span><span class="sxs-lookup"><span data-stu-id="838bf-136">Order</span></span>         | <span data-ttu-id="838bf-137">entier</span><span class="sxs-lookup"><span data-stu-id="838bf-137">integer</span></span> |     | <span data-ttu-id="838bf-138">O</span><span class="sxs-lookup"><span data-stu-id="838bf-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="838bf-139">Colonnes</span><span class="sxs-lookup"><span data-stu-id="838bf-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="838bf-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famille</span><span class="sxs-lookup"><span data-stu-id="838bf-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="838bf-141">Clé étrangère vers la colonne Family de la [table ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="838bf-141">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="838bf-142"><span id="FTK"></span><span id="ftk"></span>TCTI</span><span class="sxs-lookup"><span data-stu-id="838bf-142"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="838bf-143">Clé étrangère dans la [table de fichiers](file-table.md) du fichier. msi de l’image mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="838bf-143">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="838bf-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>Cheminfichier</span><span class="sxs-lookup"><span data-stu-id="838bf-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span></span>
</dt> <dd>

<span data-ttu-id="838bf-145">Chemin d’accès complet du fichier externe, y compris le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="838bf-145">Full path of the external file including the file name.</span></span> <span data-ttu-id="838bf-146">Le champ FilePath est utilisé pour localiser le fichier spécifié dans la colonne TCTI.</span><span class="sxs-lookup"><span data-stu-id="838bf-146">FilePath field is used to locate the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="838bf-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="838bf-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="838bf-148">Chemin d’accès complet dans lequel les fichiers de symboles du fichier spécifiés dans la colonne TCTI sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="838bf-148">Full path searched for symbol files of the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="838bf-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="838bf-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="838bf-150">La valeur de ce champ est une liste délimitée par des virgules de nombres de décalages de plage pour les plages à ignorer dans le fichier externe.</span><span class="sxs-lookup"><span data-stu-id="838bf-150">The value in this field is a comma-delimited list of range offset numbers for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="838bf-151">L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne IgnoreLengths.</span><span class="sxs-lookup"><span data-stu-id="838bf-151">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="838bf-152">Cette colonne est facultative.</span><span class="sxs-lookup"><span data-stu-id="838bf-152">This column is optional.</span></span>

<span data-ttu-id="838bf-153">Les valeurs peuvent être décimales ou hexadécimales.</span><span class="sxs-lookup"><span data-stu-id="838bf-153">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="838bf-154">[Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ».</span><span class="sxs-lookup"><span data-stu-id="838bf-154">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="838bf-155">Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="838bf-155">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="838bf-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="838bf-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="838bf-157">La valeur de ce champ est une liste délimitée par des virgules de longueurs de plage, en octets, pour les plages à ignorer dans le fichier externe.</span><span class="sxs-lookup"><span data-stu-id="838bf-157">The value in this field is a comma-delimited list of range lengths in bytes for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="838bf-158">L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne IgnoreOffsets.</span><span class="sxs-lookup"><span data-stu-id="838bf-158">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="838bf-159">Cette colonne est facultative.</span><span class="sxs-lookup"><span data-stu-id="838bf-159">This column is optional.</span></span>

<span data-ttu-id="838bf-160">Les valeurs peuvent être décimales ou hexadécimales.</span><span class="sxs-lookup"><span data-stu-id="838bf-160">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="838bf-161">[Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ».</span><span class="sxs-lookup"><span data-stu-id="838bf-161">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="838bf-162">Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="838bf-162">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="838bf-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="838bf-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="838bf-164">La valeur de ce champ est une liste délimitée par des virgules de nombres de décalages de plage pour les plages à conserver dans le fichier externe.</span><span class="sxs-lookup"><span data-stu-id="838bf-164">The value in this field is a comma-delimited list of range offset numbers for the ranges to be retained in the External file.</span></span> <span data-ttu-id="838bf-165">L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne RetainOffsets de l’enregistrement correspondant dans la [table FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="838bf-165">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span></span>

<span data-ttu-id="838bf-166">Les valeurs peuvent être décimales ou hexadécimales.</span><span class="sxs-lookup"><span data-stu-id="838bf-166">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="838bf-167">[Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ».</span><span class="sxs-lookup"><span data-stu-id="838bf-167">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="838bf-168">Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="838bf-168">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="838bf-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordre</span><span class="sxs-lookup"><span data-stu-id="838bf-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="838bf-170">Si deux versions ou plus sont spécifiées pour le même fichier externe, la table peut contenir plusieurs enregistrements avec des valeurs correspondantes dans les champs TCTI et Family.</span><span class="sxs-lookup"><span data-stu-id="838bf-170">If two or more versions are specified for the same external file, the table may contain multiple records with matching values in the FTK and Family fields.</span></span> <span data-ttu-id="838bf-171">Dans ce cas, le champ order peut spécifier l’ordre des fichiers externes à utiliser lors de la création du correctif.</span><span class="sxs-lookup"><span data-stu-id="838bf-171">In this case, the Order field may specify the order of external files to use when creating the patch.</span></span> <span data-ttu-id="838bf-172">L’ordre passe de la version la plus ancienne à la plus récente.</span><span class="sxs-lookup"><span data-stu-id="838bf-172">The order is from the oldest to the most recent version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="838bf-173">Notes</span><span class="sxs-lookup"><span data-stu-id="838bf-173">Remarks</span></span>

<span data-ttu-id="838bf-174">Cette table accepte les variables d’environnement en tant que chemins d’accès commençant par la version 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="838bf-174">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="838bf-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="838bf-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="838bf-176">Mise à jour corrective des régions sélectionnées d’un fichier</span><span class="sxs-lookup"><span data-stu-id="838bf-176">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 




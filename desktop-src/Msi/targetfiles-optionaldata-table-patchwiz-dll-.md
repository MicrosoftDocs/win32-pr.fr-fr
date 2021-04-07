---
description: La \_ table TargetFiles OptionalData contient des informations sur des fichiers spécifiques dans une image cible. Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction UiCreatePatchPackageEx.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: Table TargetFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952396"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="bbf10-104">TargetFiles \_ OptionalData, table (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="bbf10-104">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="bbf10-105">La \_ table TargetFiles OptionalData contient des informations sur des fichiers spécifiques dans une image cible.</span><span class="sxs-lookup"><span data-stu-id="bbf10-105">The TargetFiles\_OptionalData table contains information about specific files in a target image.</span></span> <span data-ttu-id="bbf10-106">Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf10-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="bbf10-107">La \_ table TargetFiles OptionalData contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bbf10-107">The TargetFiles\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="bbf10-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="bbf10-108">Column</span></span>        | <span data-ttu-id="bbf10-109">Type</span><span class="sxs-lookup"><span data-stu-id="bbf10-109">Type</span></span> | <span data-ttu-id="bbf10-110">Clé</span><span class="sxs-lookup"><span data-stu-id="bbf10-110">Key</span></span> | <span data-ttu-id="bbf10-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="bbf10-111">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="bbf10-112">Cible</span><span class="sxs-lookup"><span data-stu-id="bbf10-112">Target</span></span>        | <span data-ttu-id="bbf10-113">text</span><span class="sxs-lookup"><span data-stu-id="bbf10-113">text</span></span> | <span data-ttu-id="bbf10-114">O</span><span class="sxs-lookup"><span data-stu-id="bbf10-114">Y</span></span>   | <span data-ttu-id="bbf10-115">N</span><span class="sxs-lookup"><span data-stu-id="bbf10-115">N</span></span>        |
| <span data-ttu-id="bbf10-116">TCTI</span><span class="sxs-lookup"><span data-stu-id="bbf10-116">FTK</span></span>           | <span data-ttu-id="bbf10-117">text</span><span class="sxs-lookup"><span data-stu-id="bbf10-117">text</span></span> | <span data-ttu-id="bbf10-118">O</span><span class="sxs-lookup"><span data-stu-id="bbf10-118">Y</span></span>   | <span data-ttu-id="bbf10-119">N</span><span class="sxs-lookup"><span data-stu-id="bbf10-119">N</span></span>        |
| <span data-ttu-id="bbf10-120">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="bbf10-120">SymbolPaths</span></span>   | <span data-ttu-id="bbf10-121">text</span><span class="sxs-lookup"><span data-stu-id="bbf10-121">text</span></span> |     | <span data-ttu-id="bbf10-122">O</span><span class="sxs-lookup"><span data-stu-id="bbf10-122">Y</span></span>        |
| <span data-ttu-id="bbf10-123">IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="bbf10-123">IgnoreOffsets</span></span> | <span data-ttu-id="bbf10-124">text</span><span class="sxs-lookup"><span data-stu-id="bbf10-124">text</span></span> |     | <span data-ttu-id="bbf10-125">O</span><span class="sxs-lookup"><span data-stu-id="bbf10-125">Y</span></span>        |
| <span data-ttu-id="bbf10-126">IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="bbf10-126">IgnoreLengths</span></span> | <span data-ttu-id="bbf10-127">text</span><span class="sxs-lookup"><span data-stu-id="bbf10-127">text</span></span> |     | <span data-ttu-id="bbf10-128">O</span><span class="sxs-lookup"><span data-stu-id="bbf10-128">Y</span></span>        |
| <span data-ttu-id="bbf10-129">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="bbf10-129">RetainOffsets</span></span> | <span data-ttu-id="bbf10-130">text</span><span class="sxs-lookup"><span data-stu-id="bbf10-130">text</span></span> |     | <span data-ttu-id="bbf10-131">O</span><span class="sxs-lookup"><span data-stu-id="bbf10-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="bbf10-132">Colonnes</span><span class="sxs-lookup"><span data-stu-id="bbf10-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="bbf10-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Indicatif</span><span class="sxs-lookup"><span data-stu-id="bbf10-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="bbf10-134">Clé étrangère vers la colonne cible de la [table TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="bbf10-134">Foreign key to the Target column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbf10-135"><span id="FTK"></span><span id="ftk"></span>TCTI</span><span class="sxs-lookup"><span data-stu-id="bbf10-135"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="bbf10-136">Clé étrangère dans la [table de fichiers](file-table.md) de l’image cible.</span><span class="sxs-lookup"><span data-stu-id="bbf10-136">Foreign key into the [File table](file-table.md) of target image.</span></span>

</dd> <dt>

<span data-ttu-id="bbf10-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="bbf10-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="bbf10-138">La valeur de ce champ est ajoutée à la liste de dossiers délimités par des points-virgules dans la colonne SymbolPaths de la [table TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) lorsque le correctif est généré et peut être utilisé pour ajouter des fichiers de symboles pour un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="bbf10-138">The value in this field is added to the semicolon delimited list of folders in the SymbolPaths column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="bbf10-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="bbf10-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="bbf10-140">La valeur de ce champ est une liste délimitée par des virgules de nombres de décalages de plage pour les plages à ignorer dans le fichier cible.</span><span class="sxs-lookup"><span data-stu-id="bbf10-140">The value in this field is a comma delimited list of range offset numbers for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="bbf10-141">L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne IgnoreLengths.</span><span class="sxs-lookup"><span data-stu-id="bbf10-141">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="bbf10-142">Cette colonne est facultative.</span><span class="sxs-lookup"><span data-stu-id="bbf10-142">This column is optional.</span></span>

<span data-ttu-id="bbf10-143">Les valeurs peuvent être décimales ou hexadécimales.</span><span class="sxs-lookup"><span data-stu-id="bbf10-143">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="bbf10-144">[Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ».</span><span class="sxs-lookup"><span data-stu-id="bbf10-144">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="bbf10-145">Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="bbf10-145">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="bbf10-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="bbf10-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="bbf10-147">La valeur de ce champ est une liste délimitée par des virgules de longueurs de plage, en octets, pour les plages à ignorer dans le fichier cible.</span><span class="sxs-lookup"><span data-stu-id="bbf10-147">The value in this field is a comma delimited list of range lengths in bytes for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="bbf10-148">L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne IgnoreOffsets.</span><span class="sxs-lookup"><span data-stu-id="bbf10-148">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="bbf10-149">Cette colonne est facultative.</span><span class="sxs-lookup"><span data-stu-id="bbf10-149">This column is optional.</span></span>

<span data-ttu-id="bbf10-150">Les valeurs peuvent être décimales ou hexadécimales.</span><span class="sxs-lookup"><span data-stu-id="bbf10-150">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="bbf10-151">[Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ».</span><span class="sxs-lookup"><span data-stu-id="bbf10-151">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="bbf10-152">Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="bbf10-152">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="bbf10-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="bbf10-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="bbf10-154">La valeur de ce champ est une liste délimitée par des virgules de nombres de décalages de plage pour les plages à conserver dans le fichier cible.</span><span class="sxs-lookup"><span data-stu-id="bbf10-154">The value in this field is a comma delimited list of range offset numbers for the ranges to be retained in the Target file.</span></span> <span data-ttu-id="bbf10-155">L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne RetainOffsets de l’enregistrement correspondant dans la [table FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span><span class="sxs-lookup"><span data-stu-id="bbf10-155">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span></span>

<span data-ttu-id="bbf10-156">Les valeurs peuvent être décimales ou hexadécimales.</span><span class="sxs-lookup"><span data-stu-id="bbf10-156">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="bbf10-157">[Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ».</span><span class="sxs-lookup"><span data-stu-id="bbf10-157">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="bbf10-158">Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="bbf10-158">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="bbf10-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bbf10-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbf10-160">Mise à jour corrective des régions sélectionnées d’un fichier</span><span class="sxs-lookup"><span data-stu-id="bbf10-160">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 




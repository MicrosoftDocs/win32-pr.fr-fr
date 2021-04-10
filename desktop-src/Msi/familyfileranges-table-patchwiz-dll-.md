---
description: La table FamilyFileRanges contient des informations sur des fichiers particuliers d’une image mise à niveau avec des plages qui ne doivent jamais être remplacées.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Table FamilyFileRanges (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114562"
---
# <a name="familyfileranges-table-patchwizdll"></a><span data-ttu-id="fb704-103">Table FamilyFileRanges (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="fb704-103">FamilyFileRanges Table (Patchwiz.dll)</span></span>

<span data-ttu-id="fb704-104">La table FamilyFileRanges contient des informations sur des fichiers particuliers d’une image mise à niveau avec des plages qui ne doivent jamais être remplacées.</span><span class="sxs-lookup"><span data-stu-id="fb704-104">The FamilyFileRanges table contains information about particular files of an upgraded image with ranges that should never be overwritten.</span></span> <span data-ttu-id="fb704-105">Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="fb704-105">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="fb704-106">La table FamilyFileRanges contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="fb704-106">The FamilyFileRanges table has the following columns.</span></span>



| <span data-ttu-id="fb704-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="fb704-107">Column</span></span>        | <span data-ttu-id="fb704-108">Type</span><span class="sxs-lookup"><span data-stu-id="fb704-108">Type</span></span> | <span data-ttu-id="fb704-109">Clé</span><span class="sxs-lookup"><span data-stu-id="fb704-109">Key</span></span> | <span data-ttu-id="fb704-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="fb704-110">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="fb704-111">Famille</span><span class="sxs-lookup"><span data-stu-id="fb704-111">Family</span></span>        | <span data-ttu-id="fb704-112">text</span><span class="sxs-lookup"><span data-stu-id="fb704-112">text</span></span> | <span data-ttu-id="fb704-113">O</span><span class="sxs-lookup"><span data-stu-id="fb704-113">Y</span></span>   | <span data-ttu-id="fb704-114">N</span><span class="sxs-lookup"><span data-stu-id="fb704-114">N</span></span>        |
| <span data-ttu-id="fb704-115">TCTI</span><span class="sxs-lookup"><span data-stu-id="fb704-115">FTK</span></span>           | <span data-ttu-id="fb704-116">text</span><span class="sxs-lookup"><span data-stu-id="fb704-116">text</span></span> | <span data-ttu-id="fb704-117">O</span><span class="sxs-lookup"><span data-stu-id="fb704-117">Y</span></span>   | <span data-ttu-id="fb704-118">N</span><span class="sxs-lookup"><span data-stu-id="fb704-118">N</span></span>        |
| <span data-ttu-id="fb704-119">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="fb704-119">RetainOffsets</span></span> | <span data-ttu-id="fb704-120">text</span><span class="sxs-lookup"><span data-stu-id="fb704-120">text</span></span> |     | <span data-ttu-id="fb704-121">N</span><span class="sxs-lookup"><span data-stu-id="fb704-121">N</span></span>        |
| <span data-ttu-id="fb704-122">RetainLengths</span><span class="sxs-lookup"><span data-stu-id="fb704-122">RetainLengths</span></span> | <span data-ttu-id="fb704-123">text</span><span class="sxs-lookup"><span data-stu-id="fb704-123">text</span></span> |     | <span data-ttu-id="fb704-124">N</span><span class="sxs-lookup"><span data-stu-id="fb704-124">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fb704-125">Colonnes</span><span class="sxs-lookup"><span data-stu-id="fb704-125">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fb704-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famille</span><span class="sxs-lookup"><span data-stu-id="fb704-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="fb704-127">Clé étrangère vers la colonne Family de la [table ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="fb704-127">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb704-128"><span id="FTK"></span><span id="ftk"></span>TCTI</span><span class="sxs-lookup"><span data-stu-id="fb704-128"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="fb704-129">Clé étrangère dans les [tables de fichiers](file-table.md) de toutes les images mises à niveau dans la famille d’images.</span><span class="sxs-lookup"><span data-stu-id="fb704-129">Foreign key into the [File tables](file-table.md) of all the upgraded images in the image family.</span></span>

</dd> <dt>

<span data-ttu-id="fb704-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="fb704-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="fb704-131">Décalage des plages qui ne peuvent pas être remplacées.</span><span class="sxs-lookup"><span data-stu-id="fb704-131">The offset of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="fb704-132">La valeur de ce champ est une liste de valeurs de décalage de plage pour les plages qui ne sont pas remplacées dans les fichiers cibles.</span><span class="sxs-lookup"><span data-stu-id="fb704-132">The value in this field is a list of the range offset numbers for ranges that are not to be overwritten in the target files.</span></span> <span data-ttu-id="fb704-133">L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne RetainLengths.</span><span class="sxs-lookup"><span data-stu-id="fb704-133">The order and number of the ranges in the list must match the items in the RetainLengths column.</span></span>

<span data-ttu-id="fb704-134">Les valeurs peuvent être décimales ou hexadécimales.</span><span class="sxs-lookup"><span data-stu-id="fb704-134">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="fb704-135">[Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ».</span><span class="sxs-lookup"><span data-stu-id="fb704-135">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="fb704-136">Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="fb704-136">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="fb704-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span><span class="sxs-lookup"><span data-stu-id="fb704-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span></span>
</dt> <dd>

<span data-ttu-id="fb704-138">Longueur, en octets, des plages qui ne peuvent pas être remplacées.</span><span class="sxs-lookup"><span data-stu-id="fb704-138">The length in bytes of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="fb704-139">La valeur de ce champ est une liste de valeurs de longueur de plage à conserver dans les fichiers cibles.</span><span class="sxs-lookup"><span data-stu-id="fb704-139">The value in this field is a list of range length numbers for ranges to retain in target files.</span></span> <span data-ttu-id="fb704-140">L’ordre et le nombre des plages dans la liste doivent correspondre aux éléments de la colonne RetainOffsets.</span><span class="sxs-lookup"><span data-stu-id="fb704-140">The order and number of the ranges in the list must match the items in the RetainOffsets column.</span></span>

<span data-ttu-id="fb704-141">Les valeurs peuvent être décimales ou hexadécimales.</span><span class="sxs-lookup"><span data-stu-id="fb704-141">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="fb704-142">[Patchwiz.dll](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ».</span><span class="sxs-lookup"><span data-stu-id="fb704-142">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="fb704-143">Les colonnes sont des colonnes de type chaîne et Patchwiz.dll convertit les valeurs en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="fb704-143">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb704-144">Notes</span><span class="sxs-lookup"><span data-stu-id="fb704-144">Remarks</span></span>

<span data-ttu-id="fb704-145">Les décalages et les longueurs entrés dans RetainOffsets et RetainLengths ne doivent pas spécifier des plages qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="fb704-145">The offsets and lengths entered in RetainOffsets and RetainLengths must not specify overlapping ranges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb704-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb704-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb704-147">Mise à jour corrective des régions sélectionnées d’un fichier</span><span class="sxs-lookup"><span data-stu-id="fb704-147">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 




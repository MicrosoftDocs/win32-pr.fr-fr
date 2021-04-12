---
description: La table UpgradedImages contient des informations sur les images mises à niveau du produit.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: Table UpgradedImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320558"
---
# <a name="upgradedimages-table-patchwizdll"></a><span data-ttu-id="f0002-103">Table UpgradedImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f0002-103">UpgradedImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="f0002-104">La table UpgradedImages contient des informations sur les images mises à niveau du produit.</span><span class="sxs-lookup"><span data-stu-id="f0002-104">The UpgradedImages table contains information about the upgraded images of the product.</span></span> <span data-ttu-id="f0002-105">L’image mise à niveau doit être une image d’installation entièrement décompressée de la version la plus récente du produit, par exemple, une image administrative ou une image d’installation non compressée à partir d’un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="f0002-105">The upgraded image should be a fully uncompressed setup image of the latest version of the product, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="f0002-106">Un package de correctifs Windows Installer met à jour une image cible en une image mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="f0002-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span> <span data-ttu-id="f0002-107">La table UpgradedImages est requise dans la base de données de création de correctifs (fichier. PCP) et est utilisée par [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="f0002-107">The UpgradedImages table is required in the patch creation database (.pcp file) and is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="f0002-108">Une table UpgradedImages contenant au moins un enregistrement est requise dans chaque base de données de création de correctif (fichier. PCP).</span><span class="sxs-lookup"><span data-stu-id="f0002-108">An UpgradedImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="f0002-109">Cette table est utilisée par [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="f0002-109">This table is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="f0002-110">La table UpgradedImages contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0002-110">The UpgradedImages table has the following columns.</span></span>



| <span data-ttu-id="f0002-111">Colonne</span><span class="sxs-lookup"><span data-stu-id="f0002-111">Column</span></span>       | <span data-ttu-id="f0002-112">Type</span><span class="sxs-lookup"><span data-stu-id="f0002-112">Type</span></span> | <span data-ttu-id="f0002-113">Clé</span><span class="sxs-lookup"><span data-stu-id="f0002-113">Key</span></span> | <span data-ttu-id="f0002-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="f0002-114">Nullable</span></span> |
|--------------|------|-----|----------|
| <span data-ttu-id="f0002-115">Upgraded</span><span class="sxs-lookup"><span data-stu-id="f0002-115">Upgraded</span></span>     | <span data-ttu-id="f0002-116">text</span><span class="sxs-lookup"><span data-stu-id="f0002-116">text</span></span> | <span data-ttu-id="f0002-117">O</span><span class="sxs-lookup"><span data-stu-id="f0002-117">Y</span></span>   | <span data-ttu-id="f0002-118">N</span><span class="sxs-lookup"><span data-stu-id="f0002-118">N</span></span>        |
| <span data-ttu-id="f0002-119">MsiPath</span><span class="sxs-lookup"><span data-stu-id="f0002-119">MsiPath</span></span>      | <span data-ttu-id="f0002-120">text</span><span class="sxs-lookup"><span data-stu-id="f0002-120">text</span></span> |     | <span data-ttu-id="f0002-121">N</span><span class="sxs-lookup"><span data-stu-id="f0002-121">N</span></span>        |
| <span data-ttu-id="f0002-122">PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="f0002-122">PatchMsiPath</span></span> | <span data-ttu-id="f0002-123">text</span><span class="sxs-lookup"><span data-stu-id="f0002-123">text</span></span> |     | <span data-ttu-id="f0002-124">O</span><span class="sxs-lookup"><span data-stu-id="f0002-124">Y</span></span>        |
| <span data-ttu-id="f0002-125">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="f0002-125">SymbolPaths</span></span>  | <span data-ttu-id="f0002-126">text</span><span class="sxs-lookup"><span data-stu-id="f0002-126">text</span></span> |     | <span data-ttu-id="f0002-127">O</span><span class="sxs-lookup"><span data-stu-id="f0002-127">Y</span></span>        |
| <span data-ttu-id="f0002-128">Famille</span><span class="sxs-lookup"><span data-stu-id="f0002-128">Family</span></span>       | <span data-ttu-id="f0002-129">text</span><span class="sxs-lookup"><span data-stu-id="f0002-129">text</span></span> |     | <span data-ttu-id="f0002-130">N</span><span class="sxs-lookup"><span data-stu-id="f0002-130">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f0002-131">Colonnes</span><span class="sxs-lookup"><span data-stu-id="f0002-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f0002-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Mis à niveau</span><span class="sxs-lookup"><span data-stu-id="f0002-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="f0002-133">Le champ mis à niveau est un identificateur arbitraire permettant de connecter les images cibles à une image mise à niveau du produit.</span><span class="sxs-lookup"><span data-stu-id="f0002-133">The Upgraded field is an arbitrary identifier to connect the target images with an upgraded image of the product.</span></span>

</dd> <dt>

<span data-ttu-id="f0002-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span><span class="sxs-lookup"><span data-stu-id="f0002-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="f0002-135">Ce champ spécifie le chemin d’accès complet, y compris le nom de fichier, à l’emplacement du fichier. msi pour l’image mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="f0002-135">This field specifies the full path, including the file name, to the location of the .msi file for the upgraded image.</span></span> <span data-ttu-id="f0002-136">Il s’agit de l’emplacement des fichiers sources de l’image mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="f0002-136">This is the location of the source files for the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="f0002-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="f0002-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span></span>
</dt> <dd>

<span data-ttu-id="f0002-138">Le patchMsiPath facultatif pointe vers une copie modifiée de la base de données d’installation mise à niveau qui contient des créations supplémentaires spécifiques au processus d’installation des correctifs.</span><span class="sxs-lookup"><span data-stu-id="f0002-138">The optional patchMsiPath points to a modified copy of the upgraded installation database that contains additional authoring specific to the patch installation process.</span></span> <span data-ttu-id="f0002-139">Par exemple, des boîtes de dialogue supplémentaires ou des actions personnalisées sont conditionnées sur la propriété [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="f0002-139">For example, additional dialogs or custom actions conditioned on the [**PATCH**](patch.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="f0002-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="f0002-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="f0002-141">Liste délimitée par des points-virgules des dossiers dans lesquels rechercher les fichiers de symboles qui peuvent être utilisés pour optimiser la génération du correctif binaire.</span><span class="sxs-lookup"><span data-stu-id="f0002-141">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="f0002-142">Notez que les sous-répertoires des dossiers spécifiés dans ce champ ne sont pas recherchés.</span><span class="sxs-lookup"><span data-stu-id="f0002-142">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="f0002-143">Un correctif binaire optimisé peut être plus petit.</span><span class="sxs-lookup"><span data-stu-id="f0002-143">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="f0002-144">Visual C++ doit être installé sur l’ordinateur générant le correctif et utilisé pour créer les fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="f0002-144">Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="f0002-145">Ce champ est facultatif et le programme d’installation crée un correctif binaire même si aucun fichier de symboles n’est spécifié ou si les fichiers de symboles ne sont pas disponibles pour Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="f0002-145">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="f0002-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famille</span><span class="sxs-lookup"><span data-stu-id="f0002-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="f0002-147">Clé étrangère dans la [table ImageFamilies](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="f0002-147">Foreign key into the [ImageFamilies table](imagefamilies-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="f0002-148">Chaque image mise à niveau ne doit appartenir qu’à une seule famille.</span><span class="sxs-lookup"><span data-stu-id="f0002-148">Each upgraded image must belong to only one family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0002-149">Notes</span><span class="sxs-lookup"><span data-stu-id="f0002-149">Remarks</span></span>

<span data-ttu-id="f0002-150">Bien que chaque image mise à niveau puisse être regroupée dans une famille d’images distincte, le regroupement d’images mises à niveau qui partagent des fichiers peut rendre le fichier. msp plus petit.</span><span class="sxs-lookup"><span data-stu-id="f0002-150">Although each upgraded image can be grouped into a separate image family, grouping upgraded images that share files together may make the .msp smaller.</span></span>

<span data-ttu-id="f0002-151">Cette table accepte les variables d’environnement en tant que chemins d’accès commençant par la version 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="f0002-151">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 




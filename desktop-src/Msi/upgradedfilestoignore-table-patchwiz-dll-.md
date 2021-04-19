---
description: La table UpgradedFilesToIgnore empêche la mise à jour de fichiers spécifiques qui sont en fait modifiés dans l’image mise à niveau par rapport aux images cibles.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Table UpgradedFilesToIgnore (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a235759251ac3dadbe01b030c0d984d1f66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541999"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a><span data-ttu-id="4d398-103">Table UpgradedFilesToIgnore (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="4d398-103">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>

<span data-ttu-id="4d398-104">La table UpgradedFilesToIgnore empêche la mise à jour de fichiers spécifiques qui sont en fait modifiés dans l’image mise à niveau par rapport aux images cibles.</span><span class="sxs-lookup"><span data-stu-id="4d398-104">The UpgradedFilesToIgnore table prevents the updating of specific files that are in fact changed in the upgraded image relative to the target images.</span></span> <span data-ttu-id="4d398-105">Il peut être utile de le faire dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="4d398-105">It may be useful to do this in certain cases.</span></span> <span data-ttu-id="4d398-106">Par exemple, un package de correctifs destiné uniquement à être utilisé avec des installations non administratives n’a pas besoin d’inclure des fichiers de mise à jour corrective qui font uniquement partie des images administratives.</span><span class="sxs-lookup"><span data-stu-id="4d398-106">For example, a patch package intended only for use with non-administrative installations does not need to include patching files that are only part of administrative images.</span></span> <span data-ttu-id="4d398-107">L’exclusion de fichiers utilisés uniquement dans les images d’administration peut réduire la taille du package de correctifs. Toutefois, les administrateurs doivent être informés de la mise à jour de ces fichiers séparément.</span><span class="sxs-lookup"><span data-stu-id="4d398-107">Excluding such files used only in administrative images can reduce the size of the patch package; however, administrators should be informed on how to update these files separately.</span></span> <span data-ttu-id="4d398-108">Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="4d398-108">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="4d398-109">La table UpgradedFilesToIgnore contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d398-109">The UpgradedFilesToIgnore table has the following columns.</span></span>



| <span data-ttu-id="4d398-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="4d398-110">Column</span></span>   | <span data-ttu-id="4d398-111">Type</span><span class="sxs-lookup"><span data-stu-id="4d398-111">Type</span></span> | <span data-ttu-id="4d398-112">Clé</span><span class="sxs-lookup"><span data-stu-id="4d398-112">Key</span></span> | <span data-ttu-id="4d398-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="4d398-113">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="4d398-114">Upgraded</span><span class="sxs-lookup"><span data-stu-id="4d398-114">Upgraded</span></span> | <span data-ttu-id="4d398-115">text</span><span class="sxs-lookup"><span data-stu-id="4d398-115">text</span></span> | <span data-ttu-id="4d398-116">O</span><span class="sxs-lookup"><span data-stu-id="4d398-116">Y</span></span>   | <span data-ttu-id="4d398-117">N</span><span class="sxs-lookup"><span data-stu-id="4d398-117">N</span></span>        |
| <span data-ttu-id="4d398-118">TCTI</span><span class="sxs-lookup"><span data-stu-id="4d398-118">FTK</span></span>      | <span data-ttu-id="4d398-119">text</span><span class="sxs-lookup"><span data-stu-id="4d398-119">text</span></span> | <span data-ttu-id="4d398-120">O</span><span class="sxs-lookup"><span data-stu-id="4d398-120">Y</span></span>   | <span data-ttu-id="4d398-121">N</span><span class="sxs-lookup"><span data-stu-id="4d398-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4d398-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="4d398-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4d398-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Mis à niveau</span><span class="sxs-lookup"><span data-stu-id="4d398-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="4d398-124">Clé étrangère vers la colonne mise à niveau de la [table UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="4d398-124">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="4d398-125">L’outil de création de correctifs exclut la mise à jour du fichier spécifié dans la colonne TCTI de la table UpgradedFilesToIgnore lors de la mise à niveau d’une cible vers l’image spécifiée dans le champ mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="4d398-125">The patch creation tool excludes updating the file specified in the FTK column of the UpgradedFilesToIgnore table when upgrading a target to the image specified in the Upgraded field.</span></span> <span data-ttu-id="4d398-126">Entrez la valeur « \* » dans le champ mis à niveau pour exclure la mise à jour du fichier pour toutes les images mises à niveau.</span><span class="sxs-lookup"><span data-stu-id="4d398-126">Enter a value of "\*" in the Upgraded field to exclude updating the file for all upgraded images.</span></span>

</dd> <dt>

<span data-ttu-id="4d398-127"><span id="FTK"></span><span id="ftk"></span>TCTI</span><span class="sxs-lookup"><span data-stu-id="4d398-127"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="4d398-128">Clé étrangère dans la [table de fichiers](file-table.md) de l’image mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="4d398-128">Foreign key into the [File table](file-table.md) of the upgraded image.</span></span> <span data-ttu-id="4d398-129">Une valeur de la forme « <prefix> \* » correspond à toutes les clés de table de fichiers de la table de fichiers qui commencent par ce préfixe.</span><span class="sxs-lookup"><span data-stu-id="4d398-129">A value of the form "<prefix>\*" matches all file table keys in the File table that begin with that prefix.</span></span> <span data-ttu-id="4d398-130">Aucun texte ne peut suivre l’astérisque.</span><span class="sxs-lookup"><span data-stu-id="4d398-130">No text can follow the asterisk.</span></span>

</dd> </dl>

 

 




---
description: La \_ table UpgradedFile OptionalData contient des informations sur des fichiers spécifiques d’une image mise à niveau. Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: Table UpgradedFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210450"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="002b7-104">UpgradedFiles \_ OptionalData, table (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="002b7-104">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="002b7-105">La \_ table UpgradedFile OptionalData contient des informations sur des fichiers spécifiques d’une image mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="002b7-105">The UpgradedFile\_OptionalData table contains information about specific files in an upgraded image.</span></span> <span data-ttu-id="002b7-106">Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="002b7-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="002b7-107">La \_ table UpgradedFile OptionalData contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="002b7-107">The UpgradedFile\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="002b7-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="002b7-108">Column</span></span>                  | <span data-ttu-id="002b7-109">Type</span><span class="sxs-lookup"><span data-stu-id="002b7-109">Type</span></span>    | <span data-ttu-id="002b7-110">Clé</span><span class="sxs-lookup"><span data-stu-id="002b7-110">Key</span></span> | <span data-ttu-id="002b7-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="002b7-111">Nullable</span></span> |
|-------------------------|---------|-----|----------|
| <span data-ttu-id="002b7-112">Upgraded</span><span class="sxs-lookup"><span data-stu-id="002b7-112">Upgraded</span></span>                | <span data-ttu-id="002b7-113">text</span><span class="sxs-lookup"><span data-stu-id="002b7-113">text</span></span>    | <span data-ttu-id="002b7-114">O</span><span class="sxs-lookup"><span data-stu-id="002b7-114">Y</span></span>   | <span data-ttu-id="002b7-115">N</span><span class="sxs-lookup"><span data-stu-id="002b7-115">N</span></span>        |
| <span data-ttu-id="002b7-116">TCTI</span><span class="sxs-lookup"><span data-stu-id="002b7-116">FTK</span></span>                     | <span data-ttu-id="002b7-117">text</span><span class="sxs-lookup"><span data-stu-id="002b7-117">text</span></span>    | <span data-ttu-id="002b7-118">O</span><span class="sxs-lookup"><span data-stu-id="002b7-118">Y</span></span>   | <span data-ttu-id="002b7-119">N</span><span class="sxs-lookup"><span data-stu-id="002b7-119">N</span></span>        |
| <span data-ttu-id="002b7-120">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="002b7-120">SymbolPaths</span></span>             | <span data-ttu-id="002b7-121">text</span><span class="sxs-lookup"><span data-stu-id="002b7-121">text</span></span>    |     | <span data-ttu-id="002b7-122">O</span><span class="sxs-lookup"><span data-stu-id="002b7-122">Y</span></span>        |
| <span data-ttu-id="002b7-123">AllowIgnoreOnPatchError</span><span class="sxs-lookup"><span data-stu-id="002b7-123">AllowIgnoreOnPatchError</span></span> | <span data-ttu-id="002b7-124">entier</span><span class="sxs-lookup"><span data-stu-id="002b7-124">integer</span></span> |     | <span data-ttu-id="002b7-125">O</span><span class="sxs-lookup"><span data-stu-id="002b7-125">Y</span></span>        |
| <span data-ttu-id="002b7-126">IncludeWholeFile</span><span class="sxs-lookup"><span data-stu-id="002b7-126">IncludeWholeFile</span></span>        | <span data-ttu-id="002b7-127">entier</span><span class="sxs-lookup"><span data-stu-id="002b7-127">integer</span></span> |     | <span data-ttu-id="002b7-128">O</span><span class="sxs-lookup"><span data-stu-id="002b7-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="002b7-129">Colonnes</span><span class="sxs-lookup"><span data-stu-id="002b7-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="002b7-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Mis à niveau</span><span class="sxs-lookup"><span data-stu-id="002b7-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="002b7-131">Clé étrangère vers la colonne mise à niveau de la [table UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="002b7-131">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="002b7-132"><span id="FTK"></span><span id="ftk"></span>TCTI</span><span class="sxs-lookup"><span data-stu-id="002b7-132"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="002b7-133">Clé de table de fichiers.</span><span class="sxs-lookup"><span data-stu-id="002b7-133">File table key.</span></span> <span data-ttu-id="002b7-134">Clé étrangère dans la [table de fichiers](file-table.md) du fichier. msi de l’image mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="002b7-134">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span> <span data-ttu-id="002b7-135">Si au moins deux images mises à niveau dans une famille ont la même valeur TCTI, la valeur doit faire référence au même fichier.</span><span class="sxs-lookup"><span data-stu-id="002b7-135">If two or more upgraded images within a family have the same FTK value, the value must refer to the same file.</span></span> <span data-ttu-id="002b7-136">Les fichiers partagés par plusieurs images de mise à niveau doivent avoir le même TCTI pour réduire la taille du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="002b7-136">Files shared by multiple upgrade images should have the same FTK to minimize cabinet file size.</span></span>

</dd> <dt>

<span data-ttu-id="002b7-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="002b7-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="002b7-138">La valeur de ce champ est ajoutée à la liste de dossiers délimités par des points-virgules dans la colonne SymbolPaths de la [table UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) lorsque le correctif est généré et peut être utilisé pour ajouter des fichiers de symboles pour un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="002b7-138">The value in this field is added to the semicolon-delimited list of folders in the SymbolPaths column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="002b7-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span><span class="sxs-lookup"><span data-stu-id="002b7-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span></span>
</dt> <dd>

<span data-ttu-id="002b7-140">Affectez la valeur 1 pour indiquer que le correctif logiciel n’est pas vital.</span><span class="sxs-lookup"><span data-stu-id="002b7-140">Set to 1 to indicate that the patch is non-vital.</span></span> <span data-ttu-id="002b7-141">Attribuez la valeur 0 pour indiquer que le correctif est vital.</span><span class="sxs-lookup"><span data-stu-id="002b7-141">Set to 0 to indicate that the patch is vital.</span></span> <span data-ttu-id="002b7-142">Si Windows Installer rencontre un problème lors de l’application de ce correctif au fichier spécifié dans la colonne TCTI, la valeur de ce champ détermine si la boîte de message d’erreur contient un bouton **Ignorer** pour permettre à l’utilisateur de poursuivre le processus de mise à jour corrective.</span><span class="sxs-lookup"><span data-stu-id="002b7-142">If Windows Installer encounters a problem when applying this patch to the file specified in the FTK column, the value in this field determines whether the error message box includes an **Ignore** button to enable the user to continue the patching process.</span></span>

</dd> <dt>

<span data-ttu-id="002b7-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span><span class="sxs-lookup"><span data-stu-id="002b7-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span></span>
</dt> <dd>

<span data-ttu-id="002b7-144">Affectez une valeur différente de zéro si l’intégralité du fichier spécifié dans la colonne TCTI doit être installée au lieu de créer un correctif binaire.</span><span class="sxs-lookup"><span data-stu-id="002b7-144">Set to a nonzero value if the entire file specified in the FTK column should be installed rather than creating a binary patch.</span></span>

</dd> </dl>

 

 




---
description: La table MsiPatchOldAssemblyFile lie un fichier de la table file à un nom d’assembly dans la table MsiPatchOldAssemblyName. Plusieurs anciens noms d’assembly peuvent être associés à un seul fichier.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Table MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518938"
---
# <a name="msipatcholdassemblyfile-table"></a><span data-ttu-id="f3162-104">Table MsiPatchOldAssemblyFile</span><span class="sxs-lookup"><span data-stu-id="f3162-104">MsiPatchOldAssemblyFile Table</span></span>

<span data-ttu-id="f3162-105">La table MsiPatchOldAssemblyFile lie un fichier de la [table file](file-table.md) à un nom d’assembly dans la [table MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md).</span><span class="sxs-lookup"><span data-stu-id="f3162-105">The MsiPatchOldAssemblyFile table relates a file in the [File table](file-table.md) to an assembly name in the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md).</span></span> <span data-ttu-id="f3162-106">Plusieurs anciens noms d’assembly peuvent être associés à un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="f3162-106">Multiple old assembly names can be associated with a single file.</span></span>

<span data-ttu-id="f3162-107">La table MsiPatchOldAssemblyFile contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f3162-107">The MsiPatchOldAssemblyFile table has the following columns.</span></span>



| <span data-ttu-id="f3162-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="f3162-108">Column</span></span>     | <span data-ttu-id="f3162-109">Type</span><span class="sxs-lookup"><span data-stu-id="f3162-109">Type</span></span>                         | <span data-ttu-id="f3162-110">Clé</span><span class="sxs-lookup"><span data-stu-id="f3162-110">Key</span></span> | <span data-ttu-id="f3162-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="f3162-111">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="f3162-112">fichier\_</span><span class="sxs-lookup"><span data-stu-id="f3162-112">File\_</span></span>     | [<span data-ttu-id="f3162-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f3162-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="f3162-114">O</span><span class="sxs-lookup"><span data-stu-id="f3162-114">Y</span></span>   | <span data-ttu-id="f3162-115">N</span><span class="sxs-lookup"><span data-stu-id="f3162-115">N</span></span>        |
| <span data-ttu-id="f3162-116">Chargeur\_</span><span class="sxs-lookup"><span data-stu-id="f3162-116">Assembly\_</span></span> | [<span data-ttu-id="f3162-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f3162-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="f3162-118">O</span><span class="sxs-lookup"><span data-stu-id="f3162-118">Y</span></span>   | <span data-ttu-id="f3162-119">N</span><span class="sxs-lookup"><span data-stu-id="f3162-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f3162-120">Colonnes</span><span class="sxs-lookup"><span data-stu-id="f3162-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f3162-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="f3162-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="f3162-122">Clé étrangère vers la [table de fichiers](file-table.md) qui spécifie l’assembly à corriger.</span><span class="sxs-lookup"><span data-stu-id="f3162-122">Foreign key to the [File table](file-table.md) that specifies the assembly to be patched.</span></span> <span data-ttu-id="f3162-123">Cette colonne fait partie de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="f3162-123">This column is part of the primary key.</span></span>

</dd> <dt>

<span data-ttu-id="f3162-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Chargeur\_</span><span class="sxs-lookup"><span data-stu-id="f3162-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembly\_</span></span>
</dt> <dd>

<span data-ttu-id="f3162-125">Clé étrangère vers la [table MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) qui identifie l’un des anciens noms d’assembly pour l’assembly.</span><span class="sxs-lookup"><span data-stu-id="f3162-125">Foreign key to the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) that identifies one of the old assembly names for the assembly.</span></span> <span data-ttu-id="f3162-126">Cette colonne fait partie de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="f3162-126">This column is part of the primary key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3162-127">Notes</span><span class="sxs-lookup"><span data-stu-id="f3162-127">Remarks</span></span>

<span data-ttu-id="f3162-128">Windows Installer utilise la table MsiPatchOldAssemblyFile et la [table MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) lors de la mise à jour corrective des assemblys installés dans le global assembly cache (GAC).</span><span class="sxs-lookup"><span data-stu-id="f3162-128">Windows Installer uses the MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="f3162-129">Lors de la publication d’une version plus récente d’un assembly, le nom fort de l’assembly est modifié.</span><span class="sxs-lookup"><span data-stu-id="f3162-129">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="f3162-130">Les deux tables identifient ensemble l’ancien nom d’assembly pour un assembly mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f3162-130">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="f3162-131">Cela permet au programme d’installation d’utiliser l’ancien nom d’assembly pour rechercher le fichier d’origine dans le GAC et d’appliquer un correctif binaire.</span><span class="sxs-lookup"><span data-stu-id="f3162-131">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="f3162-132">Sans ces informations, le programme d’installation devra peut-être accéder à la source d’installation d’origine afin de corriger un assembly installé dans le GAC.</span><span class="sxs-lookup"><span data-stu-id="f3162-132">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="f3162-133">La table MsiPatchOldAssemblyFile et la [table MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) ne sont pas générées automatiquement par [PatchWiz](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="f3162-133">The MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="f3162-134">Le package de mise à jour spécifié dans la [table UpgradedImages](upgradedimages-table-patchwiz-dll-.md) doit contenir ces tables pour que le correctif dispose de ces informations.</span><span class="sxs-lookup"><span data-stu-id="f3162-134">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="f3162-135">Validation</span><span class="sxs-lookup"><span data-stu-id="f3162-135">Validation</span></span>

<dl>

[<span data-ttu-id="f3162-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="f3162-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f3162-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="f3162-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f3162-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="f3162-138">ICE32</span></span>](ice32.md)  
</dl>

 

 




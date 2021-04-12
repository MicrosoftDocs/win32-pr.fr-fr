---
description: La table MsiPatchOldAssemblyName spécifie l’ancien nom d’un assembly.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Table MsiPatchOldAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319914"
---
# <a name="msipatcholdassemblyname-table"></a><span data-ttu-id="02211-103">Table MsiPatchOldAssemblyName</span><span class="sxs-lookup"><span data-stu-id="02211-103">MsiPatchOldAssemblyName Table</span></span>

<span data-ttu-id="02211-104">La table MsiPatchOldAssemblyName spécifie l’ancien nom d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="02211-104">The MsiPatchOldAssemblyName table specifies the old name for an assembly.</span></span>

<span data-ttu-id="02211-105">La table MsiPatchOldAssemblyName contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="02211-105">The MsiPatchOldAssemblyName table has the following columns.</span></span>



| <span data-ttu-id="02211-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="02211-106">Column</span></span>   | <span data-ttu-id="02211-107">Type</span><span class="sxs-lookup"><span data-stu-id="02211-107">Type</span></span>                         | <span data-ttu-id="02211-108">Clé</span><span class="sxs-lookup"><span data-stu-id="02211-108">Key</span></span> | <span data-ttu-id="02211-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="02211-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="02211-110">Assembly</span><span class="sxs-lookup"><span data-stu-id="02211-110">Assembly</span></span> | [<span data-ttu-id="02211-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="02211-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="02211-112">O</span><span class="sxs-lookup"><span data-stu-id="02211-112">Y</span></span>   | <span data-ttu-id="02211-113">N</span><span class="sxs-lookup"><span data-stu-id="02211-113">N</span></span>        |
| <span data-ttu-id="02211-114">Nom</span><span class="sxs-lookup"><span data-stu-id="02211-114">Name</span></span>     | [<span data-ttu-id="02211-115">Text</span><span class="sxs-lookup"><span data-stu-id="02211-115">Text</span></span>](text.md)             | <span data-ttu-id="02211-116">O</span><span class="sxs-lookup"><span data-stu-id="02211-116">Y</span></span>   | <span data-ttu-id="02211-117">N</span><span class="sxs-lookup"><span data-stu-id="02211-117">N</span></span>        |
| <span data-ttu-id="02211-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="02211-118">Value</span></span>    | [<span data-ttu-id="02211-119">Text</span><span class="sxs-lookup"><span data-stu-id="02211-119">Text</span></span>](text.md)             | <span data-ttu-id="02211-120">N</span><span class="sxs-lookup"><span data-stu-id="02211-120">N</span></span>   | <span data-ttu-id="02211-121">N</span><span class="sxs-lookup"><span data-stu-id="02211-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="02211-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="02211-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="02211-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Chargeur</span><span class="sxs-lookup"><span data-stu-id="02211-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembly</span></span>
</dt> <dd>

<span data-ttu-id="02211-124">Identificateur unique de l’ancien nom de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="02211-124">Unique identifier for the old assembly name.</span></span> <span data-ttu-id="02211-125">Cette clé est utilisée comme mappage entre cette table et la [table MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md).</span><span class="sxs-lookup"><span data-stu-id="02211-125">This key is used as a mapping between this and the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="02211-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="02211-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="02211-127">Nom de l’attribut associé à la valeur spécifiée dans la colonne valeur.</span><span class="sxs-lookup"><span data-stu-id="02211-127">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="02211-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="02211-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="02211-129">Valeur associée au nom spécifié dans la colonne nom.</span><span class="sxs-lookup"><span data-stu-id="02211-129">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02211-130">Notes</span><span class="sxs-lookup"><span data-stu-id="02211-130">Remarks</span></span>

<span data-ttu-id="02211-131">Windows Installer utilise la table [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) et la table MsiPatchOldAssemblyName lors de la mise à jour corrective des assemblys installés dans le global assembly cache (GAC).</span><span class="sxs-lookup"><span data-stu-id="02211-131">Windows Installer uses the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="02211-132">Lors de la publication d’une version plus récente d’un assembly, le nom fort de l’assembly est modifié.</span><span class="sxs-lookup"><span data-stu-id="02211-132">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="02211-133">Les deux tables identifient ensemble l’ancien nom d’assembly pour un assembly mis à jour.</span><span class="sxs-lookup"><span data-stu-id="02211-133">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="02211-134">Cela permet au programme d’installation d’utiliser l’ancien nom d’assembly pour rechercher le fichier d’origine dans le GAC et d’appliquer un correctif binaire.</span><span class="sxs-lookup"><span data-stu-id="02211-134">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="02211-135">Sans ces informations, le programme d’installation devra peut-être accéder à la source d’installation d’origine afin de corriger un assembly installé dans le GAC.</span><span class="sxs-lookup"><span data-stu-id="02211-135">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="02211-136">La table [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) et la table MsiPatchOldAssemblyName ne sont pas générées automatiquement par [PatchWiz](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="02211-136">The [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="02211-137">Le package de mise à jour spécifié dans la [table UpgradedImages](upgradedimages-table-patchwiz-dll-.md) doit contenir ces tables pour que le correctif dispose de ces informations.</span><span class="sxs-lookup"><span data-stu-id="02211-137">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="02211-138">Validation</span><span class="sxs-lookup"><span data-stu-id="02211-138">Validation</span></span>

<dl>

[<span data-ttu-id="02211-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="02211-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="02211-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="02211-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="02211-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="02211-141">ICE32</span></span>](ice32.md)  
</dl>

 

 




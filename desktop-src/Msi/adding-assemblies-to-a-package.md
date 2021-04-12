---
description: Windows Installer développeurs peuvent utiliser les instructions de cette rubrique pour créer des packages Windows Installer qui contiennent des assemblys.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Ajout d’assemblys à un package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202565"
---
# <a name="adding-assemblies-to-a-package"></a><span data-ttu-id="de251-103">Ajout d’assemblys à un package</span><span class="sxs-lookup"><span data-stu-id="de251-103">Adding Assemblies to a Package</span></span>

<span data-ttu-id="de251-104">Windows Installer développeurs peuvent utiliser les instructions de cette rubrique pour créer des packages Windows Installer qui contiennent des assemblys.</span><span class="sxs-lookup"><span data-stu-id="de251-104">Windows Installer developers can use the guidelines in this topic to author Windows Installer packages that contain assemblies.</span></span>

<span data-ttu-id="de251-105">Les indications suivantes s’appliquent aux assemblys Win32 et aux assemblys que la common language runtime de l’infrastructure de Microsoft .NET utilise.</span><span class="sxs-lookup"><span data-stu-id="de251-105">The following guidelines apply to Win32 assemblies, and assemblies that the common language runtime of the Microsoft .NET Framework uses.</span></span>

-   <span data-ttu-id="de251-106">Un composant Windows Installer ne doit pas contenir plus d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="de251-106">A Windows Installer component should contain no more than one assembly.</span></span>
-   <span data-ttu-id="de251-107">Tous les fichiers de l’assembly doivent se trouver dans un seul composant.</span><span class="sxs-lookup"><span data-stu-id="de251-107">All of the files in the assembly should be in a single component.</span></span>
-   <span data-ttu-id="de251-108">Chaque composant qui contient un assembly doit avoir une entrée dans la table [MsiAssembly](msiassembly-table.md) .</span><span class="sxs-lookup"><span data-stu-id="de251-108">Each component that contains an assembly should have an entry in the [MsiAssembly](msiassembly-table.md) table.</span></span>
-   <span data-ttu-id="de251-109">Le nom fort du cache d’assembly de chaque assembly doit être créé dans la table [MsiAssemblyName](msiassemblyname-table.md) .</span><span class="sxs-lookup"><span data-stu-id="de251-109">The strong assembly cache name of each assembly should be authored into the [MsiAssemblyName](msiassemblyname-table.md) table.</span></span>
-   <span data-ttu-id="de251-110">Utilisez la table de [Registre](registry-table.md) au lieu de la table de [classe](class-table.md) lorsque vous inscrivez COM Interop pour un assembly.</span><span class="sxs-lookup"><span data-stu-id="de251-110">Use the [Registry](registry-table.md) table instead of the [Class](class-table.md) table when you register COM Interop for an assembly.</span></span>
-   <span data-ttu-id="de251-111">Les assemblys qui ont le même nom fort sont le même assembly.</span><span class="sxs-lookup"><span data-stu-id="de251-111">Assemblies that have the same strong name are the same assembly.</span></span> <span data-ttu-id="de251-112">Lorsque le même assembly est installé par différentes applications, les composants qui contiennent l’assembly doivent utiliser la même valeur pour l’ID de composant dans leurs tables de [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="de251-112">When the same assembly is installed by different applications, the components that contain the assembly should use the same value for the ComponentId in their [Component](component-table.md) tables.</span></span>

> [!Note]  
> <span data-ttu-id="de251-113">Les publications de produit identifient les assemblys qui peuvent être installés et utilisés par différentes applications.</span><span class="sxs-lookup"><span data-stu-id="de251-113">Product advertisements identify assemblies that can be installed and used by different applications.</span></span> <span data-ttu-id="de251-114">Les publications de produit n’identifient pas les assemblys privés.</span><span class="sxs-lookup"><span data-stu-id="de251-114">Product advertisements do not identify private assemblies.</span></span>

 

## <a name="adding-win32-assemblies"></a><span data-ttu-id="de251-115">Ajout d’assemblys Win32</span><span class="sxs-lookup"><span data-stu-id="de251-115">Adding Win32 Assemblies</span></span>

<span data-ttu-id="de251-116">Utilisez les instructions suivantes lorsque vous incluez des assemblys Win32 :</span><span class="sxs-lookup"><span data-stu-id="de251-116">Use the following guidelines when you include Win32 assemblies:</span></span>

-   <span data-ttu-id="de251-117">La valeur keyPath dans la table [Component](component-table.md) pour un composant qui contient un assembly Win32 ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="de251-117">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly should not be Null.</span></span>
-   <span data-ttu-id="de251-118">La valeur keyPath dans la table [Component](component-table.md) pour un composant qui contient un assembly de stratégie Win32 doit être le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="de251-118">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 policy assembly should be the manifest file.</span></span>
-   <span data-ttu-id="de251-119">La valeur keyPath dans la table [Component](component-table.md) pour un composant qui contient un assembly Win32, qui n’est pas un assembly de stratégie, ne doit pas être le fichier manifeste ou le fichier catalogue.</span><span class="sxs-lookup"><span data-stu-id="de251-119">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly, that is not a policy assembly, should not be the manifest file or catalog file.</span></span> <span data-ttu-id="de251-120">Il doit s’agir d’un fichier différent dans l’assembly.</span><span class="sxs-lookup"><span data-stu-id="de251-120">It should be a different file in the assembly.</span></span>
-   <span data-ttu-id="de251-121">Ajoutez une ligne à la table [MsiAssemblyName](msiassemblyname-table.md) pour chaque paire nom/valeur répertoriée dans la section **assemblyIdentity** du manifeste de l’assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="de251-121">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each name and value pair that are listed in the **assemblyIdentity** section of the Win32 assembly's manifest.</span></span>

## <a name="adding-assemblies-used-with-the-net-framework"></a><span data-ttu-id="de251-122">Ajout d’assemblys utilisés avec le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="de251-122">Adding Assemblies used with the .NET Framework</span></span>

<span data-ttu-id="de251-123">Utilisez les instructions suivantes lorsque vous incluez des assemblys que la common language runtime de la .NET Framework utilise.</span><span class="sxs-lookup"><span data-stu-id="de251-123">Use the following guidelines when you include assemblies that the common language runtime of the .NET Framework uses.</span></span>

-   <span data-ttu-id="de251-124">La valeur keyPath dans la table des [composants](component-table.md) pour un composant qui contient l’assembly ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="de251-124">The KeyPath value in the [Component](component-table.md) table for a component that contains the assembly should not be Null.</span></span>
-   <span data-ttu-id="de251-125">Quand vous installez un assembly utilisé par le common language runtime dans le Global Assembly Cache, la valeur dans la \_ colonne application de fichier de la table MsiAssembly doit être null.</span><span class="sxs-lookup"><span data-stu-id="de251-125">When you install an assembly used by the common language runtime to the global assembly cache, the value in the File\_Application column of the MsiAssembly table must be Null.</span></span>
-   <span data-ttu-id="de251-126">Ajoutez une ligne à la table [MsiAssemblyName](msiassemblyname-table.md) pour chaque attribut du nom fort de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="de251-126">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each attribute of the assembly's strong name.</span></span> <span data-ttu-id="de251-127">Tous les assemblys doivent avoir les attributs Name, version et culture qui sont spécifiés dans la table MsiAssemblyName.</span><span class="sxs-lookup"><span data-stu-id="de251-127">All assemblies must have the Name, Version, and Culture attributes that are specified in the MsiAssemblyName table.</span></span> <span data-ttu-id="de251-128">Un attribut publicKeyToken est requis pour un assembly global.</span><span class="sxs-lookup"><span data-stu-id="de251-128">A publicKeyToken attribute is required for a global assembly.</span></span> <span data-ttu-id="de251-129">Le tableau suivant est un exemple de la table MsiAssemblyName pour un assembly global utilisé par le common language runtime.</span><span class="sxs-lookup"><span data-stu-id="de251-129">The following table is an example of the MsiAssemblyName table for a global assembly for use by the common language runtime.</span></span>

[<span data-ttu-id="de251-130">Table MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="de251-130">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)



| <span data-ttu-id="de251-131">Composant</span><span class="sxs-lookup"><span data-stu-id="de251-131">Component</span></span>  | <span data-ttu-id="de251-132">Nom</span><span class="sxs-lookup"><span data-stu-id="de251-132">Name</span></span>           | <span data-ttu-id="de251-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="de251-133">Value</span></span>            |
|------------|----------------|------------------|
| <span data-ttu-id="de251-134">Composant</span><span class="sxs-lookup"><span data-stu-id="de251-134">ComponentA</span></span> | <span data-ttu-id="de251-135">Nom</span><span class="sxs-lookup"><span data-stu-id="de251-135">Name</span></span>           | <span data-ttu-id="de251-136">simple</span><span class="sxs-lookup"><span data-stu-id="de251-136">simple</span></span>           |
| <span data-ttu-id="de251-137">Composant</span><span class="sxs-lookup"><span data-stu-id="de251-137">ComponentA</span></span> | <span data-ttu-id="de251-138">version</span><span class="sxs-lookup"><span data-stu-id="de251-138">version</span></span>        | <span data-ttu-id="de251-139">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="de251-139">1.0.0.0</span></span>          |
| <span data-ttu-id="de251-140">Composant</span><span class="sxs-lookup"><span data-stu-id="de251-140">ComponentA</span></span> | <span data-ttu-id="de251-141">Culture</span><span class="sxs-lookup"><span data-stu-id="de251-141">Culture</span></span>        | <span data-ttu-id="de251-142">neutre</span><span class="sxs-lookup"><span data-stu-id="de251-142">neutral</span></span>          |
| <span data-ttu-id="de251-143">Composant</span><span class="sxs-lookup"><span data-stu-id="de251-143">ComponentA</span></span> | <span data-ttu-id="de251-144">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="de251-144">publicKeyToken</span></span> | <span data-ttu-id="de251-145">9d1ec8380f483f5a</span><span class="sxs-lookup"><span data-stu-id="de251-145">9d1ec8380f483f5a</span></span> |



 

 

 




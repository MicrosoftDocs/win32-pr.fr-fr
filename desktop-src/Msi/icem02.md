---
description: ICEM02 vérifie que toutes les dépendances et exclusions de module sont liées au module en cours.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201792"
---
# <a name="icem02"></a><span data-ttu-id="93e23-103">ICEM02</span><span class="sxs-lookup"><span data-stu-id="93e23-103">ICEM02</span></span>

<span data-ttu-id="93e23-104">ICEM02 vérifie que toutes les dépendances et exclusions de module sont liées au module en cours.</span><span class="sxs-lookup"><span data-stu-id="93e23-104">ICEM02 verifies that all the module dependencies and exclusions are related to the current module.</span></span>

<span data-ttu-id="93e23-105">Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.</span><span class="sxs-lookup"><span data-stu-id="93e23-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="93e23-106">Résultats</span><span class="sxs-lookup"><span data-stu-id="93e23-106">Result</span></span>

<span data-ttu-id="93e23-107">ICEM02 publie des messages d’erreur si la base de données du module tente de spécifier des dépendances ou des exclusions qui ne sont pas liées au module en cours.</span><span class="sxs-lookup"><span data-stu-id="93e23-107">ICEM02 posts error messages if the module database attempts to specify dependencies or exclusions that do not relate to the current module.</span></span> <span data-ttu-id="93e23-108">ICEM02 publie un message d’erreur si la base de données du module tente de spécifier le module en cours comme dépendant ou comme étant exclu par lui-même.</span><span class="sxs-lookup"><span data-stu-id="93e23-108">ICEM02 posts an error message if the module database attempts to specify the current module as dependent or as excluded by itself.</span></span>

## <a name="example"></a><span data-ttu-id="93e23-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="93e23-109">Example</span></span>

<span data-ttu-id="93e23-110">ICEM02 publie les messages d’erreur suivants pour un module contenant les entrées de base de données indiquées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="93e23-110">ICEM02 would post the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[<span data-ttu-id="93e23-111">ModuleSignature, table</span><span class="sxs-lookup"><span data-stu-id="93e23-111">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="93e23-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="93e23-112">ModuleID</span></span>         | <span data-ttu-id="93e23-113">Langage</span><span class="sxs-lookup"><span data-stu-id="93e23-113">Language</span></span> | <span data-ttu-id="93e23-114">Version</span><span class="sxs-lookup"><span data-stu-id="93e23-114">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="93e23-115">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="93e23-115">MyModule.*GUID1*</span></span> | <span data-ttu-id="93e23-116">1033</span><span class="sxs-lookup"><span data-stu-id="93e23-116">1033</span></span>     | <span data-ttu-id="93e23-117">1.0</span><span class="sxs-lookup"><span data-stu-id="93e23-117">1.0</span></span>     |



 

[<span data-ttu-id="93e23-118">Table ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="93e23-118">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="93e23-119">ModuleID</span><span class="sxs-lookup"><span data-stu-id="93e23-119">ModuleID</span></span>            | <span data-ttu-id="93e23-120">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="93e23-120">ModuleLanguage</span></span> | <span data-ttu-id="93e23-121">RequiredID</span><span class="sxs-lookup"><span data-stu-id="93e23-121">RequiredID</span></span>          | <span data-ttu-id="93e23-122">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="93e23-122">RequiredLanguage</span></span> | <span data-ttu-id="93e23-123">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="93e23-123">RequiredVersion</span></span> |
|---------------------|----------------|---------------------|------------------|-----------------|
| <span data-ttu-id="93e23-124">OtherModule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="93e23-124">OtherModule.*GUID2*</span></span> | <span data-ttu-id="93e23-125">1033</span><span class="sxs-lookup"><span data-stu-id="93e23-125">1033</span></span>           | <span data-ttu-id="93e23-126">OtherModule. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="93e23-126">OtherModule.*GUID3*</span></span> | <span data-ttu-id="93e23-127">0</span><span class="sxs-lookup"><span data-stu-id="93e23-127">0</span></span>                | <span data-ttu-id="93e23-128">1.0</span><span class="sxs-lookup"><span data-stu-id="93e23-128">1.0</span></span>             |
| <span data-ttu-id="93e23-129">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="93e23-129">MyModule.*GUID1*</span></span>    | <span data-ttu-id="93e23-130">1033</span><span class="sxs-lookup"><span data-stu-id="93e23-130">1033</span></span>           | <span data-ttu-id="93e23-131">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="93e23-131">MyModule.*GUID1*</span></span>    | <span data-ttu-id="93e23-132">1033</span><span class="sxs-lookup"><span data-stu-id="93e23-132">1033</span></span>             | <span data-ttu-id="93e23-133">1.2</span><span class="sxs-lookup"><span data-stu-id="93e23-133">1.2</span></span>             |



 

<span data-ttu-id="93e23-134">[Table ModuleExclusion](moduleexclusion-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="93e23-134">[ModuleExclusion Table](moduleexclusion-table.md) (partial)</span></span>



| <span data-ttu-id="93e23-135">ModuleID</span><span class="sxs-lookup"><span data-stu-id="93e23-135">ModuleID</span></span>            | <span data-ttu-id="93e23-136">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="93e23-136">ModuleLanguage</span></span> | <span data-ttu-id="93e23-137">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="93e23-137">ExcludedID</span></span>          | <span data-ttu-id="93e23-138">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="93e23-138">ExcludedLanguage</span></span> |
|---------------------|----------------|---------------------|------------------|
| <span data-ttu-id="93e23-139">OtherModule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="93e23-139">OtherModule.*GUID2*</span></span> | <span data-ttu-id="93e23-140">1033</span><span class="sxs-lookup"><span data-stu-id="93e23-140">1033</span></span>           | <span data-ttu-id="93e23-141">OtherModule. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="93e23-141">OtherModule.*GUID3*</span></span> | <span data-ttu-id="93e23-142">0</span><span class="sxs-lookup"><span data-stu-id="93e23-142">0</span></span>                |
| <span data-ttu-id="93e23-143">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="93e23-143">MyModule.*GUID1*</span></span>    | <span data-ttu-id="93e23-144">1033</span><span class="sxs-lookup"><span data-stu-id="93e23-144">1033</span></span>           | <span data-ttu-id="93e23-145">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="93e23-145">MyModule.*GUID1*</span></span>    | <span data-ttu-id="93e23-146">1033</span><span class="sxs-lookup"><span data-stu-id="93e23-146">1033</span></span>             |



 

<span data-ttu-id="93e23-147">Le module de fusion ICE publie la première erreur en raison de la de la première ligne dans la table ModuleDependency, qui ne spécifie pas de dépendance requise pour le module en cours spécifié dans la table ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="93e23-147">The merge module ICE posts the first error because the of the first row in the ModuleDependency table, which does not specify a required dependency for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="93e23-148">Les dépendances d’un module ne peuvent être spécifiées que dans sa propre table ModuleDependency.</span><span class="sxs-lookup"><span data-stu-id="93e23-148">The dependencies of a module can only be specified in its own ModuleDependency table.</span></span> <span data-ttu-id="93e23-149">Si OtherModule. *GUID3* est requis par le module en cours, remplacez les deux premières colonnes de la ligne par les données de la table ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="93e23-149">If OtherModule.*GUID3* is required by the current module, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="93e23-150">Si OtherModule. *GUID3* n’est pas requis par ce module, supprimez cette ligne.</span><span class="sxs-lookup"><span data-stu-id="93e23-150">If OtherModule.*GUID3* is not required by this module, delete this row.</span></span>

<span data-ttu-id="93e23-151">Le module de fusion ICE publie la deuxième erreur, car un module ne peut pas spécifier une dépendance sur lui-même.</span><span class="sxs-lookup"><span data-stu-id="93e23-151">The merge module ICE posts the second error because a module cannot specify a dependency upon itself.</span></span>

<span data-ttu-id="93e23-152">Le module de fusion ICE publie la troisième erreur en raison de la première ligne dans la table ModuleExclusion, qui ne spécifie pas d’exclusion requise pour le module en cours spécifié dans la table ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="93e23-152">The merge module ICE posts the third error because of the first row in the ModuleExclusion table, which does not specify a required exclusion for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="93e23-153">Les exclusions d’un module ne peuvent être spécifiées que dans sa propre table ModuleExclusion.</span><span class="sxs-lookup"><span data-stu-id="93e23-153">The exclusions of a module can only be specified in its own ModuleExclusion table.</span></span> <span data-ttu-id="93e23-154">Si le module en cours exclut OtherModule. *GUID3*, remplacez les deux premières colonnes de la ligne par les données de la table ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="93e23-154">If the current module excludes OtherModule.*GUID3*, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="93e23-155">Si le module actuel n’exclut pas OtherModule. *GUID3*, supprimez cette ligne.</span><span class="sxs-lookup"><span data-stu-id="93e23-155">If the current module does not exclude OtherModule.*GUID3*, delete this row.</span></span>

<span data-ttu-id="93e23-156">Le module de fusion ICE publie la quatrième erreur, car un module ne peut pas spécifier qu’il s’exclut.</span><span class="sxs-lookup"><span data-stu-id="93e23-156">The merge module ICE posts the fourth error because a module cannot specify that it exclude itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93e23-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="93e23-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93e23-158">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="93e23-158">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 




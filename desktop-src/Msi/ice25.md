---
description: ICE25 vérifie qu’un fichier. msi satisfait à toutes ses dépendances et exclusions de module de fusion internes.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866294"
---
# <a name="ice25"></a><span data-ttu-id="feb8b-103">ICE25</span><span class="sxs-lookup"><span data-stu-id="feb8b-103">ICE25</span></span>

<span data-ttu-id="feb8b-104">ICE25 vérifie qu’un fichier. msi satisfait à toutes ses dépendances et exclusions de [module de fusion](merge-modules.md) internes.</span><span class="sxs-lookup"><span data-stu-id="feb8b-104">ICE25 validates that a .msi file satisfies all of its internal [merge module](merge-modules.md) dependencies and exclusions.</span></span> <span data-ttu-id="feb8b-105">ICE valide les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="feb8b-105">ICE validates the following:</span></span>

-   <span data-ttu-id="feb8b-106">Toutes les dépendances de module de fusion indiquées dans la [table ModuleDependency](moduledependency-table.md) du fichier. msi sont satisfaites par au moins un module de fusion répertorié dans la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="feb8b-106">That all merge module dependencies indicated in the .msi file's [ModuleDependency table](moduledependency-table.md) are satisfied by at least one merge module listed in the [ModuleSignature table](modulesignature-table.md).</span></span>
-   <span data-ttu-id="feb8b-107">Aucun module de fusion exclu dans la [table ModuleExclusion](moduleexclusion-table.md) n’est pas compatible avec les modules de fusion répertoriés dans la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="feb8b-107">That none of the excluded merge modules in the [ModuleExclusion table](moduleexclusion-table.md) are incompatible with the merge modules listed in the [ModuleSignature table](modulesignature-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="feb8b-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="feb8b-108">Result</span></span>

<span data-ttu-id="feb8b-109">ICE25 publie un message d’erreur si le fichier. msi a été précédemment fusionné avec un module de fusion incompatible ou s’il n’a pas été fusionné avec un module de fusion nécessaire.</span><span class="sxs-lookup"><span data-stu-id="feb8b-109">ICE25 posts an error message if .msi file has previously been merged with an incompatible merge module or if it has not been merged with a necessary merge module.</span></span>

## <a name="example"></a><span data-ttu-id="feb8b-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="feb8b-110">Example</span></span>

<span data-ttu-id="feb8b-111">ICE25 publie les erreurs suivantes pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="feb8b-111">ICE25 posts the following errors for the example shown.</span></span>

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[<span data-ttu-id="feb8b-112">ModuleSignature, table</span><span class="sxs-lookup"><span data-stu-id="feb8b-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="feb8b-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="feb8b-113">ModuleID</span></span> | <span data-ttu-id="feb8b-114">Langage</span><span class="sxs-lookup"><span data-stu-id="feb8b-114">Language</span></span> | <span data-ttu-id="feb8b-115">Version</span><span class="sxs-lookup"><span data-stu-id="feb8b-115">Version</span></span> |
|----------|----------|---------|
| <span data-ttu-id="feb8b-116">Module</span><span class="sxs-lookup"><span data-stu-id="feb8b-116">ModuleA</span></span>  | <span data-ttu-id="feb8b-117">0</span><span class="sxs-lookup"><span data-stu-id="feb8b-117">0</span></span>        | <span data-ttu-id="feb8b-118">1.0</span><span class="sxs-lookup"><span data-stu-id="feb8b-118">1.0</span></span>     |
| <span data-ttu-id="feb8b-119">ModuleB</span><span class="sxs-lookup"><span data-stu-id="feb8b-119">ModuleB</span></span>  | <span data-ttu-id="feb8b-120">1033</span><span class="sxs-lookup"><span data-stu-id="feb8b-120">1033</span></span>     | <span data-ttu-id="feb8b-121">1.0</span><span class="sxs-lookup"><span data-stu-id="feb8b-121">1.0</span></span>     |



 

[<span data-ttu-id="feb8b-122">Table ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="feb8b-122">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="feb8b-123">ModuleID</span><span class="sxs-lookup"><span data-stu-id="feb8b-123">ModuleID</span></span> | <span data-ttu-id="feb8b-124">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="feb8b-124">ModuleLanguage</span></span> | <span data-ttu-id="feb8b-125">RequiredID</span><span class="sxs-lookup"><span data-stu-id="feb8b-125">RequiredID</span></span> | <span data-ttu-id="feb8b-126">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="feb8b-126">RequiredLanguage</span></span> | <span data-ttu-id="feb8b-127">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="feb8b-127">RequiredVersion</span></span> |
|----------|----------------|------------|------------------|-----------------|
| <span data-ttu-id="feb8b-128">Module</span><span class="sxs-lookup"><span data-stu-id="feb8b-128">ModuleA</span></span>  | <span data-ttu-id="feb8b-129">0</span><span class="sxs-lookup"><span data-stu-id="feb8b-129">0</span></span>              | <span data-ttu-id="feb8b-130">ModuleX</span><span class="sxs-lookup"><span data-stu-id="feb8b-130">ModuleX</span></span>    | <span data-ttu-id="feb8b-131">0</span><span class="sxs-lookup"><span data-stu-id="feb8b-131">0</span></span>                | <span data-ttu-id="feb8b-132">2.0</span><span class="sxs-lookup"><span data-stu-id="feb8b-132">2.0</span></span>             |



 

[<span data-ttu-id="feb8b-133">Table ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="feb8b-133">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="feb8b-134">ModuleID</span><span class="sxs-lookup"><span data-stu-id="feb8b-134">ModuleID</span></span> | <span data-ttu-id="feb8b-135">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="feb8b-135">ModuleLanguage</span></span> | <span data-ttu-id="feb8b-136">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="feb8b-136">ExcludedID</span></span> | <span data-ttu-id="feb8b-137">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="feb8b-137">ExcludedLanguage</span></span> | <span data-ttu-id="feb8b-138">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="feb8b-138">ExcludedMinVersion</span></span> | <span data-ttu-id="feb8b-139">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="feb8b-139">ExcludedMaxVersion</span></span> |
|----------|----------------|------------|------------------|--------------------|--------------------|
| <span data-ttu-id="feb8b-140">Module</span><span class="sxs-lookup"><span data-stu-id="feb8b-140">ModuleA</span></span>  | <span data-ttu-id="feb8b-141">0</span><span class="sxs-lookup"><span data-stu-id="feb8b-141">0</span></span>              | <span data-ttu-id="feb8b-142">ModuleB</span><span class="sxs-lookup"><span data-stu-id="feb8b-142">ModuleB</span></span>    | <span data-ttu-id="feb8b-143">1033</span><span class="sxs-lookup"><span data-stu-id="feb8b-143">1033</span></span>             |                    |                    |



 

## <a name="related-topics"></a><span data-ttu-id="feb8b-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="feb8b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feb8b-145">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="feb8b-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




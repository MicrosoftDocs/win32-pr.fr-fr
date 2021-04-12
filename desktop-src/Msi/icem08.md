---
description: ICEM08 garantit qu’un module n’exclut pas un autre module dont il dépend.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9767c6748f5a21d83bddb3b5fe93a0a8d7ea67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203781"
---
# <a name="icem08"></a><span data-ttu-id="06500-103">ICEM08</span><span class="sxs-lookup"><span data-stu-id="06500-103">ICEM08</span></span>

<span data-ttu-id="06500-104">ICEM08 garantit qu’un module n’exclut pas un autre module dont il dépend.</span><span class="sxs-lookup"><span data-stu-id="06500-104">ICEM08 ensures that a module does not exclude another module that it depends on.</span></span>

## <a name="result"></a><span data-ttu-id="06500-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="06500-105">Result</span></span>

<span data-ttu-id="06500-106">ICEM08 publie une erreur lorsqu’un module exclut un autre module dont il dépend.</span><span class="sxs-lookup"><span data-stu-id="06500-106">ICEM08 posts an error when a module excludes another module that it depends on.</span></span>

## <a name="example"></a><span data-ttu-id="06500-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="06500-107">Example</span></span>

<span data-ttu-id="06500-108">ICEM08 publie le message d’erreur suivant pour un module contenant les entrées de base de données indiquées dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="06500-108">ICEM08 posts the following error message for a module containing the database entries shown in the example.</span></span>

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[<span data-ttu-id="06500-109">Table ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="06500-109">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="06500-110">ModuleID</span><span class="sxs-lookup"><span data-stu-id="06500-110">ModuleID</span></span>             | <span data-ttu-id="06500-111">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="06500-111">ModuleLanguage</span></span> | <span data-ttu-id="06500-112">RequiredID</span><span class="sxs-lookup"><span data-stu-id="06500-112">RequiredID</span></span>           | <span data-ttu-id="06500-113">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="06500-113">RequiredLanguage</span></span> | <span data-ttu-id="06500-114">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="06500-114">RequiredVersion</span></span> |
|----------------------|----------------|----------------------|------------------|-----------------|
| <span data-ttu-id="06500-115">Modulea.<GUID></span><span class="sxs-lookup"><span data-stu-id="06500-115">ModuleA.<GUID></span></span> | <span data-ttu-id="06500-116">1033</span><span class="sxs-lookup"><span data-stu-id="06500-116">1033</span></span>           | <span data-ttu-id="06500-117">ModuleB.<GUID></span><span class="sxs-lookup"><span data-stu-id="06500-117">ModuleB.<GUID></span></span> | <span data-ttu-id="06500-118">1033</span><span class="sxs-lookup"><span data-stu-id="06500-118">1033</span></span>             | <span data-ttu-id="06500-119">1.0</span><span class="sxs-lookup"><span data-stu-id="06500-119">1.0</span></span>             |



 

[<span data-ttu-id="06500-120">Table ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="06500-120">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="06500-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="06500-121">ModuleID</span></span>             | <span data-ttu-id="06500-122">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="06500-122">ModuleLanguage</span></span> | <span data-ttu-id="06500-123">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="06500-123">ExcludedID</span></span>           | <span data-ttu-id="06500-124">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="06500-124">ExcludedLanguage</span></span> | <span data-ttu-id="06500-125">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="06500-125">ExcludedMinVersion</span></span> | <span data-ttu-id="06500-126">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="06500-126">ExcludedMaxVersion</span></span> |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| <span data-ttu-id="06500-127">Modulea.<GUID></span><span class="sxs-lookup"><span data-stu-id="06500-127">ModuleA.<GUID></span></span> | <span data-ttu-id="06500-128">1033</span><span class="sxs-lookup"><span data-stu-id="06500-128">1033</span></span>           | <span data-ttu-id="06500-129">ModuleB.<GUID></span><span class="sxs-lookup"><span data-stu-id="06500-129">ModuleB.<GUID></span></span> | <span data-ttu-id="06500-130">1033</span><span class="sxs-lookup"><span data-stu-id="06500-130">1033</span></span>             |                    | <span data-ttu-id="06500-131">1.0</span><span class="sxs-lookup"><span data-stu-id="06500-131">1.0</span></span>                |



 

<span data-ttu-id="06500-132">Pour corriger l’erreur, supprimez la dépendance ou l’exclusion.</span><span class="sxs-lookup"><span data-stu-id="06500-132">To fix the error, remove either the dependency or the exclusion.</span></span> <span data-ttu-id="06500-133">Si ModuleB est une dépendance (RequiredID) de modulea, vous ne pouvez pas l’exclure (comme indiqué dans la colonne ExludedID de la table ModuleExclusion).</span><span class="sxs-lookup"><span data-stu-id="06500-133">If ModuleB is a dependency (RequiredID) of ModuleA, you cannot exclude it (as shown in the ExludedID column of the ModuleExclusion table).</span></span> <span data-ttu-id="06500-134">Si vous devez exclure ModuleB, vous devez supprimer la dépendance entre les modules.</span><span class="sxs-lookup"><span data-stu-id="06500-134">If you must exclude ModuleB, then you must remove ModuleA's dependency on it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06500-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06500-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06500-136">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="06500-136">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 




---
description: Le ICE11 est utilisé avec les installations simultanées. Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public. Pour plus d’informations sur les installations simultanées, consultez installations simultanées.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952289"
---
# <a name="ice11"></a><span data-ttu-id="76703-105">ICE11</span><span class="sxs-lookup"><span data-stu-id="76703-105">ICE11</span></span>

<span data-ttu-id="76703-106">Le ICE11 est utilisé avec les installations simultanées.</span><span class="sxs-lookup"><span data-stu-id="76703-106">The ICE11 is used with concurrent installations.</span></span> <span data-ttu-id="76703-107">Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public.</span><span class="sxs-lookup"><span data-stu-id="76703-107">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="76703-108">Pour plus d’informations sur les installations simultanées, consultez [installations simultanées](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="76703-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

## <a name="result"></a><span data-ttu-id="76703-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="76703-109">Result</span></span>

<span data-ttu-id="76703-110">ICE11 valide la colonne source de la [table CustomAction](customaction-table.md) des actions personnalisées d’installation simultanée.</span><span class="sxs-lookup"><span data-stu-id="76703-110">ICE11 validates the Source column of the [CustomAction table](customaction-table.md) of concurrent installation custom actions.</span></span> <span data-ttu-id="76703-111">La colonne source doit contenir un [GUID](guid.md) valide (code de produit msi).</span><span class="sxs-lookup"><span data-stu-id="76703-111">The Source column must contain a valid [GUID](guid.md) (MSI product code).</span></span>

<span data-ttu-id="76703-112">ICE11 publie une erreur si la colonne source de la table CustomAction est créée de manière incorrecte pour les actions personnalisées d’installation simultanée.</span><span class="sxs-lookup"><span data-stu-id="76703-112">ICE11 posts an error if the Source column of the CustomAction table is authored incorrectly for concurrent installation custom actions.</span></span>

## <a name="example"></a><span data-ttu-id="76703-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="76703-113">Example</span></span>

<span data-ttu-id="76703-114">ICE publie les messages d’erreur suivants pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="76703-114">ICE posts the following error messages for the example shown.</span></span>

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

<span data-ttu-id="76703-115">[Table de propriétés](property-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="76703-115">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="76703-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="76703-116">Property</span></span>        | <span data-ttu-id="76703-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="76703-117">Value</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="76703-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="76703-118">**ProductCode**</span></span> | <span data-ttu-id="76703-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="76703-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |



 

<span data-ttu-id="76703-120">[Table CustomAction](customaction-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="76703-120">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="76703-121">CustomAction</span><span class="sxs-lookup"><span data-stu-id="76703-121">CustomAction</span></span> | <span data-ttu-id="76703-122">Type</span><span class="sxs-lookup"><span data-stu-id="76703-122">Type</span></span> | <span data-ttu-id="76703-123">Source</span><span class="sxs-lookup"><span data-stu-id="76703-123">Source</span></span>                                 |
|--------------|------|----------------------------------------|
| <span data-ttu-id="76703-124">AC1</span><span class="sxs-lookup"><span data-stu-id="76703-124">CA1</span></span>          | <span data-ttu-id="76703-125">39</span><span class="sxs-lookup"><span data-stu-id="76703-125">39</span></span>   | <span data-ttu-id="76703-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="76703-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |
| <span data-ttu-id="76703-127">CA2</span><span class="sxs-lookup"><span data-stu-id="76703-127">CA2</span></span>          | <span data-ttu-id="76703-128">39</span><span class="sxs-lookup"><span data-stu-id="76703-128">39</span></span>   | <span data-ttu-id="76703-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="76703-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span></span> |
| <span data-ttu-id="76703-130">CA3</span><span class="sxs-lookup"><span data-stu-id="76703-130">CA3</span></span>          | <span data-ttu-id="76703-131">39</span><span class="sxs-lookup"><span data-stu-id="76703-131">39</span></span>   | <span data-ttu-id="76703-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="76703-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span></span> |
| <span data-ttu-id="76703-133">CA4</span><span class="sxs-lookup"><span data-stu-id="76703-133">CA4</span></span>          | <span data-ttu-id="76703-134">39</span><span class="sxs-lookup"><span data-stu-id="76703-134">39</span></span>   | <span data-ttu-id="76703-135">ProductCode</span><span class="sxs-lookup"><span data-stu-id="76703-135">ProductCode</span></span>                            |



 

<span data-ttu-id="76703-136">Pour résoudre les erreurs, pour CA1, vous ne pouvez pas effectuer une installation simultanée du « package de base ».</span><span class="sxs-lookup"><span data-stu-id="76703-136">To fix the errors, for CA1, you cannot do a concurrent installation of the "base package".</span></span> <span data-ttu-id="76703-137">Cela entraînerait une installation récursive.</span><span class="sxs-lookup"><span data-stu-id="76703-137">This would result in a recursive installation.</span></span> <span data-ttu-id="76703-138">Cette entrée doit être supprimée ou la colonne source doit être remplacée par un GUID pour un MSI publié qui diffère du GUID du package de base.</span><span class="sxs-lookup"><span data-stu-id="76703-138">This entry should be removed or the Source column should be changed to a GUID for an advertised MSI that differs from the base package's GUID.</span></span> <span data-ttu-id="76703-139">Pour CA2, mettez tous les caractères du GUID en majuscules.</span><span class="sxs-lookup"><span data-stu-id="76703-139">For CA2, make all characters of the GUID uppercase.</span></span> <span data-ttu-id="76703-140">Enfin, modifiez la colonne source CA4's pour référencer un GUID valide d’un MSI publié.</span><span class="sxs-lookup"><span data-stu-id="76703-140">Lastly, change CA4's Source column to reference a valid GUID of an advertised MSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76703-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76703-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76703-142">Installations simultanées</span><span class="sxs-lookup"><span data-stu-id="76703-142">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="76703-143">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="76703-143">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




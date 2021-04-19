---
description: ICE41 vérifie que les entrées dans les tables de classes et d’extensions font référence aux entrées de la table de composants qui implémentent l’objet de classe ou l’extension du composant.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536717"
---
# <a name="ice41"></a><span data-ttu-id="e1f38-103">ICE41</span><span class="sxs-lookup"><span data-stu-id="e1f38-103">ICE41</span></span>

<span data-ttu-id="e1f38-104">ICE41 vérifie que les entrées dans les tables de [classes](class-table.md) et d' [Extensions](extension-table.md) font référence aux entrées de la [table de composants](component-table.md) qui implémentent l’objet de classe ou l’extension du composant.</span><span class="sxs-lookup"><span data-stu-id="e1f38-104">ICE41 validates that the entries in the [Class](class-table.md) and [Extension](extension-table.md) tables refer to entries in the [Component table](component-table.md) that implement the class object or extension of the component.</span></span>

## <a name="result"></a><span data-ttu-id="e1f38-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="e1f38-105">Result</span></span>

<span data-ttu-id="e1f38-106">ICE41 publie une erreur s’il existe une fonctionnalité qui ne contient pas le composant qui implémente l’extension ou l’objet de classe.</span><span class="sxs-lookup"><span data-stu-id="e1f38-106">ICE41 posts an error if there is a feature that does not contain the component implementing the class object or extension.</span></span>

## <a name="example"></a><span data-ttu-id="e1f38-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="e1f38-107">Example</span></span>

<span data-ttu-id="e1f38-108">ICE41 signale les erreurs suivantes pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="e1f38-108">ICE41 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="e1f38-109">Erreur ICE41</span><span class="sxs-lookup"><span data-stu-id="e1f38-109">ICE41 error</span></span>                                                                                                                                                                                    | <span data-ttu-id="e1f38-110">Description</span><span class="sxs-lookup"><span data-stu-id="e1f38-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f38-111">{00000000-0000-0000-0000-0000000000000}La classe référence la fonctionnalité feature2 et le composant Composant1, mais ce composant n’est pas associé à cette fonctionnalité dans la table FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="e1f38-111">Class {00000000-0000-0000-0000-0000000000000} references feature Feature2 and component Component1, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span> | <span data-ttu-id="e1f38-112">Il existe une fonctionnalité qui ne contient pas le composant qui implémente l’objet de classe.</span><span class="sxs-lookup"><span data-stu-id="e1f38-112">There is a feature that does not contain the component implementing the class object.</span></span> <span data-ttu-id="e1f38-113">Cela signifie que le programme d’installation n’installe pas le composant avec la fonctionnalité et que la publicité peut ne pas fonctionner comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e1f38-113">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="e1f38-114">Pour corriger cette erreur, modifiez l’entrée dans la colonne Feature \_ de l’entrée de la [table de classes](class-table.md) afin de faire référence à une fonctionnalité qui installe le composant figurant dans la \_ colonne composant ou modifiez la fonctionnalité et le composant associés dans la [table FeatureComponents](featurecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1f38-114">To fix this error, change the entry in the Feature\_ column of the [Class table](class-table.md) entry to reference a feature that installs component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/>          |
| <span data-ttu-id="e1f38-115">Extension. Yip fait référence à Feature1 et au composant COMPONENT2, mais ce composant n’est pas associé à cette fonctionnalité dans la table FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="e1f38-115">Extension .yip references feature Feature1 and component Component2, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span>                                | <span data-ttu-id="e1f38-116">Il existe une fonctionnalité qui ne contient pas le composant qui implémente l’extension.</span><span class="sxs-lookup"><span data-stu-id="e1f38-116">There is a feature that does not contain the component implementing the extension.</span></span> <span data-ttu-id="e1f38-117">Cela signifie que le programme d’installation n’installe pas le composant avec la fonctionnalité et que la publicité peut ne pas fonctionner comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e1f38-117">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="e1f38-118">Pour corriger cette erreur, modifiez l’entrée dans la colonne Feature \_ de l’entrée de la [table d’extension](extension-table.md) pour faire référence à une fonctionnalité qui installe le composant figurant dans la \_ colonne composant ou modifiez la fonctionnalité et le composant associés dans la [table FeatureComponents](featurecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1f38-118">To fix this error, change the entry in the Feature\_ column of the [Extension table](extension-table.md) entry to reference a feature that installs the component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/> |



 

<span data-ttu-id="e1f38-119">[Table FeatureComponents](featurecomponents-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="e1f38-119">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="e1f38-120">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="e1f38-120">Feature\_</span></span> |
|-----------|
| <span data-ttu-id="e1f38-121">Feature1</span><span class="sxs-lookup"><span data-stu-id="e1f38-121">Feature1</span></span>  |
| <span data-ttu-id="e1f38-122">Feature2</span><span class="sxs-lookup"><span data-stu-id="e1f38-122">Feature2</span></span>  |



 

<span data-ttu-id="e1f38-123">[Table de classe](class-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="e1f38-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="e1f38-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="e1f38-124">CLSID</span></span>                                  | <span data-ttu-id="e1f38-125">-\_</span><span class="sxs-lookup"><span data-stu-id="e1f38-125">Component\_</span></span> | <span data-ttu-id="e1f38-126">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="e1f38-126">Feature\_</span></span> |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | <span data-ttu-id="e1f38-127">Composant1</span><span class="sxs-lookup"><span data-stu-id="e1f38-127">Component1</span></span>  | <span data-ttu-id="e1f38-128">Feature2</span><span class="sxs-lookup"><span data-stu-id="e1f38-128">Feature2</span></span>  |



 

<span data-ttu-id="e1f38-129">[Table de classe](class-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="e1f38-129">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="e1f38-130">Extension</span><span class="sxs-lookup"><span data-stu-id="e1f38-130">Extension</span></span> | <span data-ttu-id="e1f38-131">-\_</span><span class="sxs-lookup"><span data-stu-id="e1f38-131">Component\_</span></span> | <span data-ttu-id="e1f38-132">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="e1f38-132">Feature\_</span></span> |
|-----------|-------------|-----------|
| <span data-ttu-id="e1f38-133">.yip</span><span class="sxs-lookup"><span data-stu-id="e1f38-133">.yip</span></span>      | <span data-ttu-id="e1f38-134">Component2</span><span class="sxs-lookup"><span data-stu-id="e1f38-134">Component2</span></span>  | <span data-ttu-id="e1f38-135">Feature1</span><span class="sxs-lookup"><span data-stu-id="e1f38-135">Feature1</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="e1f38-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1f38-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1f38-137">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="e1f38-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 





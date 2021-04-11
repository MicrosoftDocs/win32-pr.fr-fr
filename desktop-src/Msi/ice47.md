---
description: ICE47 vérifie la fonctionnalité et les tables FeatureComponents pour les fonctionnalités avec 1600 ou plus de composants.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202750"
---
# <a name="ice47"></a><span data-ttu-id="91b22-103">ICE47</span><span class="sxs-lookup"><span data-stu-id="91b22-103">ICE47</span></span>

<span data-ttu-id="91b22-104">ICE47 vérifie la [fonctionnalité](feature-table.md) et les tables [FeatureComponents](featurecomponents-table.md) pour les fonctionnalités avec 1600 ou plus de composants.</span><span class="sxs-lookup"><span data-stu-id="91b22-104">ICE47 checks the [Feature](feature-table.md) and [FeatureComponents](featurecomponents-table.md) tables for features with 1600 or more components.</span></span>

## <a name="result"></a><span data-ttu-id="91b22-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="91b22-105">Result</span></span>

<span data-ttu-id="91b22-106">ICE47 publie un message d’erreur si une fonctionnalité dépasse la limite maximale de 1600 composants par fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="91b22-106">ICE47 posts an error message if a feature exceeds the maximum limit of 1600 components per feature.</span></span>

## <a name="example"></a><span data-ttu-id="91b22-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="91b22-107">Example</span></span>

<span data-ttu-id="91b22-108">ICE47 signale l’avertissement suivant :</span><span class="sxs-lookup"><span data-stu-id="91b22-108">ICE47 would report the following warning:</span></span>

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

<span data-ttu-id="91b22-109">[Table des fonctionnalités](feature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="91b22-109">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="91b22-110">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="91b22-110">Feature</span></span>  |
|----------|
| <span data-ttu-id="91b22-111">Feature1</span><span class="sxs-lookup"><span data-stu-id="91b22-111">Feature1</span></span> |



 

<span data-ttu-id="91b22-112">[Table FeatureComponents](featurecomponents-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="91b22-112">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="91b22-113">Action</span><span class="sxs-lookup"><span data-stu-id="91b22-113">Action</span></span>   | <span data-ttu-id="91b22-114">Condition</span><span class="sxs-lookup"><span data-stu-id="91b22-114">Condition</span></span>     |
|----------|---------------|
| <span data-ttu-id="91b22-115">Feature1</span><span class="sxs-lookup"><span data-stu-id="91b22-115">Feature1</span></span> | <span data-ttu-id="91b22-116">Composant1</span><span class="sxs-lookup"><span data-stu-id="91b22-116">Component1</span></span>    |
| <span data-ttu-id="91b22-117">Feature1</span><span class="sxs-lookup"><span data-stu-id="91b22-117">Feature1</span></span> | <span data-ttu-id="91b22-118">Component1600</span><span class="sxs-lookup"><span data-stu-id="91b22-118">Component1600</span></span> |



 

<span data-ttu-id="91b22-119">Pour résoudre cet avertissement, essayez de fractionner la fonctionnalité en plusieurs fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="91b22-119">To fix this warning, try splitting the feature into several features</span></span>

## <a name="related-topics"></a><span data-ttu-id="91b22-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91b22-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91b22-121">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="91b22-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




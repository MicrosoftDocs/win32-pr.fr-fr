---
description: ICE22 utilise la table FeatureComponents pour valider le mappage des fonctionnalités et des composants référencés dans la table PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526141"
---
# <a name="ice22"></a><span data-ttu-id="71da2-103">ICE22</span><span class="sxs-lookup"><span data-stu-id="71da2-103">ICE22</span></span>

<span data-ttu-id="71da2-104">ICE22 utilise la [table FeatureComponents](featurecomponents-table.md) pour valider le mappage des fonctionnalités et des composants référencés dans la [table PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="71da2-104">ICE22 uses the [FeatureComponents table](featurecomponents-table.md) to validate the mapping of features and components referenced in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="71da2-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="71da2-105">Result</span></span>

<span data-ttu-id="71da2-106">ICE22 publie un message d’erreur si les fonctionnalités et les composants sont mappés de manière incorrecte dans la [table PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="71da2-106">ICE22 posts an error message if the features and components are mapped incorrectly in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="71da2-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="71da2-107">Example</span></span>

<span data-ttu-id="71da2-108">Dans l’exemple suivant, ICE22 publie une erreur qui {00000003-0004-0000-0000-624474732465} n’a pas le mappage correct pour les \_ colonnes de composants et de fonctionnalités \_ .</span><span class="sxs-lookup"><span data-stu-id="71da2-108">For the following example ICE22 posts an error that {00000003-0004-0000-0000-624474732465} does not have the correct mapping for the Feature\_ and Component\_ columns.</span></span>

<span data-ttu-id="71da2-109">[Table PublishComponent](publishcomponent-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="71da2-109">[PublishComponent Table](publishcomponent-table.md) (partial)</span></span>



| <span data-ttu-id="71da2-110">ComponentId</span><span class="sxs-lookup"><span data-stu-id="71da2-110">ComponentId</span></span>                            | <span data-ttu-id="71da2-111">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="71da2-111">Feature\_</span></span> | <span data-ttu-id="71da2-112">-\_</span><span class="sxs-lookup"><span data-stu-id="71da2-112">Component\_</span></span> |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="71da2-113">Feat1</span><span class="sxs-lookup"><span data-stu-id="71da2-113">Feat1</span></span>     | <span data-ttu-id="71da2-114">COMP1</span><span class="sxs-lookup"><span data-stu-id="71da2-114">Comp1</span></span>       |
| {00000003-0004-0000-0000-624474732465} | <span data-ttu-id="71da2-115">Feat1</span><span class="sxs-lookup"><span data-stu-id="71da2-115">Feat1</span></span>     | <span data-ttu-id="71da2-116">COMP2</span><span class="sxs-lookup"><span data-stu-id="71da2-116">Comp2</span></span>       |



 

<span data-ttu-id="71da2-117">[Table FeatureComponents](featurecomponents-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="71da2-117">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="71da2-118">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="71da2-118">Feature\_</span></span> | <span data-ttu-id="71da2-119">-\_</span><span class="sxs-lookup"><span data-stu-id="71da2-119">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="71da2-120">Feat1</span><span class="sxs-lookup"><span data-stu-id="71da2-120">Feat1</span></span>     | <span data-ttu-id="71da2-121">COMP1</span><span class="sxs-lookup"><span data-stu-id="71da2-121">Comp1</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="71da2-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71da2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71da2-123">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="71da2-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




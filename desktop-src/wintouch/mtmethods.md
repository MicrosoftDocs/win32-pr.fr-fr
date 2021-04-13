---
title: Méthodes (IManipulationProcessor)
description: Cette section contient les méthodes de l’interface IManipulationProcessor.
ms.assetid: 33736f79-cb61-449c-80b9-1358db2621e9
keywords:
- Tactile Windows, interface IManipulationProcessor
- Tactile Windows, méthodes d’interface
- manipulations, interface IManipulationProcessor
- Interface IManipulationProcessor, méthodes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 995a848e18b8308d46ceda717bf7eec291953505
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383688"
---
# <a name="methods-imanipulationprocessor"></a><span data-ttu-id="56b39-107">Méthodes (IManipulationProcessor)</span><span class="sxs-lookup"><span data-stu-id="56b39-107">Methods (IManipulationProcessor)</span></span>

<span data-ttu-id="56b39-108">Cette section contient les méthodes de l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="56b39-108">This section contains the methods for the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>

<span data-ttu-id="56b39-109">Les méthodes suivantes sont exposées par l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="56b39-109">The following methods are exposed by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>



| <span data-ttu-id="56b39-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="56b39-110">Method</span></span>                                                                      | <span data-ttu-id="56b39-111">Description</span><span class="sxs-lookup"><span data-stu-id="56b39-111">Description</span></span>                                                                              |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56b39-112">**CompleteManipulation**</span><span class="sxs-lookup"><span data-stu-id="56b39-112">**CompleteManipulation**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-completemanipulation) | <span data-ttu-id="56b39-113">Cette méthode est appelée lorsque le développeur choisit de terminer la manipulation.</span><span class="sxs-lookup"><span data-stu-id="56b39-113">This method is called when the developer chooses to end the manipulation.</span></span>                |
| [<span data-ttu-id="56b39-114">**GetAngularVelocity**</span><span class="sxs-lookup"><span data-stu-id="56b39-114">**GetAngularVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getangularvelocity)     | <span data-ttu-id="56b39-115">Calcule la rapidité de rotation à laquelle l’objet cible se déplace.</span><span class="sxs-lookup"><span data-stu-id="56b39-115">Calculates the rotational velocity that the target object is moving at.</span></span>                  |
| [<span data-ttu-id="56b39-116">**GetExpansionVelocity**</span><span class="sxs-lookup"><span data-stu-id="56b39-116">**GetExpansionVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getexpansionvelocity) | <span data-ttu-id="56b39-117">Calcule le taux auquel l’objet cible s’étend.</span><span class="sxs-lookup"><span data-stu-id="56b39-117">Calculates the rate that the target object is expanding at.</span></span>                              |
| [<span data-ttu-id="56b39-118">**GetVelocityX**</span><span class="sxs-lookup"><span data-stu-id="56b39-118">**GetVelocityX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx)                 | <span data-ttu-id="56b39-119">Calcule et retourne la vélocité horizontale de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="56b39-119">Calculates and returns the horizontal velocity for the target object.</span></span>                    |
| [<span data-ttu-id="56b39-120">**GetVelocityY**</span><span class="sxs-lookup"><span data-stu-id="56b39-120">**GetVelocityY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy)                 | <span data-ttu-id="56b39-121">Calcule et retourne la vélocité verticale.</span><span class="sxs-lookup"><span data-stu-id="56b39-121">Calculates and returns the vertical velocity.</span></span>                                            |
| [<span data-ttu-id="56b39-122">**ProcessDown**</span><span class="sxs-lookup"><span data-stu-id="56b39-122">**ProcessDown**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown)                   | <span data-ttu-id="56b39-123">Alimente les données vers le processeur de manipulation associé à une cible.</span><span class="sxs-lookup"><span data-stu-id="56b39-123">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="56b39-124">**ProcessMove**</span><span class="sxs-lookup"><span data-stu-id="56b39-124">**ProcessMove**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove)                   | <span data-ttu-id="56b39-125">Alimente les données vers le processeur de manipulation associé à une cible.</span><span class="sxs-lookup"><span data-stu-id="56b39-125">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="56b39-126">**ProcessUp**</span><span class="sxs-lookup"><span data-stu-id="56b39-126">**ProcessUp**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup)                       | <span data-ttu-id="56b39-127">Alimente les données vers le processeur de manipulation associé à une cible.</span><span class="sxs-lookup"><span data-stu-id="56b39-127">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="56b39-128">**ProcessDownWithTime**</span><span class="sxs-lookup"><span data-stu-id="56b39-128">**ProcessDownWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)   | <span data-ttu-id="56b39-129">Flux de données incluant un horodateur au processeur de manipulation associé à une cible.</span><span class="sxs-lookup"><span data-stu-id="56b39-129">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="56b39-130">**ProcessMoveWithTime**</span><span class="sxs-lookup"><span data-stu-id="56b39-130">**ProcessMoveWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime)   | <span data-ttu-id="56b39-131">Flux de données incluant un horodateur au processeur de manipulation associé à une cible.</span><span class="sxs-lookup"><span data-stu-id="56b39-131">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="56b39-132">**ProcessUpWithTime**</span><span class="sxs-lookup"><span data-stu-id="56b39-132">**ProcessUpWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime)       | <span data-ttu-id="56b39-133">Flux de données incluant un horodateur au processeur de manipulation associé à une cible.</span><span class="sxs-lookup"><span data-stu-id="56b39-133">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="56b39-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56b39-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56b39-135">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="56b39-135">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 





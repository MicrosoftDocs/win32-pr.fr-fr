---
description: COM+ gère les threads pour vous. Chaque composant COM a une propriété ThreadingModel que vous pouvez spécifier lors du développement du composant. Cette propriété détermine comment les objets de composants sont assignés aux threads pour l’exécution de la méthode.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Attribut de modèle de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392999"
---
# <a name="threading-model-attribute"></a><span data-ttu-id="eadc4-105">Attribut de modèle de thread</span><span class="sxs-lookup"><span data-stu-id="eadc4-105">Threading Model Attribute</span></span>

<span data-ttu-id="eadc4-106">COM+ gère les threads pour vous.</span><span class="sxs-lookup"><span data-stu-id="eadc4-106">COM+ manages threads for you.</span></span> <span data-ttu-id="eadc4-107">Chaque composant COM a une propriété **ThreadingModel** que vous pouvez spécifier lors du développement du composant.</span><span class="sxs-lookup"><span data-stu-id="eadc4-107">Every COM component has a **ThreadingModel** property that you can specify when you develop the component.</span></span> <span data-ttu-id="eadc4-108">Cette propriété détermine comment les objets du composant sont assignés aux threads pour l’exécution de la méthode.</span><span class="sxs-lookup"><span data-stu-id="eadc4-108">This property determines how the component's objects are assigned to threads for method execution.</span></span>

<span data-ttu-id="eadc4-109">Vous pouvez utiliser l’outil d’administration Services de composants pour afficher la propriété de modèle de thread en cliquant avec le bouton droit sur un composant dans le dossier **composants** , en cliquant sur **Propriétés**, puis sur l’onglet **accès concurrentiel** . Dans le **modèle de thread**, les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="eadc4-109">You can use the Component Services administrative tool to view the threading-model property by right-clicking a component in the **Components** folder, clicking **Properties**, and then clicking the **Concurrency** tab. Under **Threading Model**, the possible values are as follows:</span></span>

-   <span data-ttu-id="eadc4-110">**Cloisonnement du thread principal**</span><span class="sxs-lookup"><span data-stu-id="eadc4-110">**Main Thread Apartment**</span></span>
-   <span data-ttu-id="eadc4-111">**Cloisonnement de thread unique**</span><span class="sxs-lookup"><span data-stu-id="eadc4-111">**Single Thread Apartment**</span></span>
-   <span data-ttu-id="eadc4-112">**Cloisonnement de threads libre**</span><span class="sxs-lookup"><span data-stu-id="eadc4-112">**Free Thread Apartment**</span></span>
-   <span data-ttu-id="eadc4-113">**Cloisonnement neutre**</span><span class="sxs-lookup"><span data-stu-id="eadc4-113">**Neutral Apartment**</span></span>
-   <span data-ttu-id="eadc4-114">**Tout cloisonnement**</span><span class="sxs-lookup"><span data-stu-id="eadc4-114">**Any Apartment**</span></span>

<span data-ttu-id="eadc4-115">Le modèle de thread préféré pour COM+ est le [cloisonnement neutre](neutral-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="eadc4-115">The preferred threading model for COM+ is the [neutral apartment](neutral-apartments.md).</span></span> <span data-ttu-id="eadc4-116">Toutefois, si vous ne spécifiez pas de modèle de thread pour votre composant, COM+ utilise le thread cloisonné principal, qui est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="eadc4-116">However, if you do not specify a threading model for your component, COM+ uses the main thread apartment, which is the default.</span></span>

> [!Note]  
> <span data-ttu-id="eadc4-117">Pour plus d’informations, consultez [choix du modèle de thread](/windows/desktop/com/choosing-the-threading-model).</span><span class="sxs-lookup"><span data-stu-id="eadc4-117">For more detailed information, see [Choosing the Threading Model](/windows/desktop/com/choosing-the-threading-model).</span></span>

 

<span data-ttu-id="eadc4-118">Le tableau suivant présente le modèle de programmation pour les cloisonnements dans COM+.</span><span class="sxs-lookup"><span data-stu-id="eadc4-118">The following table shows the programming model for apartments in COM+.</span></span>



| <span data-ttu-id="eadc4-119">Modèle</span><span class="sxs-lookup"><span data-stu-id="eadc4-119">Model</span></span>                     | <span data-ttu-id="eadc4-120">STA</span><span class="sxs-lookup"><span data-stu-id="eadc4-120">Apartment</span></span>                                                 | <span data-ttu-id="eadc4-121">Gratuit</span><span class="sxs-lookup"><span data-stu-id="eadc4-121">Free</span></span>                               | <span data-ttu-id="eadc4-122">Les deux</span><span class="sxs-lookup"><span data-stu-id="eadc4-122">Both</span></span>                               | <span data-ttu-id="eadc4-123">Neutre</span><span class="sxs-lookup"><span data-stu-id="eadc4-123">Neutral</span></span>                      | <span data-ttu-id="eadc4-124">Non spécifié</span><span class="sxs-lookup"><span data-stu-id="eadc4-124">Not Specified</span></span>                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| <span data-ttu-id="eadc4-125">À thread unique, non principal</span><span class="sxs-lookup"><span data-stu-id="eadc4-125">Single-threaded, not main</span></span> | <span data-ttu-id="eadc4-126">Créé dans le cloisonnement actuel</span><span class="sxs-lookup"><span data-stu-id="eadc4-126">Created in current apartment</span></span>                              | <span data-ttu-id="eadc4-127">Créé dans un cloisonnement multithread</span><span class="sxs-lookup"><span data-stu-id="eadc4-127">Created in multithreaded apartment</span></span> | <span data-ttu-id="eadc4-128">Créé dans le cloisonnement actuel</span><span class="sxs-lookup"><span data-stu-id="eadc4-128">Created in current apartment</span></span>       | <span data-ttu-id="eadc4-129">Créé dans le cloisonnement neutre</span><span class="sxs-lookup"><span data-stu-id="eadc4-129">Created in neutral apartment</span></span> | <span data-ttu-id="eadc4-130">Créé dans le thread cloisonné principal</span><span class="sxs-lookup"><span data-stu-id="eadc4-130">Created in main threaded apartment</span></span> |
| <span data-ttu-id="eadc4-131">À thread unique, main</span><span class="sxs-lookup"><span data-stu-id="eadc4-131">Single-threaded, main</span></span>     | <span data-ttu-id="eadc4-132">Créé dans le cloisonnement actuel</span><span class="sxs-lookup"><span data-stu-id="eadc4-132">Created in current apartment</span></span>                              | <span data-ttu-id="eadc4-133">Créé dans un cloisonnement multithread</span><span class="sxs-lookup"><span data-stu-id="eadc4-133">Created in multithreaded apartment</span></span> | <span data-ttu-id="eadc4-134">Créé dans le cloisonnement actuel</span><span class="sxs-lookup"><span data-stu-id="eadc4-134">Created in current apartment</span></span>       | <span data-ttu-id="eadc4-135">Créé dans le cloisonnement neutre</span><span class="sxs-lookup"><span data-stu-id="eadc4-135">Created in neutral apartment</span></span> | <span data-ttu-id="eadc4-136">Créé dans le cloisonnement actuel</span><span class="sxs-lookup"><span data-stu-id="eadc4-136">Created in current apartment</span></span>       |
| <span data-ttu-id="eadc4-137">Multithread</span><span class="sxs-lookup"><span data-stu-id="eadc4-137">Multithreaded</span></span>             | <span data-ttu-id="eadc4-138">Créé dans l’hôte du cloisonnement à thread unique</span><span class="sxs-lookup"><span data-stu-id="eadc4-138">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="eadc4-139">Créé dans un cloisonnement multithread</span><span class="sxs-lookup"><span data-stu-id="eadc4-139">Created in multithreaded apartment</span></span> | <span data-ttu-id="eadc4-140">Créé dans un cloisonnement multithread</span><span class="sxs-lookup"><span data-stu-id="eadc4-140">Created in multithreaded apartment</span></span> | <span data-ttu-id="eadc4-141">Créé dans le cloisonnement neutre</span><span class="sxs-lookup"><span data-stu-id="eadc4-141">Created in neutral apartment</span></span> | <span data-ttu-id="eadc4-142">Créé dans le thread cloisonné principal</span><span class="sxs-lookup"><span data-stu-id="eadc4-142">Created in main threaded apartment</span></span> |
| <span data-ttu-id="eadc4-143">Neutral (sur thread STA)</span><span class="sxs-lookup"><span data-stu-id="eadc4-143">Neutral (on STA thread)</span></span>   | <span data-ttu-id="eadc4-144">Créé dans l’hôte du cloisonnement à thread unique pour ce thread</span><span class="sxs-lookup"><span data-stu-id="eadc4-144">Created in host single-threaded apartment for this thread</span></span> | <span data-ttu-id="eadc4-145">Créé dans un cloisonnement multithread</span><span class="sxs-lookup"><span data-stu-id="eadc4-145">Created in multithreaded apartment</span></span> | <span data-ttu-id="eadc4-146">Créé dans le cloisonnement neutre</span><span class="sxs-lookup"><span data-stu-id="eadc4-146">Created in neutral apartment</span></span>       | <span data-ttu-id="eadc4-147">Créé dans le cloisonnement neutre</span><span class="sxs-lookup"><span data-stu-id="eadc4-147">Created in neutral apartment</span></span> | <span data-ttu-id="eadc4-148">Créé dans le thread cloisonné principal</span><span class="sxs-lookup"><span data-stu-id="eadc4-148">Created in main threaded apartment</span></span> |
| <span data-ttu-id="eadc4-149">Neutral (sur thread MTA)</span><span class="sxs-lookup"><span data-stu-id="eadc4-149">Neutral (on MTA thread)</span></span>   | <span data-ttu-id="eadc4-150">Créé dans l’hôte du cloisonnement à thread unique</span><span class="sxs-lookup"><span data-stu-id="eadc4-150">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="eadc4-151">Créé dans un cloisonnement multithread</span><span class="sxs-lookup"><span data-stu-id="eadc4-151">Created in multithreaded apartment</span></span> | <span data-ttu-id="eadc4-152">Créé dans le cloisonnement neutre</span><span class="sxs-lookup"><span data-stu-id="eadc4-152">Created in neutral apartment</span></span>       | <span data-ttu-id="eadc4-153">Créé dans le cloisonnement neutre</span><span class="sxs-lookup"><span data-stu-id="eadc4-153">Created in neutral apartment</span></span> | <span data-ttu-id="eadc4-154">Créé dans le thread cloisonné principal</span><span class="sxs-lookup"><span data-stu-id="eadc4-154">Created in main threaded apartment</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="eadc4-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eadc4-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eadc4-156">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="eadc4-156">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 

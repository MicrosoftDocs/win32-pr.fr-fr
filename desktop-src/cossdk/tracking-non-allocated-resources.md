---
description: Suivi des ressources non allouées
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Suivi des ressources non allouées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513946"
---
# <a name="tracking-non-allocated-resources"></a><span data-ttu-id="b04b2-103">Suivi des ressources non allouées</span><span class="sxs-lookup"><span data-stu-id="b04b2-103">Tracking Non-Allocated Resources</span></span>

<span data-ttu-id="b04b2-104">Le gestionnaire de distribution peut effectuer le suivi d’une ressource qui n’est pas inventoriée, en fonction de la connaissance de la durée de vie de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b04b2-104">The dispenser manager can track a resource that is not inventoried, based on knowledge of the object's lifetime.</span></span> <span data-ttu-id="b04b2-105">Lorsqu’une ressource suivie non allouée est libérée, elle est détruite et n’est donc pas renvoyée à l’inventaire.</span><span class="sxs-lookup"><span data-stu-id="b04b2-105">When a tracked, non-allocated resource is freed, it is destroyed and therefore not returned to inventory.</span></span> <span data-ttu-id="b04b2-106">Ce mode de suivi uniquement pour les ressources qui sont peu coûteuses à créer et à détruire est plus utile que de les stocker dans l’inventaire.</span><span class="sxs-lookup"><span data-stu-id="b04b2-106">This track-only mode for resources that are inexpensive to create and destroy is more useful than storing them in inventory.</span></span> <span data-ttu-id="b04b2-107">Ce mode est également utile pour gérer un distributeur de mémoire ou pour une ressource difficile à inventorier, car il existe trop de types différents.</span><span class="sxs-lookup"><span data-stu-id="b04b2-107">This mode is also useful for managing a memory dispenser or for a resource that is difficult to inventory because there are too many different types.</span></span>

<span data-ttu-id="b04b2-108">En mode suivi uniquement, un distributeur de ressources crée directement une ressource demandée au lieu de demander au gestionnaire de distribution d’en allouer un à partir de l’inventaire.</span><span class="sxs-lookup"><span data-stu-id="b04b2-108">In track-only mode, a resource dispenser directly creates a requested resource instead of asking the dispenser manager to allocate one from inventory.</span></span> <span data-ttu-id="b04b2-109">Avant de renvoyer cette ressource au composant d’application demandeur, le distributeur de ressources indique au gestionnaire du distributeur d’effectuer le suivi de la ressource, ce qui garantit que même si le composant oublie de libérer la ressource, le gestionnaire du distributeur le fera quand la durée de vie du composant est supérieure à.</span><span class="sxs-lookup"><span data-stu-id="b04b2-109">Before returning this resource to the requesting application component, the resource dispenser tells the dispenser manager to track the resource, which ensures that even if the component neglects to free the resource, the dispenser manager will do so when the component's lifetime is over.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b04b2-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b04b2-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b04b2-111">Concepts du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="b04b2-111">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 




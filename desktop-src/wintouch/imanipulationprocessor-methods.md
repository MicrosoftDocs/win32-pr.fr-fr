---
title: Méthodes (IInertiaProcessor)
description: Cette section contient les méthodes de l’interface IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Tactile Windows, interface IInertiaProcessor
- Tactile Windows, méthodes d’interface
- inertie, interface IInertiaProcessor
- Interface IInertiaProcessor, méthodes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106512352"
---
# <a name="methods-iinertiaprocessor"></a><span data-ttu-id="f40b0-107">Méthodes (IInertiaProcessor)</span><span class="sxs-lookup"><span data-stu-id="f40b0-107">Methods (IInertiaProcessor)</span></span>

<span data-ttu-id="f40b0-108">Cette section contient les méthodes de l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="f40b0-108">This section contains the methods for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface.</span></span>



| <span data-ttu-id="f40b0-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="f40b0-109">Method</span></span>                                                 | <span data-ttu-id="f40b0-110">Description</span><span class="sxs-lookup"><span data-stu-id="f40b0-110">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f40b0-111">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="f40b0-111">**Reset**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | <span data-ttu-id="f40b0-112">Initialise le processeur avec l’horodatage initial et redémarre l’inertie.</span><span class="sxs-lookup"><span data-stu-id="f40b0-112">Initializes the processor with initial time stamp and restarts inertia.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="f40b0-113">**Processus**</span><span class="sxs-lookup"><span data-stu-id="f40b0-113">**Process**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | <span data-ttu-id="f40b0-114">Effectue des calculs pour le cycle actuel et peut déclencher l’événement **Delta** ou **Complete** selon que l’extrapolation est terminée ou non.</span><span class="sxs-lookup"><span data-stu-id="f40b0-114">Performs calculations for the current tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span> <span data-ttu-id="f40b0-115">Si l’extrapolation s’est terminée au battement précédent, la méthode est no-op.</span><span class="sxs-lookup"><span data-stu-id="f40b0-115">If extrapolation finished at the previous tick, the method is no-op.</span></span> |
| [<span data-ttu-id="f40b0-116">**ProcessTime**</span><span class="sxs-lookup"><span data-stu-id="f40b0-116">**ProcessTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | <span data-ttu-id="f40b0-117">Effectue des calculs pour le cycle donné et peut déclencher l’événement **Delta** ou **Complete** selon que l’extrapolation est terminée ou non.</span><span class="sxs-lookup"><span data-stu-id="f40b0-117">Performs calculations for the given tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span>                                                                        |
| [<span data-ttu-id="f40b0-118">**Terminé**</span><span class="sxs-lookup"><span data-stu-id="f40b0-118">**Complete**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | <span data-ttu-id="f40b0-119">Termine la manipulation actuelle et arrête l’inertie sur le processeur d’inertie.</span><span class="sxs-lookup"><span data-stu-id="f40b0-119">Finishes the current manipulation and stops inertia on the inertia processor.</span></span>                                                                                                                                              |
| [<span data-ttu-id="f40b0-120">**CompleteTime**</span><span class="sxs-lookup"><span data-stu-id="f40b0-120">**CompleteTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | <span data-ttu-id="f40b0-121">Termine la manipulation actuelle au battement donné, arrête l’inertie sur le processeur d’inertie et déclenche l’événement ManipulationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f40b0-121">Finishes the current manipulation at the given tick, stops inertia on the inertia processor, and raises the ManipulationCompleted event.</span></span>                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="f40b0-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f40b0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f40b0-123">**IInertiaProcessor**</span><span class="sxs-lookup"><span data-stu-id="f40b0-123">**IInertiaProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 





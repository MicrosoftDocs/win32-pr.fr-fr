---
description: Composition
ms.assetid: b5f607b2-9cca-4eef-9c63-d2015bd10469
title: Composition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030e02ab77ec54e1e340d72db7210665d649bfb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515120"
---
# <a name="composition"></a><span data-ttu-id="c4289-103">Composition</span><span class="sxs-lookup"><span data-stu-id="c4289-103">Composition</span></span>

> [!Note]  
> <span data-ttu-id="c4289-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c4289-104">\[Deprecated.</span></span> <span data-ttu-id="c4289-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c4289-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c4289-106">L’objet composition est un conteneur pour les pistes.</span><span class="sxs-lookup"><span data-stu-id="c4289-106">The composition object is a container for tracks.</span></span> <span data-ttu-id="c4289-107">Il peut également contenir d’autres compositions (pour l’imbrication des pistes), des effets et des transitions.</span><span class="sxs-lookup"><span data-stu-id="c4289-107">It can also hold other compositions (for nesting of tracks), effects, and transitions.</span></span> <span data-ttu-id="c4289-108">Pour créer cet objet, appelez la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="c4289-108">To create this object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span>

<span data-ttu-id="c4289-109">L’objet composition expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="c4289-109">The composition object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="c4289-110">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="c4289-110">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)
-   [<span data-ttu-id="c4289-111">**IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="c4289-111">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)
-   [<span data-ttu-id="c4289-112">**IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="c4289-112">**IAMTimelineObj**</span></span>](iamtimelineobj.md)
-   [<span data-ttu-id="c4289-113">**IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="c4289-113">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)
-   [<span data-ttu-id="c4289-114">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="c4289-114">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md)

## <a name="related-topics"></a><span data-ttu-id="c4289-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4289-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4289-116">Modèle de chronologie</span><span class="sxs-lookup"><span data-stu-id="c4289-116">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="c4289-117">Construction d’une chronologie</span><span class="sxs-lookup"><span data-stu-id="c4289-117">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 




---
description: Objets Timeline
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Objets Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523709"
---
# <a name="timeline-objects"></a><span data-ttu-id="f782e-103">Objets Timeline</span><span class="sxs-lookup"><span data-stu-id="f782e-103">Timeline Objects</span></span>

<span data-ttu-id="f782e-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="f782e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f782e-105">Chaque type d’objet dans la chronologie (source, suivi, effet, etc.) est un objet COM distinct.</span><span class="sxs-lookup"><span data-stu-id="f782e-105">Each type of object in the timeline—source, track, effect, and so forth—is a distinct COM object.</span></span> <span data-ttu-id="f782e-106">Toutefois, une application ne les crée pas à l’aide de la fonction **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="f782e-106">However, an application does not create them using the **CoCreateInstance** function.</span></span> <span data-ttu-id="f782e-107">Au lieu de cela, il appelle la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="f782e-107">Instead, it calls the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="f782e-108">Cette méthode crée un objet du type demandé, l’initialise et retourne un pointeur vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="f782e-108">This method creates an object of the requested type, initializes it, and returns a pointer to the object.</span></span> <span data-ttu-id="f782e-109">Pour plus d’informations, consultez [construction d’une chronologie](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="f782e-109">For details, see [Constructing a Timeline](constructing-a-timeline.md).</span></span>

<span data-ttu-id="f782e-110">Chaque objet Timeline expose l’interface [**IAMTimelineObj**](iamtimelineobj.md) .</span><span class="sxs-lookup"><span data-stu-id="f782e-110">Every timeline object exposes the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="f782e-111">En outre, les différents types d’objets prennent en charge leurs propres interfaces spécialisées :</span><span class="sxs-lookup"><span data-stu-id="f782e-111">In addition, the various object types support their own specialized interfaces:</span></span>

-   <span data-ttu-id="f782e-112">Source : [ **IAMTimelineSrc**](iamtimelinesrc.md)</span><span class="sxs-lookup"><span data-stu-id="f782e-112">Source: [**IAMTimelineSrc**](iamtimelinesrc.md)</span></span>
-   <span data-ttu-id="f782e-113">Suivi : [ **IAMTimelineTrack**](iamtimelinetrack.md)</span><span class="sxs-lookup"><span data-stu-id="f782e-113">Track: [**IAMTimelineTrack**](iamtimelinetrack.md)</span></span>
-   <span data-ttu-id="f782e-114">Composition : [ **IAMTimelineComp**](iamtimelinecomp.md)</span><span class="sxs-lookup"><span data-stu-id="f782e-114">Composition: [**IAMTimelineComp**](iamtimelinecomp.md)</span></span>
-   <span data-ttu-id="f782e-115">Groupe : [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span><span class="sxs-lookup"><span data-stu-id="f782e-115">Group: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span></span>
-   <span data-ttu-id="f782e-116">Effet : [ **IAMTimelineEffect**](iamtimelineeffect.md)</span><span class="sxs-lookup"><span data-stu-id="f782e-116">Effect: [**IAMTimelineEffect**](iamtimelineeffect.md)</span></span>
-   <span data-ttu-id="f782e-117">Transition : [ **IAMTimelineTrans**](iamtimelinetrans.md)</span><span class="sxs-lookup"><span data-stu-id="f782e-117">Transition: [**IAMTimelineTrans**](iamtimelinetrans.md)</span></span>

<span data-ttu-id="f782e-118">Notez que les groupes sont un type de composition, donc ils prennent en charge [**IAMTimelineComp**](iamtimelinecomp.md), ainsi que leur propre interface [**IAMTimelineGroup**](iamtimelinegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="f782e-118">Note that groups are a type of composition, so they support [**IAMTimelineComp**](iamtimelinecomp.md), as well as their own [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="f782e-119">Outre les interfaces listées précédemment, les objets Timeline exposent d’autres interfaces secondaires.</span><span class="sxs-lookup"><span data-stu-id="f782e-119">In addition to the interfaces listed previously, timeline objects expose other, secondary interfaces.</span></span> <span data-ttu-id="f782e-120">Ces interfaces déterminent les relations entre les types d’objets.</span><span class="sxs-lookup"><span data-stu-id="f782e-120">These interfaces determine the relationships between the object types.</span></span>



| <span data-ttu-id="f782e-121">Interface</span><span class="sxs-lookup"><span data-stu-id="f782e-121">Interface</span></span>                                                  | <span data-ttu-id="f782e-122">Signification</span><span class="sxs-lookup"><span data-stu-id="f782e-122">Meaning</span></span>                                                                                                       | <span data-ttu-id="f782e-123">Exposé par</span><span class="sxs-lookup"><span data-stu-id="f782e-123">Exposed By</span></span>                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="f782e-124">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="f782e-124">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="f782e-125">L’objet est une piste virtuelle. Les pistes virtuelles peuvent résider dans les compositions et contenir d’autres objets Timeline.</span><span class="sxs-lookup"><span data-stu-id="f782e-125">The object is a virtual track. Virtual tracks can reside inside compositions and hold other timeline objects.</span></span> | <span data-ttu-id="f782e-126">Composition, suivi</span><span class="sxs-lookup"><span data-stu-id="f782e-126">Composition, Track</span></span>                |
| [<span data-ttu-id="f782e-127">**IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="f782e-127">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)     | <span data-ttu-id="f782e-128">L’objet peut avoir des effets.</span><span class="sxs-lookup"><span data-stu-id="f782e-128">The object can have effects.</span></span>                                                                                  | <span data-ttu-id="f782e-129">Composition, suivi, source</span><span class="sxs-lookup"><span data-stu-id="f782e-129">Composition, Track, Source</span></span>        |
| [<span data-ttu-id="f782e-130">**IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="f782e-130">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)       | <span data-ttu-id="f782e-131">L’objet peut avoir des transitions.</span><span class="sxs-lookup"><span data-stu-id="f782e-131">The object can have transitions.</span></span>                                                                              | <span data-ttu-id="f782e-132">Composition, suivi</span><span class="sxs-lookup"><span data-stu-id="f782e-132">Composition, Track</span></span>                |
| [<span data-ttu-id="f782e-133">**IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="f782e-133">**IAMTimelineSplittable**</span></span>](iamtimelinesplittable.md)     | <span data-ttu-id="f782e-134">L’objet peut être fractionné en deux objets.</span><span class="sxs-lookup"><span data-stu-id="f782e-134">The object can be split into two objects.</span></span>                                                                     | <span data-ttu-id="f782e-135">Track, source, Effect, transition</span><span class="sxs-lookup"><span data-stu-id="f782e-135">Track, Source, Effect, Transition</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f782e-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f782e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f782e-137">Vue d’ensemble des composants de la chronologie</span><span class="sxs-lookup"><span data-stu-id="f782e-137">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 




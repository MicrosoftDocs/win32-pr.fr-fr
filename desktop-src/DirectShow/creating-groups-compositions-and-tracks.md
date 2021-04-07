---
description: Création de groupes de compositions et de pistes
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Création de groupes de compositions et de pistes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846797"
---
# <a name="creating-groups-compositions-and-tracks"></a><span data-ttu-id="b3cd4-103">Création de groupes de compositions et de pistes</span><span class="sxs-lookup"><span data-stu-id="b3cd4-103">Creating Groups Compositions and Tracks</span></span>

<span data-ttu-id="b3cd4-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="b3cd4-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b3cd4-105">Les groupes, les compositions et les suivis sont les couches intermédiaires entre la chronologie et les éléments sources.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-105">Groups, compositions, and tracks are the intermediate layers between the timeline and the source clips.</span></span> <span data-ttu-id="b3cd4-106">Ils se distinguent par le type d’objet qu’ils peuvent contenir.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-106">They are distinguished by the type of object they can contain.</span></span>

-   <span data-ttu-id="b3cd4-107">Les suivis contiennent des objets sources.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-107">Tracks contain source objects.</span></span>
-   <span data-ttu-id="b3cd4-108">Les compositions contiennent des pistes et d’autres compositions, mais pas des objets sources.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-108">Compositions contain tracks and other compositions, but not source objects.</span></span>
-   <span data-ttu-id="b3cd4-109">Les groupes sont des compositions de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-109">Groups are top-level compositions.</span></span> <span data-ttu-id="b3cd4-110">Les groupes contiennent des compositions et des pistes, mais les compositions ne peuvent pas contenir de groupes.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-110">Groups contain compositions and tracks, but compositions cannot contain groups.</span></span>
-   <span data-ttu-id="b3cd4-111">Une *piste virtuelle* est un objet qui peut résider dans une composition ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-111">A *virtual track* is any object that can reside inside a composition or a group.</span></span> <span data-ttu-id="b3cd4-112">Cela comprend les pistes et les compositions.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-112">This includes tracks and compositions.</span></span>

<span data-ttu-id="b3cd4-113">Ces objets exposent les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3cd4-113">These objects expose the following interfaces:</span></span>



| <span data-ttu-id="b3cd4-114">Interface</span><span class="sxs-lookup"><span data-stu-id="b3cd4-114">Interface</span></span>                                                  | <span data-ttu-id="b3cd4-115">Exposé par</span><span class="sxs-lookup"><span data-stu-id="b3cd4-115">Exposed By</span></span>           |
|------------------------------------------------------------|----------------------|
| [<span data-ttu-id="b3cd4-116">**IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="b3cd4-116">**IAMTimelineTrack**</span></span>](iamtimelinetrack.md)               | <span data-ttu-id="b3cd4-117">Pistes</span><span class="sxs-lookup"><span data-stu-id="b3cd4-117">Tracks</span></span>               |
| [<span data-ttu-id="b3cd4-118">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="b3cd4-118">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="b3cd4-119">Pistes, compositions</span><span class="sxs-lookup"><span data-stu-id="b3cd4-119">Tracks, Compositions</span></span> |
| [<span data-ttu-id="b3cd4-120">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="b3cd4-120">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)                 | <span data-ttu-id="b3cd4-121">Compositions, groupes</span><span class="sxs-lookup"><span data-stu-id="b3cd4-121">Compositions, Groups</span></span> |
| [<span data-ttu-id="b3cd4-122">**IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="b3cd4-122">**IAMTimelineGroup**</span></span>](iamtimelinegroup.md)               | <span data-ttu-id="b3cd4-123">Groupes</span><span class="sxs-lookup"><span data-stu-id="b3cd4-123">Groups</span></span>               |



 

<span data-ttu-id="b3cd4-124">Ces interfaces contiennent les méthodes permettant d’ajouter des objets à la chronologie.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-124">These interfaces contain the methods for adding objects to the timeline.</span></span>

-   <span data-ttu-id="b3cd4-125">[**IAMTimeline :: addgroup**](iamtimeline-addgroup.md): insère un groupe dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-125">[**IAMTimeline::AddGroup**](iamtimeline-addgroup.md): Inserts a group into the timeline.</span></span>
-   <span data-ttu-id="b3cd4-126">[**IAMTimelineComp :: VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): insère une piste virtuelle dans une composition ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-126">[**IAMTimelineComp::VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): Inserts a virtual track into a composition or group.</span></span>
-   <span data-ttu-id="b3cd4-127">[**IAMTimelineTrack :: SrcAdd**](iamtimelinetrack-srcadd.md): insère une source dans une piste.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-127">[**IAMTimelineTrack::SrcAdd**](iamtimelinetrack-srcadd.md): Inserts a source into a track.</span></span>

<span data-ttu-id="b3cd4-128">Par exemple, le code suivant insère une nouvelle piste dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-128">For example, the following code inserts a new track into a group.</span></span> <span data-ttu-id="b3cd4-129">Comme indiqué dans le tableau précédent, un groupe est considéré comme un type de composition, et une piste est un type de piste virtuelle. Par conséquent, pour insérer la piste dans le groupe, vous devez interroger le groupe pour son interface **IAMTimelineComp** et appeler la méthode **IAMTimelineComp :: VTrackInsBefore** .</span><span class="sxs-lookup"><span data-stu-id="b3cd4-129">As shown in the previous table, a group is considered a kind of composition, and a track is a kind of virtual track. Therefore, to insert the track into the group, you must query the group for its **IAMTimelineComp** interface and call the **IAMTimelineComp::VTrackInsBefore** method.</span></span>


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



<span data-ttu-id="b3cd4-130">Le deuxième paramètre de **VTrackInsBefore** spécifie la priorité de la piste virtuelle. Les niveaux de priorité commencent à zéro.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-130">The second parameter to **VTrackInsBefore** specifies the priority of the virtual track. Priority levels start at zero.</span></span> <span data-ttu-id="b3cd4-131">Si vous spécifiez la valeur – 1, la piste virtuelle est insérée à la fin de la liste de priorité.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-131">If you specify the value –1, the virtual track is inserted at the end of the priority list.</span></span> <span data-ttu-id="b3cd4-132">Si vous spécifiez une valeur alors qu’il existe déjà une piste virtuelle, tout ce qui suit descend dans la liste d’un niveau de priorité.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-132">If you specify a value where there is already a virtual track, everything from that point on moves down the list by one priority level.</span></span> <span data-ttu-id="b3cd4-133">N’insérez pas une piste virtuelle à une priorité supérieure au nombre de pistes virtuelles, car elle entraîne un comportement indéfini.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-133">Do not insert a virtual track at a priority greater than the number of virtual tracks, because it will cause undefined behavior.</span></span>

<span data-ttu-id="b3cd4-134">Pour supprimer définitivement un objet de la chronologie, appelez [**IAMTimelineObj :: RemoveAll**](iamtimelineobj-removeall.md) sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-134">To delete an object permanently from the timeline, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md) on the object.</span></span> <span data-ttu-id="b3cd4-135">Cette méthode supprime l’objet et tous ses enfants.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-135">This method removes the object and all its children.</span></span> <span data-ttu-id="b3cd4-136">Pour supprimer un objet en vue de le réinsérer ailleurs dans la chronologie, appelez [**IAMTimelineObj :: Remove**](iamtimelineobj-remove.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-136">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md) instead.</span></span> <span data-ttu-id="b3cd4-137">Contrairement à **RemoveAll**, cette méthode ne supprime pas les enfants de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b3cd4-137">Unlike **RemoveAll**, this method does not delete the object's children.</span></span> <span data-ttu-id="b3cd4-138">Pour tout supprimer de la chronologie, appelez [**IAMTimeline :: ClearAllGroups**](iamtimeline-clearallgroups.md).</span><span class="sxs-lookup"><span data-stu-id="b3cd4-138">To remove everything from the timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3cd4-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3cd4-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3cd4-140">Construction d’une chronologie</span><span class="sxs-lookup"><span data-stu-id="b3cd4-140">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 




---
description: Création d’objets Timeline
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Création d’objets Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106536094"
---
# <a name="creating-timeline-objects"></a><span data-ttu-id="8c65e-103">Création d’objets Timeline</span><span class="sxs-lookup"><span data-stu-id="8c65e-103">Creating Timeline Objects</span></span>

<span data-ttu-id="8c65e-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="8c65e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8c65e-105">L’exemple de code présenté dans cet article commence par une chronologie vide, mais les mêmes étapes s’appliquent si vous chargez un projet existant et souhaitez y ajouter des objets.</span><span class="sxs-lookup"><span data-stu-id="8c65e-105">The sample code presented in this article starts with an empty timeline, but the same steps apply if you load an existing project and want to add objects to it.</span></span>

<span data-ttu-id="8c65e-106">Pour créer tout type d’objet dans la chronologie, appelez la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="8c65e-106">To create any type of object in the timeline, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="8c65e-107">Par exemple, le code suivant crée un nouveau groupe :</span><span class="sxs-lookup"><span data-stu-id="8c65e-107">For example, the following code creates a new group:</span></span>


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



<span data-ttu-id="8c65e-108">Le deuxième paramètre est un membre de l’énumération de [**\_ \_ type principal**](timeline-major-type.md) de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="8c65e-108">The second parameter is a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumeration.</span></span> <span data-ttu-id="8c65e-109">Elle spécifie le type d’objet de chronologie à créer, tel qu’un groupe ou une piste.</span><span class="sxs-lookup"><span data-stu-id="8c65e-109">It specifies the type of timeline object to create, such as a group or a track.</span></span>

<span data-ttu-id="8c65e-110">La méthode **CreateEmptyNode** crée l’objet et retourne un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8c65e-110">The **CreateEmptyNode** method creates the object and returns a pointer to the object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="8c65e-111">Il incrémente également le nombre de références sur l’interface **IAMTimelineObj** . vous devez donc libérer l’interface lorsque vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="8c65e-111">It also increments the reference count on the **IAMTimelineObj** interface, so you must release the interface when you finish using it.</span></span> <span data-ttu-id="8c65e-112">N’appelez pas la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="8c65e-112">Do not call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="8c65e-113">Au lieu de cela, utilisez toujours **CreateEmptyNode** pour créer un objet Timeline, car il initialise le nouvel objet pour une utilisation dans une chronologie.</span><span class="sxs-lookup"><span data-stu-id="8c65e-113">Instead, always use **CreateEmptyNode** to create a timeline object, because it initializes the new object for use in a timeline.</span></span>

<span data-ttu-id="8c65e-114">L’interface [**IAMTimelineObj**](iamtimelineobj.md) est une interface générique.</span><span class="sxs-lookup"><span data-stu-id="8c65e-114">The [**IAMTimelineObj**](iamtimelineobj.md) interface is a generic interface.</span></span> <span data-ttu-id="8c65e-115">Il fournit des méthodes qui sont communes à tous les types d’objets Timeline.</span><span class="sxs-lookup"><span data-stu-id="8c65e-115">It provides methods that are common to all types of timeline object.</span></span> <span data-ttu-id="8c65e-116">Chaque type d’objet expose également d’autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="8c65e-116">Each type of object exposes other interfaces as well.</span></span> <span data-ttu-id="8c65e-117">Par exemple, les groupes exposent l’interface [**IAMTimelineGroup**](iamtimelinegroup.md) , entre autres.</span><span class="sxs-lookup"><span data-stu-id="8c65e-117">For example, groups expose the [**IAMTimelineGroup**](iamtimelinegroup.md) interface, among others.</span></span> <span data-ttu-id="8c65e-118">Vous pouvez obtenir des pointeurs vers les autres interfaces en appelant **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="8c65e-118">You can obtain pointers to the other interfaces by calling **QueryInterface**.</span></span>

<span data-ttu-id="8c65e-119">Une fois que vous avez créé un objet, il ne fait pas encore partie de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="8c65e-119">After you create an object, it is not yet a part of the timeline.</span></span> <span data-ttu-id="8c65e-120">La méthode pour ajouter un objet à la chronologie dépend du type d’objet.</span><span class="sxs-lookup"><span data-stu-id="8c65e-120">The method to add an object to the timeline depends on the object type.</span></span> <span data-ttu-id="8c65e-121">La section suivante décrit comment ajouter des groupes, des compositions et des suivis à la chronologie.</span><span class="sxs-lookup"><span data-stu-id="8c65e-121">The following section describes how to add groups, compositions, and tracks to the timeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c65e-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c65e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c65e-123">Construction d’une chronologie</span><span class="sxs-lookup"><span data-stu-id="8c65e-123">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 

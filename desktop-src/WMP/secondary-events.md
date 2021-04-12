---
title: Événements secondaires
description: Événements secondaires
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Apparences du lecteur Windows Media, événements secondaires
- apparences, événements secondaires
- événements, secondaires
- écriture de code pour les apparences, événements secondaires
- événements secondaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462383"
---
# <a name="secondary-events"></a><span data-ttu-id="fdee4-108">Événements secondaires</span><span class="sxs-lookup"><span data-stu-id="fdee4-108">Secondary Events</span></span>

<span data-ttu-id="fdee4-109">Vous pouvez déterminer les autres événements qui se produisent lors du déclenchement d’un événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="fdee4-109">You can determine what other events are taking place when a specific event is triggered.</span></span> <span data-ttu-id="fdee4-110">Par exemple, quand l’utilisateur clique sur un bouton de la souris, vous pouvez être amené à savoir si la touche ALT a été déverrouillée en même temps.</span><span class="sxs-lookup"><span data-stu-id="fdee4-110">For example, when a mouse button is clicked, you may want to know whether the ALT key was down at the same time.</span></span>

## <a name="event-attributes"></a><span data-ttu-id="fdee4-111">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="fdee4-111">Event Attributes</span></span>

<span data-ttu-id="fdee4-112">Les attributs d’événement suivants sont pris en charge pour les habillages :</span><span class="sxs-lookup"><span data-stu-id="fdee4-112">The following event attributes are supported for skins:</span></span>

-   <span data-ttu-id="fdee4-113">**altKey**</span><span class="sxs-lookup"><span data-stu-id="fdee4-113">**altKey**</span></span>
-   <span data-ttu-id="fdee4-114">**bouton**</span><span class="sxs-lookup"><span data-stu-id="fdee4-114">**button**</span></span>
-   <span data-ttu-id="fdee4-115">**Une fois**</span><span class="sxs-lookup"><span data-stu-id="fdee4-115">**clientX**</span></span>
-   <span data-ttu-id="fdee4-116">**client**</span><span class="sxs-lookup"><span data-stu-id="fdee4-116">**clientY**</span></span>
-   <span data-ttu-id="fdee4-117">**ctrlKey**</span><span class="sxs-lookup"><span data-stu-id="fdee4-117">**ctrlKey**</span></span>
-   <span data-ttu-id="fdee4-118">**fromElement**</span><span class="sxs-lookup"><span data-stu-id="fdee4-118">**fromElement**</span></span>
-   <span data-ttu-id="fdee4-119">**offsetX**</span><span class="sxs-lookup"><span data-stu-id="fdee4-119">**offsetX**</span></span>
-   <span data-ttu-id="fdee4-120">**décalage**</span><span class="sxs-lookup"><span data-stu-id="fdee4-120">**offsetY**</span></span>
-   <span data-ttu-id="fdee4-121">**screenX**</span><span class="sxs-lookup"><span data-stu-id="fdee4-121">**screenX**</span></span>
-   <span data-ttu-id="fdee4-122">**écran**</span><span class="sxs-lookup"><span data-stu-id="fdee4-122">**screenY**</span></span>
-   <span data-ttu-id="fdee4-123">**shiftKey**</span><span class="sxs-lookup"><span data-stu-id="fdee4-123">**shiftKey**</span></span>
-   <span data-ttu-id="fdee4-124">**srcElement**</span><span class="sxs-lookup"><span data-stu-id="fdee4-124">**srcElement**</span></span>
-   <span data-ttu-id="fdee4-125">**toElement**</span><span class="sxs-lookup"><span data-stu-id="fdee4-125">**toElement**</span></span>
-   <span data-ttu-id="fdee4-126">**x**</span><span class="sxs-lookup"><span data-stu-id="fdee4-126">**x**</span></span>
-   <span data-ttu-id="fdee4-127">**y**</span><span class="sxs-lookup"><span data-stu-id="fdee4-127">**y**</span></span>
-   <span data-ttu-id="fdee4-128">**keycode**</span><span class="sxs-lookup"><span data-stu-id="fdee4-128">**keyCode**</span></span>

<span data-ttu-id="fdee4-129">Pour plus d’informations sur ces attributs, consultez la référence sur la programmation de l' [apparence](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="fdee4-129">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="using-secondary-events"></a><span data-ttu-id="fdee4-130">Utilisation d’événements secondaires</span><span class="sxs-lookup"><span data-stu-id="fdee4-130">Using Secondary Events</span></span>

<span data-ttu-id="fdee4-131">Vous pouvez uniquement traiter des attributs d’événement dans du code JScript.</span><span class="sxs-lookup"><span data-stu-id="fdee4-131">You can only process event attributes in JScript code.</span></span> <span data-ttu-id="fdee4-132">Vous devez utiliser la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fdee4-132">You must use the following syntax:</span></span>


```C++
event.eventattributename
```



<span data-ttu-id="fdee4-133">*eventattributename* est le nom de l’attribut d’événement.</span><span class="sxs-lookup"><span data-stu-id="fdee4-133">*eventattributename* is the name of the event attribute.</span></span> <span data-ttu-id="fdee4-134">Par exemple, pour déterminer si la touche ALT a été enfoncée pendant un événement Click, vous pouvez utiliser les lignes suivantes dans votre code JScript :</span><span class="sxs-lookup"><span data-stu-id="fdee4-134">For example, to determine whether the ALT key was pressed during a click event, you could use the following lines in your JScript code:</span></span>


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a><span data-ttu-id="fdee4-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fdee4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdee4-136">**Gestion des événements**</span><span class="sxs-lookup"><span data-stu-id="fdee4-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 





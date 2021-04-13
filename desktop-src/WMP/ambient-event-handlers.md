---
title: Gestionnaires d’événements ambiants
description: Gestionnaires d’événements ambiants
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Apparences du lecteur Windows Media, gestionnaires d’événements ambiants
- apparences, gestionnaires d’événements ambiants
- informations de référence sur les apparences, les gestionnaires d’événements ambiants
- gestionnaires d’événements ambiants
- événements, ambiant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379719"
---
# <a name="ambient-event-handlers"></a><span data-ttu-id="0c029-108">Gestionnaires d’événements ambiants</span><span class="sxs-lookup"><span data-stu-id="0c029-108">Ambient Event Handlers</span></span>

<span data-ttu-id="0c029-109">Les gestionnaires d’événements suivants peuvent être implémentés pour la plupart des éléments d’apparence.</span><span class="sxs-lookup"><span data-stu-id="0c029-109">The following event handlers can be implemented for most skin elements.</span></span> <span data-ttu-id="0c029-110">Les attributs d’événement ambiant accessibles avec le mot clé **Event** peuvent être utilisés dans un gestionnaire d’événements pour déterminer l’état du clavier et de la souris au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="0c029-110">The ambient event attributes accessed with the **event** keyword can be used within an event handler to determine the state of the keyboard and mouse at the time of the event.</span></span>



| <span data-ttu-id="0c029-111">Gestionnaire d'événements</span><span class="sxs-lookup"><span data-stu-id="0c029-111">Event handler</span></span>                                   | <span data-ttu-id="0c029-112">Description</span><span class="sxs-lookup"><span data-stu-id="0c029-112">Description</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c029-113">*attribut* \_ changement</span><span class="sxs-lookup"><span data-stu-id="0c029-113">*attribute*\_onchange</span></span>](attribute-onchange.md) | <span data-ttu-id="0c029-114">Lorsqu’un attribut d’apparence change de valeur, un événement qui peut être géré par un gestionnaire d’événements se produit.</span><span class="sxs-lookup"><span data-stu-id="0c029-114">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="0c029-115">Le nom du gestionnaire d’événements est le nom de l’attribut suivi d’un trait de soulignement et de « OnChange », tels que « valeur \_ OnChange ».</span><span class="sxs-lookup"><span data-stu-id="0c029-115">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span> |
| [<span data-ttu-id="0c029-116">onblur</span><span class="sxs-lookup"><span data-stu-id="0c029-116">onblur</span></span>](onblur.md)                            | <span data-ttu-id="0c029-117">Gère un événement qui se produit lorsque l’élément perd le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="0c029-117">Handles an event that occurs when the element loses the keyboard focus.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="0c029-118">OnClick</span><span class="sxs-lookup"><span data-stu-id="0c029-118">onclick</span></span>](onclick.md)                          | <span data-ttu-id="0c029-119">Gère un événement qui se produit lorsque l’utilisateur clique sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="0c029-119">Handles an event that occurs when the user clicks the element.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="0c029-120">ondblclick</span><span class="sxs-lookup"><span data-stu-id="0c029-120">ondblclick</span></span>](ondblclick.md)                    | <span data-ttu-id="0c029-121">Gère un événement qui se produit lorsque l’utilisateur double-clique sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="0c029-121">Handles an event that occurs when the user double-clicks the element.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="0c029-122">onendalphablend</span><span class="sxs-lookup"><span data-stu-id="0c029-122">onendalphablend</span></span>](onendalphablend.md)          | <span data-ttu-id="0c029-123">Gère un événement qui se produit lorsqu’un élément termine une opération **alphaBlendTo** .</span><span class="sxs-lookup"><span data-stu-id="0c029-123">Handles an event that occurs when an element completes an **alphaBlendTo** operation.</span></span>                                                                                                                                         |
| [<span data-ttu-id="0c029-124">onendmove</span><span class="sxs-lookup"><span data-stu-id="0c029-124">onendmove</span></span>](onendmove.md)                      | <span data-ttu-id="0c029-125">Gère un événement qui se produit lorsqu’un élément termine une opération **MoveTo** .</span><span class="sxs-lookup"><span data-stu-id="0c029-125">Handles an event that occurs when an element completes a **moveTo** operation.</span></span>                                                                                                                                                |
| [<span data-ttu-id="0c029-126">onfocus</span><span class="sxs-lookup"><span data-stu-id="0c029-126">onfocus</span></span>](onfocus.md)                          | <span data-ttu-id="0c029-127">Gère un événement qui se produit lorsque l’élément reçoit le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="0c029-127">Handles an event that occurs when the element receives the keyboard focus.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="0c029-128">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="0c029-128">onkeydown</span></span>](onkeydown.md)                      | <span data-ttu-id="0c029-129">Gère un événement qui se produit lorsqu’une touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="0c029-129">Handles an event that occurs when a key is pressed.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="0c029-130">OnKeyPress</span><span class="sxs-lookup"><span data-stu-id="0c029-130">onkeypress</span></span>](onkeypress.md)                    | <span data-ttu-id="0c029-131">Gère un événement qui se produit lorsque l’utilisateur appuie sur une touche alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="0c029-131">Handles an event that occurs when the user presses an alphanumeric key.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="0c029-132">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="0c029-132">onkeyup</span></span>](onkeyup.md)                          | <span data-ttu-id="0c029-133">Gère un événement qui se produit lorsqu’une touche est relâchée.</span><span class="sxs-lookup"><span data-stu-id="0c029-133">Handles an event that occurs when a key is released.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="0c029-134">OnMouseDown</span><span class="sxs-lookup"><span data-stu-id="0c029-134">onmousedown</span></span>](onmousedown.md)                  | <span data-ttu-id="0c029-135">Gère un événement qui se produit lorsque l’utilisateur clique sur un bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="0c029-135">Handles an event that occurs when the user clicks a mouse button.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="0c029-136">OnMouseMove</span><span class="sxs-lookup"><span data-stu-id="0c029-136">onmousemove</span></span>](onmousemove.md)                  | <span data-ttu-id="0c029-137">Gère un événement qui se produit lorsque l’utilisateur déplace le pointeur de la souris pendant qu’il se trouve sur un élément.</span><span class="sxs-lookup"><span data-stu-id="0c029-137">Handles an event that occurs when the user moves the mouse pointer while it is over an element.</span></span>                                                                                                                               |
| [<span data-ttu-id="0c029-138">onmouseout</span><span class="sxs-lookup"><span data-stu-id="0c029-138">onmouseout</span></span>](onmouseout.md)                    | <span data-ttu-id="0c029-139">Gère un événement qui se produit lorsque l’utilisateur déplace le pointeur hors de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0c029-139">Handles an event that occurs when the user moves the pointer off the element.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="0c029-140">onmouseover</span><span class="sxs-lookup"><span data-stu-id="0c029-140">onmouseover</span></span>](onmouseover.md)                  | <span data-ttu-id="0c029-141">Gère un événement qui se produit lorsque l’utilisateur place d’abord le pointeur sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="0c029-141">Handles an event that occurs when the user first places the pointer over the element.</span></span>                                                                                                                                         |
| [<span data-ttu-id="0c029-142">OnMouseUp</span><span class="sxs-lookup"><span data-stu-id="0c029-142">onmouseup</span></span>](onmouseup.md)                      | <span data-ttu-id="0c029-143">Gère un événement qui se produit lorsque l’utilisateur relâche un bouton de la souris alors que le pointeur se trouve sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="0c029-143">Handles an event that occurs when the user releases a mouse button while the pointer is over the element.</span></span>                                                                                                                     |
| [<span data-ttu-id="0c029-144">OnResize</span><span class="sxs-lookup"><span data-stu-id="0c029-144">onresize</span></span>](onresize.md)                        | <span data-ttu-id="0c029-145">Gère un événement qui se produit lorsqu’un contrôle est redimensionné.</span><span class="sxs-lookup"><span data-stu-id="0c029-145">Handles an event that occurs when a control resizes.</span></span>                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="0c029-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c029-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c029-147">**Attributs d’événement ambiant**</span><span class="sxs-lookup"><span data-stu-id="0c029-147">**Ambient Event Attributes**</span></span>](ambient-event-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c029-148">**Référence de programmation de l’apparence**</span><span class="sxs-lookup"><span data-stu-id="0c029-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 





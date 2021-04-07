---
title: Attributs d’événement ambiant
description: Attributs d’événement ambiant
ms.assetid: 56cd2701-53b3-4456-8fcd-d65f8a6aefd7
keywords:
- Apparences du lecteur Windows Media, attributs d’événement ambiant
- apparences, attributs d’événement ambiant
- informations de référence sur les apparences, les attributs d’événement ambiant
- attributs d’événement ambiant
- attributs, événement ambiant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40522a741509e56d2e4c9201c305126067a0fe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672022"
---
# <a name="ambient-event-attributes"></a><span data-ttu-id="2f63b-108">Attributs d’événement ambiant</span><span class="sxs-lookup"><span data-stu-id="2f63b-108">Ambient Event Attributes</span></span>

<span data-ttu-id="2f63b-109">Les attributs suivants sont communs à tous les événements d’apparence.</span><span class="sxs-lookup"><span data-stu-id="2f63b-109">The following attributes are common to all skin events.</span></span> <span data-ttu-id="2f63b-110">Elles sont accessibles avec le mot clé **Event** dans un gestionnaire d’événements pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="2f63b-110">They are accessed with the **event** keyword within an event handler for the element.</span></span>



| <span data-ttu-id="2f63b-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="2f63b-111">Attribute</span></span>                              | <span data-ttu-id="2f63b-112">Description</span><span class="sxs-lookup"><span data-stu-id="2f63b-112">Description</span></span>                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f63b-113">altKey</span><span class="sxs-lookup"><span data-stu-id="2f63b-113">altKey</span></span>](event-altkey.md)             | <span data-ttu-id="2f63b-114">Récupère une valeur indiquant si la touche ALT était enfoncée lorsque l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="2f63b-114">Retrieves a value indicating whether the ALT key was down when the event occurred.</span></span>                           |
| [<span data-ttu-id="2f63b-115">bouton</span><span class="sxs-lookup"><span data-stu-id="2f63b-115">button</span></span>](event-button.md)             | <span data-ttu-id="2f63b-116">Récupère une valeur indiquant les boutons de la souris qui étaient inactifs lorsque l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="2f63b-116">Retrieves a value indicating which mouse buttons were down when the event occurred.</span></span>                          |
| [<span data-ttu-id="2f63b-117">Une fois</span><span class="sxs-lookup"><span data-stu-id="2f63b-117">clientX</span></span>](event-clientx.md)           | <span data-ttu-id="2f63b-118">Récupère la coordonnée x du pointeur de la souris par rapport à la zone cliente de la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="2f63b-118">Retrieves the x-coordinate of the mouse pointer with respect to the client region of the application window.</span></span> |
| [<span data-ttu-id="2f63b-119">client</span><span class="sxs-lookup"><span data-stu-id="2f63b-119">clientY</span></span>](event-clienty.md)           | <span data-ttu-id="2f63b-120">Récupère la coordonnée y du pointeur de la souris par rapport à la zone cliente de la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="2f63b-120">Retrieves the y-coordinate of the mouse pointer with respect to the client region of the application window.</span></span> |
| [<span data-ttu-id="2f63b-121">ctrlKey</span><span class="sxs-lookup"><span data-stu-id="2f63b-121">ctrlKey</span></span>](event-ctrlkey.md)           | <span data-ttu-id="2f63b-122">Récupère une valeur indiquant si la touche CTRL était enfoncée lorsque l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="2f63b-122">Retrieves a value indicating whether the CTRL key was down when the event occurred.</span></span>                          |
| [<span data-ttu-id="2f63b-123">fromElement</span><span class="sxs-lookup"><span data-stu-id="2f63b-123">fromElement</span></span>](event-fromelement.md)   | <span data-ttu-id="2f63b-124">Récupère l’élément d’origine de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2f63b-124">Retrieves the element the event came from.</span></span>                                                                   |
| [<span data-ttu-id="2f63b-125">keycode</span><span class="sxs-lookup"><span data-stu-id="2f63b-125">keyCode</span></span>](event-keycode.md)           | <span data-ttu-id="2f63b-126">Récupère le code de touche ASCII si une touche a été enfoncée lorsque l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="2f63b-126">Retrieves the ASCII key code if a key was pressed when the event occurred.</span></span>                                   |
| [<span data-ttu-id="2f63b-127">offsetX</span><span class="sxs-lookup"><span data-stu-id="2f63b-127">offsetX</span></span>](event-offsetx.md)           | <span data-ttu-id="2f63b-128">Récupère la coordonnée x du pointeur de la souris par rapport à l’élément déclenchant l’événement.</span><span class="sxs-lookup"><span data-stu-id="2f63b-128">Retrieves the x-coordinate of the mouse pointer with respect to the element firing the event.</span></span>                |
| [<span data-ttu-id="2f63b-129">décalage</span><span class="sxs-lookup"><span data-stu-id="2f63b-129">offsetY</span></span>](event-offsety.md)           | <span data-ttu-id="2f63b-130">Récupère la coordonnée y du pointeur de la souris par rapport à l’élément déclenchant l’événement.</span><span class="sxs-lookup"><span data-stu-id="2f63b-130">Retrieves the y-coordinate of the mouse pointer with respect to the element firing the event.</span></span>                |
| [<span data-ttu-id="2f63b-131">screenHeight</span><span class="sxs-lookup"><span data-stu-id="2f63b-131">screenHeight</span></span>](event-screenheight.md) | <span data-ttu-id="2f63b-132">Récupère la hauteur de la taille d’écran disponible, en pixels.</span><span class="sxs-lookup"><span data-stu-id="2f63b-132">Retrieves the height of the available screen size in pixels.</span></span>                                                 |
| [<span data-ttu-id="2f63b-133">Largeur</span><span class="sxs-lookup"><span data-stu-id="2f63b-133">screenWidth</span></span>](event-screenwidth.md)   | <span data-ttu-id="2f63b-134">Récupère la largeur de la taille d’écran disponible, en pixels.</span><span class="sxs-lookup"><span data-stu-id="2f63b-134">Retrieves the width of the available screen size in pixels.</span></span>                                                  |
| [<span data-ttu-id="2f63b-135">screenX</span><span class="sxs-lookup"><span data-stu-id="2f63b-135">screenX</span></span>](event-screenx.md)           | <span data-ttu-id="2f63b-136">Récupère la coordonnée x absolue du pointeur de la souris par rapport à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2f63b-136">Retrieves the absolute x-coordinate of the mouse pointer with respect to the screen.</span></span>                         |
| [<span data-ttu-id="2f63b-137">écran</span><span class="sxs-lookup"><span data-stu-id="2f63b-137">screenY</span></span>](event-screeny.md)           | <span data-ttu-id="2f63b-138">Récupère la coordonnée y absolue du pointeur de la souris par rapport à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2f63b-138">Retrieves the absolute y-coordinate of the mouse pointer with respect to the screen.</span></span>                         |
| [<span data-ttu-id="2f63b-139">shiftKey</span><span class="sxs-lookup"><span data-stu-id="2f63b-139">shiftKey</span></span>](event-shiftkey.md)         | <span data-ttu-id="2f63b-140">Récupère une valeur indiquant si la touche Maj était enfoncée lorsque l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="2f63b-140">Retrieves a value indicating whether the SHIFT key was down when the event occurred.</span></span>                         |
| [<span data-ttu-id="2f63b-141">srcElement</span><span class="sxs-lookup"><span data-stu-id="2f63b-141">srcElement</span></span>](event-srcelement.md)     | <span data-ttu-id="2f63b-142">Récupère l’élément qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="2f63b-142">Retrieves the element that fired the event.</span></span>                                                                  |
| [<span data-ttu-id="2f63b-143">toElement</span><span class="sxs-lookup"><span data-stu-id="2f63b-143">toElement</span></span>](event-toelement.md)       | <span data-ttu-id="2f63b-144">Récupère l’élément vers lequel le focus clavier a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="2f63b-144">Retrieves the element the keyboard focus moved to.</span></span>                                                           |
| [<span data-ttu-id="2f63b-145">x</span><span class="sxs-lookup"><span data-stu-id="2f63b-145">x</span></span>](event-x.md)                       | <span data-ttu-id="2f63b-146">Récupère la coordonnée x du pointeur de la souris par rapport à la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="2f63b-146">Retrieves the x-coordinate of the mouse pointer with respect to the application window.</span></span>                      |
| [<span data-ttu-id="2f63b-147">y</span><span class="sxs-lookup"><span data-stu-id="2f63b-147">y</span></span>](event-y.md)                       | <span data-ttu-id="2f63b-148">Récupère la coordonnée y du pointeur de la souris par rapport à la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="2f63b-148">Retrieves the y-coordinate of the mouse pointer with respect to the application window.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="2f63b-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f63b-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f63b-150">**Référence de programmation de l’apparence**</span><span class="sxs-lookup"><span data-stu-id="2f63b-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 





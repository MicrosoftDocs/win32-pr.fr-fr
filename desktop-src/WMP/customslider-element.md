---
title: Élément CUSTOMSLIDER
description: Élément CUSTOMSLIDER
ms.assetid: 9cba9bdd-ea5b-4a4a-a61e-e6aff29fc3e0
keywords:
- Apparences du lecteur Windows Media, élément CUSTOMSLIDER
- habillages, élément CUSTOMSLIDER
- Élément CUSTOMSLIDER
- informations de référence sur les habillages, élément CUSTOMSLIDER
- éléments, CUSTOMSLIDER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f49fc6260df295e3266ae9ddf7b5b3eceee43d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310478"
---
# <a name="customslider-element"></a><span data-ttu-id="bcc1f-108">Élément CUSTOMSLIDER</span><span class="sxs-lookup"><span data-stu-id="bcc1f-108">CUSTOMSLIDER Element</span></span>

<span data-ttu-id="bcc1f-109">L’élément **CUSTOMSLIDER** fournit un moyen de créer et de manipuler un contrôle Slider d’une forme quelconque, tel qu’un bouton circulaire.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-109">The **CUSTOMSLIDER** element provides a way to create and manipulate a slider control of any shape, such as a circular knob.</span></span> <span data-ttu-id="bcc1f-110">Les tableaux suivants répertorient les attributs et les gestionnaires d’événements pris en charge par cet élément.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-110">The following tables list the attributes and event handlers supported by this element.</span></span>

<span data-ttu-id="bcc1f-111">L’élément **CUSTOMSLIDER** prend en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-111">The **CUSTOMSLIDER** element supports the following attributes.</span></span>



| <span data-ttu-id="bcc1f-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="bcc1f-112">Attribute</span></span>                                               | <span data-ttu-id="bcc1f-113">Description</span><span class="sxs-lookup"><span data-stu-id="bcc1f-113">Description</span></span>                                                                                                                 |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcc1f-114">cursor</span><span class="sxs-lookup"><span data-stu-id="bcc1f-114">cursor</span></span>](customslider-cursor.md)                       | <span data-ttu-id="bcc1f-115">Spécifie ou récupère la valeur du curseur de contrôle de curseur qui apparaît lorsque la souris se trouve sur le curseur.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-115">Specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>               |
| [<span data-ttu-id="bcc1f-116">disabledImage</span><span class="sxs-lookup"><span data-stu-id="bcc1f-116">disabledImage</span></span>](customslider-disabledimage.md)         | <span data-ttu-id="bcc1f-117">Spécifie ou récupère l’image du curseur utilisé lorsque le curseur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-117">Specifies or retrieves the image of the slider used when the slider is disabled.</span></span>                                            |
| [<span data-ttu-id="bcc1f-118">downImage</span><span class="sxs-lookup"><span data-stu-id="bcc1f-118">downImage</span></span>](customslider-downimage.md)                 | <span data-ttu-id="bcc1f-119">Spécifie ou récupère l’image de l’état inactif du curseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-119">Specifies or retrieves the down state image of the custom slider.</span></span>                                                           |
| [<span data-ttu-id="bcc1f-120">hoverImage</span><span class="sxs-lookup"><span data-stu-id="bcc1f-120">hoverImage</span></span>](customslider-hoverimage.md)               | <span data-ttu-id="bcc1f-121">Spécifie ou récupère l’image qui s’affiche lorsque la souris se trouve sur le curseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-121">Specifies or retrieves the image that displays when the mouse is over the custom slider.</span></span>                                    |
| [<span data-ttu-id="bcc1f-122">image</span><span class="sxs-lookup"><span data-stu-id="bcc1f-122">image</span></span>](customslider-image.md)                         | <span data-ttu-id="bcc1f-123">Spécifie ou récupère le nom du fichier contenant les images correspondant aux différents États du curseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-123">Specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span> |
| [<span data-ttu-id="bcc1f-124">max</span><span class="sxs-lookup"><span data-stu-id="bcc1f-124">max</span></span>](customslider-max.md)                             | <span data-ttu-id="bcc1f-125">Spécifie ou récupère la valeur maximale de la plage définie par le curseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-125">Specifies or retrieves the maximum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="bcc1f-126">min</span><span class="sxs-lookup"><span data-stu-id="bcc1f-126">min</span></span>](customslider-min.md)                             | <span data-ttu-id="bcc1f-127">Spécifie ou récupère la valeur minimale de la plage définie par le curseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-127">Specifies or retrieves the minimum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="bcc1f-128">positionImage</span><span class="sxs-lookup"><span data-stu-id="bcc1f-128">positionImage</span></span>](customslider-positionimage.md)         | <span data-ttu-id="bcc1f-129">Spécifie ou récupère l’image interactive utilisée pour déterminer l’image de position à partir du fichier **image** à afficher.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-129">Specifies or retrieves the image map used to determine which position image from the **image** file to display.</span></span>             |
| [<span data-ttu-id="bcc1f-130">Bulle</span><span class="sxs-lookup"><span data-stu-id="bcc1f-130">toolTip</span></span>](customslider-tooltip.md)                     | <span data-ttu-id="bcc1f-131">Spécifie ou récupère le texte d’info-bulle pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-131">Specifies or retrieves the ToolTip text for the slider.</span></span>                                                                     |
| [<span data-ttu-id="bcc1f-132">Transparente</span><span class="sxs-lookup"><span data-stu-id="bcc1f-132">transparencyColor</span></span>](customslider-transparencycolor.md) | <span data-ttu-id="bcc1f-133">Spécifie ou récupère la couleur de transparence des images de curseur personnalisées.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-133">Specifies or retrieves the transparency color of the custom slider images.</span></span>                                                  |
| [<span data-ttu-id="bcc1f-134">value</span><span class="sxs-lookup"><span data-stu-id="bcc1f-134">value</span></span>](customslider-value.md)                         | <span data-ttu-id="bcc1f-135">Spécifie ou récupère la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-135">Specifies or retrieves the current position of the slider.</span></span>                                                                  |



 

<span data-ttu-id="bcc1f-136">L’élément **CUSTOMSLIDER** peut implémenter les gestionnaires d’événements suivants.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-136">The **CUSTOMSLIDER** element can implement the following event handlers.</span></span>



| <span data-ttu-id="bcc1f-137">Gestionnaire d'événements</span><span class="sxs-lookup"><span data-stu-id="bcc1f-137">Event handler</span></span>                                         | <span data-ttu-id="bcc1f-138">Description</span><span class="sxs-lookup"><span data-stu-id="bcc1f-138">Description</span></span>                                                                                                          |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcc1f-139">onDragBegin</span><span class="sxs-lookup"><span data-stu-id="bcc1f-139">onDragBegin</span></span>](customslider-ondragbegin.md)           | <span data-ttu-id="bcc1f-140">Gère un événement qui se produit lorsque l’utilisateur clique et maintient le bouton gauche de la souris enfoncé et commence à faire glisser la souris.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-140">Handles an event that occurs when the user clicks and holds the left mouse button down and begins to drag the mouse.</span></span> |
| [<span data-ttu-id="bcc1f-141">onDragEnd</span><span class="sxs-lookup"><span data-stu-id="bcc1f-141">onDragEnd</span></span>](customslider-ondragend.md)               | <span data-ttu-id="bcc1f-142">Gère un événement qui se produit lorsque le bouton gauche de la souris est relâché après une opération de glissement.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-142">Handles an event that occurs when the left mouse button is released after a dragging operation.</span></span>                      |
| [<span data-ttu-id="bcc1f-143">onPositionChange</span><span class="sxs-lookup"><span data-stu-id="bcc1f-143">onPositionChange</span></span>](customslider-onpositionchange.md) | <span data-ttu-id="bcc1f-144">Gère un événement qui se produit lorsque la position du curseur change suite à un clic ou un glissement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-144">Handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>   |



 

<span data-ttu-id="bcc1f-145">L’élément **CUSTOMSLIDER** prend en charge les attributs ambiants et peut implémenter les gestionnaires d’événements ambiants.</span><span class="sxs-lookup"><span data-stu-id="bcc1f-145">The **CUSTOMSLIDER** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="bcc1f-146">Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md) et [gestionnaires d’événements ambiants](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="bcc1f-146">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bcc1f-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bcc1f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcc1f-148">**Référence de programmation de l’apparence**</span><span class="sxs-lookup"><span data-stu-id="bcc1f-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 





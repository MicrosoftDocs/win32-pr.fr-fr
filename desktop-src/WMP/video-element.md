---
title: Élément VIDEO
description: Élément VIDEO
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Apparences du lecteur Windows Media, élément vidéo
- Skins, élément VIDEO
- Élément VIDEO
- référence pour les apparences, élément VIDEO
- éléments, vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673602"
---
# <a name="video-element"></a><span data-ttu-id="bc378-108">Élément VIDEO</span><span class="sxs-lookup"><span data-stu-id="bc378-108">VIDEO Element</span></span>

<span data-ttu-id="bc378-109">L’élément **Video** permet de manipuler une fenêtre vidéo dans une apparence, en utilisant les attributs et les événements suivants.</span><span class="sxs-lookup"><span data-stu-id="bc378-109">The **VIDEO** element provides a way to manipulate a video window in a skin, using the following attributes and events.</span></span> <span data-ttu-id="bc378-110">Un élément **vidéo** prédéfini est également fourni pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="bc378-110">A predefined **VIDEO** element is also provided for convenience.</span></span>

<span data-ttu-id="bc378-111">L’élément **Video** prend en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="bc378-111">The **VIDEO** element supports the following attributes.</span></span>



| <span data-ttu-id="bc378-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="bc378-112">Attribute</span></span>                                            | <span data-ttu-id="bc378-113">Description</span><span class="sxs-lookup"><span data-stu-id="bc378-113">Description</span></span>                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc378-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="bc378-114">backgroundColor</span></span>](video-backgroundcolor.md)         | <span data-ttu-id="bc378-115">Spécifie ou récupère la couleur d’arrière-plan du contrôle Video.</span><span class="sxs-lookup"><span data-stu-id="bc378-115">Specifies or retrieves the background color of the Video control.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="bc378-116">cursor</span><span class="sxs-lookup"><span data-stu-id="bc378-116">cursor</span></span>](video-cursor.md)                           | <span data-ttu-id="bc378-117">Spécifie ou récupère la valeur de curseur utilisée lorsque la souris se trouve sur une zone cliquable de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="bc378-117">Specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>                                                                                                                               |
| [<span data-ttu-id="bc378-118">Large</span><span class="sxs-lookup"><span data-stu-id="bc378-118">fullScreen</span></span>](video-fullscreen.md)                   | <span data-ttu-id="bc378-119">Spécifie ou récupère une valeur indiquant si la vidéo est affichée en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="bc378-119">Specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span> <span data-ttu-id="bc378-120">Ne peut être défini qu’au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bc378-120">Can only be set at run time.</span></span>                                                                                                               |
| [<span data-ttu-id="bc378-121">maintainAspectRatio</span><span class="sxs-lookup"><span data-stu-id="bc378-121">maintainAspectRatio</span></span>](video-maintainaspectratio.md) | <span data-ttu-id="bc378-122">Spécifie ou récupère une valeur indiquant si la vidéo conserve les proportions lors de la tentative d’ajustement de la largeur et de la hauteur définies pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="bc378-122">Specifies or retrieves a value indicating whether the video will maintain the aspect ratio when trying to fit within the width and height defined for the control.</span></span>                                                                       |
| [<span data-ttu-id="bc378-123">shrinkToFit</span><span class="sxs-lookup"><span data-stu-id="bc378-123">shrinkToFit</span></span>](video-shrinktofit.md)                 | <span data-ttu-id="bc378-124">Spécifie ou récupère une valeur indiquant si la vidéo sera réduite à la largeur et à la hauteur définies pour le contrôle vidéo.</span><span class="sxs-lookup"><span data-stu-id="bc378-124">Specifies or retrieves a value indicating whether the video will shrink to the width and height defined for the Video control.</span></span>                                                                                                           |
| [<span data-ttu-id="bc378-125">stretchToFit</span><span class="sxs-lookup"><span data-stu-id="bc378-125">stretchToFit</span></span>](video-stretchtofit.md)               | <span data-ttu-id="bc378-126">Spécifie ou récupère une valeur indiquant si la vidéo se redimensionnera à la largeur et à la hauteur définies pour le contrôle vidéo.</span><span class="sxs-lookup"><span data-stu-id="bc378-126">Specifies or retrieves a value indicating whether the video will stretch itself to the width and height defined for the Video control.</span></span>                                                                                                   |
| [<span data-ttu-id="bc378-127">Bulle</span><span class="sxs-lookup"><span data-stu-id="bc378-127">toolTip</span></span>](video-tooltip.md)                         | <span data-ttu-id="bc378-128">Spécifie ou récupère le texte d’info-bulle pour la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="bc378-128">Specifies or retrieves the ToolTip text for the video window.</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="bc378-129">sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="bc378-129">windowless</span></span>](video-windowless.md)                   | <span data-ttu-id="bc378-130">Spécifie ou récupère une valeur indiquant si le contrôle vidéo sera fenêtre ou sans fenêtre ; autrement dit, si le rectangle entier du contrôle est visible à tout moment ou s’il peut être coupé.</span><span class="sxs-lookup"><span data-stu-id="bc378-130">Specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="bc378-131">Ne peut être défini qu’au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="bc378-131">Can only be set at design time.</span></span> |
| [<span data-ttu-id="bc378-132">focale</span><span class="sxs-lookup"><span data-stu-id="bc378-132">zoom</span></span>](video-zoom.md)                               | <span data-ttu-id="bc378-133">Spécifie le pourcentage de mise à l’échelle de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="bc378-133">Specifies the percentage by which to scale the video.</span></span>                                                                                                                                                                                    |



 

<span data-ttu-id="bc378-134">L’élément **Video** peut implémenter les gestionnaires d’événements suivants.</span><span class="sxs-lookup"><span data-stu-id="bc378-134">The **VIDEO** element can implement the following event handlers.</span></span>



| <span data-ttu-id="bc378-135">Gestionnaire d'événements</span><span class="sxs-lookup"><span data-stu-id="bc378-135">Event handler</span></span>                          | <span data-ttu-id="bc378-136">Description</span><span class="sxs-lookup"><span data-stu-id="bc378-136">Description</span></span>                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="bc378-137">onvideoend</span><span class="sxs-lookup"><span data-stu-id="bc378-137">onvideoend</span></span>](video-onvideoend.md)     | <span data-ttu-id="bc378-138">Gère un événement qui se produit lorsque la vidéo arrête le rendu et est déchargée.</span><span class="sxs-lookup"><span data-stu-id="bc378-138">Handles an event that occurs when the video stops rendering and is unloaded.</span></span> |
| [<span data-ttu-id="bc378-139">onvideostart</span><span class="sxs-lookup"><span data-stu-id="bc378-139">onvideostart</span></span>](video-onvideostart.md) | <span data-ttu-id="bc378-140">Gère un événement qui se produit lorsque la vidéo est chargée et commence à effectuer le rendu.</span><span class="sxs-lookup"><span data-stu-id="bc378-140">Handles an event that occurs when the video is loaded and begins to render.</span></span>  |



 

<span data-ttu-id="bc378-141">L’élément **Video** prend en charge les attributs ambiants et peut implémenter les gestionnaires d’événements ambiants, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="bc378-141">The **VIDEO** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="bc378-142">Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md) et [gestionnaires d’événements ambiants](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="bc378-142">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

<span data-ttu-id="bc378-143">Les éléments vidéo prédéfinis sont des éléments **vidéo** normaux avec divers paramètres d’attribut communs spécifiés par défaut.</span><span class="sxs-lookup"><span data-stu-id="bc378-143">Predefined video elements are normal **VIDEO** elements with various common attribute settings specified by default.</span></span> <span data-ttu-id="bc378-144">Les éléments vidéo prédéfinis suivants sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="bc378-144">The following predefined video elements are available.</span></span>



| <span data-ttu-id="bc378-145">VIDÉO prédéfinie</span><span class="sxs-lookup"><span data-stu-id="bc378-145">Predefined VIDEO</span></span>         | <span data-ttu-id="bc378-146">Description</span><span class="sxs-lookup"><span data-stu-id="bc378-146">Description</span></span>                                                |
|--------------------------|------------------------------------------------------------|
| [<span data-ttu-id="bc378-147">WMPVIDEO</span><span class="sxs-lookup"><span data-stu-id="bc378-147">WMPVIDEO</span></span>](wmpvideo.md) | <span data-ttu-id="bc378-148">Élément **vidéo** qui étire la vidéo lorsqu’elle est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="bc378-148">A **VIDEO** element that stretches the video when resized.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bc378-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc378-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc378-150">**Référence de programmation de l’apparence**</span><span class="sxs-lookup"><span data-stu-id="bc378-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 





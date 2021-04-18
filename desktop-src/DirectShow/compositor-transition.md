---
description: Transition de compositeur
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Transition de compositeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566262"
---
# <a name="compositor-transition"></a><span data-ttu-id="df0f7-103">Transition de compositeur</span><span class="sxs-lookup"><span data-stu-id="df0f7-103">Compositor Transition</span></span>

> [!Note]  
> <span data-ttu-id="df0f7-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="df0f7-104">\[Deprecated.</span></span> <span data-ttu-id="df0f7-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="df0f7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="df0f7-106">La transition de compositeur composite composite un sous-rectangle du premier plan dans un rectangle désigné sur l’arrière-plan, sans modifier le reste de l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="df0f7-106">The Compositor transition composites a subrectangle from the foreground into a designated rectangle on the background, without altering the rest of the background.</span></span> <span data-ttu-id="df0f7-107">Utilisez cette transition pour créer des effets de fractionnement ou d’image en image.</span><span class="sxs-lookup"><span data-stu-id="df0f7-107">Use this transition to create split-screen or picture-in-picture effects.</span></span>

<span data-ttu-id="df0f7-108">L’illustration suivante montre la transition de compositeur :</span><span class="sxs-lookup"><span data-stu-id="df0f7-108">The following image shows the compositor transition:</span></span>

![transition de compositeur](images/trans-compositor.png)

<span data-ttu-id="df0f7-110">ID de classe (CLSID) : {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span><span class="sxs-lookup"><span data-stu-id="df0f7-110">Class ID (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span></span>

<span data-ttu-id="df0f7-111">Nom de la variable CLSID : CLSID \_ DxtCompositor</span><span class="sxs-lookup"><span data-stu-id="df0f7-111">CLSID Variable Name: CLSID\_DxtCompositor</span></span>

<span data-ttu-id="df0f7-112">Nom convivial : « DxtCompositor »</span><span class="sxs-lookup"><span data-stu-id="df0f7-112">Friendly Name: "DxtCompositor"</span></span>

<span data-ttu-id="df0f7-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df0f7-113">Properties</span></span>



| <span data-ttu-id="df0f7-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="df0f7-114">Property</span></span>   | <span data-ttu-id="df0f7-115">Type</span><span class="sxs-lookup"><span data-stu-id="df0f7-115">Type</span></span> | <span data-ttu-id="df0f7-116">Default</span><span class="sxs-lookup"><span data-stu-id="df0f7-116">Default</span></span> | <span data-ttu-id="df0f7-117">Description</span><span class="sxs-lookup"><span data-stu-id="df0f7-117">Description</span></span>                                                    |
|------------|------|---------|----------------------------------------------------------------|
| <span data-ttu-id="df0f7-118">Hauteur</span><span class="sxs-lookup"><span data-stu-id="df0f7-118">Height</span></span>     | <span data-ttu-id="df0f7-119">long</span><span class="sxs-lookup"><span data-stu-id="df0f7-119">long</span></span> | <span data-ttu-id="df0f7-120">0</span><span class="sxs-lookup"><span data-stu-id="df0f7-120">0</span></span>       | <span data-ttu-id="df0f7-121">Hauteur, en pixels, du rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="df0f7-121">Height of the target rectangle, in pixels.</span></span>                     |
| <span data-ttu-id="df0f7-122">OffsetX</span><span class="sxs-lookup"><span data-stu-id="df0f7-122">OffsetX</span></span>    | <span data-ttu-id="df0f7-123">long</span><span class="sxs-lookup"><span data-stu-id="df0f7-123">long</span></span> | <span data-ttu-id="df0f7-124">0</span><span class="sxs-lookup"><span data-stu-id="df0f7-124">0</span></span>       | <span data-ttu-id="df0f7-125">Décalage horizontal du rectangle cible, en pixels.</span><span class="sxs-lookup"><span data-stu-id="df0f7-125">Horizontal offset of the target rectangle, in pixels.</span></span>          |
| <span data-ttu-id="df0f7-126">OffsetY</span><span class="sxs-lookup"><span data-stu-id="df0f7-126">OffsetY</span></span>    | <span data-ttu-id="df0f7-127">long</span><span class="sxs-lookup"><span data-stu-id="df0f7-127">long</span></span> | <span data-ttu-id="df0f7-128">0</span><span class="sxs-lookup"><span data-stu-id="df0f7-128">0</span></span>       | <span data-ttu-id="df0f7-129">Décalage vertical du rectangle cible, en pixels.</span><span class="sxs-lookup"><span data-stu-id="df0f7-129">Vertical offset of the target rectangle, in pixels.</span></span>            |
| <span data-ttu-id="df0f7-130">SrcHeight</span><span class="sxs-lookup"><span data-stu-id="df0f7-130">SrcHeight</span></span>  | <span data-ttu-id="df0f7-131">long</span><span class="sxs-lookup"><span data-stu-id="df0f7-131">long</span></span> | <span data-ttu-id="df0f7-132">0</span><span class="sxs-lookup"><span data-stu-id="df0f7-132">0</span></span>       | <span data-ttu-id="df0f7-133">Hauteur du sous-rectangle sur la source, en pixels.</span><span class="sxs-lookup"><span data-stu-id="df0f7-133">The height of the subrectangle on the source, in pixels.</span></span>       |
| <span data-ttu-id="df0f7-134">SrcOffsetX</span><span class="sxs-lookup"><span data-stu-id="df0f7-134">SrcOffsetX</span></span> | <span data-ttu-id="df0f7-135">long</span><span class="sxs-lookup"><span data-stu-id="df0f7-135">long</span></span> | <span data-ttu-id="df0f7-136">0</span><span class="sxs-lookup"><span data-stu-id="df0f7-136">0</span></span>       | <span data-ttu-id="df0f7-137">Coordonnée x du sous-rectangle sur la source, en pixels.</span><span class="sxs-lookup"><span data-stu-id="df0f7-137">The x-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="df0f7-138">SrcOffsetY</span><span class="sxs-lookup"><span data-stu-id="df0f7-138">SrcOffsetY</span></span> | <span data-ttu-id="df0f7-139">long</span><span class="sxs-lookup"><span data-stu-id="df0f7-139">long</span></span> | <span data-ttu-id="df0f7-140">0</span><span class="sxs-lookup"><span data-stu-id="df0f7-140">0</span></span>       | <span data-ttu-id="df0f7-141">Coordonnée y du sous-rectangle sur la source, en pixels.</span><span class="sxs-lookup"><span data-stu-id="df0f7-141">The y-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="df0f7-142">SrcWidth</span><span class="sxs-lookup"><span data-stu-id="df0f7-142">SrcWidth</span></span>   | <span data-ttu-id="df0f7-143">long</span><span class="sxs-lookup"><span data-stu-id="df0f7-143">long</span></span> | <span data-ttu-id="df0f7-144">0</span><span class="sxs-lookup"><span data-stu-id="df0f7-144">0</span></span>       | <span data-ttu-id="df0f7-145">Largeur du sous-rectangle sur la source, en pixels.</span><span class="sxs-lookup"><span data-stu-id="df0f7-145">The width of the subrectangle on the source, in pixels.</span></span>        |
| <span data-ttu-id="df0f7-146">Largeur</span><span class="sxs-lookup"><span data-stu-id="df0f7-146">Width</span></span>      | <span data-ttu-id="df0f7-147">long</span><span class="sxs-lookup"><span data-stu-id="df0f7-147">long</span></span> | <span data-ttu-id="df0f7-148">0</span><span class="sxs-lookup"><span data-stu-id="df0f7-148">0</span></span>       | <span data-ttu-id="df0f7-149">Largeur du rectangle cible, en pixels.</span><span class="sxs-lookup"><span data-stu-id="df0f7-149">Width of the target rectangle, in pixels.</span></span>                      |



 

<span data-ttu-id="df0f7-150">Le diagramme suivant illustre ces propriétés :</span><span class="sxs-lookup"><span data-stu-id="df0f7-150">The following diagram illustrates these properties:</span></span>

![Propriétés de compositeur](images/compmeasure.png)

## <a name="related-topics"></a><span data-ttu-id="df0f7-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df0f7-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df0f7-153">Transitions et effets</span><span class="sxs-lookup"><span data-stu-id="df0f7-153">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> </dl>

 

 




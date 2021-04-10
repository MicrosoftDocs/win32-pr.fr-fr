---
description: Représente la gestion des mappages de l’entrée manuscrite à la fenêtre d’affichage. Utilisez l’objet InkRenderer pour afficher l’encre dans une fenêtre. Vous pouvez également l’utiliser pour repositionner et redimensionner le trait.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: InkRenderer, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210825"
---
# <a name="inkrenderer-class"></a><span data-ttu-id="42367-105">InkRenderer, classe</span><span class="sxs-lookup"><span data-stu-id="42367-105">InkRenderer class</span></span>

<span data-ttu-id="42367-106">Représente la gestion des mappages de l’entrée manuscrite à la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="42367-106">Represents the management of mappings from ink to the display window.</span></span> <span data-ttu-id="42367-107">Utilisez l’objet **InkRenderer** pour afficher l’encre dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="42367-107">Use the **InkRenderer** object to display ink in a window.</span></span> <span data-ttu-id="42367-108">Vous pouvez également l’utiliser pour repositionner et redimensionner le trait.</span><span class="sxs-lookup"><span data-stu-id="42367-108">You can also use it to reposition and resize stroke.</span></span>

<span data-ttu-id="42367-109">**InkRenderer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="42367-109">**InkRenderer** has these types of members:</span></span>

-   [<span data-ttu-id="42367-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="42367-110">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="42367-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="42367-111">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="42367-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="42367-112">Interfaces</span></span>

<span data-ttu-id="42367-113">La classe **InkRenderer** définit ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="42367-113">The **InkRenderer** class defines these interfaces.</span></span>



| <span data-ttu-id="42367-114">Interface</span><span class="sxs-lookup"><span data-stu-id="42367-114">Interface</span></span>        | <span data-ttu-id="42367-115">Description</span><span class="sxs-lookup"><span data-stu-id="42367-115">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="42367-116">**IInkRenderer**</span><span class="sxs-lookup"><span data-stu-id="42367-116">**IInkRenderer**</span></span> | <span data-ttu-id="42367-117">Cet objet implémente l’interface com **IInkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="42367-117">This object implements the **IInkRenderer** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="42367-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="42367-118">Methods</span></span>

<span data-ttu-id="42367-119">La classe **InkRenderer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="42367-119">The **InkRenderer** class has these methods.</span></span>



| <span data-ttu-id="42367-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="42367-120">Method</span></span>                                                                     | <span data-ttu-id="42367-121">Description</span><span class="sxs-lookup"><span data-stu-id="42367-121">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42367-122">**Dessin**</span><span class="sxs-lookup"><span data-stu-id="42367-122">**Draw**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | <span data-ttu-id="42367-123">Dessine des traits sur un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="42367-123">Draws strokes on a device context.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="42367-124">**DrawStroke**</span><span class="sxs-lookup"><span data-stu-id="42367-124">**DrawStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | <span data-ttu-id="42367-125">Dessine un trait sur le contexte de périphérique Windows spécifié.</span><span class="sxs-lookup"><span data-stu-id="42367-125">Draws a stroke on the specified windows device context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="42367-126">**GetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="42367-126">**GetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | <span data-ttu-id="42367-127">Récupère la transformation d’objet qui a été utilisée pour restituer l’encre.</span><span class="sxs-lookup"><span data-stu-id="42367-127">Retrieves the object transform that was used to render ink.</span></span><br/>                                                                                   |
| [<span data-ttu-id="42367-128">**GetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="42367-128">**GetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | <span data-ttu-id="42367-129">Récupère la transformation de vue qui est utilisée pour restituer l’encre.</span><span class="sxs-lookup"><span data-stu-id="42367-129">Retrieves the view transform that is used to render ink.</span></span><br/>                                                                                      |
| [<span data-ttu-id="42367-130">**InkSpaceToPixel**</span><span class="sxs-lookup"><span data-stu-id="42367-130">**InkSpaceToPixel**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | <span data-ttu-id="42367-131">Convertit un emplacement dans les coordonnées de l’espace d’encre en espace en pixels.</span><span class="sxs-lookup"><span data-stu-id="42367-131">Converts a location in ink space coordinates to be in pixel space.</span></span><br/>                                                                            |
| [<span data-ttu-id="42367-132">**InkSpaceToPixelFromPoints**</span><span class="sxs-lookup"><span data-stu-id="42367-132">**InkSpaceToPixelFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | <span data-ttu-id="42367-133">Convertit un tableau de points dans les coordonnées d’espace d’encre en espace de pixels.</span><span class="sxs-lookup"><span data-stu-id="42367-133">Converts an array of points in ink space coordinates to pixel space.</span></span><br/>                                                                          |
| [<span data-ttu-id="42367-134">**Unité**</span><span class="sxs-lookup"><span data-stu-id="42367-134">**Measure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | <span data-ttu-id="42367-135">Calcule le rectangle sur le contexte de périphérique qui contient une collection de traits s’ils ont été dessinés avec l’objet **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="42367-135">Calculates the rectangle on the device context that would contain a collection of strokes if they were drawn with the **InkRenderer** object.</span></span><br/> |
| [<span data-ttu-id="42367-136">**MeasureStroke**</span><span class="sxs-lookup"><span data-stu-id="42367-136">**MeasureStroke**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | <span data-ttu-id="42367-137">Calcule le rectangle sur le contexte de périphérique qui contiendra un trait s’il a été dessiné avec l’objet **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="42367-137">Calculates the rectangle on the device context that would contain a stroke if they were drawn with the **InkRenderer** object.</span></span><br/>                |
| [<span data-ttu-id="42367-138">**Activer**</span><span class="sxs-lookup"><span data-stu-id="42367-138">**Move**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | <span data-ttu-id="42367-139">Applique une translation à la transformation de vue dans les coordonnées d’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="42367-139">Applies a translation to the view transform in ink space coordinates.</span></span><br/>                                                                         |
| [<span data-ttu-id="42367-140">**PixelToInkSpace**</span><span class="sxs-lookup"><span data-stu-id="42367-140">**PixelToInkSpace**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | <span data-ttu-id="42367-141">Convertit un emplacement en coordonnées en pixels en espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="42367-141">Converts a location in pixel coordinates to be in ink space.</span></span><br/>                                                                                  |
| [<span data-ttu-id="42367-142">**PixelToInkSpaceFromPoints**</span><span class="sxs-lookup"><span data-stu-id="42367-142">**PixelToInkSpaceFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | <span data-ttu-id="42367-143">Convertit un tableau de points en coordonnées d’espace de pixels en espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="42367-143">Converts an array of points in pixel space coordinates to ink space.</span></span><br/>                                                                          |
| [<span data-ttu-id="42367-144">**Faire pivoter**</span><span class="sxs-lookup"><span data-stu-id="42367-144">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | <span data-ttu-id="42367-145">Applique une rotation à la transformation de la vue.</span><span class="sxs-lookup"><span data-stu-id="42367-145">Applies a rotation to the view transform.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="42367-146">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="42367-146">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | <span data-ttu-id="42367-147">Met à l’échelle la transformation de la vue dans la dimension X et Y.</span><span class="sxs-lookup"><span data-stu-id="42367-147">Scales the view transform in the X and Y dimension.</span></span><br/>                                                                                           |
| [<span data-ttu-id="42367-148">**SetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="42367-148">**SetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | <span data-ttu-id="42367-149">Définit la transformation d’objet utilisée pour restituer l’encre.</span><span class="sxs-lookup"><span data-stu-id="42367-149">Sets the object transform that is used to render ink.</span></span><br/>                                                                                         |
| [<span data-ttu-id="42367-150">**SetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="42367-150">**SetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | <span data-ttu-id="42367-151">Définit la transformation de vue utilisée pour restituer l’encre.</span><span class="sxs-lookup"><span data-stu-id="42367-151">Sets the view transform that is used to render ink.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="42367-152">Notes</span><span class="sxs-lookup"><span data-stu-id="42367-152">Remarks</span></span>

<span data-ttu-id="42367-153">L’impression s’effectue également par le biais de l’objet **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="42367-153">Printing is also done through the **InkRenderer** object.</span></span>

<span data-ttu-id="42367-154">Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="42367-154">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="42367-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42367-155">Requirements</span></span>



| <span data-ttu-id="42367-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42367-156">Requirement</span></span> | <span data-ttu-id="42367-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="42367-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42367-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42367-158">Minimum supported client</span></span><br/> | <span data-ttu-id="42367-159">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42367-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="42367-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42367-160">Minimum supported server</span></span><br/> | <span data-ttu-id="42367-161">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="42367-161">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="42367-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="42367-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="42367-163"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="42367-163"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="42367-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="42367-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="42367-165"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42367-165"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="42367-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42367-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42367-167">**Renderer (propriété)**</span><span class="sxs-lookup"><span data-stu-id="42367-167">**Renderer Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[<span data-ttu-id="42367-168">**InkDrawingAttributes, classe**</span><span class="sxs-lookup"><span data-stu-id="42367-168">**InkDrawingAttributes Class**</span></span>](inkdrawingattributes-class.md)
</dt> <dt>

[<span data-ttu-id="42367-169">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="42367-169">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="42367-170">[Collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="42367-170">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 


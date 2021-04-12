---
description: Représente les attributs qui sont appliqués à l’encre lorsqu’elle est dessinée.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: InkDrawingAttributes, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320138"
---
# <a name="inkdrawingattributes-class"></a><span data-ttu-id="8d865-103">InkDrawingAttributes, classe</span><span class="sxs-lookup"><span data-stu-id="8d865-103">InkDrawingAttributes class</span></span>

<span data-ttu-id="8d865-104">Représente les attributs qui sont appliqués à l’encre lorsqu’elle est dessinée.</span><span class="sxs-lookup"><span data-stu-id="8d865-104">Represents the attributes that are applied to ink when it is drawn.</span></span>

<span data-ttu-id="8d865-105">**InkDrawingAttributes** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8d865-105">**InkDrawingAttributes** has these types of members:</span></span>

-   [<span data-ttu-id="8d865-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="8d865-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="8d865-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8d865-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="8d865-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d865-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="8d865-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="8d865-109">Interfaces</span></span>

<span data-ttu-id="8d865-110">La classe **InkDrawingAttributes** définit ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="8d865-110">The **InkDrawingAttributes** class defines these interfaces.</span></span>



| <span data-ttu-id="8d865-111">Interface</span><span class="sxs-lookup"><span data-stu-id="8d865-111">Interface</span></span>                 | <span data-ttu-id="8d865-112">Description</span><span class="sxs-lookup"><span data-stu-id="8d865-112">Description</span></span>                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="8d865-113">**IInkDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="8d865-113">**IInkDrawingAttributes**</span></span> | <span data-ttu-id="8d865-114">Cet objet implémente l’interface com **IInkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="8d865-114">This object implements the **IInkDrawingAttributes** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="8d865-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8d865-115">Methods</span></span>

<span data-ttu-id="8d865-116">La classe **InkDrawingAttributes** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8d865-116">The **InkDrawingAttributes** class has these methods.</span></span>



| <span data-ttu-id="8d865-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="8d865-117">Method</span></span>                         | <span data-ttu-id="8d865-118">Description</span><span class="sxs-lookup"><span data-stu-id="8d865-118">Description</span></span>                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d865-119">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="8d865-119">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | <span data-ttu-id="8d865-120">Crée un objet [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes** ou [**InkRecognizerContext**](inkrecognizercontext-class.md) dupliqué.</span><span class="sxs-lookup"><span data-stu-id="8d865-120">Creates a duplicate [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes**, or [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8d865-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d865-121">Properties</span></span>

<span data-ttu-id="8d865-122">La classe **InkDrawingAttributes** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8d865-122">The **InkDrawingAttributes** class has these properties.</span></span>



| <span data-ttu-id="8d865-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="8d865-123">Property</span></span>                                                                           | <span data-ttu-id="8d865-124">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="8d865-124">Access type</span></span>           | <span data-ttu-id="8d865-125">Description</span><span class="sxs-lookup"><span data-stu-id="8d865-125">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d865-126">**Crénelées**</span><span class="sxs-lookup"><span data-stu-id="8d865-126">**AntiAliased**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | <span data-ttu-id="8d865-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d865-127">Read/write</span></span><br/> | <span data-ttu-id="8d865-128">Obtient ou définit la valeur qui spécifie si les couleurs de premier plan et d’arrière-plan le long du bord de l’encre sont fusionnées pour augmenter la fluidité d’un trait d’encre.</span><span class="sxs-lookup"><span data-stu-id="8d865-128">Gets or sets the value that specifies whether the foreground and background colors along the edge of the ink are blended to increase the smoothness of an ink stroke.</span></span><br/> |
| [<span data-ttu-id="8d865-129">**Couleur**</span><span class="sxs-lookup"><span data-stu-id="8d865-129">**Color**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | <span data-ttu-id="8d865-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d865-130">Read/write</span></span><br/> | <span data-ttu-id="8d865-131">Obtient ou définit la couleur de l’encre dessinée avec cet objet **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="8d865-131">Gets or sets the color of the ink drawn with this **InkDrawingAttributes** object.</span></span><br/>                                                                                    |
| [<span data-ttu-id="8d865-132">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="8d865-132">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="8d865-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d865-133">Read-only</span></span><br/>  | <span data-ttu-id="8d865-134">Obtient la collection de données définies par l’application qui est stockée dans l’objet **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="8d865-134">Gets the collection of application-defined data that is stored in the **InkDrawingAttributes** object.</span></span><br/>                                                                |
| [<span data-ttu-id="8d865-135">**FitToCurve**</span><span class="sxs-lookup"><span data-stu-id="8d865-135">**FitToCurve**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | <span data-ttu-id="8d865-136">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d865-136">Read/write</span></span><br/> | <span data-ttu-id="8d865-137">Obtient ou définit la valeur qui spécifie si l’entrée manuscrite est rendue sous la forme d’une série de courbes au lieu de lignes entre des points d’échantillon de stylet.</span><span class="sxs-lookup"><span data-stu-id="8d865-137">Gets or sets the value that specifies whether ink is rendered as a series of curves instead of as lines between pen sample points.</span></span><br/>                                    |
| [<span data-ttu-id="8d865-138">**Height**</span><span class="sxs-lookup"><span data-stu-id="8d865-138">**Height**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | <span data-ttu-id="8d865-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d865-139">Read/write</span></span><br/> | <span data-ttu-id="8d865-140">Obtient ou définit la hauteur du stylet lors du dessin de l’encre avec cet objet **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="8d865-140">Gets or sets the height of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                        |
| [<span data-ttu-id="8d865-141">**IgnorePressure**</span><span class="sxs-lookup"><span data-stu-id="8d865-141">**IgnorePressure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | <span data-ttu-id="8d865-142">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d865-142">Read/write</span></span><br/> | <span data-ttu-id="8d865-143">Obtient ou définit la valeur qui spécifie si l’encre dessinée devient automatiquement plus grande, avec une pression accrue du Conseil du stylet sur l’aire de tablette.</span><span class="sxs-lookup"><span data-stu-id="8d865-143">Gets or sets the value that specifies whether drawn ink automatically becomes wider with increased pressure of the pen tip on the tablet surface.</span></span><br/>                     |
| [<span data-ttu-id="8d865-144">**PenTip**</span><span class="sxs-lookup"><span data-stu-id="8d865-144">**PenTip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | <span data-ttu-id="8d865-145">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d865-145">Read/write</span></span><br/> | <span data-ttu-id="8d865-146">Obtient ou définit l’info-bulle du stylet à utiliser (boule ou rectangle) lors du dessin de l’encre avec cet objet **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="8d865-146">Gets or sets the pen tip to use (ball or rectangle) when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                       |
| [<span data-ttu-id="8d865-147">**RasterOperation**</span><span class="sxs-lookup"><span data-stu-id="8d865-147">**RasterOperation**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | <span data-ttu-id="8d865-148">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d865-148">Read/write</span></span><br/> | <span data-ttu-id="8d865-149">Obtient ou définit la manière dont la couleur du stylet interagit avec les couleurs d’arrière-plan existantes sur l’affichage lorsque l’encre est dessinée.</span><span class="sxs-lookup"><span data-stu-id="8d865-149">Gets or sets how the pen color interacts with the existing background colors on the display when the ink is drawn.</span></span><br/>                                                    |
| [<span data-ttu-id="8d865-150">**Transparence**</span><span class="sxs-lookup"><span data-stu-id="8d865-150">**Transparency**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | <span data-ttu-id="8d865-151">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d865-151">Read/write</span></span><br/> | <span data-ttu-id="8d865-152">Obtient ou définit la valeur de transparence de l’encre dessinée.</span><span class="sxs-lookup"><span data-stu-id="8d865-152">Gets or sets the transparency value of drawn ink.</span></span> <span data-ttu-id="8d865-153">Les valeurs sont comprises entre zéro (entièrement opaque) et 255 (entièrement transparent).</span><span class="sxs-lookup"><span data-stu-id="8d865-153">Values range from zero (totally opaque) to 255 (totally transparent).</span></span><br/>                                               |
| [<span data-ttu-id="8d865-154">**Width**</span><span class="sxs-lookup"><span data-stu-id="8d865-154">**Width**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | <span data-ttu-id="8d865-155">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d865-155">Read/write</span></span><br/> | <span data-ttu-id="8d865-156">Obtient ou définit la largeur du stylet lors du dessin de l’encre avec cet objet **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="8d865-156">Gets or sets the width of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="8d865-157">Notes</span><span class="sxs-lookup"><span data-stu-id="8d865-157">Remarks</span></span>

<span data-ttu-id="8d865-158">Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="8d865-158">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="8d865-159">Ces attributs de dessin peuvent être associés à un trait ou à un curseur et spécifier des paramètres tels que la couleur, la largeur et la transparence.</span><span class="sxs-lookup"><span data-stu-id="8d865-159">These drawing attributes can be associated with a stroke or a cursor and specify settings such as color, width, and transparency.</span></span>

<span data-ttu-id="8d865-160">Pour spécifier les attributs de dessin d’un trait, utilisez la propriété [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) de l’objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="8d865-160">To specify the drawing attributes of a stroke, use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span> <span data-ttu-id="8d865-161">Pour spécifier les attributs de dessin de tous les traits dans une collection de traits, appelez la méthode [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) de la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8d865-161">To specify the drawing attributes of all of the strokes within a collection of strokes, call the [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) method of the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

<span data-ttu-id="8d865-162">Chaque objet [**InkCollector**](inkcollector-class.md) , objet [**InkOverlay**](inkoverlay-class.md) et contrôle [InkPicture](inkpicture-control-reference.md) peuvent spécifier un ensemble différent d’attributs de dessin pour le même curseur.</span><span class="sxs-lookup"><span data-stu-id="8d865-162">Each [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control can specify a different set of drawing attributes for the same cursor.</span></span> <span data-ttu-id="8d865-163">Utilisez la propriété [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) pour obtenir ou définir les attributs de dessin d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="8d865-163">Use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object to get or set the drawing attributes of a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d865-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d865-164">Requirements</span></span>



| <span data-ttu-id="8d865-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d865-165">Requirement</span></span> | <span data-ttu-id="8d865-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d865-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d865-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d865-167">Minimum supported client</span></span><br/> | <span data-ttu-id="8d865-168">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d865-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8d865-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d865-169">Minimum supported server</span></span><br/> | <span data-ttu-id="8d865-170">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d865-170">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8d865-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d865-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d865-172"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8d865-172"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8d865-173">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8d865-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d865-174"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d865-174"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8d865-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d865-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d865-176">**DrawingAttributes, propriété**</span><span class="sxs-lookup"><span data-stu-id="8d865-176">**DrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

<span data-ttu-id="8d865-177">**DrawingAttributes, propriété**</span><span class="sxs-lookup"><span data-stu-id="8d865-177">**DrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="8d865-178">**DrawingAttributes, propriété**</span><span class="sxs-lookup"><span data-stu-id="8d865-178">**DrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="8d865-179">**Propriété DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="8d865-179">**DefaultDrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

<span data-ttu-id="8d865-180">**Propriété DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="8d865-180">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="8d865-181">**Propriété DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="8d865-181">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="8d865-182">**Méthode ModifyDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="8d865-182">**ModifyDrawingAttributes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[<span data-ttu-id="8d865-183">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="8d865-183">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="8d865-184">**InkDisp, classe**</span><span class="sxs-lookup"><span data-stu-id="8d865-184">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

[<span data-ttu-id="8d865-185">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="8d865-185">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


---
description: Cette page explique comment dessiner des graphiques dans un modèle d’objet XPS.
ms.assetid: 2384b522-208a-48db-ae0d-f82fa0214d09
title: Dessiner des graphiques dans un modèle d’objet XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabbf8cfb821c80dfff43e2e7844331c8920f726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533870"
---
# <a name="draw-graphics-in-an-xps-om"></a><span data-ttu-id="069ee-103">Dessiner des graphiques dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="069ee-103">Draw Graphics in an XPS OM</span></span>

<span data-ttu-id="069ee-104">Cette page explique comment dessiner des graphiques dans un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="069ee-104">This page describes how to draw graphics in an XPS OM.</span></span>

<span data-ttu-id="069ee-105">Pour dessiner des graphiques vectoriels dans une page, instanciez une interface [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) , remplissez-la avec le contenu souhaité, puis ajoutez-la à la liste d’objets visuels de la page ou de la zone de dessin.</span><span class="sxs-lookup"><span data-stu-id="069ee-105">To draw vector-based graphics in a page, instantiate an [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface, populate it with the desired content, and add it to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="069ee-106">Une interface **IXpsOMPath** contient les propriétés d’une forme vectorielle en tant que contour, couleur de remplissage, style de ligne et couleur de ligne.</span><span class="sxs-lookup"><span data-stu-id="069ee-106">An **IXpsOMPath** interface contains such properties of a vector-based shape as the outline, fill color, line style, and line color.</span></span> <span data-ttu-id="069ee-107">La forme du chemin d’accès est spécifiée par une interface [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) , qui contient une collection d’interfaces [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) et, éventuellement, une interface [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) .</span><span class="sxs-lookup"><span data-stu-id="069ee-107">The path's shape is specified by an [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface, which contains a collection of [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interfaces and, optionally, an [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) interface.</span></span> <span data-ttu-id="069ee-108">Vous pouvez utiliser n’importe quelle interface qui hérite de l’interface [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) pour remplir le périmètre du chemin d’accès et l’intérieur de la forme qui est décrite par le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="069ee-108">You can use any interface that inherits from the [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) interface to fill the perimeter of the path and the interior of the shape that is described by the path.</span></span>

<span data-ttu-id="069ee-109">Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="069ee-109">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="069ee-110">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="069ee-110">Code Example</span></span>

<span data-ttu-id="069ee-111">L’exemple de code suivant crée un tracé simple qui décrit un rectangle rempli avec une couleur unique.</span><span class="sxs-lookup"><span data-stu-id="069ee-111">The following code example creates a simple path that describes a rectangle that is filled with a single color.</span></span>

### <a name="create-the-stroke-and-the-fill-brushes"></a><span data-ttu-id="069ee-112">Créer le trait et les pinceaux de remplissage</span><span class="sxs-lookup"><span data-stu-id="069ee-112">Create the stroke and the fill brushes</span></span>

<span data-ttu-id="069ee-113">La première section de l’exemple de code crée le [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) qui sera utilisé pour remplir l’objet Path.</span><span class="sxs-lookup"><span data-stu-id="069ee-113">The first section of the code example creates the [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) that will be used to fill the path object.</span></span>


```C++
    HRESULT               hr = S_OK;

    XPS_COLOR             xpsColor;
    IXpsOMSolidColorBrush *xpsFillBrush = NULL;
    IXpsOMSolidColorBrush *xpsStrokeBrush = NULL;

    // Set the fill brush color to RED.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColor,
        NULL,          // color profile resource
        &xpsFillBrush);
    // The color profile resource parameter is NULL because
    //  this color type does not use a color profile resource.

    // Set the stroke brush color to BLACK.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0x00;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
            &xpsColor,
            NULL, // This color type does not use a color profile resource.
            &xpsStrokeBrush);

    // The brushes are released below after they have been used.
```



### <a name="define-the-shape"></a><span data-ttu-id="069ee-114">Définir la forme</span><span class="sxs-lookup"><span data-stu-id="069ee-114">Define the shape</span></span>

<span data-ttu-id="069ee-115">La deuxième section de l’exemple de code crée l’interface [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) .</span><span class="sxs-lookup"><span data-stu-id="069ee-115">The second section of the code example creates the [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface.</span></span> <span data-ttu-id="069ee-116">Il crée ensuite l’interface [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) qui spécifie la forme de la figure et ajoute la figure à l’interface **IXpsOMGeometry** .</span><span class="sxs-lookup"><span data-stu-id="069ee-116">It then creates the [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interface that specifies the figure's shape, and adds the figure to the **IXpsOMGeometry** interface.</span></span> <span data-ttu-id="069ee-117">L’exemple crée un rectangle qui est spécifié par *Rect*.</span><span class="sxs-lookup"><span data-stu-id="069ee-117">The example creates a rectangle that is specified by *rect*.</span></span> <span data-ttu-id="069ee-118">Les segments doivent être définis pour seulement trois des quatre côtés du rectangle.</span><span class="sxs-lookup"><span data-stu-id="069ee-118">Segments must be defined for only three of the four sides of the rectangle.</span></span> <span data-ttu-id="069ee-119">Le périmètre de la forme, le rectangle dans ce cas, démarre à partir du point de départ et s’étend comme défini par les segments de la figure Geometry.</span><span class="sxs-lookup"><span data-stu-id="069ee-119">The perimeter of the shape, the rectangle in this case, starts from the start point and extends as defined by the segments of the geometry figure.</span></span> <span data-ttu-id="069ee-120">L’affectation de la **valeur true** à la propriété **IsClosed** indique que le rectangle est fermé en ajoutant un segment supplémentaire qui connecte la fin du dernier segment au point de départ.</span><span class="sxs-lookup"><span data-stu-id="069ee-120">Setting the **IsClosed** property to **TRUE** indicates that the rectangle is closed by adding one additional segment that connects the end of the last segment to the start point.</span></span>


```C++
    // rect is initialized outside of the sample and 
    //  contains the coordinates of the rectangular geometry to create.
    XPS_RECT                            rect = {0,0,100,100};       

    HRESULT                             hr = S_OK;
    IXpsOMGeometryFigure                *rectFigure;
    IXpsOMGeometry                      *imageRectGeometry;
    IXpsOMGeometryFigureCollection      *geomFigureCollection;

    // Define the start point and create an empty figure.
    XPS_POINT                           startPoint = {rect.x, rect.y};
    hr = xpsFactory->CreateGeometryFigure( &startPoint, &rectFigure );
    // Define the segments of the geometry figure.
    //  First, define the type of each segment.
    XPS_SEGMENT_TYPE segmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE,  // each segment is a straight line
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };

    // Define the x and y coordinates of each corner of the figure
    //  the start point has already been defined so only the 
    //  remaining three corners need to be defined.
    FLOAT segmentData[6] = {
        rect.x,                (rect.y + rect.height),
        (rect.x + rect.width), (rect.y + rect.height), 
        (rect.x + rect.width), rect.y 
    };

    // Describe if the segments are stroked (that is if the segment lines
    //  should be drawn as a line).
    BOOL segmentStrokes[3] = {
        TRUE, TRUE, TRUE // Yes, draw each of the segment lines.
    };

    // Add the segment data to the figure.
    hr = rectFigure->SetSegments(
                        3, 
                        6, 
                        segmentTypes, 
                        segmentData, 
                        segmentStrokes);

    // Set the closed and filled properties of the figure.
    hr = rectFigure->SetIsClosed( TRUE );
    hr = rectFigure->SetIsFilled( TRUE );
 
    // Create the geometry object.
    hr = xpsFactory->CreateGeometry( &imageRectGeometry );
    
    // Get a pointer to the figure collection interface of the geometry...
    hr = imageRectGeometry->GetFigures( &geomFigureCollection );

    // ...and then add the figure created above to this geometry.
    hr = geomFigureCollection->Append( rectFigure );
    // If not needed for anything else, release the rectangle figure.
    rectFigure->Release();

    // when done adding figures, release the figure collection. 
    geomFigureCollection->Release();

    //  When done with the geometry object, release the object.
    // imageRectGeometry->Release();
    //  In this case, imageRectGeometry is used in the next sample
    //  so the geometry object is not released, yet.
    
```



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a><span data-ttu-id="069ee-121">Créer le chemin d’accès et l’ajouter à la collection d’éléments visuels</span><span class="sxs-lookup"><span data-stu-id="069ee-121">Create the path and add it to the visual collection</span></span>

<span data-ttu-id="069ee-122">La dernière section de cet exemple de code crée et configure l’objet Path, puis l’ajoute à la liste des objets visuels de la page.</span><span class="sxs-lookup"><span data-stu-id="069ee-122">The final section of this code example creates and configures the path object, then adds it to the page's list of visual objects.</span></span>


```C++
    HRESULT                    hr = S_OK;
    // The page interface pointer is initialized outside of this sample.
    IXpsOMPath                *rectPath = NULL;
    IXpsOMVisualCollection    *pageVisuals = NULL;

    // Create the new path object.
    hr = xpsFactory->CreatePath( &rectPath );

    // Add the geometry to the path.
    //  imageRectGeometry is initialized outside of this example.
    hr = rectPath->SetGeometryLocal( imageRectGeometry );

    // Set the short description of the path to provide
    //  a textual description of the object for accessibility.
    hr = rectPath->SetAccessibilityShortDescription( L"Red Rectangle" );
    
    // Set the fill and stroke brushes to use the brushes 
    //  created in the first section.
    hr = rectPath->SetFillBrushLocal( xpsFillBrush );
    hr = rectPath->SetStrokeBrushLocal( xpsStrokeBrush);

    // Get the visual collection of this page and add this path to it.
    hr = xpsPage->GetVisuals( &pageVisuals );
    hr = pageVisuals->Append( rectPath );
    // If not needed for anything else, release the rectangle path.
    rectPath->Release();
    
    // When done with the visual collection, release it.
    pageVisuals->Release();

    // When finished with the brushes, release the interface pointers.
    if (NULL != xpsFillBrush) xpsFillBrush->Release();
    if (NULL != xpsStrokeBrush) xpsStrokeBrush->Release();

    // When done with the geometry interface, release it.
    imageRectGeometry->Release();

    // When done with the path interface, release it.
    rectPath->Release();

```



## <a name="best-practices"></a><span data-ttu-id="069ee-123">Bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="069ee-123">Best Practices</span></span>

<span data-ttu-id="069ee-124">Ajoutez une description textuelle de la forme spécifiée par l’interface [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) .</span><span class="sxs-lookup"><span data-stu-id="069ee-124">Add a textual description of the shape that is specified by the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface.</span></span> <span data-ttu-id="069ee-125">Pour les utilisateurs malvoyants, utilisez les méthodes [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) et [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) pour fournir du contenu textuel aux fonctionnalités de prise en charge de l’accessibilité, telles que les lecteurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="069ee-125">For the benefit of visually impaired users, use the [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) and [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) methods to provide textual content for accessibility support features, such as screen readers.</span></span>

## <a name="additional-information"></a><span data-ttu-id="069ee-126">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="069ee-126">Additional Information</span></span>

<span data-ttu-id="069ee-127">L’exemple de code sur cette page utilise une interface [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) comme pinceau de remplissage et pinceau de trait pour le tracé.</span><span class="sxs-lookup"><span data-stu-id="069ee-127">The code example on this page uses an [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) interface as the fill brush and stroke brush for the path.</span></span> <span data-ttu-id="069ee-128">En plus de l’interface **IXpsOMSolidColorBrush** , vous pouvez utiliser une interface [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)ou [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) .</span><span class="sxs-lookup"><span data-stu-id="069ee-128">In addition to the **IXpsOMSolidColorBrush** interface, you can use an [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush), or [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) interface.</span></span>

<span data-ttu-id="069ee-129">Le trait est la ligne qui peut être dessinée autour du périmètre de la figure.</span><span class="sxs-lookup"><span data-stu-id="069ee-129">The stroke is the line that can be drawn around the perimeter of the figure.</span></span> <span data-ttu-id="069ee-130">La [spécification Paper XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) prend en charge de nombreux styles de trait de trait différents.</span><span class="sxs-lookup"><span data-stu-id="069ee-130">The [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) supports many different stroke line styles.</span></span> <span data-ttu-id="069ee-131">Pour spécifier le style de trait, définissez les propriétés de trait à l’aide des méthodes suivantes de l’interface [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) :</span><span class="sxs-lookup"><span data-stu-id="069ee-131">To specify the stroke line style, set the stroke properties with the following methods of the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface:</span></span>

-   <span data-ttu-id="069ee-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) ou [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) pour définir le pinceau de trait</span><span class="sxs-lookup"><span data-stu-id="069ee-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) or [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) to set the stroke brush</span></span>
-   <span data-ttu-id="069ee-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) pour récupérer la collection de tirets du trait qui décrit les traits</span><span class="sxs-lookup"><span data-stu-id="069ee-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) to get the stroke dash collection that describes the strokes</span></span>
-   <span data-ttu-id="069ee-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) à et [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) pour décrire l’apparence d’un trait en pointillés</span><span class="sxs-lookup"><span data-stu-id="069ee-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) to and [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) to describe the appearance of a dashed stroke</span></span>
-   <span data-ttu-id="069ee-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) et [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) pour définir le style de fin de ligne</span><span class="sxs-lookup"><span data-stu-id="069ee-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) and [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) to define the line termination style</span></span>
-   <span data-ttu-id="069ee-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) et [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) pour décrire comment les segments sont joints</span><span class="sxs-lookup"><span data-stu-id="069ee-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) and [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) to describe how the segments are joined</span></span>
-   <span data-ttu-id="069ee-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) pour définir l’épaisseur du trait</span><span class="sxs-lookup"><span data-stu-id="069ee-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) to set the stroke thickness</span></span>

## <a name="related-topics"></a><span data-ttu-id="069ee-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="069ee-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="069ee-139">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="069ee-139">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="069ee-140">Naviguer dans le modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="069ee-140">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="069ee-141">Écrire du texte dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="069ee-141">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="069ee-142">Placer des images dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="069ee-142">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="069ee-143">Écrire un modèle OM XPS dans un document XPS</span><span class="sxs-lookup"><span data-stu-id="069ee-143">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="069ee-144">Imprimer un modèle OM XPS</span><span class="sxs-lookup"><span data-stu-id="069ee-144">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="069ee-145">**Utilisé dans cette page**</span><span class="sxs-lookup"><span data-stu-id="069ee-145">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="069ee-146">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="069ee-146">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="069ee-147">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="069ee-147">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[<span data-ttu-id="069ee-148">**IXpsOMGeometryFigure**</span><span class="sxs-lookup"><span data-stu-id="069ee-148">**IXpsOMGeometryFigure**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[<span data-ttu-id="069ee-149">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="069ee-149">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[<span data-ttu-id="069ee-150">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="069ee-150">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="069ee-151">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="069ee-151">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="069ee-152">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="069ee-152">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[<span data-ttu-id="069ee-153">**IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="069ee-153">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="069ee-154">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="069ee-154">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="069ee-155">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="069ee-155">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="069ee-156">Initialiser un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="069ee-156">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="069ee-157">Informations de référence sur l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="069ee-157">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="069ee-158">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="069ee-158">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

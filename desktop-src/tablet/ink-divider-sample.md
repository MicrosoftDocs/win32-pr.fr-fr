---
description: Cet exemple est basé sur l’exemple Ink collection. Il montre comment utiliser l’objet diviseur pour analyser l’entrée d’encre.
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: Exemple de diviseur d’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a272d6a5530938e6fecfeefc9f46ffdd0835d045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484377"
---
# <a name="ink-divider-sample"></a><span data-ttu-id="9fae4-104">Exemple de diviseur d’encre</span><span class="sxs-lookup"><span data-stu-id="9fae4-104">Ink Divider Sample</span></span>

<span data-ttu-id="9fae4-105">Cet exemple est basé sur l' [exemple Ink collection](ink-collection-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9fae4-105">This sample is based on the [Ink Collection Sample](ink-collection-sample.md).</span></span> <span data-ttu-id="9fae4-106">Il montre comment utiliser l’objet [diviseur](/previous-versions/ms839398(v=msdn.10)) pour analyser l’entrée d’encre.</span><span class="sxs-lookup"><span data-stu-id="9fae4-106">It shows how to use the [Divider](/previous-versions/ms839398(v=msdn.10)) object to analyze ink input.</span></span>

<span data-ttu-id="9fae4-107">Pour obtenir des informations conceptuelles détaillées sur le [séparateur](/previous-versions/ms839398(v=msdn.10)), consultez [l’objet diviseur](the-divider-object.md).</span><span class="sxs-lookup"><span data-stu-id="9fae4-107">For detailed conceptual information about [Divider](/previous-versions/ms839398(v=msdn.10)), see [The Divider Object](the-divider-object.md).</span></span>

<span data-ttu-id="9fae4-108">Quand le formulaire est mis à jour, l’échantillon dessine un rectangle englobant autour de chaque unité analysée, divisé en mots, lignes, paragraphes et dessins.</span><span class="sxs-lookup"><span data-stu-id="9fae4-108">When the form is updated, the sample draws a bounding rectangle around each analyzed unit, broken into words, lines, paragraphs, and drawings.</span></span> <span data-ttu-id="9fae4-109">Outre l’utilisation de différentes couleurs, ces rectangles sont agrandis par différents montants pour garantir qu’aucun rectangle n’est masqué par d’autres.</span><span class="sxs-lookup"><span data-stu-id="9fae4-109">Besides using different colors, these rectangles are enlarged by different amounts to ensure that none of the rectangles is obscured by others.</span></span> <span data-ttu-id="9fae4-110">Le tableau suivant spécifie la couleur et l’élargissement de chaque unité analysée.</span><span class="sxs-lookup"><span data-stu-id="9fae4-110">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="9fae4-111">Unité analysée</span><span class="sxs-lookup"><span data-stu-id="9fae4-111">analyzed Unit</span></span>        | <span data-ttu-id="9fae4-112">Couleur</span><span class="sxs-lookup"><span data-stu-id="9fae4-112">Color</span></span>              | <span data-ttu-id="9fae4-113">Agrandissement des pixels</span><span class="sxs-lookup"><span data-stu-id="9fae4-113">Pixel Enlargement</span></span> |
|----------------------|--------------------|-------------------|
| <span data-ttu-id="9fae4-114">Word</span><span class="sxs-lookup"><span data-stu-id="9fae4-114">Word</span></span><br/>      | <span data-ttu-id="9fae4-115">Vert</span><span class="sxs-lookup"><span data-stu-id="9fae4-115">Green</span></span><br/>   | <span data-ttu-id="9fae4-116">1</span><span class="sxs-lookup"><span data-stu-id="9fae4-116">1</span></span><br/>      |
| <span data-ttu-id="9fae4-117">Lignes</span><span class="sxs-lookup"><span data-stu-id="9fae4-117">Line</span></span><br/>      | <span data-ttu-id="9fae4-118">Magenta</span><span class="sxs-lookup"><span data-stu-id="9fae4-118">Magenta</span></span><br/> | <span data-ttu-id="9fae4-119">3</span><span class="sxs-lookup"><span data-stu-id="9fae4-119">3</span></span><br/>      |
| <span data-ttu-id="9fae4-120">Paragraph</span><span class="sxs-lookup"><span data-stu-id="9fae4-120">Paragraph</span></span><br/> | <span data-ttu-id="9fae4-121">Bleu</span><span class="sxs-lookup"><span data-stu-id="9fae4-121">Blue</span></span><br/>    | <span data-ttu-id="9fae4-122">5</span><span class="sxs-lookup"><span data-stu-id="9fae4-122">5</span></span><br/>      |
| <span data-ttu-id="9fae4-123">Dessin</span><span class="sxs-lookup"><span data-stu-id="9fae4-123">Drawing</span></span><br/>   | <span data-ttu-id="9fae4-124">Rouge</span><span class="sxs-lookup"><span data-stu-id="9fae4-124">Red</span></span><br/>     | <span data-ttu-id="9fae4-125">1</span><span class="sxs-lookup"><span data-stu-id="9fae4-125">1</span></span><br/>      |



 

## <a name="setting-up-the-form"></a><span data-ttu-id="9fae4-126">Configuration du formulaire</span><span class="sxs-lookup"><span data-stu-id="9fae4-126">Setting Up the Form</span></span>

<span data-ttu-id="9fae4-127">Lorsque le formulaire est chargé, un objet [diviseur](/previous-versions/ms839398(v=msdn.10)) est créé.</span><span class="sxs-lookup"><span data-stu-id="9fae4-127">When the form loads, a [Divider](/previous-versions/ms839398(v=msdn.10)) object is created.</span></span> <span data-ttu-id="9fae4-128">Un objet [InkOverlay](/previous-versions/ms833057(v=msdn.10)) est créé et associé à un panneau sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="9fae4-128">An [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object is created and associated with a panel on the form.</span></span> <span data-ttu-id="9fae4-129">Les gestionnaires d’événements sont ensuite attachés à l’objet InkOverlay pour suivre le moment où les traits sont ajoutés et supprimés.</span><span class="sxs-lookup"><span data-stu-id="9fae4-129">Then event handlers are attached to the InkOverlay object to track when strokes are added and deleted.</span></span> <span data-ttu-id="9fae4-130">Ensuite, si des détecteurs sont disponibles, un objet [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) pour le module de reconnaissance par défaut est assigné au diviseur.</span><span class="sxs-lookup"><span data-stu-id="9fae4-130">Then if recognizers are available, a [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) object for the default recognizer is assigned to the Divider.</span></span> <span data-ttu-id="9fae4-131">La propriété [LineHeight](/previous-versions/ms839409(v=msdn.10)) de l’objet de séparateur est ensuite définie et la collection [Strokes](/previous-versions/ms827799(v=msdn.10)) de l’objet InkOverlay est assignée au diviseur.</span><span class="sxs-lookup"><span data-stu-id="9fae4-131">Then the Divider object's [LineHeight](/previous-versions/ms839409(v=msdn.10)) property is set and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection from the InkOverlay object is assigned to the Divider.</span></span> <span data-ttu-id="9fae4-132">Enfin, l’objet InkOverlay est activé.</span><span class="sxs-lookup"><span data-stu-id="9fae4-132">Finally, the InkOverlay object is enabled.</span></span>


```C++
// Create the ink overlay and associate it with the form
myInkOverlay = new Microsoft.Ink.InkOverlay(DrawArea.Handle);

// Set the erasing mode to stroke erase.
myInkOverlay.EraserMode = InkOverlayEraserMode.StrokeErase;

// Hook event handler for the Stroke event to myInkOverlay_Stroke.
// This is necessary since the application needs to pass the strokes 
// to the ink divider.
myInkOverlay.Stroke += new InkCollectorStrokeEventHandler(myInkOverlay_Stroke); 

// Hook the event handler for StrokeDeleting event to myInkOverlay_StrokeDeleting.
// This is necessary as the application needs to remove the strokes from 
// ink divider object as well.
myInkOverlay.StrokesDeleting += new InkOverlayStrokesDeletingEventHandler(myInkOverlay_StrokeDeleting);

// Hook the event handler for StrokeDeleted event to myInkOverlay_StrokeDeleted.
// This is necessary to update the layout analysis result when automatic layout analysis
// option is selected.
myInkOverlay.StrokesDeleted += new InkOverlayStrokesDeletedEventHandler(myInkOverlay_StrokeDeleted);

// Create the ink divider object
myInkDivider = new Divider();

// Add a default recognizer context to the divider object
// without adding the recognizer context, the divider would
// not use a recognizer to do its word segmentation and would
// have less accurate results.
// Adding the recognizer context slows down the call to 
// myInkDivider.Divide though.
// It is possible that there is no recognizer installed on the
// machine for this language. In that case the divider does
// not use a recognizer to improve its accuracy.
// Get the default recognizer if any
try
{
    Recognizers recognizers = new Recognizers();
     myInkDivider.RecognizerContext = recognizers.GetDefaultRecognizer().CreateRecognizerContext();
}
catch (InvalidOperationException)
{
     //We are in the case where no default recognizers can be found
}

    // The LineHeight property helps the InkDivider distinguish between 
    // drawing and handwriting. The value should be the expected height 
    // of the user's handwriting in ink space units (0.01mm).
    // Here we set the LineHeight to 840, which is about 1/3 of an inch.
    myInkDivider.LineHeight = 840;

// Assign ink overlay's strokes collection to the ink divider
// This strokes collection is updated in the event handler
myInkDivider.Strokes = myInkOverlay.Ink.Strokes;

// Enable ink collection
myInkOverlay.Enabled = true;
```



<span data-ttu-id="9fae4-133">La collection [Strokes](/previous-versions/ms839422(v=msdn.10)) de l’objet de [séparateur](/previous-versions/ms839398(v=msdn.10)) doit être maintenue synchronisée avec la collection [Strokes](/previous-versions/ms827799(v=msdn.10)) de l’objet [InkOverlay](/previous-versions/ms833057(v=msdn.10)) (accessible via la propriété [Ink](/previous-versions/ms833110(v=msdn.10)) de l’objet InkOverlay).</span><span class="sxs-lookup"><span data-stu-id="9fae4-133">The [Divider](/previous-versions/ms839398(v=msdn.10)) object's [Strokes](/previous-versions/ms839422(v=msdn.10)) collection must be kept in sync with the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Strokes](/previous-versions/ms827799(v=msdn.10)) collection (accessed through the InkOverlay object's [Ink](/previous-versions/ms833110(v=msdn.10)) property).</span></span> <span data-ttu-id="9fae4-134">Pour vous assurer que cela se produit, le gestionnaire d’événements [Stroke](/previous-versions/ms835344(v=msdn.10)) pour l’objet InkOverlay est écrit comme suit.</span><span class="sxs-lookup"><span data-stu-id="9fae4-134">To ensure that this happens, the [Stroke](/previous-versions/ms835344(v=msdn.10)) event handler for the InkOverlay object is written as follows.</span></span> <span data-ttu-id="9fae4-135">Notez que le gestionnaire d’événements effectue d’abord un test pour voir si le [EditingMode](/previous-versions/ms833105(v=msdn.10)) est défini sur **Ink** pour filtrer les traits de gomme.</span><span class="sxs-lookup"><span data-stu-id="9fae4-135">Note that the event handler first tests to see if the [EditingMode](/previous-versions/ms833105(v=msdn.10)) is set to **Ink** to filter out eraser strokes.</span></span> <span data-ttu-id="9fae4-136">Si l’utilisateur a demandé une analyse de la disposition automatique, l’application appelle la méthode DivideInk du formulaire et actualise la zone de dessin.</span><span class="sxs-lookup"><span data-stu-id="9fae4-136">If the user has requested automatic layout analysis, then the application calls the form's DivideInk method and refreshes the drawing area.</span></span>


```C++
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e )
{
    // Filter out the eraser stroke.
    if(InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
    {
        // Add the new stroke to the ink divider's strokes collection
        myInkDivider.Strokes.Add(e.Stroke);
        
        if(miAutomaticLayoutAnalysis.Checked)
        {
            // Call DivideInk
            DivideInk();

            // Repaint the screen to reflect the change
            DrawArea.Refresh();
        }
    }
}
```



## <a name="dividing-the-ink"></a><span data-ttu-id="9fae4-137">Division de l’encre</span><span class="sxs-lookup"><span data-stu-id="9fae4-137">Dividing the Ink</span></span>

<span data-ttu-id="9fae4-138">Quand l’utilisateur clique sur diviser dans le menu fichier, la méthode [Divide](/previous-versions/ms839461(v=msdn.10)) est appelée sur l’objet [diviseur](/previous-versions/ms839398(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="9fae4-138">When the user clicks Divide on the File menu, the [Divide](/previous-versions/ms839461(v=msdn.10)) method is called on the [Divider](/previous-versions/ms839398(v=msdn.10)) object.</span></span> <span data-ttu-id="9fae4-139">Le module de reconnaissance par défaut est utilisé, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="9fae4-139">The default recognizer is used, if available.</span></span>


```C++
DivisionResult divResult = myInkDivider.Divide();
```



<span data-ttu-id="9fae4-140">L’objet [DivisionResult](/previous-versions/ms839371(v=msdn.10)) résultant, référencé par la variable `divResult` , est passé à une fonction utilitaire, `getUnitBBBoxes()` .</span><span class="sxs-lookup"><span data-stu-id="9fae4-140">The resulting [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object, referenced by the variable `divResult`, is passed to a utility function, `getUnitBBBoxes()`.</span></span> <span data-ttu-id="9fae4-141">La fonction utilitaire retourne un tableau de rectangles pour n’importe quel type de division demandé : segments, lignes, paragraphes ou dessins.</span><span class="sxs-lookup"><span data-stu-id="9fae4-141">The utility function returns an array of rectangles for whatever division type is requested: segments, lines, paragraphs, or drawings.</span></span>


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



<span data-ttu-id="9fae4-142">Enfin, le panneau de formulaire est forcé à redessiner afin que les rectangles englobants apparaissent.</span><span class="sxs-lookup"><span data-stu-id="9fae4-142">Finally, the form panel is forced to redraw so that the bounding rectangles appear.</span></span>


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a><span data-ttu-id="9fae4-143">Résultats de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="9fae4-143">Ink Analysis Results</span></span>

<span data-ttu-id="9fae4-144">Dans la fonction utilitaire, l’objet [DivisionResult](/previous-versions/ms839371(v=msdn.10)) est interrogé pour obtenir ses résultats à l’aide de la méthode [ResultByType](/previous-versions/ms839388(v=msdn.10)) , en fonction du type de division demandé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9fae4-144">In the utility function, the [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object is queried for its results by using the [ResultByType](/previous-versions/ms839388(v=msdn.10)) method, based on the division type requested by the caller.</span></span> <span data-ttu-id="9fae4-145">La méthode ResultByType retourne une collection [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="9fae4-145">The ResultByType method returns a [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) collection.</span></span> <span data-ttu-id="9fae4-146">Chaque [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) de la collection représente un dessin, un segment unique de reconnaissance de l’écriture manuscrite, une ligne d’écriture manuscrite ou un bloc d’écriture, en fonction de ce qui a été spécifié lors de l’appel de la fonction utilitaire.</span><span class="sxs-lookup"><span data-stu-id="9fae4-146">Each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) in the collection represents a drawing, a single recognition segment of handwriting, a line of handwriting, or a block of handwriting, depending upon what was specified when the utility function was called.</span></span>


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



<span data-ttu-id="9fae4-147">S’il existe au moins un [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), un tableau de rectangles est créé, contenant un rectangle englobant par unité.</span><span class="sxs-lookup"><span data-stu-id="9fae4-147">If there is at least one [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), an array of rectangles is created containing one bounding rectangle per unit.</span></span> <span data-ttu-id="9fae4-148">(Les rectangles sont gonflés par des montants différents pour chaque type d’unité, conservé dans la variable de gonflage, pour empêcher le chevauchement).</span><span class="sxs-lookup"><span data-stu-id="9fae4-148">(The rectangles are inflated by differing amounts for each type of unit, held in the inflate variable, to prevent overlapping.)</span></span>


```C++
// If there is at least one unit, we construct the rectangles
if((null != units) && (0 < units.Count))
{
    // We need to convert rectangles from ink units to
    // pixel units. For that, we need Graphics object
    // to pass to InkRenderer.InkSpaceToPixel method
    using (Graphics g = DrawArea.CreateGraphics())
    {

    // InkSpace to Pixel Space conversion setup done here. 
    // Not shown for brevity.

        // Iterate through the collection of division units to obtain the bounding boxes
        foreach(DivisionUnit unit in units)
        {
            // Get the bounding box of the strokes of the division unit
            divRects[i] = unit.Strokes.GetBoundingBox();

            // Div unit rect Ink space to Pixel space conversion done here. 
            // Not shown for brevity.

            // Inflate the rectangle by inflate pixels in both directions
            divRects[i].Inflate(inflate, inflate);

            // Increment the index
            ++i;
        }

    } // Relinquish the Graphics object
}
```



## <a name="redrawing-the-form"></a><span data-ttu-id="9fae4-149">Redessiner le formulaire</span><span class="sxs-lookup"><span data-stu-id="9fae4-149">Redrawing the Form</span></span>

<span data-ttu-id="9fae4-150">Lorsque le redessin est forcé ci-dessus, le code suivant s’exécute pour peindre les zones englobantes pour chaque [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) du formulaire autour de l’encre.</span><span class="sxs-lookup"><span data-stu-id="9fae4-150">When the redraw is forced above, the following code executes to paint the bounding boxes for each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) on the form around the ink.</span></span>


```C++
private void DrawArea_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
        {
            // Create the Pen used to draw bounding boxes.
            // First set of bounding boxes drawn here are 
            // the bounding boxes of paragraphs.
            // These boxes are drawn with Blue pen.
            Pen penBox = new Pen(Color.Blue, 2);

            // First, draw the bounding boxes for Paragraphs
            if(null != myParagraphBoundingBoxes)
            {
                // Draw bounding boxes for Paragraphs
                e.Graphics.DrawRectangles(penBox, myParagraphBoundingBoxes);
            }

            // Next, draw the bounding boxes for Lines
            if(null != myLineBoundingBoxes)
            {
                // Color is Magenta pen
                penBox.Color = Color.Magenta;
                // Draw the bounding boxes for Lines
                e.Graphics.DrawRectangles(penBox, myLineBoundingBoxes);
            }
            
            // Then, draw the bounding boxes for Words
            if(null != myWordBoundingBoxes)
            {
                // Color is Green
                penBox.Color = Color.Green;
                // Draw bounding boxes for Words
                e.Graphics.DrawRectangles(penBox, myWordBoundingBoxes);
            }
            
            // Finally, draw the boxes for Drawings
            if(null != myDrawingBoundingBoxes)
            {
                // Color is Red pen
                penBox.Color = Color.Red;
                // Draw bounding boxes for Drawings
                e.Graphics.DrawRectangles(penBox, myDrawingBoundingBoxes);
            }
        }
```



## <a name="closing-the-form"></a><span data-ttu-id="9fae4-151">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="9fae4-151">Closing the Form</span></span>

<span data-ttu-id="9fae4-152">La méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire supprime les objets [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [diviseur](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) et les [traits](/previous-versions/ms827799(v=msdn.10)) utilisés dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9fae4-152">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [Divider](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) objects and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection used in the sample.</span></span>

 


---
description: Cet exemple est basé sur l’exemple Ink collection. Il montre comment utiliser l’objet diviseur pour analyser l’entrée d’encre.
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: Exemple de diviseur d’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c74592606ba98ec913dd419deda1b2b766066e17545e95f18a14980f36dafde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452096"
---
# <a name="ink-divider-sample"></a>Exemple de diviseur d’encre

Cet exemple est basé sur l' [exemple Ink collection](ink-collection-sample.md). Il montre comment utiliser l’objet [diviseur](/previous-versions/ms839398(v=msdn.10)) pour analyser l’entrée d’encre.

Pour obtenir des informations conceptuelles détaillées sur le [séparateur](/previous-versions/ms839398(v=msdn.10)), consultez [l’objet diviseur](the-divider-object.md).

Quand le formulaire est mis à jour, l’échantillon dessine un rectangle englobant autour de chaque unité analysée, divisé en mots, lignes, paragraphes et dessins. Outre l’utilisation de différentes couleurs, ces rectangles sont agrandis par différents montants pour garantir qu’aucun rectangle n’est masqué par d’autres. Le tableau suivant spécifie la couleur et l’élargissement de chaque unité analysée.



| Unité analysée        | Couleur              | Agrandissement des pixels |
|----------------------|--------------------|-------------------|
| Word<br/>      | Vert<br/>   | 1<br/>      |
| Ligne<br/>      | Magenta<br/> | 3<br/>      |
| Paragraph<br/> | Bleu<br/>    | 5<br/>      |
| Dessin<br/>   | Rouge<br/>     | 1<br/>      |



 

## <a name="setting-up-the-form"></a>Configuration du formulaire

Lorsque le formulaire est chargé, un objet [diviseur](/previous-versions/ms839398(v=msdn.10)) est créé. Un objet [InkOverlay](/previous-versions/ms833057(v=msdn.10)) est créé et associé à un panneau sur le formulaire. Les gestionnaires d’événements sont ensuite attachés à l’objet InkOverlay pour suivre le moment où les traits sont ajoutés et supprimés. Ensuite, si des détecteurs sont disponibles, un objet [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) pour le module de reconnaissance par défaut est assigné au diviseur. La propriété [LineHeight](/previous-versions/ms839409(v=msdn.10)) de l’objet de séparateur est ensuite définie et la collection [Strokes](/previous-versions/ms827799(v=msdn.10)) de l’objet InkOverlay est assignée au diviseur. Enfin, l’objet InkOverlay est activé.


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



La collection [Strokes](/previous-versions/ms839422(v=msdn.10)) de l’objet de [séparateur](/previous-versions/ms839398(v=msdn.10)) doit être maintenue synchronisée avec la collection [Strokes](/previous-versions/ms827799(v=msdn.10)) de l’objet [InkOverlay](/previous-versions/ms833057(v=msdn.10)) (accessible via la propriété [Ink](/previous-versions/ms833110(v=msdn.10)) de l’objet InkOverlay). Pour vous assurer que cela se produit, le gestionnaire d’événements [Stroke](/previous-versions/ms835344(v=msdn.10)) pour l’objet InkOverlay est écrit comme suit. Notez que le gestionnaire d’événements effectue d’abord un test pour voir si le [EditingMode](/previous-versions/ms833105(v=msdn.10)) est défini sur **Ink** pour filtrer les traits de gomme. Si l’utilisateur a demandé une analyse de la disposition automatique, l’application appelle la méthode DivideInk du formulaire et actualise la zone de dessin.


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



## <a name="dividing-the-ink"></a>Division de l’encre

Quand l’utilisateur clique sur diviser dans le menu fichier, la méthode [Divide](/previous-versions/ms839461(v=msdn.10)) est appelée sur l’objet [diviseur](/previous-versions/ms839398(v=msdn.10)) . Le module de reconnaissance par défaut est utilisé, s’il est disponible.


```C++
DivisionResult divResult = myInkDivider.Divide();
```



L’objet [DivisionResult](/previous-versions/ms839371(v=msdn.10)) résultant, référencé par la variable `divResult` , est passé à une fonction utilitaire, `getUnitBBBoxes()` . La fonction utilitaire retourne un tableau de rectangles pour n’importe quel type de division demandé : segments, lignes, paragraphes ou dessins.


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



Enfin, le panneau de formulaire est forcé à redessiner afin que les rectangles englobants apparaissent.


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a>Résultats de l’analyse de l’encre

Dans la fonction utilitaire, l’objet [DivisionResult](/previous-versions/ms839371(v=msdn.10)) est interrogé pour obtenir ses résultats à l’aide de la méthode [ResultByType](/previous-versions/ms839388(v=msdn.10)) , en fonction du type de division demandé par l’appelant. La méthode ResultByType retourne une collection [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) . Chaque [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) de la collection représente un dessin, un segment unique de reconnaissance de l’écriture manuscrite, une ligne d’écriture manuscrite ou un bloc d’écriture, en fonction de ce qui a été spécifié lors de l’appel de la fonction utilitaire.


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



S’il existe au moins un [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), un tableau de rectangles est créé, contenant un rectangle englobant par unité. (Les rectangles sont gonflés par des montants différents pour chaque type d’unité, conservé dans la variable de gonflage, pour empêcher le chevauchement).


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



## <a name="redrawing-the-form"></a>Redessiner le formulaire

Lorsque le redessin est forcé ci-dessus, le code suivant s’exécute pour peindre les zones englobantes pour chaque [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) du formulaire autour de l’encre.


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



## <a name="closing-the-form"></a>Fermeture du formulaire

La méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire supprime les objets [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [diviseur](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) et les [traits](/previous-versions/ms827799(v=msdn.10)) utilisés dans l’exemple.

 


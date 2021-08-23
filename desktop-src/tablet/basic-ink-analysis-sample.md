---
description: L’exemple Basic Ink Analysis montre comment la classe InkAnalyzer divise l’écriture manuscrite en plusieurs segments de mots et de dessins. Cet exemple est une version mise à jour de l’exemple de diviseur d’encre.
ms.assetid: cb9a28d9-f8c6-478e-ae43-2d30106edc7b
title: Exemple d’analyse de base de l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ab307deac8ac58a741b0c7f332986b09074f4f5c6a8afa53f0156a94916bf16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660829"
---
# <a name="basic-ink-analysis-sample"></a>Exemple d’analyse de base de l’encre

L’exemple Basic Ink Analysis montre comment la classe [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) divise l’écriture manuscrite en plusieurs segments de mots et de dessins.

Cet exemple est une version mise à jour de l' [exemple de diviseur d’encre](ink-divider-sample.md). Tandis que l’exemple Ink diviseur utilise la classe [diviseur](/previous-versions/ms839398(v=msdn.10)) , cet exemple utilise l’API InkAnalysis plus récente et préférée. L’API InkAnalysis combine le [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) et le diviseur en une seule API et développe les fonctionnalités des deux.

Lorsque vous mettez à jour le formulaire, l’échantillon dessine un rectangle autour de chaque unité analysée : mots, lignes, paragraphes, régions d’écriture, dessins et puces. Le formulaire utilise des couleurs différentes pour les différentes unités. Les rectangles sont également agrandis par différents montants pour garantir qu’aucun rectangle n’est obscurci par d’autres.

Le tableau suivant spécifie la couleur et l’élargissement de chaque unité analysée.



| Unité analysée             | Couleur du rectangle | Agrandissement des rectangles (pixels) |
|---------------------------|--------------------|--------------------------------|
| Word<br/>           | Vert<br/>   | 1<br/>                   |
| Ligne<br/>           | Magenta<br/> | 3<br/>                   |
| Paragraph<br/>      | Bleu<br/>    | 5<br/>                   |
| Région d’écriture<br/> | Yellow<br/>  | 7<br/>                   |
| Dessin<br/>        | Rouge<br/>     | 1<br/>                   |
| Sélectionnées<br/>         | Orange<br/>  | 1<br/>                   |



 

Vous pouvez effacer les traits dans le formulaire. Dans l’exemple d’application, vous pouvez basculer entre l’écriture manuscrite et le mode d’effacement pour modifier la fonction du stylet.


```C++
        private void miInk_Click(object sender, System.EventArgs e)
        {
            // Turn on the inking mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Ink;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = true;
            miErase.Checked = false;

            // Update the UI
            this.Refresh();
        }

        private void miErase_Click(object sender, System.EventArgs e)
        {
            // Turn on the ink deletion mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Delete;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = false;
            miErase.Checked = true;

            // Update the UI
            this.Refresh();
        }
```



Lorsque vous ajoutez ou supprimez des traits, l’exemple met à jour le [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).


```C++
        private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
        {
            // Filter out the eraser stroke.
            if (InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
            {

                // Add the new stroke to the InkAnalyzer's stroke collection
                myInkAnalyzer.AddStroke(e.Stroke);

                if (miAutomaticLayoutAnalysis.Checked)
                {
                    // Invoke an analysis operation on the background thread
                    myInkAnalyzer.BackgroundAnalyze();
                }
            }
        }

        void myInkOverlay_StrokeDeleting(object sender, InkOverlayStrokesDeletingEventArgs e)
        {
            // Remove the strokes to be deleted from the InkAnalyzer's stroke collection
            myInkAnalyzer.RemoveStrokes(e.StrokesToDelete);

            // If automatic layout analysis is turned on, analyze the ink on the background thread
            if ( miAutomaticLayoutAnalysis.Checked )
            {
                // Invoke an analysis operation on the background thread
                myInkAnalyzer.BackgroundAnalyze ( );
            }
        }
```



Notez que dans le menu mode, l’analyse de la disposition automatique est activée par défaut. Lorsque cette option est sélectionnée, les gestionnaires d’événements [Stroke](/previous-versions/ms835344(v=msdn.10)) et [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) de l’objet [InkOverlay](/previous-versions/ms833057(v=msdn.10)) appellent la méthode [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) à chaque fois qu’un trait est créé ou supprimé.

> [!Note]  
> L’appel de la méthode [analyze](/previous-versions/ms568971(v=vs.100)) de l’objet [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) avec plus de quelques traits présents crée un retard notable dans une application. Cela est dû au fait que l’analyse est une opération d’analyse d’encre synchrone. Dans la pratique, appelez la méthode Analyze uniquement lorsque vous avez besoin du résultat. Sinon, utilisez la méthode [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) asynchrone, comme indiqué dans l’exemple.

 

## <a name="handling-the-analysis-results"></a>Gestion des résultats de l’analyse

L’exemple crée deux tableaux pour contenir les différents rectangles, qu’ils soient horizontaux ou pivotés. Utilisez un rectangle englobant pivoté pour obtenir l’angle d’écriture d’une ligne de mots. L’exemple montre les propriétés retournées par le [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) et affiche le cadre englobant ou le rectangle englobant pivoté (en fonction de la sélection du menu).


```C++
      private Rectangle[] GetHorizontalBBoxes(Guid nodeType, int inflate)
        {
            // Declare the array of rectangles to hold the result
            Rectangle[] analysisRects;

            // Get the division units from the division result of division type
            ContextNodeCollection nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // If there is at least one unit, we construct the rectangles
            if ((null != nodes) && (0 < nodes.Count))
            {
                // We need to convert rectangles from ink units to
                // pixel units. For that, we need Graphics object
                // to pass to InkRenderer.InkSpaceToPixel method
                using (Graphics g = drawArea.CreateGraphics())
                {
                    // Construct the rectangles
                    analysisRects = new Rectangle[nodes.Count];

                    // InkRenderer.InkSpaceToPixel takes Point as parameter. 
                    // Create two Point objects to point to (Top, Left) and
                    // (Width, Height) properties of rectangle. (Width, Height)
                    // is used instead of (Right, Bottom) because (Right, Bottom)
                    // are read-only properties on Rectangle
                    Point ptLocation = new Point();
                    Point ptSize = new Point();

                    // Index into the bounding boxes
                    int i = 0;

                    // Iterate through the collection of division units to obtain the bounding boxes
                    foreach (ContextNode node in nodes)
                    {
                        // Get the bounding box of the strokes of the division unit
                        analysisRects[i] = node.Location.GetBounds();

                        // The bounding box is in ink space unit. Convert them into pixel unit. 
                        ptLocation = analysisRects[i].Location;
                        ptSize.X = analysisRects[i].Width;
                        ptSize.Y = analysisRects[i].Height;

                        // Convert the Location from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptLocation);

                        // Convert the Size from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptSize);

                        // Assign the result back to the corresponding properties
                        analysisRects[i].Location = ptLocation;
                        analysisRects[i].Width = ptSize.X;
                        analysisRects[i].Height = ptSize.Y;

                        // Inflate the rectangle by inflate pixels in both directions
                        analysisRects[i].Inflate(inflate, inflate);

                        // Increment the index
                        ++i;
                    }

                } // Relinquish the Graphics object
            }
            else
            {
                // Otherwise we return null
                analysisRects = null;
            }

            // Return the Rectangle[] object
            return analysisRects;
        }

        private System.Collections.ArrayList GetRotatedBBoxes(Guid nodeType, int inflate)
        {
            //Find the correct collection of results nodes.
            ContextNodeCollection Nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // Declare the array list to hold the results; 
            // This array represents the four points of a rectangle, with the first point
            // copied again to complete the cycle of points.

            ArrayList polygonPoints = new ArrayList(Nodes.Count);

            // Cycle through each results node, get and convert the
            // rotated bounding box points
            foreach (ContextNode node in Nodes)
            {
                //Declare the point array
                Point[] rotatedBoundingBox = null;

                //Switch on the type of ContextNode to cast into the
                //appropriate type.  This is required to access the 
                //type specific property "RotatedBoundingBox" which
                //is not found on all ContextNode types.
                if (nodeType == ContextNodeType.InkWord)
                {
                    rotatedBoundingBox = ((InkWordNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Line)
                {
                    rotatedBoundingBox = ((LineNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Paragraph)
                {
                    rotatedBoundingBox = ((ParagraphNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.WritingRegion ||
                         nodeType == ContextNodeType.InkDrawing ||
                         nodeType == ContextNodeType.InkBullet )
                {

                    // Rotated Bounding Boxes are not a supported option for 
                    // Writing Regions or Drawings.  We return the axis aligned 
                    // bounding box instead
                    Rectangle rect = node.Location.GetBounds();

                    // We need to create a looped list of 4 points to be consistent
                    // with the way InkAnalysis represents rotated bounding boxes.  
                    rotatedBoundingBox = new Point[4];

                    rotatedBoundingBox[0] = new Point(rect.X, rect.Y);
                    rotatedBoundingBox[1] = new Point(rect.Right, rect.Y);
                    rotatedBoundingBox[2] = new Point(rect.Right, rect.Bottom);
                    rotatedBoundingBox[3] = new Point(rect.X, rect.Bottom);

                }


                if (null != rotatedBoundingBox)
                {
                    // We need to convert rectangles from ink units to
                    // pixel units. For that, we need Graphics object
                    // to pass to InkRenderer.InkSpaceToPixel method
                    using (Graphics g = drawArea.CreateGraphics())
                    {
                        // convert each of the points from ink space to pixel space
                        for (int i = 0; i < rotatedBoundingBox.Length; i++)
                        {
                            myInkOverlay.Renderer.InkSpaceToPixel(g, ref rotatedBoundingBox[i]);
                        }

                        //inflate the points by calling helper method
                        InflateHelperMethod(ref rotatedBoundingBox, inflate);

                        // increment the node portion of the polygonPoints array
                        polygonPoints.Add(rotatedBoundingBox);
                    }
                }
            }
            //Return the results
            return polygonPoints;
        }
```



L’analyseur calcule les [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) lors de l’analyse. Vous pouvez accéder aux informations à partir des zones englobantes pivotées de votre application pour plusieurs raisons utiles :

-   Détectez ou dessinez les limites d’une seule ligne, d’un paragraphe ou d’une autre unité.
-   Détermine l’angle d’écriture d’une ligne ou d’un paragraphe.
-   Implémentez des fonctionnalités telles que la sélection d’une ligne, d’un paragraphe ou d’une autre unité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Reconnaissance de base et analyse de l’encre](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[Exemple de formulaire papier numérisé](scanned-paper-form-sample.md)
</dt> <dt>

[Exemple de diviseur d’encre](ink-divider-sample.md)
</dt> </dl>

 


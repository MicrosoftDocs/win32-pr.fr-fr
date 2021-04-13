---
description: Ce programme montre comment copier et coller de l’encre dans une autre application. Elle permet également à l’utilisateur de copier une sélection de traits et de coller le résultat dans l’objet Ink existant.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Exemple de presse-papiers Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525971"
---
# <a name="ink-clipboard-sample"></a>Exemple de presse-papiers Ink

Ce programme montre comment copier et coller de l’encre dans une autre application. Elle permet également à l’utilisateur de copier une sélection de traits et de coller le résultat dans l’objet Ink existant.

Les modes de presse-papiers suivants sont disponibles :

-   ISF (Ink Serialized Format)
-   Métafichiers
-   métafichier amélioré (EMF)
-   Bitmap
-   Texte manuscrit
-   Esquisser l’encre

L’encre de texte et l’écriture manuscrite sont deux types de contrôles manuscrits utilisés respectivement comme texte ou dessin. Il est possible de coller de la Ink, de l’encre du texte et d’esquisser de l’encre dans l’encre existante.

En plus du presse-papiers, cet exemple montre également comment sélectionner des traits avec l’outil lasso. L’utilisateur peut déplacer les traits sélectionnés et modifier leurs attributs de dessin. Cette fonctionnalité est un sous-ensemble de la fonctionnalité de sélection déjà fournie par le contrôle d’incrustation d’encre. elle est implémentée ici à des fins d’illustration.

Les fonctionnalités suivantes sont utilisées dans cet exemple :

-   Objet [InkCollector](/previous-versions/ms583683(v=vs.100)) .
-   Prise en charge du presse-papiers Ink.
-   Utilisation du lasso avec la méthode [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) .

Cet exemple illustre le rendu de l’encre, la copie de cette encre, puis le collage de l’encre dans une autre application telle que Microsoft Paint.

## <a name="collecting-ink-and-setting-up-the-form"></a>Collecte de l’encre et configuration du formulaire

Tout d’abord, référencez les interfaces d’automatisation Tablet PC, qui sont installées avec le <entity type="reg"/> Kit de développement logiciel (SDK) de Microsoft Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



Ensuite, le formulaire déclare des constantes et des champs notés plus loin dans cet exemple.


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



Enfin, dans le gestionnaire d’événements [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire, le formulaire est initialisé, un objet [InkCollector](/previous-versions/ms583683(v=vs.100)) pour le formulaire est créé et le collecteur d’entrée manuscrite est activé.


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a>Gestion des événements de menu

Les gestionnaires d’événements d’élément de menu mettent essentiellement à jour l’état du formulaire.

La commande Clear supprime le rectangle de sélection et supprime les traits de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) du collecteur d’encre.

La commande exit désactive le collecteur d’encres avant de quitter l’application.

Le menu Edition active les commandes Couper et copier en fonction de l’état de sélection du formulaire, et active la commande Coller en fonction du contenu du presse-papiers, déterminé à l’aide de la méthode [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) .

Les commandes Couper et copier utilisent toutes les deux une méthode d’assistance pour copier l’encre dans le presse-papiers. La commande Cut utilise une méthode d’assistance pour supprimer les traits sélectionnés.

La commande Coller vérifie d’abord la méthode [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) pour déterminer si l’objet dans le presse-papiers peut être collé. La commande Coller calcule ensuite l’angle supérieur gauche de la zone de collage, convertit les coordonnées de pixels en espace d’encre, puis colle les traits du presse-papiers dans le collecteur d’encre. Enfin, la zone de sélection est mise à jour.


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



Les commandes SELECT et Ink mettent à jour le mode d’application et les attributs de dessin par défaut, effacent la sélection actuelle, mettent à jour l’état du menu et actualisent le formulaire. D’autres gestionnaires s’appuient sur l’état de l’application pour exécuter la fonction correcte, par le biais du lasso ou pour la disposition de l’encre. En outre, la commande SELECT ajoute les gestionnaires d’événements [NewPackets](/previous-versions/ms567621(v=vs.100)) et [Stroke](/previous-versions/ms567622(v=vs.100)) au collecteur d’encre et la commande Ink supprime ces gestionnaires d’événements du collecteur d’encre.

Les formats disponibles dans le presse-papiers lorsque les traits sont copiés sont répertoriés dans le menu Format, et l’utilisateur sélectionne le format de copie de l’encre dans cette liste. Les types de formats disponibles incluent Ink Serialized Format (ISF), Metafile, Enhanced Metafile et bitmap. Les formats d’encre et de texte d’esquisse s’excluent mutuellement et s’appuient sur l’encre copiée dans le presse-papiers en tant qu’objet OLE.

Le menu style permet à l’utilisateur de modifier les propriétés de couleur et de largeur du stylet et des traits sélectionnés.

Par exemple, la commande Red définit la propriété [Color](/previous-versions/ms582103(v=vs.100)) de la propriété [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) du collecteur d’encre sur la couleur rouge. Étant donné que la propriété [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) de l’objet [Cursor](/previous-versions/ms552104(v=vs.100)) n’a pas été définie, toute nouvelle encre dessinée sur le collecteur d’encre hérite de la couleur de dessin par défaut. En outre, si des traits sont actuellement sélectionnés, la propriété couleur des attributs de dessin de chaque trait est également mise à jour.


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a>Gestion des événements de souris

Le gestionnaire d’événements [MouseMove](/previous-versions/ms567617(v=vs.100)) vérifie le mode d’application. Si le mode est MoveInk et qu’un bouton de la souris est enfoncé, le gestionnaire déplace les traits à l’aide de la méthode Move de la collection [Strokes](/previous-versions/ms552701(v=vs.100)) et met à jour la zone de sélection. Dans le cas contraire, le gestionnaire vérifie si le rectangle de sélection contient le curseur, active la collecte d’encre en conséquence et définit également le curseur en conséquence.

Le gestionnaire d’événements [MouseDown](/previous-versions/ms567616(v=vs.100)) vérifie le paramètre de curseur. Si le curseur est défini sur [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), le gestionnaire définit le mode d’application sur MoveInk et enregistre l’emplacement du curseur. Sinon, si une sélection est en cours, effacez-la.

Le gestionnaire d’événements [MouseUp](/previous-versions/ms567618(v=vs.100)) vérifie le mode d’application. Si le mode est MoveInk, le gestionnaire définit le mode d’application en fonction de l’état activé de la commande SELECT.

L’événement [NewPackets](/previous-versions/ms567621(v=vs.100)) est déclenché en mode de sélection lorsque le collecteur d’encre reçoit de nouvelles données de paquets. Si l’application est en mode de sélection, il est nécessaire d’intercepter les nouveaux paquets et de les utiliser pour dessiner le lasso de sélection.

La coordonnée de chaque paquet est convertie en pixels, restreinte à la zone de dessin et ajoutée à la collection de points du lasso. Une méthode d’assistance est ensuite appelée pour dessiner le lasso sur le formulaire.

## <a name="handling-a-new-stroke"></a>Gestion d’un nouveau trait

L’événement [Stroke](/previous-versions/ms567622(v=vs.100)) est déclenché dans le mode de sélection lorsqu’un nouveau trait est dessiné. Si l’application est en mode de sélection, ce trait correspond au lasso et il est nécessaire de mettre à jour les informations des traits sélectionnés.

Le gestionnaire annule l’événement [Stroke](/previous-versions/ms567622(v=vs.100)) , vérifie plus de deux points de lasso, copie la collection points dans un tableau d’objets [point](/dotnet/api/system.drawing.point?view=netcore-3.1) et convertit les coordonnées des points du tableau de pixels en espace d’encre. Ensuite, le gestionnaire utilise la méthode [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) pour récupérer les traits sélectionnés par les points du lasso et met à jour l’état de sélection du formulaire. Enfin, le trait qui a déclenché l’événement est supprimé de la collection de traits sélectionnés, la collection de points de lasso est vidée et une méthode d’assistance dessine le rectangle de sélection.


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a>Copie de l’encre dans le presse-papiers

La méthode d’assistance CopyInkToClipboard crée une valeur [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) , vérifie l’état du menu Format pour mettre à jour les formats à placer dans le presse-papiers et utilise la méthode [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) pour copier les traits dans le presse-papiers.


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a>Mise à jour d’une sélection

La méthode d’assistance SetSelection met à jour la selectedStrokes déposée et, si la collection est **null** ou **vide**, le rectangle de sélection est défini sur le rectangle vide. Si la collection [Strokes](/previous-versions/ms552701(v=vs.100)) sélectionnée n’est pas vide, la méthode SetSelection effectue les étapes suivantes :

-   Détermine le rectangle englobant à l’aide de la méthode [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) de la collection Strokes
-   Convertit les coordonnées des rectangles de l’espace d’encre en pixels
-   Augmente le rectangle pour fournir un espace visuel entre celui-ci et les traits sélectionnés
-   Crée des poignées de sélection pour la zone de sélection actuelle

Enfin, la méthode SetSelection définit la visibilité des poignées de sélection et définit la propriété [AutoRedraw](/previous-versions/ms571706(v=vs.100)) du collecteur d’encre sur **false**, si les traits sont sélectionnés.


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a>Dessin du lasso

Le lasso est dessiné sous la forme d’une série de points ouverts qui suivent le tracé du trait du lasso et une ligne de connecteur en pointillés entre les deux extrémités. L’événement [NewPackets](/previous-versions/ms567621(v=vs.100)) est déclenché lors du dessin du lasso, et le gestionnaire d’événements passe les informations de trait à la méthode DrawLasso.

La méthode d’assistance DrawLasso supprime d’abord l’ancienne ligne de connecteur, puis itère au sein des points du trait. Ensuite, DrawLasso calcule où placer les points le long du trait et les dessine. Enfin, il dessine une nouvelle ligne de connecteur.

## <a name="closing-the-form"></a>Fermeture du formulaire

La méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire supprime l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) , myInkCollector.

 

 

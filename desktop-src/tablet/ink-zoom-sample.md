---
description: Cet exemple de programme montre comment zoomer et faire défiler l’encre.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Exemple de zoom d’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20253a3f56b2a03b5a6dad45ab9a8b72090b5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525287"
---
# <a name="ink-zoom-sample"></a>Exemple de zoom d’encre

Cet exemple de programme montre comment zoomer et faire défiler l’encre. En particulier, il permet à l’utilisateur d’effectuer un zoom avant ou arrière de l’encre par incréments. Il montre également comment effectuer un zoom sur une région particulière à l’aide d’un rectangle de zoom. Enfin, cet exemple montre comment collecter de l’encre à différents taux de zoom et comment configurer le défilement dans la zone de dessin avec zoom.

Dans l’exemple, les transformations d’objet et de vue de l’objet de [convertisseur](/previous-versions/ms828481(v=msdn.10)) sont utilisées pour effectuer un zoom et un défilement. La transformation de vue s’applique aux points et à la largeur du stylet. La transformation d’objet s’applique uniquement aux points. L’utilisateur peut contrôler la transformation qui est utilisée en modifiant l’élément largeur du stylet de l’échelle dans le menu mode.

> [!Note]  
> Il est difficile d’effectuer certains appels COM sur certaines méthodes d’interface ([**InkRenderer. SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) et [**InkRenderer. SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), par exemple) lorsqu’un message a été envoyé. Lorsque des messages sont envoyés, ils doivent être marshalés vers la file d’attente de messages de publication. Pour résoudre ce scénario, testez si vous gérez un message de la publication en appelant [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) et publiez le message à vous-même si le message a été envoyé.

 

Les fonctionnalités suivantes sont utilisées dans cet exemple :

-   Objet [InkCollector](/previous-versions/ms583683(v=vs.100))
-   Méthode [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) de l’objet [Renderer](/previous-versions/ms828481(v=msdn.10))
-   Méthode [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) de l’objet [Renderer](/previous-versions/ms828481(v=msdn.10))

## <a name="initializing-the-form"></a>Initialisation du formulaire

Tout d’abord, l’exemple fait référence aux interfaces d’automatisation Tablet PC fournies dans le kit de développement logiciel (SDK) Windows Vista ou Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



L’exemple déclare un [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` , et certains membres privés pour faciliter la mise à l’échelle.


```C++
// Declare the Ink Collector object
private InkCollector myInkCollector = null;
...
// The starting and ending points of the zoom rectangle
private Rectangle zoomRectangle = Rectangle.Empty;

// The current zoom factor (1 = 100% zoom level)
private float zoomFactor = 1;

// Declare constants for the width and height of the 
// drawing area (in ink space coordinates).
private const int InkSpaceWidth = 50000;
private const int InkSpaceHeight = 50000;
...
// Declare constant for the pen width used by this application
private const float MediumInkWidth = 100;
```



L’exemple crée et active l' [InkCollector](/previous-versions/ms583683(v=vs.100)) dans le gestionnaire d’événements [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire. En outre, la propriété [Width](/previous-versions/ms837941(v=msdn.10)) de la propriété [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) de l’objet InkCollector est définie. Enfin, les plages de la barre de défilement sont définies et la méthode de l’application `UpdateZoomAndScroll` est appelée.


```C++
private void InkZoom_Load(object sender, System.EventArgs e)
{
   // Create the pen used to draw the zoom rectangle
    blackPen = new Pen(Color.Black, 1);

    // Create the ink collector and associate it with the form
    myInkCollector = new InkCollector(pnlDrawingArea.Handle);

    // Set the pen width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth;

    // Enable ink collection
    myInkCollector.Enabled = true;

    // Define ink space size - note that the scroll bars
    // map directly to ink space
    hScrollBar.Minimum = 0;
    hScrollBar.Maximum = InkSpaceWidth;
    vScrollBar.Minimum = 0;
    vScrollBar.Maximum = InkSpaceHeight;

    // Set the scroll bars to map to the current zoom level
    UpdateZoomAndScroll();
}
```



## <a name="updating-the-zoom-and-scroll-values"></a>Mise à jour des valeurs de zoom et de défilement

La zone de dessin du collecteur d’encre est affectée par de nombreux événements. Dans la `UpdateZoomAndScroll` méthode, une matrice de transformation est utilisée pour mettre à l’échelle et traduire le collecteur d’encres dans la fenêtre.

> [!Note]  
> La méthode [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) de l’objet [Renderer](/previous-versions/ms828481(v=msdn.10)) applique la transformation aux traits et à la largeur du stylet, tandis que la méthode [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) applique uniquement la transformation aux traits.

 

Enfin, la méthode de l’application `UpdateScrollBars` est appelée et l’actualisation du formulaire est forcée.


```C++
// Create a transformation matrix
Matrix m = new Matrix();

// Apply the current scale factor
m.Scale(zoomFactor,zoomFactor);

// Apply the current translation factor - note that since 
// the scroll bars map directly to ink space, their values
// can be used directly.
m.Translate(-hScrollBar.Value, -vScrollBar.Value);

// ...
if (miScalePenWidth.Checked)
{
    myInkCollector.Renderer.SetViewTransform(m);
}
else
{
    myInkCollector.Renderer.SetObjectTransform(m);
}

// Set the scroll bars to map to the current zoom level
UpdateScrollBars();

Refresh();
```



## <a name="managing-the-scroll-bars"></a>Gestion des barres de défilement

La `UpdateScrollBars` méthode Configure les barres de défilement pour fonctionner correctement avec la taille de fenêtre actuelle, le paramètre de zoom et l’emplacement de défilement dans le [InkCollector](/previous-versions/ms583683(v=vs.100)). Cette méthode calcule la grande modification et les petites valeurs de modification pour les barres de défilement verticales et horizontales. Elle calcule également la valeur actuelle des barres de défilement et indique si elles doivent être visibles. La méthode [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) de l’objet [Renderer](/previous-versions/ms828481(v=msdn.10)) gère la conversion de pixels vers l’espace de coordonnées zoomé et les comptes pour toute mise à l’échelle et le défilement appliqués via les transformations d’affichage et d’objet.


```C++
// Create a point representing the top left of the drawing area (in pixels)
Point ptUpperLeft = new Point(0, 0);

// Create a point representing the size of a small change
Point ptSmallChange = new Point(SmallChangeSize, SmallChangeSize);

// Create a point representing the lower right of the drawing area (in pixels)
Point ptLowerRight = new Point(hScrollBar.Width, vScrollBar.Height);

using (Graphics g = CreateGraphics())
{
    // Convert each of the points to ink space
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptUpperLeft);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptLowerRight);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptSmallChange);
}

// Set the SmallChange values (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.SmallChange = ptSmallChange.X - ptUpperLeft.X;
vScrollBar.SmallChange = ptSmallChange.Y - ptUpperLeft.Y;

// Set the LargeChange values to the drawing area width (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.LargeChange = ptLowerRight.X - ptUpperLeft.X;
vScrollBar.LargeChange = ptLowerRight.Y - ptUpperLeft.Y;

// If the scroll bars are not needed, hide them
hScrollBar.Visible = hScrollBar.LargeChange < hScrollBar.Maximum;
vScrollBar.Visible = vScrollBar.LargeChange < vScrollBar.Maximum;

// If the horizontal scroll bar value would run off of the drawing area, 
// adjust it
if(hScrollBar.Visible && (hScrollBar.Value + hScrollBar.LargeChange > hScrollBar.Maximum)) 
{
    hScrollBar.Value = hScrollBar.Maximum - hScrollBar.LargeChange;
}

// If the vertical scroll bar value would run off of the drawing area, 
// adjust it
if(vScrollBar.Visible && (vScrollBar.Value + vScrollBar.LargeChange > vScrollBar.Maximum))
{
    vScrollBar.Value = vScrollBar.Maximum - vScrollBar.LargeChange;
}
```



## <a name="zooming-to-a-rectangle"></a>Zoom sur un rectangle

Les `pnlDrawingArea` gestionnaires d’événements du panneau gèrent le dessin du rectangle dans la fenêtre. Si la commande zoom sur Rect est cochée dans le menu mode, le gestionnaire d’événements [MouseUp](/previous-versions/ms567618(v=vs.100)) appelle la méthode de l’application `ZoomToRectangle` . La `ZoomToRectangle` méthode calcule la largeur et la hauteur du rectangle, vérifie les conditions limites, met à jour les valeurs de la barre de défilement et le facteur d’échelle, puis appelle la méthode de l’application `UpdateZoomAndScroll` pour appliquer les nouveaux paramètres.

## <a name="closing-the-form"></a>Fermeture du formulaire

La méthode dispose du formulaire [supprime](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 

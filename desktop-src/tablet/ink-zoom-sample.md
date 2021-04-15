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
# <a name="ink-zoom-sample"></a><span data-ttu-id="4f89b-103">Exemple de zoom d’encre</span><span class="sxs-lookup"><span data-stu-id="4f89b-103">Ink Zoom Sample</span></span>

<span data-ttu-id="4f89b-104">Cet exemple de programme montre comment zoomer et faire défiler l’encre.</span><span class="sxs-lookup"><span data-stu-id="4f89b-104">This sample program demonstrates how to zoom and scroll ink.</span></span> <span data-ttu-id="4f89b-105">En particulier, il permet à l’utilisateur d’effectuer un zoom avant ou arrière de l’encre par incréments.</span><span class="sxs-lookup"><span data-stu-id="4f89b-105">In particular, it enables the user to zoom in and out of ink in increments.</span></span> <span data-ttu-id="4f89b-106">Il montre également comment effectuer un zoom sur une région particulière à l’aide d’un rectangle de zoom.</span><span class="sxs-lookup"><span data-stu-id="4f89b-106">It also demonstrates how to zoom into a particular region using a zoom rectangle.</span></span> <span data-ttu-id="4f89b-107">Enfin, cet exemple montre comment collecter de l’encre à différents taux de zoom et comment configurer le défilement dans la zone de dessin avec zoom.</span><span class="sxs-lookup"><span data-stu-id="4f89b-107">Finally, this sample illustrates how to collect ink at different zoom ratios and how to set up scrolling within the zoomed drawing area.</span></span>

<span data-ttu-id="4f89b-108">Dans l’exemple, les transformations d’objet et de vue de l’objet de [convertisseur](/previous-versions/ms828481(v=msdn.10)) sont utilisées pour effectuer un zoom et un défilement.</span><span class="sxs-lookup"><span data-stu-id="4f89b-108">In the sample, the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's view and object transforms are used to perform zooming and scrolling.</span></span> <span data-ttu-id="4f89b-109">La transformation de vue s’applique aux points et à la largeur du stylet.</span><span class="sxs-lookup"><span data-stu-id="4f89b-109">The view transform applies to the points and the pen width.</span></span> <span data-ttu-id="4f89b-110">La transformation d’objet s’applique uniquement aux points.</span><span class="sxs-lookup"><span data-stu-id="4f89b-110">The object transform applies only to the points.</span></span> <span data-ttu-id="4f89b-111">L’utilisateur peut contrôler la transformation qui est utilisée en modifiant l’élément largeur du stylet de l’échelle dans le menu mode.</span><span class="sxs-lookup"><span data-stu-id="4f89b-111">The user can control which transform is used by changing the Scale Pen Width item on the Mode menu.</span></span>

> [!Note]  
> <span data-ttu-id="4f89b-112">Il est difficile d’effectuer certains appels COM sur certaines méthodes d’interface ([**InkRenderer. SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) et [**InkRenderer. SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), par exemple) lorsqu’un message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="4f89b-112">It is problematic to perform some COM calls on certain interface methods ([**InkRenderer.SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) and [**InkRenderer.SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), for example) when a message has been SENT.</span></span> <span data-ttu-id="4f89b-113">Lorsque des messages sont envoyés, ils doivent être marshalés vers la file d’attente de messages de publication.</span><span class="sxs-lookup"><span data-stu-id="4f89b-113">When messages are SENT, they need to be marshalled to the POST message queue.</span></span> <span data-ttu-id="4f89b-114">Pour résoudre ce scénario, testez si vous gérez un message de la publication en appelant [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) et publiez le message à vous-même si le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="4f89b-114">To address this scenario, test whether you are handling a message from POST by calling [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) and POST the message to yourself if the message was SENT.</span></span>

 

<span data-ttu-id="4f89b-115">Les fonctionnalités suivantes sont utilisées dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="4f89b-115">The following features are used in this sample:</span></span>

-   <span data-ttu-id="4f89b-116">Objet [InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4f89b-116">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object</span></span>
-   <span data-ttu-id="4f89b-117">Méthode [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) de l’objet [Renderer](/previous-versions/ms828481(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="4f89b-117">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method</span></span>
-   <span data-ttu-id="4f89b-118">Méthode [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) de l’objet [Renderer](/previous-versions/ms828481(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="4f89b-118">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method</span></span>

## <a name="initializing-the-form"></a><span data-ttu-id="4f89b-119">Initialisation du formulaire</span><span class="sxs-lookup"><span data-stu-id="4f89b-119">Initializing the Form</span></span>

<span data-ttu-id="4f89b-120">Tout d’abord, l’exemple fait référence aux interfaces d’automatisation Tablet PC fournies dans le kit de développement logiciel (SDK) Windows Vista ou Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="4f89b-120">First, the sample references the Tablet PC Automation interfaces, which are provided in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="4f89b-121">L’exemple déclare un [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` , et certains membres privés pour faciliter la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="4f89b-121">The sample declares an [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector`, and some private members to help with scaling.</span></span>


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



<span data-ttu-id="4f89b-122">L’exemple crée et active l' [InkCollector](/previous-versions/ms583683(v=vs.100)) dans le gestionnaire d’événements [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire.</span><span class="sxs-lookup"><span data-stu-id="4f89b-122">Then the sample creates and enables the [InkCollector](/previous-versions/ms583683(v=vs.100)) in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="4f89b-123">En outre, la propriété [Width](/previous-versions/ms837941(v=msdn.10)) de la propriété [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) de l’objet InkCollector est définie.</span><span class="sxs-lookup"><span data-stu-id="4f89b-123">Also, the [Width](/previous-versions/ms837941(v=msdn.10)) property of the InkCollector object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property is set.</span></span> <span data-ttu-id="4f89b-124">Enfin, les plages de la barre de défilement sont définies et la méthode de l’application `UpdateZoomAndScroll` est appelée.</span><span class="sxs-lookup"><span data-stu-id="4f89b-124">Finally, the scroll bar ranges are defined and the application's `UpdateZoomAndScroll` method is called.</span></span>


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



## <a name="updating-the-zoom-and-scroll-values"></a><span data-ttu-id="4f89b-125">Mise à jour des valeurs de zoom et de défilement</span><span class="sxs-lookup"><span data-stu-id="4f89b-125">Updating the Zoom and Scroll Values</span></span>

<span data-ttu-id="4f89b-126">La zone de dessin du collecteur d’encre est affectée par de nombreux événements.</span><span class="sxs-lookup"><span data-stu-id="4f89b-126">The drawing area of the ink collector is affected by many events.</span></span> <span data-ttu-id="4f89b-127">Dans la `UpdateZoomAndScroll` méthode, une matrice de transformation est utilisée pour mettre à l’échelle et traduire le collecteur d’encres dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4f89b-127">In the `UpdateZoomAndScroll` method, a transformation matrix is used to both scale and translate the ink collector within the window.</span></span>

> [!Note]  
> <span data-ttu-id="4f89b-128">La méthode [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) de l’objet [Renderer](/previous-versions/ms828481(v=msdn.10)) applique la transformation aux traits et à la largeur du stylet, tandis que la méthode [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) applique uniquement la transformation aux traits.</span><span class="sxs-lookup"><span data-stu-id="4f89b-128">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method applies the transform to both the strokes and the pen width, while the [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method only applies the transform to the strokes.</span></span>

 

<span data-ttu-id="4f89b-129">Enfin, la méthode de l’application `UpdateScrollBars` est appelée et l’actualisation du formulaire est forcée.</span><span class="sxs-lookup"><span data-stu-id="4f89b-129">Finally, the application's `UpdateScrollBars` method is called and the form is forced to refresh.</span></span>


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



## <a name="managing-the-scroll-bars"></a><span data-ttu-id="4f89b-130">Gestion des barres de défilement</span><span class="sxs-lookup"><span data-stu-id="4f89b-130">Managing the Scroll Bars</span></span>

<span data-ttu-id="4f89b-131">La `UpdateScrollBars` méthode Configure les barres de défilement pour fonctionner correctement avec la taille de fenêtre actuelle, le paramètre de zoom et l’emplacement de défilement dans le [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="4f89b-131">The `UpdateScrollBars` method sets up the scroll bars to work correctly with the current window size, zoom setting, and scroll location within the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span> <span data-ttu-id="4f89b-132">Cette méthode calcule la grande modification et les petites valeurs de modification pour les barres de défilement verticales et horizontales.</span><span class="sxs-lookup"><span data-stu-id="4f89b-132">This method calculates the large change and small change values for the vertical and horizontal scroll bars.</span></span> <span data-ttu-id="4f89b-133">Elle calcule également la valeur actuelle des barres de défilement et indique si elles doivent être visibles.</span><span class="sxs-lookup"><span data-stu-id="4f89b-133">It also calculates the current value of the scroll bars and whether they should be visible.</span></span> <span data-ttu-id="4f89b-134">La méthode [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) de l’objet [Renderer](/previous-versions/ms828481(v=msdn.10)) gère la conversion de pixels vers l’espace de coordonnées zoomé et les comptes pour toute mise à l’échelle et le défilement appliqués via les transformations d’affichage et d’objet.</span><span class="sxs-lookup"><span data-stu-id="4f89b-134">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method handles the conversion from pixels to the zoomed coordinate space and accounts for any scaling and scrolling that is applied through the view and object transforms.</span></span>


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



## <a name="zooming-to-a-rectangle"></a><span data-ttu-id="4f89b-135">Zoom sur un rectangle</span><span class="sxs-lookup"><span data-stu-id="4f89b-135">Zooming to a Rectangle</span></span>

<span data-ttu-id="4f89b-136">Les `pnlDrawingArea` gestionnaires d’événements du panneau gèrent le dessin du rectangle dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4f89b-136">The `pnlDrawingArea` panel event handlers manage drawing the rectangle to the window.</span></span> <span data-ttu-id="4f89b-137">Si la commande zoom sur Rect est cochée dans le menu mode, le gestionnaire d’événements [MouseUp](/previous-versions/ms567618(v=vs.100)) appelle la méthode de l’application `ZoomToRectangle` .</span><span class="sxs-lookup"><span data-stu-id="4f89b-137">If the Zoom To Rect command is checked on the Mode menu, then the [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler calls the application's `ZoomToRectangle` method.</span></span> <span data-ttu-id="4f89b-138">La `ZoomToRectangle` méthode calcule la largeur et la hauteur du rectangle, vérifie les conditions limites, met à jour les valeurs de la barre de défilement et le facteur d’échelle, puis appelle la méthode de l’application `UpdateZoomAndScroll` pour appliquer les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="4f89b-138">The `ZoomToRectangle` method calculates the width and height of the rectangle, checks for boundary conditions, updates the scroll bar values and the scale factor, and then calls the application's `UpdateZoomAndScroll` method to apply the new settings.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="4f89b-139">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="4f89b-139">Closing the Form</span></span>

<span data-ttu-id="4f89b-140">La méthode dispose du formulaire [supprime](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="4f89b-140">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 

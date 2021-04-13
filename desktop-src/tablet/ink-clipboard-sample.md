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
# <a name="ink-clipboard-sample"></a><span data-ttu-id="0faf0-104">Exemple de presse-papiers Ink</span><span class="sxs-lookup"><span data-stu-id="0faf0-104">Ink Clipboard Sample</span></span>

<span data-ttu-id="0faf0-105">Ce programme montre comment copier et coller de l’encre dans une autre application.</span><span class="sxs-lookup"><span data-stu-id="0faf0-105">This program demonstrates how to copy and paste ink into another application.</span></span> <span data-ttu-id="0faf0-106">Elle permet également à l’utilisateur de copier une sélection de traits et de coller le résultat dans l’objet Ink existant.</span><span class="sxs-lookup"><span data-stu-id="0faf0-106">It also enables the user to copy a selection of strokes and paste the result into the existing ink object.</span></span>

<span data-ttu-id="0faf0-107">Les modes de presse-papiers suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="0faf0-107">The following clipboard modes are available:</span></span>

-   <span data-ttu-id="0faf0-108">ISF (Ink Serialized Format)</span><span class="sxs-lookup"><span data-stu-id="0faf0-108">Ink serialized format (ISF)</span></span>
-   <span data-ttu-id="0faf0-109">Métafichiers</span><span class="sxs-lookup"><span data-stu-id="0faf0-109">Metafile</span></span>
-   <span data-ttu-id="0faf0-110">métafichier amélioré (EMF)</span><span class="sxs-lookup"><span data-stu-id="0faf0-110">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="0faf0-111">Bitmap</span><span class="sxs-lookup"><span data-stu-id="0faf0-111">Bitmap</span></span>
-   <span data-ttu-id="0faf0-112">Texte manuscrit</span><span class="sxs-lookup"><span data-stu-id="0faf0-112">Text Ink</span></span>
-   <span data-ttu-id="0faf0-113">Esquisser l’encre</span><span class="sxs-lookup"><span data-stu-id="0faf0-113">Sketch Ink</span></span>

<span data-ttu-id="0faf0-114">L’encre de texte et l’écriture manuscrite sont deux types de contrôles manuscrits utilisés respectivement comme texte ou dessin.</span><span class="sxs-lookup"><span data-stu-id="0faf0-114">Text ink and sketch ink are two types of ink controls used as text or drawing respectively.</span></span> <span data-ttu-id="0faf0-115">Il est possible de coller de la Ink, de l’encre du texte et d’esquisser de l’encre dans l’encre existante.</span><span class="sxs-lookup"><span data-stu-id="0faf0-115">It is possible to paste ISF, text ink, and sketch ink into existing ink.</span></span>

<span data-ttu-id="0faf0-116">En plus du presse-papiers, cet exemple montre également comment sélectionner des traits avec l’outil lasso.</span><span class="sxs-lookup"><span data-stu-id="0faf0-116">In addition to the clipboard, this sample also illustrates how to select strokes with the lasso tool.</span></span> <span data-ttu-id="0faf0-117">L’utilisateur peut déplacer les traits sélectionnés et modifier leurs attributs de dessin.</span><span class="sxs-lookup"><span data-stu-id="0faf0-117">The user can move selected strokes and modify their drawing attributes.</span></span> <span data-ttu-id="0faf0-118">Cette fonctionnalité est un sous-ensemble de la fonctionnalité de sélection déjà fournie par le contrôle d’incrustation d’encre. elle est implémentée ici à des fins d’illustration.</span><span class="sxs-lookup"><span data-stu-id="0faf0-118">This functionality is a subset of the selection functionality already provided by the ink overlay control; it is implemented here for illustrative purposes.</span></span>

<span data-ttu-id="0faf0-119">Les fonctionnalités suivantes sont utilisées dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="0faf0-119">The following features are used in this sample:</span></span>

-   <span data-ttu-id="0faf0-120">Objet [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="0faf0-120">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>
-   <span data-ttu-id="0faf0-121">Prise en charge du presse-papiers Ink.</span><span class="sxs-lookup"><span data-stu-id="0faf0-121">Ink clipboard support.</span></span>
-   <span data-ttu-id="0faf0-122">Utilisation du lasso avec la méthode [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) .</span><span class="sxs-lookup"><span data-stu-id="0faf0-122">The use of the lasso with the [Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method.</span></span>

<span data-ttu-id="0faf0-123">Cet exemple illustre le rendu de l’encre, la copie de cette encre, puis le collage de l’encre dans une autre application telle que Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="0faf0-123">This sample demonstrates rendering ink, copying that ink, and then pasting the ink into another application such as Microsoft Paint.</span></span>

## <a name="collecting-ink-and-setting-up-the-form"></a><span data-ttu-id="0faf0-124">Collecte de l’encre et configuration du formulaire</span><span class="sxs-lookup"><span data-stu-id="0faf0-124">Collecting Ink and Setting Up the Form</span></span>

<span data-ttu-id="0faf0-125">Tout d’abord, référencez les interfaces d’automatisation Tablet PC, qui sont installées avec le <entity type="reg"/> Kit de développement logiciel (SDK) de Microsoft Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="0faf0-125">First, reference the Tablet PC Automation interfaces, which are installed with the Microsoft Windows<entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="0faf0-126">Ensuite, le formulaire déclare des constantes et des champs notés plus loin dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="0faf0-126">Next, the form declares some constants and fields that are noted later in this sample.</span></span>


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



<span data-ttu-id="0faf0-127">Enfin, dans le gestionnaire d’événements [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire, le formulaire est initialisé, un objet [InkCollector](/previous-versions/ms583683(v=vs.100)) pour le formulaire est créé et le collecteur d’entrée manuscrite est activé.</span><span class="sxs-lookup"><span data-stu-id="0faf0-127">Finally, in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler, the form is initialized, an [InkCollector](/previous-versions/ms583683(v=vs.100)) object for the form is created and the ink collector is enabled.</span></span>


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a><span data-ttu-id="0faf0-128">Gestion des événements de menu</span><span class="sxs-lookup"><span data-stu-id="0faf0-128">Handling Menu Events</span></span>

<span data-ttu-id="0faf0-129">Les gestionnaires d’événements d’élément de menu mettent essentiellement à jour l’état du formulaire.</span><span class="sxs-lookup"><span data-stu-id="0faf0-129">The menu item event handlers primarily update the form's state.</span></span>

<span data-ttu-id="0faf0-130">La commande Clear supprime le rectangle de sélection et supprime les traits de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) du collecteur d’encre.</span><span class="sxs-lookup"><span data-stu-id="0faf0-130">The Clear command removes the selection rectangle, and deletes the strokes from the ink collector's [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span>

<span data-ttu-id="0faf0-131">La commande exit désactive le collecteur d’encres avant de quitter l’application.</span><span class="sxs-lookup"><span data-stu-id="0faf0-131">The Exit command disables the ink collector before exiting the application.</span></span>

<span data-ttu-id="0faf0-132">Le menu Edition active les commandes Couper et copier en fonction de l’état de sélection du formulaire, et active la commande Coller en fonction du contenu du presse-papiers, déterminé à l’aide de la méthode [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="0faf0-132">The Edit menu enables the Cut and Copy commands based on the selection state of the form, and enables the Paste command based on the contents of the clipboard, determined by using the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method.</span></span>

<span data-ttu-id="0faf0-133">Les commandes Couper et copier utilisent toutes les deux une méthode d’assistance pour copier l’encre dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="0faf0-133">The Cut and Copy commands both use a helper method to copy ink to the clipboard.</span></span> <span data-ttu-id="0faf0-134">La commande Cut utilise une méthode d’assistance pour supprimer les traits sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="0faf0-134">The Cut command uses a helper method to delete the selected strokes.</span></span>

<span data-ttu-id="0faf0-135">La commande Coller vérifie d’abord la méthode [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) pour déterminer si l’objet dans le presse-papiers peut être collé.</span><span class="sxs-lookup"><span data-stu-id="0faf0-135">The Paste command first checks the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method to see if the object on the clipboard can be pasted.</span></span> <span data-ttu-id="0faf0-136">La commande Coller calcule ensuite l’angle supérieur gauche de la zone de collage, convertit les coordonnées de pixels en espace d’encre, puis colle les traits du presse-papiers dans le collecteur d’encre.</span><span class="sxs-lookup"><span data-stu-id="0faf0-136">The Paste command then computes the upper-left corner for the paste region, converts the coordinates from pixels to ink space, and pastes the strokes from the clipboard to the ink collector.</span></span> <span data-ttu-id="0faf0-137">Enfin, la zone de sélection est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0faf0-137">Finally, the selection box is updated.</span></span>


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



<span data-ttu-id="0faf0-138">Les commandes SELECT et Ink mettent à jour le mode d’application et les attributs de dessin par défaut, effacent la sélection actuelle, mettent à jour l’état du menu et actualisent le formulaire.</span><span class="sxs-lookup"><span data-stu-id="0faf0-138">The Select and Ink commands update the application mode and the default drawing attributes, clear the current selection, update the menu state, and refresh the form.</span></span> <span data-ttu-id="0faf0-139">D’autres gestionnaires s’appuient sur l’état de l’application pour exécuter la fonction correcte, par le biais du lasso ou pour la disposition de l’encre.</span><span class="sxs-lookup"><span data-stu-id="0faf0-139">Other handlers rely on the application state to perform the correct function, either lassoing or laying down ink.</span></span> <span data-ttu-id="0faf0-140">En outre, la commande SELECT ajoute les gestionnaires d’événements [NewPackets](/previous-versions/ms567621(v=vs.100)) et [Stroke](/previous-versions/ms567622(v=vs.100)) au collecteur d’encre et la commande Ink supprime ces gestionnaires d’événements du collecteur d’encre.</span><span class="sxs-lookup"><span data-stu-id="0faf0-140">In addition, the Select command adds the [NewPackets](/previous-versions/ms567621(v=vs.100)) and [Stroke](/previous-versions/ms567622(v=vs.100)) event handlers to the ink collector and the Ink command removes these event handlers from the ink collector.</span></span>

<span data-ttu-id="0faf0-141">Les formats disponibles dans le presse-papiers lorsque les traits sont copiés sont répertoriés dans le menu Format, et l’utilisateur sélectionne le format de copie de l’encre dans cette liste.</span><span class="sxs-lookup"><span data-stu-id="0faf0-141">The formats that are available on the Clipboard when strokes are copied are listed on the Format menu, and the user selects the format for copying the ink from this list.</span></span> <span data-ttu-id="0faf0-142">Les types de formats disponibles incluent Ink Serialized Format (ISF), Metafile, Enhanced Metafile et bitmap.</span><span class="sxs-lookup"><span data-stu-id="0faf0-142">The types of formats available include Ink Serialized Format (ISF), metafile, enhanced metafile, and bitmap.</span></span> <span data-ttu-id="0faf0-143">Les formats d’encre et de texte d’esquisse s’excluent mutuellement et s’appuient sur l’encre copiée dans le presse-papiers en tant qu’objet OLE.</span><span class="sxs-lookup"><span data-stu-id="0faf0-143">The sketch ink and text ink formats are mutually exclusive, and rely on the ink being copied to the clipboard as an OLE object.</span></span>

<span data-ttu-id="0faf0-144">Le menu style permet à l’utilisateur de modifier les propriétés de couleur et de largeur du stylet et des traits sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="0faf0-144">The Style menu enables the user to change the color and width properties of the pen and any selected strokes.</span></span>

<span data-ttu-id="0faf0-145">Par exemple, la commande Red définit la propriété [Color](/previous-versions/ms582103(v=vs.100)) de la propriété [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) du collecteur d’encre sur la couleur rouge.</span><span class="sxs-lookup"><span data-stu-id="0faf0-145">For example, the Red command sets the [Color](/previous-versions/ms582103(v=vs.100)) property of the ink collector's [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) property to the color red.</span></span> <span data-ttu-id="0faf0-146">Étant donné que la propriété [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) de l’objet [Cursor](/previous-versions/ms552104(v=vs.100)) n’a pas été définie, toute nouvelle encre dessinée sur le collecteur d’encre hérite de la couleur de dessin par défaut.</span><span class="sxs-lookup"><span data-stu-id="0faf0-146">Because the [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) property of the [Cursor](/previous-versions/ms552104(v=vs.100)) object has not been set, any new ink drawn to the ink collector inherits to default drawing color.</span></span> <span data-ttu-id="0faf0-147">En outre, si des traits sont actuellement sélectionnés, la propriété couleur des attributs de dessin de chaque trait est également mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0faf0-147">Also, if any strokes are currently selected, each stroke's drawing attributes Color property is updated as well.</span></span>


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



## <a name="handling-mouse-events"></a><span data-ttu-id="0faf0-148">Gestion des événements de souris</span><span class="sxs-lookup"><span data-stu-id="0faf0-148">Handling Mouse Events</span></span>

<span data-ttu-id="0faf0-149">Le gestionnaire d’événements [MouseMove](/previous-versions/ms567617(v=vs.100)) vérifie le mode d’application.</span><span class="sxs-lookup"><span data-stu-id="0faf0-149">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="0faf0-150">Si le mode est MoveInk et qu’un bouton de la souris est enfoncé, le gestionnaire déplace les traits à l’aide de la méthode Move de la collection [Strokes](/previous-versions/ms552701(v=vs.100)) et met à jour la zone de sélection.</span><span class="sxs-lookup"><span data-stu-id="0faf0-150">If the mode is MoveInk and a mouse button is down, then the handler moves the strokes by using the [Strokes](/previous-versions/ms552701(v=vs.100)) collection's Move method and updates the selection box.</span></span> <span data-ttu-id="0faf0-151">Dans le cas contraire, le gestionnaire vérifie si le rectangle de sélection contient le curseur, active la collecte d’encre en conséquence et définit également le curseur en conséquence.</span><span class="sxs-lookup"><span data-stu-id="0faf0-151">Otherwise, the handler checks to determine whether the selection rectangle contains the cursor, enables ink collection accordingly, and also sets the cursor accordingly.</span></span>

<span data-ttu-id="0faf0-152">Le gestionnaire d’événements [MouseDown](/previous-versions/ms567616(v=vs.100)) vérifie le paramètre de curseur.</span><span class="sxs-lookup"><span data-stu-id="0faf0-152">The [MouseDown](/previous-versions/ms567616(v=vs.100)) event handler checks the cursor setting.</span></span> <span data-ttu-id="0faf0-153">Si le curseur est défini sur [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), le gestionnaire définit le mode d’application sur MoveInk et enregistre l’emplacement du curseur.</span><span class="sxs-lookup"><span data-stu-id="0faf0-153">If the cursor is set to [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), then the handler sets the application mode to MoveInk and records the cursor location.</span></span> <span data-ttu-id="0faf0-154">Sinon, si une sélection est en cours, effacez-la.</span><span class="sxs-lookup"><span data-stu-id="0faf0-154">Otherwise, if there is a current selection, clear it.</span></span>

<span data-ttu-id="0faf0-155">Le gestionnaire d’événements [MouseUp](/previous-versions/ms567618(v=vs.100)) vérifie le mode d’application.</span><span class="sxs-lookup"><span data-stu-id="0faf0-155">The [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="0faf0-156">Si le mode est MoveInk, le gestionnaire définit le mode d’application en fonction de l’état activé de la commande SELECT.</span><span class="sxs-lookup"><span data-stu-id="0faf0-156">If the mode is MoveInk, then the handler sets the application mode based on the Select command's checked state.</span></span>

<span data-ttu-id="0faf0-157">L’événement [NewPackets](/previous-versions/ms567621(v=vs.100)) est déclenché en mode de sélection lorsque le collecteur d’encre reçoit de nouvelles données de paquets.</span><span class="sxs-lookup"><span data-stu-id="0faf0-157">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised in selection mode when the ink collector receives new packet data.</span></span> <span data-ttu-id="0faf0-158">Si l’application est en mode de sélection, il est nécessaire d’intercepter les nouveaux paquets et de les utiliser pour dessiner le lasso de sélection.</span><span class="sxs-lookup"><span data-stu-id="0faf0-158">If the application is in selection mode, it is necessary to intercept the new packets and use them to draw the selection lasso.</span></span>

<span data-ttu-id="0faf0-159">La coordonnée de chaque paquet est convertie en pixels, restreinte à la zone de dessin et ajoutée à la collection de points du lasso.</span><span class="sxs-lookup"><span data-stu-id="0faf0-159">Each packet's coordinate is converted to pixels, constrained to the drawing area, and added to the lasso's collection of points.</span></span> <span data-ttu-id="0faf0-160">Une méthode d’assistance est ensuite appelée pour dessiner le lasso sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="0faf0-160">A helper method is then called to draw the lasso on the form.</span></span>

## <a name="handling-a-new-stroke"></a><span data-ttu-id="0faf0-161">Gestion d’un nouveau trait</span><span class="sxs-lookup"><span data-stu-id="0faf0-161">Handling a New Stroke</span></span>

<span data-ttu-id="0faf0-162">L’événement [Stroke](/previous-versions/ms567622(v=vs.100)) est déclenché dans le mode de sélection lorsqu’un nouveau trait est dessiné.</span><span class="sxs-lookup"><span data-stu-id="0faf0-162">The [Stroke](/previous-versions/ms567622(v=vs.100)) event is raised in the selection mode when a new stroke is drawn.</span></span> <span data-ttu-id="0faf0-163">Si l’application est en mode de sélection, ce trait correspond au lasso et il est nécessaire de mettre à jour les informations des traits sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="0faf0-163">If the application is in selection mode, this stroke corresponds to the lasso and it is necessary to update the selected strokes' information.</span></span>

<span data-ttu-id="0faf0-164">Le gestionnaire annule l’événement [Stroke](/previous-versions/ms567622(v=vs.100)) , vérifie plus de deux points de lasso, copie la collection points dans un tableau d’objets [point](/dotnet/api/system.drawing.point?view=netcore-3.1) et convertit les coordonnées des points du tableau de pixels en espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="0faf0-164">The handler cancels the [Stroke](/previous-versions/ms567622(v=vs.100)) event, checks for more than two lasso points, copies the Points collection to an array of [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) objects, and converts the coordinates of the points in the array from pixels to ink space.</span></span> <span data-ttu-id="0faf0-165">Ensuite, le gestionnaire utilise la méthode [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) pour récupérer les traits sélectionnés par les points du lasso et met à jour l’état de sélection du formulaire.</span><span class="sxs-lookup"><span data-stu-id="0faf0-165">Then, the handler uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to get the strokes selected by the lasso points and updates the selection state of the form.</span></span> <span data-ttu-id="0faf0-166">Enfin, le trait qui a déclenché l’événement est supprimé de la collection de traits sélectionnés, la collection de points de lasso est vidée et une méthode d’assistance dessine le rectangle de sélection.</span><span class="sxs-lookup"><span data-stu-id="0faf0-166">Finally, the stroke that raised the event is removed from the collection of selected strokes, the lasso Points collection is emptied, and a helper method draws the selection rectangle.</span></span>


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



## <a name="copying-ink-to-the-clipboard"></a><span data-ttu-id="0faf0-167">Copie de l’encre dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="0faf0-167">Copying Ink to the Clipboard</span></span>

<span data-ttu-id="0faf0-168">La méthode d’assistance CopyInkToClipboard crée une valeur [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) , vérifie l’état du menu Format pour mettre à jour les formats à placer dans le presse-papiers et utilise la méthode [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) pour copier les traits dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="0faf0-168">The CopyInkToClipboard helper method creates an [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) value, checks the Format menu's state to update the formats to put on the clipboard, and uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) method to copy the strokes to the clipboard.</span></span>


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



## <a name="updating-a-selection"></a><span data-ttu-id="0faf0-169">Mise à jour d’une sélection</span><span class="sxs-lookup"><span data-stu-id="0faf0-169">Updating a Selection</span></span>

<span data-ttu-id="0faf0-170">La méthode d’assistance SetSelection met à jour la selectedStrokes déposée et, si la collection est **null** ou **vide**, le rectangle de sélection est défini sur le rectangle vide.</span><span class="sxs-lookup"><span data-stu-id="0faf0-170">The SetSelection helper method updates the selectedStrokes filed and if the collection is **NULL** or **EMPTY**, the selection rectangle is set to the empty rectangle.</span></span> <span data-ttu-id="0faf0-171">Si la collection [Strokes](/previous-versions/ms552701(v=vs.100)) sélectionnée n’est pas vide, la méthode SetSelection effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0faf0-171">If the selected [Strokes](/previous-versions/ms552701(v=vs.100)) collection is not empty the SetSelection method performs the following steps:</span></span>

-   <span data-ttu-id="0faf0-172">Détermine le rectangle englobant à l’aide de la méthode [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) de la collection Strokes</span><span class="sxs-lookup"><span data-stu-id="0faf0-172">Determines the bounding rectangle by using the [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) method of the strokes collection</span></span>
-   <span data-ttu-id="0faf0-173">Convertit les coordonnées des rectangles de l’espace d’encre en pixels</span><span class="sxs-lookup"><span data-stu-id="0faf0-173">Converts the rectangle coordinates from ink space to pixels</span></span>
-   <span data-ttu-id="0faf0-174">Augmente le rectangle pour fournir un espace visuel entre celui-ci et les traits sélectionnés</span><span class="sxs-lookup"><span data-stu-id="0faf0-174">Inflates the rectangle to provide some visual space between it and the selected strokes</span></span>
-   <span data-ttu-id="0faf0-175">Crée des poignées de sélection pour la zone de sélection actuelle</span><span class="sxs-lookup"><span data-stu-id="0faf0-175">Creates selection handles for the current selection box</span></span>

<span data-ttu-id="0faf0-176">Enfin, la méthode SetSelection définit la visibilité des poignées de sélection et définit la propriété [AutoRedraw](/previous-versions/ms571706(v=vs.100)) du collecteur d’encre sur **false**, si les traits sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="0faf0-176">Finally, the SetSelection method sets the visibility of the selection handles and sets the ink collector's [AutoRedraw](/previous-versions/ms571706(v=vs.100)) property to **FALSE**, if strokes are selected.</span></span>


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



## <a name="drawing-the-lasso"></a><span data-ttu-id="0faf0-177">Dessin du lasso</span><span class="sxs-lookup"><span data-stu-id="0faf0-177">Drawing the Lasso</span></span>

<span data-ttu-id="0faf0-178">Le lasso est dessiné sous la forme d’une série de points ouverts qui suivent le tracé du trait du lasso et une ligne de connecteur en pointillés entre les deux extrémités.</span><span class="sxs-lookup"><span data-stu-id="0faf0-178">The lasso is drawn as a series of open dots that follow the path of the lasso stroke and a dashed connector line between the two ends.</span></span> <span data-ttu-id="0faf0-179">L’événement [NewPackets](/previous-versions/ms567621(v=vs.100)) est déclenché lors du dessin du lasso, et le gestionnaire d’événements passe les informations de trait à la méthode DrawLasso.</span><span class="sxs-lookup"><span data-stu-id="0faf0-179">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised as the lasso is being drawn, and the event handler passes the stroke information to the DrawLasso method.</span></span>

<span data-ttu-id="0faf0-180">La méthode d’assistance DrawLasso supprime d’abord l’ancienne ligne de connecteur, puis itère au sein des points du trait.</span><span class="sxs-lookup"><span data-stu-id="0faf0-180">The DrawLasso helper method first removes the old connector line and then iterates over the points in the stroke.</span></span> <span data-ttu-id="0faf0-181">Ensuite, DrawLasso calcule où placer les points le long du trait et les dessine.</span><span class="sxs-lookup"><span data-stu-id="0faf0-181">Then, DrawLasso calculates where to place the dots along the stroke and draws them.</span></span> <span data-ttu-id="0faf0-182">Enfin, il dessine une nouvelle ligne de connecteur.</span><span class="sxs-lookup"><span data-stu-id="0faf0-182">Finally, it draws a new connector line.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="0faf0-183">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="0faf0-183">Closing the Form</span></span>

<span data-ttu-id="0faf0-184">La méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire supprime l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) , myInkCollector.</span><span class="sxs-lookup"><span data-stu-id="0faf0-184">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object, myInkCollector.</span></span>

 

 

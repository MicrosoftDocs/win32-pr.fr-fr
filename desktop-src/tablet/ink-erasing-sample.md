---
description: 'Cette application s’appuie sur l’exemple d’exemple de collection Ink en montrant la suppression des traits d’encre. L’exemple fournit à l’utilisateur un menu avec quatre modes d’accès : activé pour l’écriture manuscrite, en effaçant au sommet, en effaçant à l’intersection et en effaçant les traits.'
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Exemple d’effacement d’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46040781d778f936815e57ba96b4ca516617d9a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525293"
---
# <a name="ink-erasing-sample"></a><span data-ttu-id="6e90c-104">Exemple d’effacement d’encre</span><span class="sxs-lookup"><span data-stu-id="6e90c-104">Ink Erasing Sample</span></span>

<span data-ttu-id="6e90c-105">Cette application s’appuie sur l’exemple d’exemple de [collection Ink](ink-collection-sample.md) en montrant la suppression des traits d’encre.</span><span class="sxs-lookup"><span data-stu-id="6e90c-105">This application builds on the [Ink Collection Sample](ink-collection-sample.md) sample by demonstrating ink strokes deletion.</span></span> <span data-ttu-id="6e90c-106">L’exemple fournit à l’utilisateur un menu avec quatre modes d’accès : activé pour l’écriture manuscrite, en effaçant au sommet, en effaçant à l’intersection et en effaçant les traits.</span><span class="sxs-lookup"><span data-stu-id="6e90c-106">The sample provides the user with a menu that has four modes to choose from: ink-enabled, erasing at cusp, erasing at intersections, and erasing strokes.</span></span>

<span data-ttu-id="6e90c-107">En mode activé pour l’écriture manuscrite, l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) collecte l’encre comme indiqué dans [exemple de collection d’encres](ink-collection-sample.md).</span><span class="sxs-lookup"><span data-stu-id="6e90c-107">In ink-enabled mode, the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object collects ink as shown in [Ink Collection Sample](ink-collection-sample.md).</span></span>

<span data-ttu-id="6e90c-108">En mode d’effacement, les segments de traits d’encre existants que l’utilisateur touche avec le curseur sont effacés.</span><span class="sxs-lookup"><span data-stu-id="6e90c-108">In an erasing mode, segments of existing ink strokes that the user touches with the cursor are erased.</span></span> <span data-ttu-id="6e90c-109">En outre, les sommets ou les intersections peuvent être signalés par un cercle rouge.</span><span class="sxs-lookup"><span data-stu-id="6e90c-109">Also, the cusps or intersections may be marked with a red circle.</span></span>

<span data-ttu-id="6e90c-110">Les parties les plus intéressantes de cet exemple se trouvent dans le `InkErase` Gestionnaire d’événements du formulaire `OnPaint` et dans les fonctions d’effacement qui sont appelées à partir du gestionnaire d’événements du formulaire `OnMouseMove` .</span><span class="sxs-lookup"><span data-stu-id="6e90c-110">The most interesting parts of this sample lie in the `InkErase` form's `OnPaint` event handler and in the erasing functions that are called from the form's `OnMouseMove` event handler.</span></span>

## <a name="circling-the-cusps-and-intersections"></a><span data-ttu-id="6e90c-111">Cercle des sommets et des intersections</span><span class="sxs-lookup"><span data-stu-id="6e90c-111">Circling the Cusps and Intersections</span></span>

<span data-ttu-id="6e90c-112">Le gestionnaire d' `OnPaint` événements du formulaire peint d’abord les traits, et selon le mode d’application, peut trouver et marquer toutes les fronces ou les intersections avec un petit cercle rouge.</span><span class="sxs-lookup"><span data-stu-id="6e90c-112">The form's `OnPaint` event handler first paints the strokes, and depending on the application mode, may find and mark all of the cusps or intersections with a small red circle.</span></span> <span data-ttu-id="6e90c-113">Un Sommet marque le point où un trait modifie le sens brusquement.</span><span class="sxs-lookup"><span data-stu-id="6e90c-113">A cusp marks the point where a stroke changes direction abruptly.</span></span> <span data-ttu-id="6e90c-114">Une intersection marque un point où un trait entre en intersection avec lui-même ou un autre trait.</span><span class="sxs-lookup"><span data-stu-id="6e90c-114">An intersection marks a point where one stroke intersects with itself or another stroke.</span></span>

<span data-ttu-id="6e90c-115">L’événement [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) se produit chaque fois qu’un contrôle est redessiné.</span><span class="sxs-lookup"><span data-stu-id="6e90c-115">The [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event occurs whenever a control is redrawn.</span></span>

> [!Note]  
> <span data-ttu-id="6e90c-116">L’exemple force le formulaire à se redessiner chaque fois qu’un trait est effacé, ou lorsque le mode d’application change, à l’aide de la méthode [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) du formulaire.</span><span class="sxs-lookup"><span data-stu-id="6e90c-116">The sample forces the form to redraw itself whenever a stroke is erased, or when the application mode changes, using the form's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method.</span></span>

 


```C++
private void InkErase_OnPaint(object sender, PaintEventArgs e)
{
    Strokes strokesToPaint = myInkCollector.Ink.Strokes;

    myInkCollector.Renderer.Draw(e.Graphics, strokesToPaint);

    switch (mode)
    {
        case ApplicationMode.CuspErase:
            PaintCusps(e.Graphics, strokesToPaint);
            break;
        case ApplicationMode.IntersectErase:
            PaintIntersections(e.Graphics, strokesToPaint);
            break;
    }
}
```



<span data-ttu-id="6e90c-117">Dans `PaintCusps` , le code itère au sein de chaque fronce dans chaque trait et dessine un cercle rouge autour.</span><span class="sxs-lookup"><span data-stu-id="6e90c-117">In `PaintCusps`, the code iterates through each cusp in each stroke, and draws a red circle around it.</span></span> <span data-ttu-id="6e90c-118">La propriété [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) du trait retourne les index des points d’un des qui correspondent aux sommets.</span><span class="sxs-lookup"><span data-stu-id="6e90c-118">The stroke's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) property returns the indices of the points within a stoke that correspond to cusps.</span></span> <span data-ttu-id="6e90c-119">Notez également la méthode [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) de l’objet de [convertisseur](/previous-versions/ms828481(v=msdn.10)) , qui convertit le point en coordonnées pertinentes pour la méthode DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="6e90c-119">Also, note the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) method, which converts the point to coordinates relevant to the DrawEllipse method.</span></span>


```C++
private void PaintCusps(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        int[] cusps = currentStroke.PolylineCusps;

        foreach (int i in cusps)
        {
            Point pt = currentStroke.GetPoint(i);

            // Convert the X, Y position to Window based pixel coordinates
            myInkCollector.Renderer.InkSpaceToPixel(g, ref pt);

            // Draw a red circle as the cusp position
            g.DrawEllipse(Pens.Red, pt.X-3, pt.Y-3, 6, 6);
        }
    }
}
```



<span data-ttu-id="6e90c-120">Dans `PaintIntersections` , le code itère au sein de chaque trait pour rechercher ses intersections avec le jeu entier de traits.</span><span class="sxs-lookup"><span data-stu-id="6e90c-120">In `PaintIntersections`, the code iterates through each stroke to find its intersections with the entire set of strokes.</span></span> <span data-ttu-id="6e90c-121">Notez que la méthode [FindIntersections](/previous-versions/ms827856(v=msdn.10)) du trait est passée à une collection [Strokes](/previous-versions/ms827799(v=msdn.10)) et retourne un tableau de valeurs d’index à virgule flottante représentant les intersections.</span><span class="sxs-lookup"><span data-stu-id="6e90c-121">Note that the stroke's [FindIntersections](/previous-versions/ms827856(v=msdn.10)) method is passed a [Strokes](/previous-versions/ms827799(v=msdn.10)) collection and returns an array of floating point index values representing the intersections.</span></span> <span data-ttu-id="6e90c-122">Le code calcule ensuite une coordonnée X-Y pour chaque intersection et dessine un cercle rouge autour.</span><span class="sxs-lookup"><span data-stu-id="6e90c-122">The code then calculates an X-Y coordinate for each intersection, and draws a red circle around it.</span></span>


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a><span data-ttu-id="6e90c-123">Gestion d’un stylet qui a deux extrémités</span><span class="sxs-lookup"><span data-stu-id="6e90c-123">Handling a Pen That Has Two Ends</span></span>

<span data-ttu-id="6e90c-124">Trois gestionnaires d’événements sont définis pour l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) pour les événements [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100))et [Stroke](/previous-versions/ms567622(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="6e90c-124">Three event handlers are defined for the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100)), and [Stroke](/previous-versions/ms567622(v=vs.100)) events.</span></span> <span data-ttu-id="6e90c-125">Chaque gestionnaire d’événements vérifie la propriété [inversée](/previous-versions/ms839525(v=msdn.10)) de l’objet [Cursor](/previous-versions/ms839521(v=msdn.10)) pour identifier la fin du stylet qui est utilisée.</span><span class="sxs-lookup"><span data-stu-id="6e90c-125">Each event handler checks the [Cursor](/previous-versions/ms839521(v=msdn.10)) object's [Inverted](/previous-versions/ms839525(v=msdn.10)) property to see which end of the pen is being used.</span></span> <span data-ttu-id="6e90c-126">Lorsque le stylet est inversé :</span><span class="sxs-lookup"><span data-stu-id="6e90c-126">When the pen is inverted:</span></span>

-   <span data-ttu-id="6e90c-127">La `myInkCollector_CursorDown` méthode rend le trait transparent.</span><span class="sxs-lookup"><span data-stu-id="6e90c-127">The `myInkCollector_CursorDown` method makes the stroke transparent.</span></span>
-   <span data-ttu-id="6e90c-128">La `myInkCollector_NewPackets` méthode efface les traits.</span><span class="sxs-lookup"><span data-stu-id="6e90c-128">The `myInkCollector_NewPackets` method erases strokes.</span></span>
-   <span data-ttu-id="6e90c-129">La `myInkCollector_Stroke` méthode annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="6e90c-129">The `myInkCollector_Stroke` method cancels the event.</span></span> <span data-ttu-id="6e90c-130">Les événements [NewPackets](/previous-versions/ms567621(v=vs.100)) sont générés avant l’événement [Stroke](/previous-versions/ms567622(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="6e90c-130">[NewPackets](/previous-versions/ms567621(v=vs.100)) events are generated prior to the [Stroke](/previous-versions/ms567622(v=vs.100)) event.</span></span>

## <a name="tracking-the-cursor"></a><span data-ttu-id="6e90c-131">Suivi du curseur</span><span class="sxs-lookup"><span data-stu-id="6e90c-131">Tracking the Cursor</span></span>

<span data-ttu-id="6e90c-132">Que l’utilisateur utilise un stylet ou une souris, les événements [MouseMove](/previous-versions/ms567617(v=vs.100)) sont générés.</span><span class="sxs-lookup"><span data-stu-id="6e90c-132">Whether the user is using a pen or a mouse, [MouseMove](/previous-versions/ms567617(v=vs.100)) events are generated.</span></span> <span data-ttu-id="6e90c-133">Le gestionnaire d’événements MouseMove commence par vérifier si le mode actuel est un mode d’effacement et si l’utilisateur appuie sur un bouton de la souris, et ignore l’événement si ces États ne sont pas présents.</span><span class="sxs-lookup"><span data-stu-id="6e90c-133">The MouseMove event handler first checks to determine whether the current mode is an erase mode and if any mouse button is pressed, and ignores the event if these states are not present.</span></span> <span data-ttu-id="6e90c-134">Ensuite, le gestionnaire d’événements convertit les coordonnées en pixels du curseur en coordonnées d’espace d’encre à l’aide de la méthode [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) de l’objet de [convertisseur](/previous-versions/ms828481(v=msdn.10)) , puis appelle l’une des méthodes d’effacement du code en fonction du mode d’effacement actuel.</span><span class="sxs-lookup"><span data-stu-id="6e90c-134">Then, the event handler converts the pixel coordinates for the cursor into ink space coordinates by using the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method, and calls one of the code's erase methods depending on the current erase mode.</span></span>

## <a name="erasing-strokes"></a><span data-ttu-id="6e90c-135">Effacer les traits</span><span class="sxs-lookup"><span data-stu-id="6e90c-135">Erasing Strokes</span></span>

<span data-ttu-id="6e90c-136">La `EraseStrokes` méthode prend l’emplacement du curseur dans l’espace d’encre et génère une collection de traits qui se trouvent dans les `HitTestRadius` unités.</span><span class="sxs-lookup"><span data-stu-id="6e90c-136">The `EraseStrokes` method takes the cursor's location in ink space and generates a collection of strokes that are within `HitTestRadius` units.</span></span> <span data-ttu-id="6e90c-137">Le `currentStroke` paramètre spécifie un objet [Stroke](/previous-versions/ms827842(v=msdn.10)) qui ne doit pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="6e90c-137">The `currentStroke` parameter specifies a [Stroke](/previous-versions/ms827842(v=msdn.10)) object that should not be deleted.</span></span> <span data-ttu-id="6e90c-138">La collection Strokes est ensuite supprimée du collecteur, et le formulaire est redessiné.</span><span class="sxs-lookup"><span data-stu-id="6e90c-138">Then the strokes collection is deleted from the collector, and the form is redrawn.</span></span>


```C++
private void EraseStrokes(Point pt, Stroke currentStroke)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    if (null!=currentStroke && strokesHit.Contains(currentStroke))
    {
        strokesHit.Remove(currentStroke);
    }

    myInkCollector.Ink.DeleteStrokes(strokesHit);

    if (strokesHit.Count > 0)
    {
        this.Refresh();
    }
}
```



## <a name="erasing-at-intersections"></a><span data-ttu-id="6e90c-139">Effacer à l’intersection</span><span class="sxs-lookup"><span data-stu-id="6e90c-139">Erasing at Intersections</span></span>

<span data-ttu-id="6e90c-140">La `EraseAtIntersections` méthode itère au sein de chaque trait qui se trouve dans le rayon de test et génère un tableau d’intersections entre ce trait et tous les autres traits de la collection.</span><span class="sxs-lookup"><span data-stu-id="6e90c-140">The `EraseAtIntersections` method iterates over each stroke that falls within the test radius and generates an array of intersections between that stroke and all the other strokes in the collection.</span></span> <span data-ttu-id="6e90c-141">Si aucune intersection n’est trouvée, alors l’intégralité du trait est supprimée. dans le cas contraire, le point le plus proche du trait vers le point de test se trouve et, à partir de cela, les intersections de chaque côté du point sont situées, décrivant le segment à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6e90c-141">If no intersections are found, then that entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="6e90c-142">La méthode de [fractionnement](/previous-versions/ms828477(v=msdn.10)) de l’objet [Stroke](/previous-versions/ms827842(v=msdn.10)) est utilisée pour séparer le segment du reste du trait, puis le segment est supprimé, ce qui laisse intact le reste du trait.</span><span class="sxs-lookup"><span data-stu-id="6e90c-142">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="6e90c-143">Comme dans `EraseStrokes` , le formulaire est redessiné avant le retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="6e90c-143">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtIntersections(Point pt)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    foreach (Stroke currentStroke in strokesHit)
    {
        float[] intersections = currentStroke.FindIntersections(myInkCollector.Ink.Strokes);
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(intersections[i]);
        ...
    }
    ...
}
```



## <a name="erasing-at-cusps"></a><span data-ttu-id="6e90c-144">Effacement aux sommets</span><span class="sxs-lookup"><span data-stu-id="6e90c-144">Erasing at Cusps</span></span>

<span data-ttu-id="6e90c-145">Pour chaque trait qui se trouve dans le rayon de test, la `EraseAtCusps` méthode récupère le tableau de sommets de la méthode [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) de l’objet [Stroke](/previous-versions/ms827842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="6e90c-145">For each stroke that falls within the test radius, the `EraseAtCusps` method retrieves the array of cusps from the [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) method.</span></span> <span data-ttu-id="6e90c-146">Chaque extrémité du trait est également un sommet. par conséquent, si le trait n’a que deux sommets, le trait entier est supprimé. dans le cas contraire, le point le plus proche du trait vers le point de test se trouve et, à partir de cela, les intersections de chaque côté du point sont situées, décrivant le segment à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6e90c-146">Each end of the stroke is also a cusp, so if the stroke only has two cusps, then the entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="6e90c-147">La méthode de [fractionnement](/previous-versions/ms828477(v=msdn.10)) de l’objet [Stroke](/previous-versions/ms827842(v=msdn.10)) est utilisée pour séparer le segment du reste du trait, puis le segment est supprimé, ce qui laisse intact le reste du trait.</span><span class="sxs-lookup"><span data-stu-id="6e90c-147">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="6e90c-148">Comme dans `EraseStrokes` , le formulaire est redessiné avant le retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="6e90c-148">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtCusps(Point pt)
{
    ...
    strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);
    
    foreach (Stroke currentStroke in strokesHit)
    {
        int[] cusps = currentStroke.PolylineCusps;
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(cusps[i]); 
        myInkCollector.Ink.DeleteStroke(strokeToDelete);
        ...
    }
    ...
}
```



## <a name="closing-the-form"></a><span data-ttu-id="6e90c-149">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="6e90c-149">Closing the Form</span></span>

<span data-ttu-id="6e90c-150">La méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire supprime l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="6e90c-150">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 

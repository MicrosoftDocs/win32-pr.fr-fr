---
description: Cet exemple illustre deux méthodes pour rechercher de l’encre, à partir d’un emplacement à l’écran.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Exemple de test d’atteinte à l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d25e6cbc0ed471384bea0cc1977dd38d3ae4830
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514009"
---
# <a name="ink-hit-test-sample"></a><span data-ttu-id="d2d5b-103">Exemple de test d’atteinte à l’encre</span><span class="sxs-lookup"><span data-stu-id="d2d5b-103">Ink Hit Test Sample</span></span>

<span data-ttu-id="d2d5b-104">Cet exemple illustre deux méthodes pour rechercher de l’encre, à partir d’un emplacement à l’écran.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-104">This sample illustrates two methods to find ink, given a screen location.</span></span>

<span data-ttu-id="d2d5b-105">Les fonctionnalités suivantes sont utilisées dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="d2d5b-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="d2d5b-106">Utilisation d’un collecteur d’encre</span><span class="sxs-lookup"><span data-stu-id="d2d5b-106">Using an ink collector</span></span>
-   <span data-ttu-id="d2d5b-107">Exécution d’un test de positionnement</span><span class="sxs-lookup"><span data-stu-id="d2d5b-107">Performing a hit test</span></span>
-   <span data-ttu-id="d2d5b-108">Localisation du point le plus proche</span><span class="sxs-lookup"><span data-stu-id="d2d5b-108">Locating the nearest point</span></span>

## <a name="accessing-the-ink-api"></a><span data-ttu-id="d2d5b-109">Accès à l’API Ink</span><span class="sxs-lookup"><span data-stu-id="d2d5b-109">Accessing the Ink API</span></span>

<span data-ttu-id="d2d5b-110">Tout d’abord, référencez les classes Tablet PC, situées dans le kit de développement logiciel (SDK) Windows Vista ou Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-110">First, reference the Tablet PC classes, located in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a><span data-ttu-id="d2d5b-111">Gestion des événements de chargement et de peinture de formulaire</span><span class="sxs-lookup"><span data-stu-id="d2d5b-111">Handling Form Load and Paint Events</span></span>

<span data-ttu-id="d2d5b-112">Le gestionnaire d’événements Load du formulaire :</span><span class="sxs-lookup"><span data-stu-id="d2d5b-112">The form's Load event handler:</span></span>

-   <span data-ttu-id="d2d5b-113">Crée un objet [InkCollector](/previous-versions/ms583683(v=vs.100)) , IC, pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-113">Creates an [InkCollector](/previous-versions/ms583683(v=vs.100)) object, ic, for the form.</span></span>
-   <span data-ttu-id="d2d5b-114">Définit la propriété [CollectionMode](/previous-versions/ms836497(v=msdn.10)) de l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) pour ignorer les gestes.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-114">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [CollectionMode](/previous-versions/ms836497(v=msdn.10)) property to ignore gestures.</span></span>
-   <span data-ttu-id="d2d5b-115">Active le [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="d2d5b-115">Enables the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span>
-   <span data-ttu-id="d2d5b-116">Affecte la **valeur true** à la propriété [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) de l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d2d5b-116">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property to **TRUE**.</span></span>


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



<span data-ttu-id="d2d5b-117">Le gestionnaire d’événements Paint du formulaire vérifie le mode de l’application :</span><span class="sxs-lookup"><span data-stu-id="d2d5b-117">The form's Paint event handler checks the application mode:</span></span>

-   <span data-ttu-id="d2d5b-118">En mode HitTest, il peint un cercle autour du curseur.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-118">In the HitTest mode, it paints a circle around the cursor.</span></span> <span data-ttu-id="d2d5b-119">Le stylet actif est défini dans la méthode handleHitTest de l’application.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-119">The active pen is set in the application's handleHitTest method.</span></span>
-   <span data-ttu-id="d2d5b-120">En mode NearestPoint, il peint une ligne rouge entre le curseur et le point le plus proche du curseur.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-120">In the NearestPoint mode, it paints a red line between the cursor and the point nearest the cursor.</span></span> <span data-ttu-id="d2d5b-121">Le point le plus proche est calculé dans la méthode handleNearestPoint de l’application.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-121">The nearest point is calculated in the application's handleNearestPoint method.</span></span>


```C++
if( mode == ApplicationMode.HitTest)
{
    e.Graphics.DrawEllipse(activepen, penPt.X - HitSize/2, penPt.Y - HitSize/2, HitSize, HitSize);
}
else if( mode == ApplicationMode.NearestPoint )
{
    e.Graphics.DrawLine(redPen, penPt, nearestPt);
}
```



<span data-ttu-id="d2d5b-122">Cet exemple présente un algorithme de redessin très simple.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-122">This sample has a very straightforward repaint algorithm.</span></span> <span data-ttu-id="d2d5b-123">Avec sa propriété [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) définie sur **true**, le collecteur d’encre se redessine quand le formulaire est redessiné.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-123">With its [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property set to **TRUE**, the ink collector repaints itself when the form is redrawn.</span></span> <span data-ttu-id="d2d5b-124">Pour simplifier le dessin du formulaire, l’application suit un cadre englobant, la variable de membre invalidateRect, pour la zone dans laquelle Paint est ajouté, ce qui est invalidé chaque fois que le formulaire est redessiné.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-124">To simplify redrawing the form, the application tracks a bounding box, the invalidateRect member variable, for the area where paint is added, which is invalidated each time the form is redrawn.</span></span>

## <a name="handling-menu-events"></a><span data-ttu-id="d2d5b-125">Gestion des événements de menu</span><span class="sxs-lookup"><span data-stu-id="d2d5b-125">Handling Menu Events</span></span>

<span data-ttu-id="d2d5b-126">La commande exit désactive le [InkCollector](/previous-versions/ms583683(v=vs.100)) avant de quitter l’application.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-126">The Exit command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) before exiting the application.</span></span>

<span data-ttu-id="d2d5b-127">La commande Ink met à jour le mode d’application et l’état du menu, active le collecteur d’encre et invalide la zone précédemment peinte du formulaire.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-127">The Ink command updates the application mode and menu status, enables the ink collector, and invalidates the previously painted region of the form.</span></span>

<span data-ttu-id="d2d5b-128">Le test de positionnement et les commandes de point les plus proches modifient le curseur, mettent à jour le mode d’application et l’état du menu, désactivent le collecteur d’encres et invalident la zone précédemment peinte du formulaire.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-128">Both the Hit Test and Nearest Point commands change the cursor, update the application mode and menu status, disable the ink collector, and invalidate the previously painted region of the form.</span></span>

<span data-ttu-id="d2d5b-129">Le clair !</span><span class="sxs-lookup"><span data-stu-id="d2d5b-129">The Clear!</span></span> <span data-ttu-id="d2d5b-130">la commande désactive le [InkCollector](/previous-versions/ms583683(v=vs.100)) lors du remplacement de la propriété [Ink](/previous-versions/ms836505(v=msdn.10)) de l’objet InkCollector par un nouvel objet [Ink](/previous-versions/ms571716(v=vs.100)) , génère un événement de commande Ink et force une actualisation sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-130">command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) while replacing InkCollector object's [Ink](/previous-versions/ms836505(v=msdn.10)) property with a new [Ink](/previous-versions/ms571716(v=vs.100)) object, generates an Ink command event, and forces a refresh on the control.</span></span>

## <a name="handling-mouse-events"></a><span data-ttu-id="d2d5b-131">Gestion des événements de souris</span><span class="sxs-lookup"><span data-stu-id="d2d5b-131">Handling Mouse Events</span></span>

<span data-ttu-id="d2d5b-132">Le gestionnaire d’événements [MouseMove](/previous-versions/ms567617(v=vs.100)) vérifie le mode d’application :</span><span class="sxs-lookup"><span data-stu-id="d2d5b-132">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode:</span></span>

-   <span data-ttu-id="d2d5b-133">En mode Ink, elle ne fait rien, ce qui permet de collecter l’encre normalement par le collecteur d’encre.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-133">In Ink mode, it does nothing, allowing ink to be collected normally by the ink collector.</span></span>
-   <span data-ttu-id="d2d5b-134">En mode HitTest, il envoie les arguments d’événement à la méthode handleHitTest de l’application.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-134">In HitTest mode, it sends the event arguments to the application's handleHitTest method.</span></span>
-   <span data-ttu-id="d2d5b-135">En mode NearestPoint, il envoie les arguments d’événement à la méthode handleNearestPoint de l’application.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-135">In NearestPoint mode, it sends the event arguments to the application's handleNearestPoint method.</span></span>

## <a name="performing-a-hit-test"></a><span data-ttu-id="d2d5b-136">Exécution d’un test de positionnement</span><span class="sxs-lookup"><span data-stu-id="d2d5b-136">Performing a Hit Test</span></span>

<span data-ttu-id="d2d5b-137">La méthode handleHitTest de l’application crée deux points, l’emplacement du curseur et un point atteignent les pixels éloignés du curseur, puis convertit ces deux points de pixels en coordonnées d’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-137">The application's handleHitTest method creates two points, the cursor location and a point HitSize pixels distant from the cursor, and then converts these two points from pixels to ink space coordinates.</span></span>


```C++
penPt = new Point(e.X, e.Y);
Point pt2 = new Point(e.X, e.Y);
Point pt3 = new Point(e.X + HitSize/2, e.Y);

using (Graphics g = CreateGraphics())
{
    ic.Renderer.PixelToInkSpace(g, ref pt1);
    ic.Renderer.PixelToInkSpace(g, ref pt2);
}
```



<span data-ttu-id="d2d5b-138">Ensuite, l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) utilise la méthode [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) pour rechercher tous les traits qui se trouvent dans PT3. X-pt2. Unités d’espace d’encre X du curseur, pt2.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-138">Then, the [InkCollector](/previous-versions/ms583683(v=vs.100)) object uses the [Microsoft.Ink.Ink.HitTest()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to find any strokes that are within pt3.X - pt2.X ink space units of the cursor, pt2.</span></span>


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



<span data-ttu-id="d2d5b-139">La méthode handleHitTest définit ensuite la couleur du stylet selon que des traits ont été trouvés, invalide la région invalidateRect, calcule une nouvelle région dans laquelle le cercle de test de positionnement est dessiné, puis invalide la nouvelle région.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-139">The handleHitTest method then sets the pen color based on whether strokes were found, invalidates the invalidateRect region, calculates a new region that the hit test circle is drawn in, and then invalidates the new region.</span></span>

## <a name="locating-the-nearest-point"></a><span data-ttu-id="d2d5b-140">Localisation du point le plus proche</span><span class="sxs-lookup"><span data-stu-id="d2d5b-140">Locating the Nearest Point</span></span>

<span data-ttu-id="d2d5b-141">La méthode handleNearestPoint de l’application crée deux points égaux à l’emplacement du curseur, l’un de ces points, PT, est converti en espace d’encre et utilisé dans l’appel à la méthode NearestPoint [de l’objet Ink de l'](/previous-versions/ms583683(v=vs.100))objet [Ink](/previous-versions/ms836505(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="d2d5b-141">The application's handleNearestPoint method creates two points both equal to the cursor's location, one of these points, pt, is converted to ink space and used in the call to the NearestPoint method of the [InkCollector](/previous-versions/ms583683(v=vs.100))'s [Ink](/previous-versions/ms836505(v=msdn.10)) object.</span></span> <span data-ttu-id="d2d5b-142">La méthode NearestPoint retourne l’objet [Stroke](/previous-versions/ms827842(v=msdn.10)) le plus proche du point, puis définit le paramètre de sortie de l’index à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-142">The NearestPoint method returns the [Stroke](/previous-versions/ms827842(v=msdn.10)) object closest to the point, and sets the floating point index output parameter.</span></span>


```C++
using (Graphics g = CreateGraphics())
{

   // Remeber pen location
    Point inkPenPt = new Point(e.X, e.Y);

    // Convert the pen location into a location in ink space
    ic.Renderer.PixelToInkSpace(g, ref inkPenPt);

    // ...

    float fIndex;
    Stroke stroke = ic.Ink.NearestPoint(inkPenPt, out fIndex);
```



<span data-ttu-id="d2d5b-143">Si aucun trait n’est présent, la méthode NearestPoint retourne la **valeur null** et l’emplacement du curseur est utilisé comme point le plus proche.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-143">If no strokes are present, the NearestPoint method returns **NULL**, and the cursor location is used as the nearest point.</span></span> <span data-ttu-id="d2d5b-144">Dans le cas contraire, l’emplacement sur le trait qui correspond à l’index à virgule flottante est calculé.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-144">Otherwise, the location on the stroke that corresponds to the floating point index is calculated.</span></span>

<span data-ttu-id="d2d5b-145">Les coordonnées de point les plus proches sont ensuite converties en pixels à partir de l’espace d’encre, la méthode handleNearestPoint invalide ensuite la région invalidateRect, calcule une nouvelle région à laquelle est tracée la ligne au point le plus proche, et invalide également la nouvelle région.</span><span class="sxs-lookup"><span data-stu-id="d2d5b-145">The nearest point coordinates are then converted to pixels from ink space, The handleNearestPoint method then invalidates the invalidateRect region, calculates a new region the line to the nearest point is drawn in, and invalidates the new region, too.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="d2d5b-146">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="d2d5b-146">Closing the Form</span></span>

<span data-ttu-id="d2d5b-147">La méthode dispose du formulaire supprime l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d2d5b-147">The form's Dispose method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 

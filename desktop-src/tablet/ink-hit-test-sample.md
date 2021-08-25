---
description: Cet exemple illustre deux méthodes pour rechercher de l’encre, à partir d’un emplacement à l’écran.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Exemple de test d’atteinte à l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995bd6f14b4a0a014452ae9392fa744ab93f01f9047c79e5dc30652c243473db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713079"
---
# <a name="ink-hit-test-sample"></a>Exemple de test d’atteinte à l’encre

Cet exemple illustre deux méthodes pour rechercher de l’encre, à partir d’un emplacement à l’écran.

Les fonctionnalités suivantes sont utilisées dans cet exemple :

-   Utilisation d’un collecteur d’encre
-   Exécution d’un test de positionnement
-   Localisation du point le plus proche

## <a name="accessing-the-ink-api"></a>Accès à l’API Ink

tout d’abord, référencez les classes Tablet pc, situées dans le kit de développement logiciel (SDK) Windows Vista ou Windows XP Tablet pc Edition.


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>gestion du chargement de formulaire et des événements de Paint

Le gestionnaire d’événements Load du formulaire :

-   Crée un objet [InkCollector](/previous-versions/ms583683(v=vs.100)) , IC, pour le formulaire.
-   Définit la propriété [CollectionMode](/previous-versions/ms836497(v=msdn.10)) de l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) pour ignorer les gestes.
-   Active le [InkCollector](/previous-versions/ms583683(v=vs.100)).
-   Affecte la **valeur true** à la propriété [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) de l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) .


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



le gestionnaire d’événements Paint du formulaire vérifie le mode de l’application :

-   En mode HitTest, il peint un cercle autour du curseur. Le stylet actif est défini dans la méthode handleHitTest de l’application.
-   En mode NearestPoint, il peint une ligne rouge entre le curseur et le point le plus proche du curseur. Le point le plus proche est calculé dans la méthode handleNearestPoint de l’application.


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



Cet exemple présente un algorithme de redessin très simple. Avec sa propriété [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) définie sur **true**, le collecteur d’encre se redessine quand le formulaire est redessiné. Pour simplifier le dessin du formulaire, l’application suit un cadre englobant, la variable de membre invalidateRect, pour la zone dans laquelle Paint est ajouté, ce qui est invalidé chaque fois que le formulaire est redessiné.

## <a name="handling-menu-events"></a>Gestion des événements de menu

La commande exit désactive le [InkCollector](/previous-versions/ms583683(v=vs.100)) avant de quitter l’application.

La commande Ink met à jour le mode d’application et l’état du menu, active le collecteur d’encre et invalide la zone précédemment peinte du formulaire.

Le test de positionnement et les commandes de point les plus proches modifient le curseur, mettent à jour le mode d’application et l’état du menu, désactivent le collecteur d’encres et invalident la zone précédemment peinte du formulaire.

Le clair ! la commande désactive le [InkCollector](/previous-versions/ms583683(v=vs.100)) lors du remplacement de la propriété [Ink](/previous-versions/ms836505(v=msdn.10)) de l’objet InkCollector par un nouvel objet [Ink](/previous-versions/ms571716(v=vs.100)) , génère un événement de commande Ink et force une actualisation sur le contrôle.

## <a name="handling-mouse-events"></a>Gestion des événements de souris

Le gestionnaire d’événements [MouseMove](/previous-versions/ms567617(v=vs.100)) vérifie le mode d’application :

-   En mode Ink, elle ne fait rien, ce qui permet de collecter l’encre normalement par le collecteur d’encre.
-   En mode HitTest, il envoie les arguments d’événement à la méthode handleHitTest de l’application.
-   En mode NearestPoint, il envoie les arguments d’événement à la méthode handleNearestPoint de l’application.

## <a name="performing-a-hit-test"></a>Exécution d’un test de positionnement

La méthode handleHitTest de l’application crée deux points, l’emplacement du curseur et un point atteignent les pixels éloignés du curseur, puis convertit ces deux points de pixels en coordonnées d’espace d’encre.


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



Ensuite, l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) utilise la méthode [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) pour rechercher tous les traits qui se trouvent dans PT3. X-pt2. Unités d’espace d’encre X du curseur, pt2.


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



La méthode handleHitTest définit ensuite la couleur du stylet selon que des traits ont été trouvés, invalide la région invalidateRect, calcule une nouvelle région dans laquelle le cercle de test de positionnement est dessiné, puis invalide la nouvelle région.

## <a name="locating-the-nearest-point"></a>Localisation du point le plus proche

La méthode handleNearestPoint de l’application crée deux points égaux à l’emplacement du curseur, l’un de ces points, PT, est converti en espace d’encre et utilisé dans l’appel à la méthode NearestPoint [de l’objet Ink de l'](/previous-versions/ms583683(v=vs.100))objet [Ink](/previous-versions/ms836505(v=msdn.10)) . La méthode NearestPoint retourne l’objet [Stroke](/previous-versions/ms827842(v=msdn.10)) le plus proche du point, puis définit le paramètre de sortie de l’index à virgule flottante.


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



Si aucun trait n’est présent, la méthode NearestPoint retourne la **valeur null** et l’emplacement du curseur est utilisé comme point le plus proche. Dans le cas contraire, l’emplacement sur le trait qui correspond à l’index à virgule flottante est calculé.

Les coordonnées de point les plus proches sont ensuite converties en pixels à partir de l’espace d’encre, la méthode handleNearestPoint invalide ensuite la région invalidateRect, calcule une nouvelle région à laquelle est tracée la ligne au point le plus proche, et invalide également la nouvelle région.

## <a name="closing-the-form"></a>Fermeture du formulaire

La méthode dispose du formulaire supprime l’objet [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 

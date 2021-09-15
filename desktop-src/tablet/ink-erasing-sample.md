---
description: 'Cette application s’appuie sur l’exemple d’exemple de collection Ink en montrant la suppression des traits d’encre. L’exemple fournit à l’utilisateur un menu avec quatre modes d’accès : activé pour l’écriture manuscrite, en effaçant au sommet, en effaçant à l’intersection et en effaçant les traits.'
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Exemple d’effacement d’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46040781d778f936815e57ba96b4ca516617d9a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523228"
---
# <a name="ink-erasing-sample"></a>Exemple d’effacement d’encre

Cette application s’appuie sur l’exemple d’exemple de [collection Ink](ink-collection-sample.md) en montrant la suppression des traits d’encre. L’exemple fournit à l’utilisateur un menu avec quatre modes d’accès : activé pour l’écriture manuscrite, en effaçant au sommet, en effaçant à l’intersection et en effaçant les traits.

En mode activé pour l’écriture manuscrite, l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) collecte l’encre comme indiqué dans [exemple de collection d’encres](ink-collection-sample.md).

En mode d’effacement, les segments de traits d’encre existants que l’utilisateur touche avec le curseur sont effacés. En outre, les sommets ou les intersections peuvent être signalés par un cercle rouge.

Les parties les plus intéressantes de cet exemple se trouvent dans le `InkErase` Gestionnaire d’événements du formulaire `OnPaint` et dans les fonctions d’effacement qui sont appelées à partir du gestionnaire d’événements du formulaire `OnMouseMove` .

## <a name="circling-the-cusps-and-intersections"></a>Cercle des sommets et des intersections

Le gestionnaire d' `OnPaint` événements du formulaire peint d’abord les traits, et selon le mode d’application, peut trouver et marquer toutes les fronces ou les intersections avec un petit cercle rouge. Un Sommet marque le point où un trait modifie le sens brusquement. Une intersection marque un point où un trait entre en intersection avec lui-même ou un autre trait.

l’événement [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) se produit chaque fois qu’un contrôle est redessiné.

> [!Note]  
> L’exemple force le formulaire à se redessiner chaque fois qu’un trait est effacé, ou lorsque le mode d’application change, à l’aide de la méthode [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) du formulaire.

 


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



Dans `PaintCusps` , le code itère au sein de chaque fronce dans chaque trait et dessine un cercle rouge autour. La propriété [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) du trait retourne les index des points d’un des qui correspondent aux sommets. Notez également la méthode [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) de l’objet de [convertisseur](/previous-versions/ms828481(v=msdn.10)) , qui convertit le point en coordonnées pertinentes pour la méthode DrawEllipse.


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



Dans `PaintIntersections` , le code itère au sein de chaque trait pour rechercher ses intersections avec le jeu entier de traits. Notez que la méthode [FindIntersections](/previous-versions/ms827856(v=msdn.10)) du trait est passée à une collection [Strokes](/previous-versions/ms827799(v=msdn.10)) et retourne un tableau de valeurs d’index à virgule flottante représentant les intersections. Le code calcule ensuite une coordonnée X-Y pour chaque intersection et dessine un cercle rouge autour.


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a>Gestion d’un stylet qui a deux extrémités

Trois gestionnaires d’événements sont définis pour l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) pour les événements [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100))et [Stroke](/previous-versions/ms567622(v=vs.100)) . Chaque gestionnaire d’événements vérifie la propriété [inversée](/previous-versions/ms839525(v=msdn.10)) de l’objet [Cursor](/previous-versions/ms839521(v=msdn.10)) pour identifier la fin du stylet qui est utilisée. Lorsque le stylet est inversé :

-   La `myInkCollector_CursorDown` méthode rend le trait transparent.
-   La `myInkCollector_NewPackets` méthode efface les traits.
-   La `myInkCollector_Stroke` méthode annule l’événement. Les événements [NewPackets](/previous-versions/ms567621(v=vs.100)) sont générés avant l’événement [Stroke](/previous-versions/ms567622(v=vs.100)) .

## <a name="tracking-the-cursor"></a>Suivi du curseur

Que l’utilisateur utilise un stylet ou une souris, les événements [MouseMove](/previous-versions/ms567617(v=vs.100)) sont générés. Le gestionnaire d’événements MouseMove commence par vérifier si le mode actuel est un mode d’effacement et si l’utilisateur appuie sur un bouton de la souris, et ignore l’événement si ces États ne sont pas présents. Ensuite, le gestionnaire d’événements convertit les coordonnées en pixels du curseur en coordonnées d’espace d’encre à l’aide de la méthode [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) de l’objet de [convertisseur](/previous-versions/ms828481(v=msdn.10)) , puis appelle l’une des méthodes d’effacement du code en fonction du mode d’effacement actuel.

## <a name="erasing-strokes"></a>Effacer les traits

La `EraseStrokes` méthode prend l’emplacement du curseur dans l’espace d’encre et génère une collection de traits qui se trouvent dans les `HitTestRadius` unités. Le `currentStroke` paramètre spécifie un objet [Stroke](/previous-versions/ms827842(v=msdn.10)) qui ne doit pas être supprimé. La collection Strokes est ensuite supprimée du collecteur, et le formulaire est redessiné.


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



## <a name="erasing-at-intersections"></a>Effacer à l’intersection

La `EraseAtIntersections` méthode itère au sein de chaque trait qui se trouve dans le rayon de test et génère un tableau d’intersections entre ce trait et tous les autres traits de la collection. Si aucune intersection n’est trouvée, alors l’intégralité du trait est supprimée. dans le cas contraire, le point le plus proche du trait vers le point de test se trouve et, à partir de cela, les intersections de chaque côté du point sont situées, décrivant le segment à supprimer.

La méthode de [fractionnement](/previous-versions/ms828477(v=msdn.10)) de l’objet [Stroke](/previous-versions/ms827842(v=msdn.10)) est utilisée pour séparer le segment du reste du trait, puis le segment est supprimé, ce qui laisse intact le reste du trait. Comme dans `EraseStrokes` , le formulaire est redessiné avant le retour de la méthode.


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



## <a name="erasing-at-cusps"></a>Effacement aux sommets

Pour chaque trait qui se trouve dans le rayon de test, la `EraseAtCusps` méthode récupère le tableau de sommets de la méthode [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) de l’objet [Stroke](/previous-versions/ms827842(v=msdn.10)) . Chaque extrémité du trait est également un sommet. par conséquent, si le trait n’a que deux sommets, le trait entier est supprimé. dans le cas contraire, le point le plus proche du trait vers le point de test se trouve et, à partir de cela, les intersections de chaque côté du point sont situées, décrivant le segment à supprimer.

La méthode de [fractionnement](/previous-versions/ms828477(v=msdn.10)) de l’objet [Stroke](/previous-versions/ms827842(v=msdn.10)) est utilisée pour séparer le segment du reste du trait, puis le segment est supprimé, ce qui laisse intact le reste du trait. Comme dans `EraseStrokes` , le formulaire est redessiné avant le retour de la méthode.


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



## <a name="closing-the-form"></a>Fermeture du formulaire

La méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire supprime l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .

 

 

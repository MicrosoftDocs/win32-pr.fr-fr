---
description: L’État graphique &\# 8212 ; la région de découpage, les transformations et les paramètres de qualité &\# 8212 ; est stocké dans un objet Graphics.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Conteneurs Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524289"
---
# <a name="graphics-containers"></a>Conteneurs Graphics

L’état des graphiques (région de découpage, transformations et paramètres de qualité) est stocké dans un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Windows GDI+ vous permet de remplacer ou d’augmenter temporairement une partie de l’état d’un objet **graphics** à l’aide d’un conteneur. Vous démarrez un conteneur en appelant la méthode [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) d’un objet **Graphics** , et vous terminez un conteneur en appelant la méthode [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) . Entre **Graphics :: BeginContainer** et **Graphics :: EndContainer**, les modifications d’État que vous apportez à l’objet **Graphics** appartiennent au conteneur et ne remplacent pas l’état existant de l’objet **Graphics** .

L’exemple suivant crée un conteneur dans un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . La transformation universelle de l’objet **Graphics** est une translation de 200 unités à droite, et la transformation universelle du conteneur est une translation de 100 unités vers le haut.


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



Notez que dans l’exemple précédent, l’instruction `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` faite entre les appels à [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) et [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produit un rectangle différent de la même instruction que celle effectuée après l’appel à **Graphics :: EndContainer**. Seule la traduction horizontale s’applique à l’appel **DrawRectangle** effectué en dehors du conteneur. Les deux transformations, à savoir la translation horizontale de 200 unités et la translation verticale de 100 unités, s’appliquent aux [**graphiques ::D appel rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) effectué à l’intérieur du conteneur. L’illustration suivante montre les deux rectangles.

![capture d’écran d’une fenêtre avec deux rectangles dessinés avec un stylet bleu, l’un placé au-dessus de l’autre](images/aboutgdip05-art17.png)

Les conteneurs peuvent être imbriqués dans des conteneurs. L’exemple suivant crée un conteneur dans un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et un autre conteneur dans le premier conteneur. La transformation universelle de l’objet **Graphics** est une translation de 100 unités sur la direction x et de 80 unités sur l’axe y. La transformation universelle du premier conteneur est une rotation à 30 degrés. La transformation universelle du deuxième conteneur est une mise à l’échelle par un facteur de 2 dans la direction x. Un appel à la méthode [**Graphics ::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) est effectué à l’intérieur du deuxième conteneur.


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



L’illustration suivante montre l’ellipse.

![capture d’écran d’une fenêtre qui contient une ellipse bleue pivotée avec son centre étiqueté comme (100, 80)](images/aboutgdip05-art18.png)

Notez que les trois transformations s’appliquent aux [**graphiques ::D appel rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) effectué dans le deuxième conteneur (le plus à l’intérieur). Notez également l’ordre des transformations : première échelle, faire pivoter, puis traduire. La transformation la plus profonde est appliquée en premier, et la transformation la plus à l’extérieur est appliquée en dernier.

Toute propriété d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) peut être définie à l’intérieur d’un conteneur (entre les appels à [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) et [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). Par exemple, une zone de découpage peut être définie à l’intérieur d’un conteneur. Tout dessin effectué à l’intérieur du conteneur sera limité à la zone de découpage de ce conteneur et sera également limité aux régions de découpage de tous les conteneurs externes et à la zone de découpage de l’objet **Graphics** lui-même.

Les propriétés abordées jusqu’à présent (la transformation universelle et la région de découpage) sont combinées par des conteneurs imbriqués. D’autres propriétés sont remplacées temporairement par un conteneur imbriqué. Par exemple, si vous définissez le mode de lissage sur SmoothingModeAntiAlias dans un conteneur, toutes les méthodes de dessin appelées à l’intérieur de ce conteneur utilisent le mode de lissage anticrénelage, mais les méthodes de dessin appelées après [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) utilisent le mode de lissage qui était en place avant l’appel à [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

Pour obtenir un autre exemple de la combinaison des transformations universelles d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un conteneur, supposons que vous souhaitiez dessiner un œil et le placer à différents emplacements sur une séquence de visages. L’exemple suivant dessine un œil centré sur l’origine du système de coordonnées.


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



L’illustration suivante montre l’œil et les axes de coordonnées.

![Illustration montrant un œil composé de trois ellipses : une pour le plan, un iris et un élève](images/aboutgdip05-art19.png)

La fonction DrawEye, définie dans l’exemple précédent, reçoit l’adresse d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et crée immédiatement un conteneur dans cet objet **Graphics** . Ce conteneur isole tout code qui appelle la fonction DrawEye des paramètres de propriété effectués lors de l’exécution de la fonction DrawEye. Par exemple, le code de la fonction DrawEye définit la zone de découpage de l’objet **Graphics** , mais lorsque DrawEye retourne le contrôle à la routine appelante, la zone de découpage est telle qu’elle était avant l’appel à DrawEye.

L’exemple suivant dessine trois ellipses (faces), chacune avec un œil à l’intérieur.


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



L’illustration suivante montre les trois ellipses.

![capture d’écran d’une fenêtre avec trois ellipses, chacune contenant un œil à une taille et une rotation différentes](images/aboutgdip05-art20.png)

Dans l’exemple précédent, toutes les ellipses sont dessinées avec l’appel `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , qui dessine une ellipse centrée sur l’origine du système de coordonnées. Les ellipses sont déplacées hors de l’angle supérieur gauche de la zone cliente en définissant la transformation universelle de l’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . L’instruction fait en sorte que la première ellipse soit centrée sur (100, 100). L’instruction amène le centre de la deuxième ellipse à 100 unités à droite du centre de la première ellipse. De même, le centre de la troisième ellipse est 100 unités à droite du centre de la deuxième ellipse.

Les conteneurs de l’exemple précédent sont utilisés pour transformer l’œil par rapport au centre d’une ellipse donnée. Le premier œil est dessiné au centre de l’ellipse sans transformation, de sorte que l’appel DrawEye n’est pas à l’intérieur d’un conteneur. Le deuxième œil fait pivoter 40 degrés et a dessiné 30 unités au-dessus du centre de l’ellipse, de sorte que la fonction DrawEye et les méthodes qui définissent la transformation sont appelées à l’intérieur d’un conteneur. Le troisième œil est étiré et pivoté et dessiné au centre de l’ellipse. Comme pour le deuxième œil, la fonction DrawEye et les méthodes qui définissent la transformation sont appelées à l’intérieur d’un conteneur.

 

 

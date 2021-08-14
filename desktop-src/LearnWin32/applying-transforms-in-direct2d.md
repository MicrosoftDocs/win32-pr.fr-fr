---
title: Application de transformations dans Direct2D
description: Application de transformations dans Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab83cb9a7981ada944de07e362c2f568889a84a4f90f2171150fbab948ab3a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388489"
---
# <a name="applying-transforms-in-direct2d"></a>Application de transformations dans Direct2D

En [dessin avec Direct2D](drawing-with-direct2d.md), nous avons vu que la méthode [**ID2D1RenderTarget :: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) dessine une ellipse alignée sur les axes x et y. Mais supposons que vous souhaitiez dessiner une ellipse inclinée à un angle ?

![image qui affiche une ellipse inclinée.](images/graphics16.png)

À l’aide de transformations, vous pouvez modifier une forme des manières suivantes.

-   Rotation autour d’un point.
-   Mise à l’échelle
-   Translation (déplacement dans la direction X ou Y).
-   Skew (également appelé *cisaillement*).

Une transformation est une opération mathématique qui mappe un ensemble de points à un nouvel ensemble de points. Par exemple, le diagramme suivant montre un triangle pivoté autour du point P3. Une fois la rotation appliquée, le point P1 est mappé à P1 ', le point P2 est mappé à P2 'et le point P3 est mappé à lui-même.

![diagramme qui montre une rotation autour d’un point.](images/graphics17.png)

Les transformations sont implémentées à l’aide de matrices. Toutefois, vous n’avez pas besoin de comprendre les mathématiques des matrices pour pouvoir les utiliser. Si vous souhaitez en savoir plus sur les mathématiques, consultez [annexe : matrice transformations](appendix--matrix-transforms.md).

Pour appliquer une transformation dans Direct2D, appelez la méthode [**ID2D1RenderTarget :: setTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) . Cette méthode prend une structure [**d2d1 \_ Matrix \_ matrice \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) qui définit la transformation. Vous pouvez initialiser cette structure en appelant des méthodes sur la classe [**d2d1 :: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Cette classe contient des méthodes statiques qui retournent une matrice pour chaque type de transformation :

-   [**Matrix3x2F :: rotation**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   [**Matrix3x2F :: Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))
-   [**Matrix3x2F :: translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))
-   [**Matrix3x2F :: Skew**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

Par exemple, le code suivant applique une rotation à 20 degrés autour du point (100, 100).


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

La transformation est appliquée à toutes les opérations de dessin ultérieures jusqu’à ce que vous rappeliez [**setTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) . Pour supprimer la transformation actuelle, appelez **setTransform** avec la matrice d’identité. Pour créer la matrice d’identité, appelez la fonction [**Matrix3x2F :: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) .


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a>Dessin des aiguilles de l’horloge

Nous allons mettre en place des transformations en convertissant notre programme Circle en horloge analogique. Nous pouvons faire cela en ajoutant des lignes pour les mains.

![capture d’écran du programme d’horloge analogique.](images/graphics18.png)

Au lieu de calculer les coordonnées des lignes, nous pouvons calculer l’angle, puis appliquer une transformation de rotation. Le code suivant illustre une fonction qui dessine une main. Le paramètre *fAngle* donne l’angle de la main, en degrés.

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

Ce code dessine une ligne verticale, en commençant par le centre de l’horloge et en se terminant au point de *terminaison* du point. La ligne pivote autour du centre de l’ellipse en appliquant une transformation de rotation. Le point central de la rotation est le centre de l’ellipse qui forme la face de l’horloge.

![diagramme qui affiche la rotation de la main d’horloge.](images/graphics19.png)

Le code suivant montre comment le cadran entier est dessiné.

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

vous pouvez télécharger le projet Visual Studio complet à partir de l' [exemple d’horloge Direct2D](direct2d-clock-sample.md). (Juste pour le plaisir, la version de téléchargement ajoute un gradiant radial à la face de l’horloge.)

## <a name="combining-transforms"></a>Combinaison de transformations

Les quatre transformations de base peuvent être combinées en multipliant au moins deux matrices. Par exemple, le code suivant combine une rotation et une translation.

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

La classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fournit l' [**opérateur \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) pour la multiplication de matrice. L’ordre dans lequel vous multipliez les matrices est important. La définition d’une transformation (M × N) signifie « Apply M First, suivi de N ». Par exemple, voici la rotation suivie d’une traduction :

![diagramme qui affiche la rotation suivie d’une traduction.](images/graphics20.png)

Voici le code de cette transformation :

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

Comparez maintenant cette transformation à une transformation dans l’ordre inverse, à la translation suivie de la rotation.

![diagramme qui affiche la translation suivie d’une rotation.](images/graphics21.png)

La rotation est effectuée autour du centre du rectangle d’origine. Voici le code de cette transformation.

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

Comme vous pouvez le voir, les matrices sont identiques, mais l’ordre des opérations a changé. Cela se produit parce que la multiplication de matrice n’est pas commutative : M × N ≠ N × M.

## <a name="next"></a>Suivant

[Annexe : transformations de matrice](appendix--matrix-transforms.md)
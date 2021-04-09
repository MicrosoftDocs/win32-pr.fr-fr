---
title: Vue d'ensemble des transformations
description: Présente l’API de transformation Microsoft Direct2D pour Windows 7. Direct2D permet aux développeurs Win32 d’effectuer des transformations graphiques 2D.
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Direct2D, vue d’ensemble des transformations
- Direct2D, systèmes de coordonnées
- Direct2D, cibles de rendu
- Direct2D, transformations 2D
- transformations 2D
- transformations, à propos de
- transformations, cibles de rendu
- transformations, objets
- cibles de rendu, transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f3678f7b194f0f0188ed907a63737a97e9e58c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941038"
---
# <a name="transforms-overview"></a>Vue d'ensemble des transformations

Cette rubrique décrit les principes de base des transformations Direct2D et comprend des exemples de diverses transformations. Il contient les éléments suivants :

-   [Qu’est-ce qu’une transformation Direct2D ?](#what-is-a-direct2d-transform)
-   [Espace de coordonnées Direct2D](#the-direct2d-coordinate-space)
-   [Création de matrices de transformation](#creating-transformation-matrices)
-   [Rendu des transformations cibles](#rendering-target-transforms)
-   [Transformations de pinceau](#brush-transforms)
-   [Transformations géométriques](#geometry-transforms)
-   [Comment une transformation de cible de rendu affecte les clips](#how-a-render-target-transform-affects-clips)
-   [Résumé](#summary)
-   [Rubriques connexes](#related-topics)

## <a name="what-is-a-direct2d-transform"></a>Qu’est-ce qu’une transformation Direct2D ?

Une transformation spécifie comment mapper les points d’un objet d’un espace de coordonnées à un autre ou d’une position à une autre dans le même espace de coordonnées. Ce mappage est décrit par une matrice de transformation, définie sous la forme d’une collection de trois lignes avec trois colonnes de valeurs FLOAT, comme indiqué dans le tableau suivant.



|                 |                 |     |
|-----------------|-----------------|-----|
| M11Default : 1,0 | M12Default : 0,0 | 0.0 |
| M21Default : 0,0 | M22Default : 1,0 | 0.0 |
| M31OffsetX : 0,0 | M32OffsetY : 0,0 | 1.0 |



 

Dans cette matrice, les membres M11, M12, M21 et M22 définissent une transformation linéaire qui peut mettre à l’échelle, faire pivoter ou incliner un objet. les éléments OffsetX et OffsetY définissent la traduction à appliquer une fois la transformation linéaire effectuée. Pour les transformations affines, les valeurs de la troisième colonne sont toujours 0,0, 0,0 et 1,0.

Comme Direct2D ne prend en charge que les transformations affinées (linéaires), sa matrice de transformation est définie en tant que matrice 3 par 2, en omettant la troisième colonne de la matrice de transformation précédente. Le tableau suivant montre la disposition de la matrice de transformation Direct2D.



|                 |                 |
|-----------------|-----------------|
| M11Default : 1,0 | M12Default : 0,0 |
| M21Default : 0,0 | M22Default : 1,0 |
| M31OffsetX : 0,0 | M32OffsetY : 0,0 |



 

Dans Direct2D, cette matrice 3 par 2 est représentée par la structure matrice de la [**\_ \_ matrice d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . Pour simplifier les opérations de matrice courantes, Direct2D fournit également une classe nommée [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f), qui est dérivée de la structure matrice de la **\_ matrice \_ d2d1** .

Le constructeur par défaut pour [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) laisse l’objet non initialisé. Pour récupérer une matrice d’identité, utilisez [**Matrix3x2F :: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix).

Lorsqu’une transformation d’identité est appliquée à un objet, elle ne modifie pas la position, la forme ou la taille de l’objet. Elle est similaire à la façon dont la multiplication d’un nombre par 1 ne change pas le nombre. En d’autres termes, la transformation d’identité laisse les coordonnées des points seuls et ne déplace pas les points vers une nouvelle position. Toute transformation autre que la transformation d’identité modifie la position, la forme et/ou la taille des objets.

Les transformations sont des coordonnées, et il est important de comprendre l’espace de coordonnées Direct2D pour comprendre l’utilisation des transformations.

## <a name="the-direct2d-coordinate-space"></a>Espace de coordonnées Direct2D

Direct2D utilise un espace de coordonnées droitier. autrement dit, les valeurs positives de l’axe des x augmentent vers la droite et les valeurs positives de l’axe des y augmentent vers le bas. Tout ce qui se trouve sur l’écran est positionné par rapport à l’origine, qui est le point où les axes x et y se croisent (0,0), comme indiqué dans l’illustration suivante. Les cibles de rendu Direct2D utilisent cet espace de coordonnées.

![illustration de l’axe x et de l’axe y d’un espace de coordonnées droitier](images/coordinatespace.png)

En manipulant des valeurs dans une matrice de transformation, vous pouvez faire pivoter, mettre à l’échelle, incliner et déplacer (translater) un objet. Par exemple, si vous définissez OffsetX sur 100 et OffsetY sur 200, vous déplacez l’objet vers la droite de 100 pixels et de 200 pixels.

Pour afficher l’effet du déplacement d’un objet, vous devez appliquer la transformation de translation pour restituer des cibles, des pinceaux ou des géométries. L’application d’une transformation aux cibles de rendu affecte la totalité de l’écran, tandis que l’application d’une transformation à un pinceau ou une géométrie affecte uniquement ce pinceau ou cette géométrie spécifique. Pour créer une matrice de transformation, utilisez la classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .

## <a name="creating-transformation-matrices"></a>Création de matrices de transformation

Pour créer des transformations de rotation, de mise à l’échelle, d’inclinaison et de translation, la classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fournit les méthodes statiques indiquées dans le tableau suivant. L’exemple de colonne de la table contient des liens vers les rubriques de procédures qui montrent comment utiliser chaque méthode de transformation.



| Méthode                                                                   | Description                                                                                                     | Exemple                                            | Illustration                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**matrix3x2f :: Rotate**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | crée une transformation de rotation qui a l’angle et le point central spécifiés.                                | [Comment faire pivoter un objet](how-to-rotate.md)       | ![illustration d’un carré pivoté de 45 degrés dans le sens des aiguilles d’une montre autour du centre du carré d’origine](images/rotate-ovw.png)                 |
| [**matrix3x2f :: Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)) | crée une transformation d’échelle qui a les facteurs d’échelle et le point central spécifiés.                           | [mise à l’échelle d’un objet](how-to-scale.md)         | ![illustration d’un 130% à l’échelle carrée](images/scale-ovw.png)                                                                           |
| [**matrix3x2f :: Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | crée une transformation d’inclinaison qui a les valeurs de l’axe des x et de l’axe des y et du point central spécifiés.                 | [comment incliner un objet](how-to-skew.md)           | ![illustration d’un carré incliné de 30 degrés dans le sens inverse des aiguilles d’une montre à partir de l’axe y](images/skew-ovw.png)                                     |
| [**matrix3x2f :: translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))                | crée une transformation de traduction et spécifie les déplacements dans la direction de l’axe x et de l’axe y. | [Comment traduire un objet](how-to-translate.md) | ![illustration d’un carré déplacé de 20 unités le long de l’axe x positif et de 10 unités le long de l’axe y positif](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a>Rendu des transformations cibles

Une cible de rendu est une ressource qui hérite de l’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Il crée des ressources pour le dessin et effectue des opérations de dessin réelles. Il fournit également des méthodes pour transformer l’espace de coordonnées. Vous pouvez appeler la méthode [**ID2D1RenderTarget :: setTransform**](id2d1rendertarget-settransform.md) pour appliquer la transformation spécifiée à la cible de rendu. Toutes les opérations de dessin suivantes se produisent dans l’espace transformé.

Pour afficher le contenu, utilisez les méthodes de dessin de la cible de rendu. Avant de commencer le dessin, appelez la méthode [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Pour terminer le rendu du contenu, appelez la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Pour obtenir un exemple, consultez Guide pratique [pour appliquer plusieurs transformations à un objet](how-to-apply-multiple-transforms.md).

## <a name="brush-transforms"></a>Transformations de pinceau

Vous pouvez ajuster la transformation sur le pinceau en appelant [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)). Pour cette transformation, vous pouvez considérer le pinceau comme un grand morceau de papier et les différentes primitives de rendu (texte, géométrie, Rectangle, etc.) en tant que stencils. Lorsque vous ajustez la transformation du pinceau, c’est comme si vous détouriez la grande partie du papier sous le gabarit, sans modifier la position du gabarit lui-même. Vous pouvez utiliser cette technique pour mettre le texte en fondu du jaune au noir dans l’espace 3D.

Lorsque la transformation du pinceau est la transformation d’identité, les pinceaux apparaissent dans le même espace de coordonnées que la cible de rendu dans laquelle elles sont dessinées. La transformation de pinceau permet à un appelant de modifier la façon dont les coordonnées du pinceau sont mappées à cet espace.

L’espace de pinceau est spécifié différemment dans Direct2D que dans Windows Presentation Foundation (WPF). Dans Direct2D, l’espace de pinceau n’est pas relatif à l’objet qui est dessiné, mais plutôt au système de coordonnées actuel de la cible de rendu, transformé par la transformation de pinceau, le cas échéant. Pour que le pinceau remplisse un objet tel qu’il a été effectué dans WPF, vous devez convertir l’origine de l’espace du pinceau en angle supérieur gauche du cadre englobant de l’objet, puis mettre à l’échelle l’espace du pinceau afin que la vignette de base remplisse le cadre englobant de l’objet.

Pour plus d’informations sur les transformations de pinceau, consultez [vue d’ensemble des pinceaux Direct2D](direct2d-brushes-overview.md).

## <a name="geometry-transforms"></a>Transformations géométriques

Lorsque vous mettez à l’échelle, déplacez, Traduisez ou inclinez des géométries, vous pouvez appliquer directement une transformation à une géométrie spécifique, et non à une transformation de cible de rendu qui affecterait la totalité de l’écran. Une transformation de cible de rendu affecte généralement le trait et le remplissage d’une géométrie. En revanche, une transformation Geometry affecte uniquement le remplissage d’une géométrie, car la transformation est appliquée à une géométrie avant d’être rayée.

> [!Note]  
> À compter de Windows 8, la transformation universelle n’a aucune incidence sur le trait si vous définissez le type de trait sur [**d2d1 \_ Stroke \_ transformation \_ type \_ fixed**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) ou [**d2d1 \_ Stroke \_ \_ type transformation \_ fine**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).

 

Vous pouvez ajuster la transformation sur une géométrie en appelant [**ID2D1Factory :: CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) pour créer un objet [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) . Pour plus d’informations sur les transformations géométriques, consultez [vue d’ensemble des géométries Direct2D](direct2d-geometries-overview.md).

## <a name="how-a-render-target-transform-affects-clips"></a>Comment une transformation de cible de rendu affecte les clips

La transformation sur une cible de rendu affecte le calcul du cadre englobant d’un élément aligné sur l’axe. Lorsque le [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) est appelé, le paramètre *clipRect* est transformé par la transformation universelle active définie sur la cible de rendu. Une fois la transformation appliquée au *clipRect*, le cadre englobant aligné sur l’axe pour le *clipRect* est calculé. Pour plus d’efficacité, le contenu est découpé dans ce cadre englobant aligné sur l’axe et non dans le *clipRect* d’origine qui est passé. Les diagrammes suivants montrent comment une transformation de rotation est appliquée à la cible de rendu, au *clipRect* résultant et à un cadre englobant aligné sur l’axe calculé.

1.  Supposons que le rectangle de l’illustration suivante est une cible de rendu qui est alignée sur les pixels de l’écran.

    ![illustration d’un rectangle (cible de rendu)](images/pushaxisalignedclip-step1-rendertarget.png)

2.  Applique une transformation de rotation à la cible de rendu. Dans l’illustration suivante, le rectangle noir représente la cible de rendu d’origine et le rectangle en pointillés rouges représente la cible de rendu transformée.

    ![illustration du rectangle d’origine et d’un rectangle pivoté (cible de rendu transformée)](images/pushaxisalignedclip-step2-transformed.png)

3.  Après l’appel de [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) , la transformation de rotation est appliquée au *clipRect*. Dans l’illustration suivante, le rectangle bleu représente le *clipRect* transformé.

    ![illustration d’un rectangle bleu plus petit (clipRect) à l’intérieur du rectangle pivoté (cible de rendu transformée)](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  Le cadre englobant aligné sur l’axe est calculé. Dans l’illustration suivante, le rectangle en pointillés verts représente le cadre englobant. Tout le contenu est découpé en zone englobante alignée sur l’axe.

    ![illustration d’un cadre englobant vert sur le petit rectangle bleu (clipRect)](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a>Résumé

Direct2D permet de transformer facilement des objets à deux dimensions à l’aide d’espaces de coordonnées simplifiés et de classes associées. À l’aide de différents types de transformations, vous pouvez traduire, faire pivoter, incliner et mettre à l’échelle vos objets pour obtenir de nombreux effets visuels impressionnants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 
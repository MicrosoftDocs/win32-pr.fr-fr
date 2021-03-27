---
description: Les sections suivantes décrivent plusieurs des nouvelles fonctionnalités de Windows GDI+.
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: Nouvelles fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79ddb4cabd14cc2eaa2493033a78cc7377f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751340"
---
# <a name="new-features"></a>Nouvelles fonctionnalités

Les sections suivantes décrivent plusieurs des nouvelles fonctionnalités de Windows GDI+.

-   [Pinceaux de dégradé](#gradient-brushes)
-   [Splines cardinales](#cardinal-splines)
-   [Objets de chemin d’accès indépendants](#independent-path-objects)
-   [Transformations et objet Matrix](#transformations-and-the-matrix-object)
-   [Régions dimensionnables](#scalable-regions)
-   [Fusion alpha](#alpha-blending)
-   [Prise en charge de plusieurs formats d’image](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a>Pinceaux de dégradé

GDI+ s’étend sur Windows Graphics Device Interface (GDI) en fournissant des pinceaux de dégradé et de tracé linéaires pour remplir des formes, des tracés et des régions. Les pinceaux de dégradé peuvent également être utilisés pour dessiner des lignes, des courbes et des tracés. Lorsque vous remplissez une forme avec un pinceau de dégradé linéaire, la couleur change progressivement à mesure que vous déplacez l’ensemble de la forme. Par exemple, supposons que vous créez un pinceau de dégradé horizontal en spécifiant le bleu sur le bord gauche d’une forme et en vert sur le bord droit. Lorsque vous remplissez cette forme avec le pinceau dégradé horizontal, elle passe progressivement du bleu au vert lorsque vous passez de son bord gauche à son bord droit. De même, une forme remplie avec un pinceau dégradé vertical change de couleur lorsque vous vous déplacez de haut en bas. L’illustration suivante montre une Ellipse remplie avec un pinceau de dégradé horizontal et une région remplie avec un pinceau de dégradé Diagonal.

![illustration d’une forme remplie d’un dégradé horizontal et d’une forme déposée par un dégradé Diagonal](images/aboutgdip01-art01.png)

Lorsque vous remplissez une forme avec un pinceau de dégradé de tracé, vous disposez d’une variété d’options pour spécifier la façon dont les couleurs changent quand vous passez d’une partie de la forme à l’autre. L’une des options consiste à avoir une couleur centrale et une couleur limite afin que les pixels changent graduellement d’une couleur à l’autre lorsque vous vous déplacez du milieu de la forme vers les bords externes. L’illustration suivante montre un tracé (créé à partir d’une paire de splines de Bézier) rempli avec un pinceau de dégradé de tracé.

![illustration d’une forme similaire à un signe infini, remplie à partir du bleu, où les deux moitiés se remplissent au cyan des bords](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a>Splines cardinales

GDI+ prend en charge les splines cardinales, qui ne sont pas prises en charge dans GDI. Une spline cardinale est une séquence de courbes individuelles jointes pour former une plus grande courbe. La spline est spécifiée par un tableau de points et passe par chaque point dans ce tableau. Une spline cardinale passe en douceur (sans angle aigu) à chaque point du tableau et est donc plus affinée qu’un tracé créé en connectant des lignes droites. L’illustration suivante montre deux chemins d’accès, un créé en connectant des lignes droites et un autre créé comme spline cardinale.

![illustration illustrant les cinq mêmes points à deux reprises : une fois connecté par une spline cardinale, l’autre par des segments de ligne](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a>Objets de chemin d’accès indépendants

Dans GDI, un chemin d’accès appartient à un contexte de périphérique, et le chemin d’accès est détruit à mesure qu’il est dessiné. Avec GDI+, le dessin est effectué par un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , et vous pouvez créer et gérer plusieurs objets [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) distincts de l’objet **Graphics** . Un objet **GraphicsPath** n’étant pas détruit par l’action de dessin, vous pouvez utiliser le même objet **GraphicsPath** pour dessiner plusieurs fois un chemin d’accès.

## <a name="transformations-and-the-matrix-object"></a>Transformations et objet Matrix

GDI+ fournit l’objet [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , un outil puissant qui rend la transformation (rotations, traductions, etc.) facile et flexible. Un objet Matrix fonctionne conjointement avec les objets qui sont transformés. Par exemple, un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) a une méthode [**GraphicsPath :: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) qui reçoit l’adresse d’un objet **Matrix** sous la forme d’un argument. Une seule matrice 3 × 3 peut stocker une transformation ou une séquence de transformations. L’illustration suivante montre un chemin d’accès avant et après une séquence de deux transformations (première mise à l’échelle, puis rotation).

![Illustration montrant le contour d’une forme, puis le même contour mais plus étroit et pivoté](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a>Régions dimensionnables

GDI+ s’étend beaucoup sur GDI avec sa prise en charge pour les régions. Dans GDI, les régions sont stockées dans des coordonnées de périphérique et la seule transformation qui peut être appliquée à une région est une traduction. GDI+ stocke des régions dans des coordonnées universelles et permet à une région de subir une transformation (mise à l’échelle, par exemple) qui peut être stockée dans une matrice de transformation. L’illustration suivante montre une région avant et après une séquence de trois transformations : mise à l’échelle, rotation et translation.

![Illustration montrant une forme centrée sur les axes de coordonnées, puis sur la même forme mais plus grande, pivotée et traduite à droite](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a>Fusion alpha

Notez que dans la figure précédente, vous pouvez voir la région sans transformation (remplie en rouge) dans la zone transformée (remplie avec un pinceau hachuré). Cela est rendu possible par la fusion alpha, qui est prise en charge par GDI+. Avec la fusion alpha, vous pouvez spécifier la transparence d’une couleur de remplissage. Une couleur transparente est fusionnée avec la couleur d’arrière-plan : plus la couleur de remplissage est transparente, plus l’arrière-plan s’affiche. L’illustration suivante montre quatre ellipses remplies avec la même couleur (rouge) à des niveaux de transparence différents.

![Illustration montrant quatre ellipses de la transparence variable chevauchant un rectangle semi-transparent](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a>Prise en charge de plusieurs formats d’image

GDI+ fournit les classes d' [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), de [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)et de [**métafichier**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , qui vous permettent de charger, d’enregistrer et de manipuler des images dans divers formats. Les formats suivants sont pris en charge :

-   BMP
-   format GIF (Graphics Interchange Format)
-   JPEG
-   Exif
-   PNG
-   TIFF
-   ICON
-   WMF
-   EMF

 

 




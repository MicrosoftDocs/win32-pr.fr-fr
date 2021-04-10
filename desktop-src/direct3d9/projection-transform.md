---
description: Vous pouvez considérer la transformation de projection comme le contrôle des éléments internes de l’appareil photo. Cela revient à choisir une lentille pour l’appareil photo.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Transformation de projection (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200765"
---
# <a name="projection-transform-direct3d-9"></a>Transformation de projection (Direct3D 9)

Vous pouvez considérer la transformation de projection comme le contrôle des éléments internes de l’appareil photo. Cela revient à choisir une lentille pour l’appareil photo. Il s’agit du plus complexe des trois types de transformation. Cette présentation de la transformation de projection est organisée dans les rubriques suivantes.

La matrice de projection est généralement une projection d’échelle et de perspective. La transformation de projection convertit le frustum d’affichage en forme de cuboid. Étant donné que la fin de la frustum d’affichage est inférieure à la fin, cela a pour effet d’étendre les objets qui sont proches de l’appareil photo. C’est ainsi que la perspective est appliquée à la scène.

Dans [le frustum de visualisation](viewports-and-clipping.md), la distance entre l’appareil photo et l’origine de l’espace de transformation d’affichage est définie arbitrairement comme D, donc la matrice de projection ressemble à l’illustration suivante.

![illustration de la matrice de projection](images/projmat1.png)

La matrice d’affichage traduit la caméra en l’origine en traduisant dans la direction z par-D. La matrice de translation ressemble à l’illustration suivante.

![illustration de la matrice de traduction](images/projmat2.png)

La multiplication de la matrice de translation par la matrice de projection (T \* P) donne à la matrice de projection composite, comme indiqué dans l’illustration suivante.

![illustration de la matrice de projection composite](images/projmat3.png)

La transformation de perspective convertit un frustum d’affichage en un nouvel espace de coordonnées. Notez que le frustum devient cuboid et que l’origine passe de l’angle supérieur droit de la scène au centre, comme indiqué dans le diagramme suivant.

![Diagramme illustrant comment la transformation de perspective change le frustum d’affichage en nouvel espace de coordonnées](images/cuboid.png)

Dans la transformation de perspective, les limites des directions x et y sont-1 et 1. Les limites de l’axe z sont 0 pour le plan avant et 1 pour le plan arrière.

Cette matrice convertit et met à l’échelle des objets en fonction d’une distance spécifiée entre l’appareil photo et le plan de découpage proche, mais il ne tient pas compte du champ de vue (l’angle de vue) et les valeurs z qu’il produit pour les objets de la distance peuvent être presque identiques, ce qui complique les comparaisons de profondeur. La matrice suivante résout ces problèmes et ajuste les sommets pour prendre en compte les proportions de la fenêtre d’affichage, ce qui en fait un bon choix pour la projection de perspective.

![illustration d’une matrice pour la projection de perspective](images/prjmatx1.png)

Dans cette matrice, Zn est la valeur z du plan de découpage proche. Les variables w, h et Q ont les significations suivantes. Notez que le point d’affichage et le fovk représentent les champs<sub>horizontal et vertical</sub> de la fenêtre d’affichage, en radians.

![équations des significations variables](images/prjmatx2.png)

Pour votre application, l’utilisation d’angles de champ pour définir les coefficients de mise à l’échelle x et y peut ne pas être aussi pratique que l’utilisation des dimensions horizontales et verticales de la fenêtre d’affichage (dans l’espace de l’appareil photo). À mesure que les mathématiques fonctionnent, les deux équations suivantes pour w et h utilisent les dimensions de la fenêtre d’affichage, et sont équivalentes aux équations précédentes.

![équations de la moyenne des variables w et h](images/prjmatx3.png)

Dans ces formules, Zn représente la position du plan de découpage proche, et les variables V<sub>w</sub> et VH représentent la largeur et la hauteur de la fenêtre d’affichage, dans l’espace de l’appareil photo.

Pour une application C++, ces deux dimensions correspondent directement aux membres Width et Height de la structure [**D3DVIEWPORT9**](d3dviewport9.md) .

Quelle que soit la formule que vous décidez d’utiliser, veillez à définir Zn sur une valeur aussi grande que possible, car les valeurs z les plus proches de l’appareil photo ne varient pas. Les comparaisons de profondeur utilisant des tampons z 16 bits sont donc quelque peu compliquées.

Comme pour le monde et les transformations d’affichage, vous appelez la méthode [**IDirect3DDevice9 :: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) pour définir la transformation de projection.

## <a name="setting-up-a-projection-matrix"></a>Configuration d’une matrice de projection

L’exemple de fonction ProjectionMatrix suivant définit les plans de l’avant et de l’arrière-plan, ainsi que le champ horizontal et vertical des angles de vue. Les champs de la vue doivent être inférieurs à pi radians.


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



Après avoir créé la matrice, définissez-la avec [**IDirect3DDevice9 :: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) en spécifiant la \_ projection D3DTS.

La bibliothèque de l’utilitaire D3DX fournit les fonctions suivantes pour vous aider à configurer votre matrice de projection.

-   [**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
-   [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
-   [**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
-   [**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
-   [**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
-   [**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a>Une matrice de projection avec l’e-friendly

Direct3D peut utiliser le composant w d’un vertex qui a été transformé par les matrices de projection, de vue et de projection pour effectuer des calculs en fonction de la profondeur dans un tampon de profondeur ou des effets de brouillard. Les calculs tels que ceux-ci requièrent que votre matrice de projection normalise le w pour être équivalente à l’espace universel z. En résumé, si votre matrice de projection comprend un coefficient (3,4) qui n’est pas 1, vous devez mettre à l’échelle tous les coefficients à l’inverse du coefficient (3,4) pour créer une matrice appropriée. Si vous ne fournissez pas de matrice conforme, les effets de brouillard et la mise en mémoire tampon de profondeur ne sont pas appliqués correctement.

L’illustration suivante montre une matrice de projection non conforme, et la même matrice mise à l’échelle afin que le brouillard relatif à l’oeil soit activé.

![illustrations d’une matrice de projection non conforme et d’une matrice avec brouillard relatif à l’oeil](images/eyerlmx.png)

Dans les matrices précédentes, toutes les variables sont supposées être non nulles. Pour plus d’informations sur le brouillard relatif à l’oeil, consultez la page relative à l’œil et à la [profondeur Z](pixel-fog.md). Pour plus d’informations sur la mise en mémoire tampon de profondeur basée sur w, consultez [mémoires tampons de profondeur (Direct3D 9)](depth-buffers.md).

Direct3D utilise la matrice de projection actuellement définie dans ses calculs de profondeur basés sur w. Par conséquent, les applications doivent définir une matrice de projection conforme pour recevoir les fonctionnalités w souhaitées, même si elles n’utilisent pas Direct3D pour les transformations.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations](transforms.md)
</dt> </dl>

 

 

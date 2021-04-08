---
title: Pipeline de transformation Direct3D
description: Cet article fournit une explication technique pour les développeurs d’applications Direct3D sur la manière de définir les paramètres du pipeline de transformation Direct3D en manipulant directement les matrices Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869325"
---
# <a name="the-direct3d-transformation-pipeline"></a>Pipeline de transformation Direct3D

Cet article fournit une explication technique pour les développeurs d’applications Direct3D sur la manière de définir les paramètres du pipeline de transformation Direct3D en manipulant directement les matrices Direct3D.

-   [Vue d’ensemble](#overview)
-   [Pipeline de transformation](#the-transformation-pipeline)
-   [Conseils d’utilisation](#usage-tips)

## <a name="overview"></a>Vue d’ensemble

Direct3D utilise trois transformations pour modifier vos coordonnées de modèle 3D en coordonnées de pixels (espace à l’écran). Ces transformations sont la transformation universelle, la transformation de vue et la transformation de projection.

La transformation universelle contrôle la manière dont les coordonnées du modèle sont transformées en coordonnées universelles. La transformation universelle peut inclure des translations, des rotations et des mises à l’échelle, mais elle ne s’applique pas aux lumières. Pour plus d’informations sur l’utilisation des transformations universelles, consultez [transformation universelle](/windows/desktop/direct3d9/world-transform).

La transformation de vue contrôle la transition des coordonnées universelles en « espace de caméra », en déterminant la position de la caméra dans le monde. Pour obtenir un exemple d’utilisation des transformations de vue, consultez [View Transform](/windows/desktop/direct3d9/view-transform).

Transformation de projection change la géométrie de l’espace de l’appareil photo en «espace et applique la distorsion de perspective. Le terme « espace du clip » fait référence à la façon dont la géométrie est découpée au volume de la vue pendant cette transformation. Pour obtenir un exemple d’utilisation des transformations de projection, consultez [projection Transform](/windows/desktop/direct3d9/projection-transform).

Enfin, la géométrie de l’espace de l’élément est transformée en coordonnées en pixels (espace à l’écran). Cette transformation est contrôlée par les paramètres de la fenêtre d’affichage.

Les vertex de découpage et de transformation doivent avoir lieu dans un espace homogène (simplement placé, espace dans lequel le système de coordonnées comprend un quatrième élément), mais le résultat final pour la plupart des applications doit être des coordonnées tridimensionnelles (3D) non homogènes définies dans l’espace d’écran. Cela signifie que les vertex d’entrée et le volume de découpage doivent être traduits dans un espace homogène pour exécuter le découpage, puis retraduits en espace non homogène pour être affichés.

Les trois transformations Direct3D (monde, vue et transformation de projection) sont définies par les matrices Direct3D. Une matrice Direct3D est une matrice de 4x4 homogène définie par une structure [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) . Bien que les matrices Direct3D ne sont pas des objets standard, elles ne sont pas représentées par une interface COM. vous pouvez les créer et les définir comme n’importe quel autre objet Direct3D. Pour plus d’informations sur les matrices Direct3D, consultez [transformations](/windows/desktop/direct3d9/transforms).

## <a name="the-transformation-pipeline"></a>Pipeline de transformation

Si un vertex dans la coordonnée du modèle est donné par PM = (XM, YM, ZM, 1), les transformations présentées dans la figure suivante sont appliquées aux coordonnées de calcul de l’écran PS = (XS, distinctes, ZS, WS).

![transformation de l’espace de modèle en espace d’écran](images/d3dxfrm61.gif)

Voici les descriptions des étapes présentées dans la figure précédente :

1.  Le Mworld de la matrice universelle transforme les vertex de l’espace du modèle en espace universel. Cette matrice est définie par :

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    L’implémentation Direct3D suppose que la dernière colonne de cette matrice est (0, 0, 0, 1). Aucune erreur n’est retournée si l’utilisateur spécifie une matrice avec une dernière colonne différente, mais l’éclairage et le brouillard sont incorrects.

2.  Afficher la matrice mView transforme les sommets de l’espace universel vers l’espace de l’appareil photo. Cette matrice est définie par :

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    L’implémentation Direct3D suppose que la dernière colonne de cette matrice est (0, 0, 0, 1). Aucune erreur n’est retournée si l’utilisateur spécifie une matrice avec une dernière colonne différente, mais l’éclairage et le brouillard sont incorrects.

3.  La matrice de projection mproj transforme les vertex de l’espace de l’appareil photo à l’espace de projection. Cette matrice est définie par :

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    La dernière colonne de la matrice de projection doit être (0, 0, 1, 0) ou (0, 0, a, 0) pour des effets de brouillard et d’éclairage corrects ; (0, 0, 1, 0) le formulaire est préféré.

    Le volume de détourage de tous les points XP = (XP, YP, ZP, WP) dans l’espace de projection est défini comme suit :

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    Tous les points qui ne répondent pas à ces équations sont découpés.

    Si un volume de vue est défini comme suit :

    -   SW-largeur de la fenêtre d’écran dans l’espace de l’appareil photo dans le plan de découpage
    -   SH-hauteur de la fenêtre d’écran dans l’espace de l’appareil photo dans le plan de découpage
    -   Zn-distance au plan de découpage proche le long des axes Z dans l’espace de caméra
    -   ZF-distance au plan de découpage lointain le long des axes Z dans l’espace de caméra

    Ensuite, une matrice de projection de perspective peut être écrite comme suit :

    ![Affiche une matrice de projection de perspective.](images/d3dxfrm62.gif)

    où mij est membre de mproj.

    Pour la projection orthogonale, nous avons :

    ![projection orthogonale](images/d3dxfrm63.gif)

    Direct3D suppose que la matrice de projection de la perspective se présente sous la forme suivante :

    ![matrice de projection de perspective](images/d3dxfrm64.gif)

    Si la matrice de projection de la perspective n’a pas cette forme, il y aura des artefacts. Par exemple, le brouillard de table ne fonctionnera pas.

4.  Direct3D permet à l’utilisateur de modifier le volume du clip comme suit :

    ![modifier le volume du clip](images/d3dxfrm65.gif)

    Elle peut être réécrite comme suit :

    ![modifier le volume du clip réécrit](images/d3dxfrm66.gif)

    où :

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    Cette transformation peut fournir une précision accrue et est équivalente à la mise à l’échelle et au décalage du volume de découpage.

    La matrice Mclip correspondante est la suivante :

    ![matrice mclip](images/d3dxfrm67.gif)

    Un vertex est transformé par :

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    Si vous ne souhaitez pas mettre à l’échelle le volume du clip, vous pouvez définir les paramètres de la fenêtre d’affichage sur les valeurs par défaut :

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  L’étape de découpage est facultative si l’utilisateur spécifie l' \_ indicateur D3DDP DONOTCLIP dans un appel DrawPrimitive. Dans ce cas, toutes les matrices (y compris MVS) peuvent être combinées.
6.  La matrice de mise à l’échelle de la fenêtre MVS met à l’échelle les coordonnées à l’intérieur de la fenêtre d’affichage et retourne l’axe Y du haut vers le haut :

    ![matrice de mise à l’échelle Viewport MVS](images/d3dxfrm68.gif)

    où :

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  Enfin, les coordonnées d’écran sont calculées et transmises au rastériseur :

    ![coordonnées d’écran calculées et transmises au rastériseur](images/d3dxfrm69.gif)

## <a name="usage-tips"></a>Conseils d’utilisation

Voici quelques conseils pour utiliser le pipeline de transformation Direct3D :

-   La dernière colonne des matrices de monde et de vue doit être (0, 0, 0, 1), sinon l’éclairage sera incorrect.
-   Définissez les paramètres de la fenêtre d’affichage pour générer une matrice de Mclip d’identité, sauf si vous comprenez exactement ce qui est nécessaire pour.

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 
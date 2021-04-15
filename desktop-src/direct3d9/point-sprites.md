---
description: La prise en charge des points sprites dans Direct3D 9 permet le rendu hautes performances des points (systèmes de particule). Les sprites point sont des généralisations de points génériques qui permettent le rendu de formes arbitraires comme défini par les textures.
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: Points sprites (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c988a104eb65b5e2d7e56ff2444e8d422c422df2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521708"
---
# <a name="point-sprites-direct3d-9"></a>Points sprites (Direct3D 9)

La prise en charge des points sprites dans Direct3D 9 permet le rendu hautes performances des points (systèmes de particule). Les sprites point sont des généralisations de points génériques qui permettent le rendu de formes arbitraires comme défini par les textures.

-   [Contrôles de rendu de primitive point](#point-primitive-rendering-controls)
-   [Calculs de la taille des points](#point-size-computations)
-   [Rendu de point](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>Contrôles de rendu de primitive point

Direct3D 9 prend en charge des paramètres supplémentaires pour contrôler le rendu des sprites point (primitives point). Ces paramètres permettent aux points d’être de taille variable et de disposer d’une carte de texture complète appliquée. La taille de chaque point est déterminée par une taille spécifiée par l’application et associée à une fonction basée sur les distances calculée par Direct3D. L’application peut spécifier la taille du point en fonction du vertex ou en définissant D3DRS Desize \_ , qui s’applique aux points sans taille par vertex. La taille en points est exprimée en unités d’espace de caméra, à l’exception du moment où l’application transmet des vertex de format de vertex flexible (prix de revient) après transformation. Dans ce cas, la fonction basée sur la distance n’est pas appliquée et la taille du point est exprimée en unités de pixels sur la cible de rendu.

Les coordonnées de texture calculées et utilisées lors du rendu des points dépendent du paramètre de D3DRS \_ POINTSPRITEENABLE. Lorsque cette valeur est définie sur **true**, les coordonnées de texture sont définies de sorte que chaque point affiche la texture complète. En général, cela n’est utile que lorsque les points sont beaucoup plus volumineux qu’un pixel. Lorsque D3DRS \_ POINTSPRITEENABLE est défini sur **false**, la coordonnée de texture vertex de chaque point est utilisée pour le point entier.

## <a name="point-size-computations"></a>Calculs de la taille des points

La taille du point est déterminée par D3DRS \_ POINTSCALEENABLE. Si cette valeur est définie sur **false**, la taille de point spécifiée par l’application est utilisée comme taille d’espace d’écran (après conversion). Les vertex passés à Direct3D dans l’espace à l’écran n’ont pas de tailles de points calculées ; la taille de point spécifiée est interprétée comme la taille de l’espace à l’écran.

Si D3DRS \_ POINTSCALEENABLE a la **valeur true**, Direct3D calcule la taille du point d’espace d’écran en fonction de la formule suivante. La taille de point spécifiée par l’application est exprimée en unités d’espace de caméra.

S s = VH \* s <sub>i</sub> \* racine (1/(A + B \* D ₑ + C \* (D ₑ ²)))

Dans cette formule, la taille du point d’entrée, S <sub>i</sub>, est soit par vertex, soit la valeur de l’état de rendu D3DRS redimensionnement \_ . Les facteurs de mise à l’échelle du point, D3DRS \_ POINTSCALE \_ A, D3DRS \_ POINTSCALE \_ B et D3DRS \_ POINTSCALE \_ C, sont représentés par les points A, B et c. La hauteur de la fenêtre d’affichage, V h, est le membre Height de la structure [**D3DVIEWPORT9**](d3dviewport9.md) représentant la fenêtre d’affichage. D ₑ, la distance entre l’œil et la position (l’œil à l’origine), est calculée en tenant la position de l’espace œil du point (X ₑ, Y ₑ, Z ₑ) et en effectuant l’opération suivante.

D ₑ = sqrt (X ₑ ² + Y ₑ ² + Z ₑ ²)

La taille maximale en points, PM ₐ ₓ, est déterminée en acceptant la valeur la plus petite du membre MaxPointSize de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) ou de l' \_ État de rendu max de l’D3DRS \_ . La taille en points minimale, P<sub>min</sub>, est déterminée par l’interrogation de la valeur de D3DRS \_ \_ . Par conséquent, la taille finale du point d’espace d’écran, S, est déterminée de la manière suivante.

-   Si SS > PM ₐ ₓ, alors S = P m ₐ ₓ
-   Si S < P<sub>min</sub>, alors s = p <sub>min</sub>
-   Sinon, S = S s

## <a name="point-rendering"></a>Rendu de point

Un point d’espace d’écran, P = (X, Y, Z, W), de taille d’espace d’écran S est pixellisé en tant que quadrangulaires des quatre sommets suivants.

((X + S/2, Y + S/2, Z, W), (X + S/2, Y-S/2, Z, W), (X-S/2, Y-S/2, Z, W), (X-S/2, Y + S/2, Z, W))

Les attributs de couleur du vertex sont dupliqués à chaque vertex ; par conséquent, chaque point est toujours rendu avec des couleurs constantes.

L’affectation d’index de texture est contrôlée par le paramètre d' \_ État de rendu D3DRS POINTSPRITEENABLE. Si D3DRS \_ POINTSPRITEENABLE est défini sur **false**, les coordonnées de texture de vertex sont dupliquées à chaque vertex. Si D3DRS \_ POINTSPRITEENABLE est défini sur **true**, les coordonnées de texture aux quatre sommets sont définies sur les valeurs suivantes.

(0. F, 0. F), (0. F, 1. F), (1. F, 0. F), (1. F, 1. F)

Cette situation est présentée dans le diagramme suivant.

![diagramme d’un carré avec des sommets étiquetés pour les valeurs de coordonnée (u, v) et (x, y)](images/spritepoint.png)

Lorsque le découpage est activé, les points sont découpés de la manière suivante. Si le vertex dépasse la plage de valeurs de profondeur-MinZ et MaxZ de la structure [**D3DVIEWPORT9**](d3dviewport9.md) -dans laquelle une scène doit être rendue, le point existe en dehors de la vue frustum et n’est pas rendu. Si le point, en tenant compte de la taille du point, est complètement à l’extérieur de la fenêtre d’affichage dans X et Y, le point n’est pas rendu ; les points restants sont rendus. Il est possible que la position du point se trouve en dehors de la fenêtre d’affichage dans X ou Y et soit toujours partiellement visible.

Les points peuvent ou ne peuvent pas être correctement découpés en plans de clip définis par l’utilisateur. Si D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS n’est pas défini dans le membre PrimitiveMiscCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) , les points sont découpés en plans de séquence définis par l’utilisateur, basés uniquement sur la position du vertex, en ignorant la taille du point. Dans ce cas, les points mis à l’échelle sont entièrement rendus lorsque la position du vertex est à l’intérieur des plans de coupe et sont ignorés lorsque la position du vertex est à l’extérieur d’un plan de découpage. Les applications peuvent empêcher des artefacts potentiels en ajoutant une géométrie de bordure aux plans de découpage qui est aussi grande que la taille maximale du point.

Si le \_ bit D3DPMISCCAPS CLIPPLANESCALEDPOINTS est défini, les points mis à l’échelle sont correctement découpés en plans de clip définis par l’utilisateur.

Le traitement du vertex matériel peut ou non prendre en charge la taille du point. Par exemple, si un appareil est créé avec \_ le matériel D3DCREATE \_ VERTEXPROCESSING sur un appareil Hal (Hardware Abstraction Layer) ( \_ HAL D3DDEVTYPE) dont le membre MaxPointSize de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) est défini sur 1,0 ou 0,0, tous les points sont un pixel unique. Pour restituer des sprites de point de pixel inférieurs à 1,0, vous devez utiliser des vertex (transformés et allumés) au prix de la Commission (D3DCREATE \_ Software \_ VERTEXPROCESSING), auquel cas le runtime Direct3D émule le rendu du point Sprite.

Un périphérique matériel qui effectue le traitement des vertex et prend en charge les sprites de point-MaxPointSize définis sur une valeur supérieure à 1.0 f-est requis pour effectuer le calcul de la taille des sprites non transformés et est requis pour définir correctement les points de par vertex ou D3DRS \_ \_ pour les vertex TL.

Pour plus d’informations sur les règles de rendu des points, des lignes et des triangles, consultez [règles de pixellisation (Direct3D 9)](rasterization-rules.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de vertex](vertex-pipeline.md)
</dt> </dl>

 

 




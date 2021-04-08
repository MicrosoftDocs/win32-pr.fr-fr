---
description: Direct3D permet à une application d’augmenter le réalisme de ses scènes en affichant des objets polygones segmentés, en particulier des caractères, qui ont des jointures lissées.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Fusion géométrique (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745381"
---
# <a name="geometry-blending-direct3d-9"></a>Fusion géométrique (Direct3D 9)

Direct3D permet à une application d’augmenter le réalisme de ses scènes en affichant des objets polygones segmentés, en particulier des caractères, qui ont des jointures lissées. Ces effets sont souvent appelés « pelures ». Le système réalise cet effet en appliquant des matrices de transformation universelles supplémentaires à un seul ensemble de vertex pour créer plusieurs résultats, puis en effectuant une fusion linéaire entre les vertex résultants pour créer un ensemble unique de géométrie pour le rendu. L’illustration suivante d’une banane illustre ce processus.

![illustration du processus de fusion de deux objets avec la texture Banana](images/geometry-blend.png)

L’illustration précédente montre comment vous pouvez imaginer le processus de fusion géométrique. Dans un appel de rendu unique, le système prend les sommets de la banane, les transforme deux fois sans modification, et une fois avec une rotation simple, et fusionne les résultats pour créer une banane tordue. Le système fusionne la position du vertex, ainsi que la normale du vertex lorsque l’éclairage est activé. Les applications ne sont pas limitées à deux chemins de fusion ; Direct3D peut mélanger la géométrie entre jusqu’à quatre matrices universelles, y compris la matrice universelle standard, [**D3DTS \_ World**](d3dts-world.md).

> [!Note]
>
> Lorsque l’éclairage est activé, les normales de vertex sont transformées par une matrice de vue mondiale inverse correspondante, pondérée de la même façon que les calculs de position de vertex. Le système normalise le vecteur normal résultant si l' \_ État de rendu D3DRS NORMALIZENORMALS est défini sur **true**.

 

Sans la fusion géométrique, les modèles articulés dynamiques sont souvent rendus dans des segments. Par exemple, considérez un modèle 3D du bras humain. Dans la vue la plus simple, un ARM a deux parties : le bras supérieur qui se connecte au corps et le bras inférieur qui se connecte à la main. Les deux sont connectés au coude et le bras inférieur tourne à ce point. Une application qui restitue un ARM peut conserver des données de vertex pour le bras supérieur et inférieur, chacun avec une matrice de transformation universelle distincte. L'exemple de code suivant illustre ceci.


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



Pour restituer le ARM, deux appels de rendu sont effectués, comme indiqué dans le code suivant.


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



L’illustration suivante est une banane, modifiée pour utiliser cette technique.

![illustration d’une banane fusionnée sans fusion géométrique](images/noblend.png)

Les différences entre la géométrie fusionnée et la géométrie qui n’est pas fusionnée sont évidentes. Cet exemple est quelque peu extrême. Dans une application réelle, les jointures de modèles segmentés sont conçues de façon à ce que les coutures ne soient pas aussi évidentes. Toutefois, les jointures sont visibles à des moments, ce qui présente des défis constants pour les concepteurs de modèles.

La fusion géométrique dans Direct3D présente une alternative au scénario de modélisation segmentée classique. Toutefois, l’amélioration de la qualité visuelle des objets segmentés survient au détriment des calculs de fusion pendant le rendu. Pour réduire l’impact de ces opérations supplémentaires, le pipeline de géométrie Direct3D est optimisé pour mélanger la géométrie avec la surcharge la moins possible. Les applications qui utilisent intelligemment les services de fusion de géométrie proposés par Direct3D peuvent améliorer le réalisme de leurs caractères tout en évitant de sérieux répercussions sur les performances.

## <a name="blending-transform-and-render-states"></a>Fusion des États de transformation et de rendu

La méthode [**IDirect3DDevice9 :: setTransform**](/windows/desktop/api) reconnaît les macros internationales [**D3DTS \_**](d3dts-world.md) et [**D3DTS \_ worldn**](d3dts-worldn.md) , qui correspondent à des valeurs qui peuvent être définies par la macro D3DTS [**\_ WORLDMATRIX**](d3dts-worldmatrix.md) . Ces macros sont utilisées pour identifier les matrices entre lesquelles la géométrie sera fusionnée.

Le type énuméré [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) comprend l' \_ État de rendu D3DRS VERTEXBLEND pour activer et contrôler la fusion géométrique. Les valeurs valides pour cet état de rendu sont définies par le type énuméré [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Si la fusion géométrique est activée, le format du vertex doit inclure le nombre approprié de poids de fusion.

## <a name="blending-weights"></a>Fusion des poids

Une pondération de fusion, parfois appelée pondération bêta, contrôle la portée à laquelle une matrice universelle donnée affecte un vertex. Les pondérations de fusion sont des valeurs à virgule flottante comprises entre 0,0 et 1,0, encodées au format vertex, où la valeur 0,0 signifie que le vertex n’est pas fusionné avec cette matrice et 1,0 signifie que le vertex est affecté en totalité par la matrice.

Les pondérations de fusion Geometry sont encodées au format de vertex, qui apparaissent juste après la position de chaque vertex, comme décrit dans la [fonction Fixed des codes d’erreur (Direct3D 9)](fixed-function-fvf-codes.md). Vous communiquez le nombre de poids de fusion dans le format de vertex en incluant l’une des [constantes](d3dfvf.md) de la Commission de la Commission dans la description de vertex que vous fournissez aux méthodes de rendu.

Le système effectue une fusion linéaire entre les résultats pondérés des matrices de fusion. L’équation suivante est la formule de fusion complète.

![équation de la fusion linéaire, à l’aide de matrices de transformation universelle](images/vert-blend-formula.png)

Dans l’équation précédente, vBlend est le vertex de sortie, les éléments v sont les vertex produits par la matrice universelle appliquée ([**D3DTS \_ worldn**](d3dts-worldn.md)). Les éléments W sont les valeurs de poids correspondantes dans le format de vertex. Un sommet fusionné entre n matrices peut avoir-1 valeurs de poids de fusion, une pour chaque matrice de fusion, à l’exception de la dernière. Le système génère automatiquement le poids de la dernière matrice mondiale de sorte que la somme de tous les poids soit 1,0, exprimée en notation Sigma ici. Cette formule peut être simplifiée pour chacun des cas pris en charge par Direct3D, qui est présenté dans les équations suivantes.

![équations de la fusion linéaire pour trois cas de fusion](images/vert-blend-formulas-simple.png)

Il s’agit des formes simplifiées de la formule de fusion complète pour les deux, trois et quatre cas de matrice de fusion.

> [!Note]  
> Bien que Direct3D comprenne des descripteurs de la Commission de la Commission pour définir des vertex qui contiennent jusqu’à cinq poids de fusion, seuls trois peuvent être utilisés dans cette version de DirectX.

 

Des informations supplémentaires sont contenues dans les rubriques suivantes.

-   [Utilisation de la fusion géométrique (Direct3D 9)](using-geometry-blending.md)
-   [Fusion de vertex indexée (Direct3D 9)](indexed-vertex-blending.md)
-   [Interpolation de vertex (Direct3D 9)](vertex-tweening.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de vertex](vertex-pipeline.md)
</dt> </dl>

 

 

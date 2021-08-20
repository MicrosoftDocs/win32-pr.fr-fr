---
title: deriv_rty (SM4-ASM)
description: Rendu-cible y équivalent de Deriv \_ RTX.
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb522076435b525252e8cab40590c649e5cc8af8a83023ebd6cace1695fbb729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515467"
---
# <a name="deriv_rty-sm4---asm"></a>Deriv \_ propriété (SM4-ASM)

Rendu-cible y équivalent de [Deriv \_ RTX](deriv-rtx--sm4---asm-.md).



| Deriv \_ propriété \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , |
|--------------------------------------------------------------------|



 



| Élément                                                            | Description                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le composant de l’opération.<br/>             |



 

## <a name="remarks"></a>Remarques

Une seule paire dérivée x, y est calculée pour chaque tampon 2x2 de pixels.

Cette opération dépend du matériel.

Implémentation du rastériseur de référence pour les triangles :

-   Le nuanceur de pixels exécute toujours le nuanceur sur des quadruples Quad de pixels dans échelons (même via le contrôle de Flow et le masquage des pixels désactivés).
-   Les quatre cœurs ont toujours des coordonnées de pixels même numérotées (à la fois x et y) pour le pixel supérieur gauche.
-   Les pixels factices s’exécutent en mode primitif si la primitive est trop petite pour remplir un quadruple Quad.
-   [Deriv \_ RTX](deriv-rtx--sm4---asm-.md) est calculé en sélectionnant d’abord 2 pixels : le pixel actuel et l’autre Pixel avec la même coordonnée y du quadruple. Ensuite, le résultat est calculé comme suit : *src0*(impair x pixel)- *src0*(même x pixel) \[ par composant\]
-   **Deriv \_ propriété** est calculé en sélectionnant d’abord 2 pixels : le pixel actuel et l’autre Pixel avec la même coordonnée x du quadruple. Ensuite, le résultat est calculé comme suit : *src0*(pixel y impair)- *src0*(y compris y pixel) \[ par composant\]

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






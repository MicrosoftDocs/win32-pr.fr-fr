---
title: log (SM4-ASM)
description: Base du journal des composants 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf99949e278ca302543437da346188b690789604
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030590"
---
# <a name="log-sm4---asm"></a>log (SM4-ASM)

Base du journal des composants 2.



| log \[ \_ sam \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle |
|----------------------------------------------------------|



 



| Élément                                                            | Description                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> dest = Log2 (src0)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] la valeur de l’opération.<br/>                                             |



 

## <a name="remarks"></a>Notes

### <a name="restrictions"></a>Restrictions

-   Suit la théorie des limites.
-   Tolérance d’erreur : si *src0* est \[ 0.5.. 2 \] , l’erreur absolue ne doit pas être supérieure à 2-21. Si *src0* est (0.. 0.5) ou (2.. + inf \] , l’erreur relative ne doit pas être supérieure à 2-21.

Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit. F signifie nombre fini-réel.



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **src**  | **-INF** | **-F** | **-dénorme** | **-0** | **+0** | **+ dénorme** | **+ F** | **+ INF** | **NaN** |
| **dest** | NaN      | NaN    | -inf        | -inf   | -inf   | -inf        | F      | +inf     | NaN     |



 

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






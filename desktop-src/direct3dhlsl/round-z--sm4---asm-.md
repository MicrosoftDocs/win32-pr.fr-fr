---
title: round_z (SM4-ASM)
description: Arrondi à virgule flottante à l’entier float. | round_z (SM4-ASM)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08a95d0cb1e8432b0b5bf0ea73bf2619c8a221754775fc0d64c3649d69086295
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095309"
---
# <a name="round_z-sm4---asm"></a>Round \_ z (SM4-ASM)

Arrondi à virgule flottante à l’entier float.



| arrondi \_ z \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|-----------------------------------------------------------------|



 



| Élément                                                            | Description                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des résultats de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants de l’opération.<br/>             |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue un arrondi de valeurs à virgule flottante au niveau du composant dans *src0*, en écrivant des valeurs à virgule flottante intégrales dans *dest*.

**round \_ z** arrondit à zéro.

Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.



| **src**  | **-INF** | **-F** | **-dénorme** | **-0** | **+0** | **+ dénorme** | **+ F** | **+ INF** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **dest** | -inf     | -F     | -0          | -0     | +0     | +0          | + F     | +inf     | NaN     |



 

F signifie nombre fini-réel.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 






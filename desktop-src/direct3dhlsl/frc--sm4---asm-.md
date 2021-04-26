---
title: FRC (SM4-ASM)
description: Composant, extraire un composant fractionnaire.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f59b747f38fb970b92b5e48610873efe781d63d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993916"
---
# <a name="frc-sm4---asm"></a>FRC (SM4-ASM)

Composant, extraire un composant fractionnaire.



| FRC \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|-------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> *dest*  =  . *src0*  -  [arrondi \_](round-ni--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le composant de l’opération.<br/>                                                                                        |



 

## <a name="remarks"></a>Remarques

Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.



| **src**  | **-INF** | **-F**     | **-dénorme** | **-0** | **+0** | **+ dénorme** | **+ F**     | **+ INF** | **NaN** |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **dest** | NaN      | \[+ 0 à 1) | +0          | +0     | +0     | +0          | \[+ 0 à 1) | NaN      | NaN     |



 

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

 

 






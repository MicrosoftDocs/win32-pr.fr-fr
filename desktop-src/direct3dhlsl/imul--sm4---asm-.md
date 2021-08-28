---
title: imul (SM4-ASM)
description: Multiplication de l’entier signé.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87eabcc07dc5c6a662494c71a26c5f60e5fa1053265e3740ad3605ed685771a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986489"
---
# <a name="imul-sm4---asm"></a>imul (SM4-ASM)

Multiplication de l’entier signé.



| imul destHI \[ . Mask \] , destLO \[ . Mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle\] |
|-------------------------------------------------------------------------------------|



 



| Élément                                                                                           | Description                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[dans \] l’adresse des 32 bits de poids fort du résultat.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[dans \] l’adresse des 32 bits de poids faible du résultat.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[dans \] la valeur à multiplier avec *src1*.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[dans \] la valeur à multiplier avec *src0*.<br/>             |



 

## <a name="remarks"></a>Remarques

Multiplication au niveau du composant des opérandes 32 bits *src0* et *src1* (les deux sont signés), ce qui génère le résultat complet 64 bits (par composant) complet. Les 32 bits de poids faible (par composant) sont placés dans *destLO*. Les 32 bits de poids fort (par composant) sont placés dans *destHI*.

*DestHI* ou *destLO* peut être spécifié comme null au lieu de spécifier un registre, si les 32 bits de poids fort ou faible du résultat de 64 bits ne sont pas nécessaires.

Le modificateur de négation facultatif sur les opérandes source prend le complément à 2 avant d’effectuer une opération arithmétique.

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

 

 






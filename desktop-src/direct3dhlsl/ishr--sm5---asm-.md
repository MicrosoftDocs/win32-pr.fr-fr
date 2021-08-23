---
title: ISHR (SM5-ASM)
description: Décalage arithmétique vers la droite (extension de signe). | ISHR (SM5-ASM)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c75d64ded9beb6cdc5660d6157b15fc989863ee9e907e67c00854fe7cfe161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488329"
---
# <a name="ishr-sm5---asm"></a>ISHR (SM5-ASM)

Décalage arithmétique vers la droite (extension de signe).



| ishl dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|--------------------------------------------------------|



 



| Élément                                                            | Description                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] contient les résultats de l’équipe de travail.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le nombre de bits à décaler.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les valeurs 32 bits à décaler.<br/>        |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue un décalage arithmétique au niveau du composant de chaque valeur 32 bits dans *src0* avec un nombre de bits entier non signé fourni par LSB 5 bits (plage 0-31) dans *src1*, en répliquant la valeur de bit 31. Le résultat 32 bits par composant est placé dans *dest*.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






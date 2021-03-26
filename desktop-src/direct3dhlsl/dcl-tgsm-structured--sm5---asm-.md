---
title: dcl_tgsm_structured (SM5-ASM)
description: Déclarez une référence à une région d’espace mémoire partagée disponible pour le groupe de threads du nuanceur de calcul. La mémoire est affichée sous la forme d’un tableau de structures.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990744"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>DCL \_ TGSM \_ structurée (SM5-ASM)

Déclarez une référence à une région d’espace mémoire partagée disponible pour le groupe de threads du nuanceur de calcul. La mémoire est affichée sous la forme d’un tableau de structures.



| DCL \_ TGSM \_ structuré g \# , structByteStride, structCount |
|----------------------------------------------------------|



 



| Élément                                                                                                                                   | Description                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*activée\#*<br/>                                                                             | \[dans \] une référence à un bloc de mémoire partagée de taille *structByteStride* \* *structCount* octets. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[dans \] la structure Stride. Cette valeur est un uint en octets et doit être un multiple de 4. <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*<br/>                     | \[dans \] le nombre de structures.<br/>                                                                   |



 

## <a name="remarks"></a>Notes

Le stockage total pour tous les g \# doit être <= la quantité de mémoire partagée disponible par groupe de threads, soit 32 Ko, soit les valeurs scalaires de 8192 32 bits.

Dans un cas extrême, vous pouvez déclarer 8192 g s au total \# , si chacun a un *structByteStride* de 4 et un *structCount* de 1.

À l’opposé, vous pouvez déclarer un g unique \# avec une structure Stride de 32KO et un nombre de structures de 1.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






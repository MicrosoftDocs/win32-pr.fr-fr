---
title: dcl_tgsm_raw (SM5-ASM)
description: Déclarez une référence à une région d’espace mémoire partagée disponible pour le groupe de threads du nuanceur de calcul.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0945cde7719129ca43368e50258c02727103209b8d467932e79acd1e1150c89f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024689"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a>DCL \_ TGSM \_ brute (SM5-ASM)

Déclarez une référence à une région d’espace mémoire partagée disponible pour le groupe de threads du nuanceur de calcul.



| DCL \_ TGSM \_ brute g \# , byteCount |
|-------------------------------|



 



| Élément                                                                                                       | Description                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*activée\#*<br/>                                                 | \[dans \] une référence à un bloc de taille *byteCount* de mémoire partagée non typée. <br/> |
| <span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*<br/> | \[dans \] doit être un multiple de 4. <br/>                                             |



 

## <a name="remarks"></a>Remarques

Le stockage total pour tous les g \# doit être <= la quantité de mémoire partagée disponible par groupe de threads, soit 32KO.

Dans un cas extrême, vous pouvez déclarer 8192 g s au total \# , chacun avec un *byteCount* de 4.

Dans l’autre extrême, vous pouvez déclarer un g unique \# avec un *byteCount* de 32768.

> [!Note]  
> CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge la [ \_ TGSM \_ structurée DCL](dcl-tgsm-structured--sm5---asm-.md), mais pas la **\_ TGSM \_ brute du DCL**.

 

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 






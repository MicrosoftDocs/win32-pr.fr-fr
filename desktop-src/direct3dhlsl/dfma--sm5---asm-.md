---
title: DFMA (SM5-ASM)
description: Effectue un ajout de multiplication par fusion.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84952ed594ba8541223df072fa59550aded581e5517dee3d6f4168b7661a87aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068389"
---
# <a name="dfma-sm5---asm"></a>DFMA (SM5-ASM)

Effectue un ajout de multiplication par fusion.



| DFMA \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération. La valeur de résultat doit être précise à 0,5 ULP.<br/> *dest*  =  . *src0* \* *src1*  +  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants à multiplier avec *src1*.<br/>                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] les composants à multiplier avec *src0*.<br/>                                                                                                 |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[dans \] les composants à ajouter à *src0* \* *src1*.<br/>                                                                                               |



 

## <a name="remarks"></a>Remarques

Les nuanceurs qui utilisent cette instruction sont marqués d’un indicateur de nuanceur qui entraîne l’échec de la liaison de ces derniers, sauf si toutes les conditions suivantes sont remplies.

-   Le système prend en charge DirectX 11,1.
-   Le système comprend un pilote WDDM 1,2.
-   Le pilote fournit une prise en charge pour cette instruction via les **\_ options d3d11 des données de la fonctionnalité d3d11 \_ \_ \_ . ExtendedDoublesShaderInstructions** défini sur **true**.

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

 

 






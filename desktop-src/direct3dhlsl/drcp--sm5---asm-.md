---
title: DRCP (SM5-ASM)
description: Calcule une réciproque à double précision au niveau du composant.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b678f4e8b3464817215de9132298fdde1f6feec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313693"
---
# <a name="drcp-sm5---asm"></a>DRCP (SM5-ASM)

Calcule une réciproque à double précision au niveau du composant.



| RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des résultats<br/> *dest*  =  . **1,0**  /  *src0*. La valeur de résultat doit être précise à 1,0 ULP<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le nombre à prendre la réciproque de.<br/>                                                                         |



 

## <a name="remarks"></a>Notes

L’instruction DRCP est émise par le compilateur HLSL uniquement lorsqu’il est appelé explicitement par le biais de l’intrinsèque RCP (), quand un double est utilisé comme argument. La précision de cette instruction doit être de 1,0 ULP.

Les nuanceurs qui utilisent cette instruction sont marqués d’un indicateur de nuanceur qui entraîne l’échec de la liaison de ces derniers, sauf si toutes les conditions suivantes sont remplies.

-   Le système prend en charge DirectX 11,1.
-   Le système comprend un pilote WDDM 1,2.
-   Le pilote fournit une prise en charge pour cette instruction via les **\_ options d3d11 des données de la fonctionnalité d3d11 \_ \_ \_ . ExtendedDoublesShaderInstructions** défini sur **true**.

Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.

Dans ce tableau, F signifie nombre fini-réel.



|               |          |        |        |        |        |          |         |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| **sources**->  | **-INF** | **-F** | **-0** | **+0** | **+ F** | **+ INF** | **NaN** |
| **dest**-> | -0       | -F     | -inf   | +inf   | + F     | +0       | NaN     |



 

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 






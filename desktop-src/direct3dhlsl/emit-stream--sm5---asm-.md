---
title: emit_stream (SM5-ASM)
description: Émet un vertex vers un flux donné.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381160"
---
# <a name="emit_stream-sm5---asm"></a>émettre \_ un flux (SM5-ASM)

Émet un vertex vers un flux donné.



| émettre un \_ flux streamIndex |
|--------------------------|



 



| Élément                                                                                                               | Description                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[dans \] l’index de flux.<br/> |



 

## <a name="remarks"></a>Notes

Cette instruction entraîne la lecture de tous les registres o déclarés \# pour le flux donné à partir du nuanceur Geometry pour générer un vertex. Après l’émission, toutes les données de tous les registres de sortie pour tous les flux de données deviennent non initialisés, pas seulement le flux émis vers.

*streamIndex* doit être une valeur immédiate \[ comprise entre 0 et 3 \] pour un flux déclaré.

À mesure que plusieurs appels de **\_ flux d’émission** sont émis, des primitives sont générées.

### <a name="restrictions"></a>Restrictions

-   **un \_ flux d’émission** peut apparaître un nombre quelconque de fois dans un nuanceur Geometry, y compris dans le contrôle de flux.
-   Si les flux n’ont pas été déclarés, vous devez utiliser [Emit](emit--sm4---asm-.md) au lieu d' **émettre le \_ flux**.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 






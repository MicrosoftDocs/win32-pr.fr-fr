---
title: émission (SM4-ASM)
description: Émettez un sommet.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce90ed4ea87c74c09c6f45d590e8bc7a70bbb8178988b059c2b3a79726aabcb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673079"
---
# <a name="emit-sm4---asm"></a>émission (SM4-ASM)

Émettez un sommet.



| émettra |
|------|



 

## <a name="remarks"></a>Remarques

l' **émission** entraîne la lecture de tous les registres o déclarés \# à partir du nuanceur Geometry pour générer un vertex.

À mesure que plusieurs appels d' **émission** sont émis, des primitives sont générées.

l' **émission** peut apparaître un nombre quelconque de fois dans un nuanceur Geometry, y compris dans le contrôle de Flow.

Si des flux ont été déclarés, vous devez utiliser l' [émission de \_ flux](emit-stream--sm5---asm-.md).

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               | x               |              |



 

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

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

 

 





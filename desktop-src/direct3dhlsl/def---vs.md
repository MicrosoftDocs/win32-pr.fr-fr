---
title: def-vs
description: Définit des constantes de nuanceur de sommets.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5e3d5cbeb4d60f7beffd70c30ba0775863a9782cfb365a4d40bdf5552a186f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855349"
---
# <a name="def---vs"></a>def-vs

Définit des constantes de nuanceur de sommets.

## <a name="syntax"></a>Syntaxe



| def DST, float1, float2, float3, float4 |
|-----------------------------------------|



 

where

-   l’heure d’été est le registre de destination.
-   float1, float2, float3, float4 sont des nombres à virgule flottante.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| def                    | x    | x    | x    | x     | x    | x     |



 

L’instruction def définit une constante de nuanceur dont la valeur est chargée chaque fois qu’un nuanceur est défini sur un appareil. Celles-ci sont appelées constantes immédiates. Les constantes immédiates sont prioritaires sur les constantes définies par les méthodes d’API SetVertexShaderConstantF.

Il existe deux façons de définir une constante dans un nuanceur.

1.  Utilisez DEF-vs pour définir la constante directement à l’intérieur d’un nuanceur.

    def-vs ne peut définir que des constantes à virgule flottante.

2.  Utilisez les méthodes de l’API pour définir une constante.
    -   Utilisez [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) pour définir une constante à virgule flottante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[signatures-vs](defi---vs.md)
</dt> <dt>

[defb-vs](defb---vs.md)
</dt> </dl>

 

 
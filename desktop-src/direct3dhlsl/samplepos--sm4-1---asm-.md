---
title: samplepos (SM 4.1-ASM)
description: Interroge la position d’un exemple dans une vue de ressource de nuanceur donnée ou dans le rastériseur.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381218"
---
# <a name="samplepos-sm41---asm"></a>samplepos (SM 4.1-ASM)

Interroge la position d’un exemple dans une vue de ressource de nuanceur donnée ou dans le rastériseur.



| samplepos dest \[ . Mask \] , srcResource \[ . Swizzle \] , sampleIndex (opérande scalaire) |
|--------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse des résultats de l’opération.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] la ressource de nuanceur.<br/>                         |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[dans \] l’index de l’exemple.<br/>                     |



 

## <a name="remarks"></a>Notes

Cette instruction retourne la position d’échantillon 2D de l’exemple de *sampleIndex* pour la ressource donnée. Elle est valide uniquement pour les ressources qui peuvent être chargées à l’aide de [**ld2dms**](ld2dms--sm4-1---asm-.md) , sauf si le rastériseur est spécifié en tant que *srcResource*.

*srcResource* peut être un \# Registre t (affichage des ressources de nuanceur) ou un registre de rastérisation.

L’instruction calcule le vecteur à virgule flottante (XPosition, YPosition, 0, 0).

Swizzle sur *srcResource* permet aux valeurs retournées d’être swizzled arbitrairement avant d’être écrites dans la destination. La position de l’échantillon est relative au centre du pixel, en fonction du système de coordonnées en pixels.

Si *sampleIndex* est hors limites, un vecteur zéro est retourné. Si aucune ressource n’est liée à l’emplacement spécifié, la valeur 0 est retournée.

**samplepos** peut être utilisé pour des tâches telles que des résolutions personnalisées dans le code du nuanceur.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






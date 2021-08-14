---
title: sampleinfo (SM 4.1-ASM)
description: Interroge le nombre d’échantillons dans une vue de ressource de nuanceur donnée ou dans le rastériseur.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2227afbf7a08a0010efc2efb8fcf87bae85c8f5775e596d92b761b556f8bfb93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510467"
---
# <a name="sampleinfo-sm41---asm"></a>sampleinfo (SM 4.1-ASM)

Interroge le nombre d’échantillons dans une vue de ressource de nuanceur donnée ou dans le rastériseur.



| \[\_uint \] dest \[ . Mask \] , srcResource \[ . Swizzle\] |
|---------------------------------------------------|



 



| Élément                                                                                                               | Description                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse des résultats de l’opération.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] la ressource de nuanceur.<br/>                         |



 

## <a name="remarks"></a>Remarques

Cette instruction retourne le nombre d’échantillons pour la ressource donnée ou le rastériseur. Elle est valide uniquement pour les ressources qui peuvent être chargées à l’aide de [**ld2dms**](ld2dms--sm4-1---asm-.md) , sauf si le rastériseur est spécifié en tant que *srcResource*. *srcResource* peut être un \# Registre t (affichage des ressources du nuanceur) ou un registre de rastérisation.

L’instruction calcule le vecteur (SampleCount, 0, 0, 0).

Swizzle sur *srcResource* permet aux valeurs retournées d’être swizzled arbitrairement avant d’être écrites dans la destination. La valeur retournée est à virgule flottante, à moins que le \_ modificateur uint soit utilisé, auquel cas la valeur retournée est un entier. Si aucune ressource n’est liée à l’emplacement spécifié, la valeur 0 est retournée.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






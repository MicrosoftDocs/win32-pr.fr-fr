---
title: LOD (SM 4.1-ASM)
description: Retourne le niveau de détail (LOD) qui serait utilisé pour le filtrage de texture.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126924423"
---
# <a name="lod-sm41---asm"></a>LOD (SM 4.1-ASM)

Retourne le niveau de détail (LOD) qui serait utilisé pour le filtrage de texture.



| LOD dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler |
|--------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse des résultats.<br/>   |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[dans \] un ensemble de coordonnées de texture.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] un registre de texture.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[dans \] un registre d’échantillonneur.<br/>           |



 

## <a name="remarks"></a>Notes

Cela se comporte comme l' [exemple](sample--sm4---asm-.md) d’instruction, mais un échantillon filtré n’est pas généré. L’instruction calcule le vecteur suivant (ClampedLOD, NonClampedLOD, 0, 0). NonClampedLOD est une valeur LOD calculée qui ignore les conversions de l’échantillonneur ou de la texture (IE : elle peut retourner des valeurs négatives.) ClampedLOD est une valeur de LOD calculée qui serait utilisée par l' **exemple** d’instruction réel. Swizzle sur *srcResource* permet aux valeurs retournées d’être swizzled arbitrairement avant d’être écrites dans la destination.

Si aucune ressource n’est liée à l’emplacement spécifié, la valeur 0 est retournée.

Si l’échantillonneur utilise le filtrage anisotrope, le LOD doit correspondre au niveau MIP fractionnaire en fonction de l’axe le plus petit de l’empreinte elliptique.

Cela est valide pour les types de texture suivants : Texture1D, Texture2D, Texture3D et TextureCube.

L’instruction **LOD** n’est pas définie quand elle est utilisée avec un échantillonneur qui spécifie le filtrage MIP point, en particulier, tout \_ enum de filtre D3D10 qui se termine par le point MIP \_ . (Voici un exemple de D3D10 \_ FILTRE \_ du \_ point MIP minimum du mag \_ \_ .)

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Pris en charge. |
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

 

 






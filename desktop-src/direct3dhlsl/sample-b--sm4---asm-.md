---
title: sample_b (SM4-ASM)
description: Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné. | sample_b (SM4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9193930aadf8874c759fde3beac7d7da4c9d01b709f6e0b1840b36fe0675ef8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790787"
---
# <a name="sample_b-sm4---asm"></a>exemple \_ b (SM4-ASM)

Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné.



| exemple \_ b \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcLODBias. Select ( \_ composant) |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse du résultat de l’opération.<br/>                                                              |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[dans \] un ensemble de coordonnées de texture. Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] un registre de texture. Pour plus d’informations, consultez l' **exemple** d’instruction.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[dans \] un registre d’échantillonneur. Pour plus d’informations, consultez l' **exemple** d’instruction.<br/>                                 |
| <span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*<br/>     | \[\]pour plus d’informations sur ce paramètre, consultez la section **Notes** .<br/>                                        |



 

## <a name="remarks"></a>Remarques

Les données sources peuvent provenir de n’importe quel type de ressource, autre que des mémoires tampons. Un décalage supplémentaire est appliqué au niveau de détail calculé dans le cadre de l’exécution de l’instruction.

Cette instruction se comporte comme l' [exemple](sample--sm4---asm-.md) d’instruction, avec l’ajout de la valeur *srcLODBias* spécifiée au niveau de détail calculé dans le cadre de l’exécution de l’instruction avant de sélectionner le ou les mappages MIP. La valeur *srcLODBias* est ajoutée au LOD calculé sur une base par pixel, avec la valeur de l’échantillonneur MipLODBias, avant la bride à MinLOD et MaxLOD.

### <a name="restrictions"></a>Restrictions

-   l' **exemple \_ b** hérite des mêmes restrictions que l' [exemple](sample--sm4---asm-.md) d’instruction, ainsi que des restrictions supplémentaires pour son paramètre supplémentaire.
-   La plage de *srcLODBias* est (-16 f à 15.99 f); les valeurs qui ne sont pas comprises dans cette plage produisent des résultats indéfinis.
-   *srcLODBias* doit utiliser un sélecteur de composant unique s’il n’est pas un scalaire immédiat.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

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

 

 






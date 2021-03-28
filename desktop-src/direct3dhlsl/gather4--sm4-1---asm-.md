---
title: gather4 (SM 4.1-ASM)
description: Rassemble les quatre texels qui seraient utilisés dans une opération de filtrage bilinéaire et les regroupe dans un seul registre. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974151"
---
# <a name="gather4-sm41---asm"></a>gather4 (SM 4.1-ASM)

Rassemble les quatre texels qui seraient utilisés dans une opération de filtrage bilinéaire et les regroupe dans un seul registre.



| gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] srcSampler. r |
|--------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse du résultat de l’opération.<br/>                                                                                                       |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[dans \] contient les coordonnées de texture. <br/>                                                                                                                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] un registre des ressources. <br/> Le Swizzle permet aux valeurs retournées d’être swizzled arbitrairement avant qu’elles soient écrites dans *dest*. <br/>            |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[dans \] un registre d’échantillonneur.<br/> Ce paramètre doit avoir un. r (rouge) Swizzle, ce qui indique que la valeur du canal R est copiée vers *dest*. <br/> |



 

## <a name="remarks"></a>Notes

Cette opération fonctionne uniquement avec les textures 2D ou carte cubique à canal unique. Pour les textures 2D, seuls les modes d’adressage de l’échantillonneur sont utilisés et le niveau supérieur d’une pyramide MIP est utilisé.

Cette instruction se comporte comme l' [exemple](sample--sm4---asm-.md) d’instruction, mais un échantillon filtré n’est pas généré. Les quatre exemples qui contribuent au filtrage sont placés dans XYZW dans le sens inverse des aiguilles d’une montre, en commençant par l’échantillon dans le coin inférieur gauche de l’emplacement interrogé. Cela est identique à l’échantillonnage de point avec les deltas de coordonnée de texture (u, v) aux emplacements suivants : (-, +), (+, +), (+,-), (-,-), où l’amplitude des deltas est toujours la moitié d’un Texel.

Pour les textures de carte cubique lorsqu’un encombrement bi-linéaire s’étend sur un contour, les texels de la facette voisine sont utilisés. Les angles utilisent les mêmes règles que l' **exemple** d’instruction. autrement dit, l’angle inconnu est considéré comme la moyenne des trois angles de face de l’Intertest.

Les restrictions de format de texture qui s’appliquent aux instructions d' **exemple** s’appliquent également à l’instruction **gather4** .

Pour les implémentations matérielles, les optimisations dans le filtrage bilinéaire traditionnel qui détectent les échantillons directement sur les texels et ignorent la lecture des texels qui auraient un poids égal à 0 ne peuvent pas être exploitées avec **gather4**. **gather4** retourne toujours tous les texels demandés.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 






---
title: gather4 (SM5-ASM)
description: Rassemble les quatre texels qui seraient utilisés dans une opération de filtrage bilinéaire et les regroupe dans un seul registre. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d613eed2f54db109dbddba59a240b535ccfbc8e4833b874719b6f3d4a51748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067939"
---
# <a name="gather4-sm5---asm"></a>gather4 (SM5-ASM)

Rassemble les quatre texels qui seraient utilisés dans une opération de filtrage bilinéaire et les regroupe dans un seul registre. Cette instruction fonctionne uniquement avec les textures 2D ou carte cubique, y compris les tableaux. Seuls les modes d’adressage de l’échantillonneur sont utilisés et le niveau supérieur d’une pyramide MIP est utilisé.



| gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . Select \_ composant\] |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse des résultats de l’opération.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[dans \] un ensemble de coordonnées de texture.<br/>                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] un registre de texture.<br/>                          |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[dans \] un registre d’échantillonneur.<br/>                          |



 

## <a name="remarks"></a>Remarques

Cette instruction se comporte comme l' [**exemple**](sample--sm4---asm-.md) d’instruction, mais un échantillon filtré n’est pas généré. Les quatre exemples qui contribuent au filtrage sont placés dans XYZW dans le sens inverse des aiguilles d’une montre, en commençant par l’échantillon dans le coin inférieur gauche de l’emplacement interrogé. Cela est identique à l’échantillonnage de point avec les deltas de coordonnée de texture (u, v) aux emplacements suivants : (-, +), (+, +), (+,-), (-,-), où l’amplitude des deltas est toujours la moitié d’un Texel.

Pour les textures carte cubique, quand un encombrement bi-linéaire s’étend sur une arête, les texels de la facette voisine sont utilisés. Les angles utilisent les mêmes règles que l' [**exemple**](sample--sm4---asm-.md) d’instruction. autrement dit, l’angle inconnu est considéré comme la moyenne des trois angles de face du test.

Des restrictions de format de texture s’appliquent aux **gather4** qui sont exprimées dans la liste de formats.

Swizzle sur *srcResource* permet aux valeurs retournées d’être swizzled arbitrairement avant d’être écrites dans la destination.

Le composant. Select \_ sur *srcSampler* choisit le composant de la texture source (r/g/b/a) à partir duquel lire 4 texels.

Pour les formats avec des composants float32, si la valeur extraite est normalisée, dénormalisée, +-0 ou +-INF, elle est retournée au nuanceur non modifié. NaN est retourné en tant que NaN, mais la représentation exacte du bit de NaN peut être modifiée. Pour TextureCubes, une certaine synthèse du 4ème Texel manquant doit se produire au niveau des angles, de sorte que les bits inchangés pour le Texel synthétisé ne s’appliquent pas et les dénormes peuvent être vidées.

Pour les implémentations matérielles, les optimisations dans le filtrage bilinéaire traditionnel qui détectent des échantillons directement sur les texels et ignorent la lecture des texels qui auraient un poids égal à 0 ne peuvent pas être exploitées avec cette instruction. *gather4* retourne toujours tous les texels demandés.

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

 

 






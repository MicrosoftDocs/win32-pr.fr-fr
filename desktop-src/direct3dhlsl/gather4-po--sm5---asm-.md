---
title: gather4_po (SM5-ASM)
description: Une variante de gather4, mais au lieu de prendre en charge un décalage immédiat \-8.. 7 \, le décalage est fourni en tant que paramètre à l’instruction, et la plus grande plage de \-32.. 31 \.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971586"
---
# <a name="gather4_po-sm5---asm"></a>gather4 \_ po (SM5-ASM)

Une variante de [gather4](gather4--sm5---asm-.md), mais au lieu de prendre en charge un offset immédiat \[ -8.. 7 \] , le décalage est fourni en tant que paramètre à l’instruction, et la plus grande plage de \[ -32.. 31 \] .



| gather4 \_ po dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . Select \_ composant\] |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse du résultat de l’opération.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[dans \] un ensemble de coordonnées de texture.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>         | \[dans \] le décalage.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] un registre de texture.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[dans \] un registre d’échantillonneur.<br/>                         |



 

## <a name="remarks"></a>Notes

Les deux premiers composants du paramètre décalage à 4 vecteurs fournissent des décalages d’entiers 32 bits. Les autres composants de ce paramètre sont ignorés.

Les 6 bits les moins significatifs de chaque valeur de décalage sont honorés en tant que valeur signée, ce qui donne \[ -32.. 31 \] .

Cette instruction fonctionne uniquement avec les textures 2D, contrairement à **gather4**, qui fonctionne également avec TextureCubes.

Les seuls modes honorés dans l’échantillonneur sont les modes d’adressage. Seul le MIP le plus détaillé dans l’affichage des ressources est utilisé.

Si l’adresse se trouve sur un centre de Texel, cela ne signifie pas que les autres texels peuvent être mis à zéro.

Le paramètre *srcSampler* inclut le \[ composant. Select \_ \] , qui permet de récupérer n’importe quel composant d’une texture, y compris les valeurs par défaut pour les composants manquants.

Pour les formats avec des composants float32, si la valeur extraite est normalisée, dénormalisée, +-0 ou +-INF, elle est retournée au nuanceur non modifié. NaN est retourné en tant que NaN, mais la représentation exacte du bit de NaN peut être modifiée. Pour TextureCubes, une certaine synthèse du 4e Texel manquant doit se produire au niveau des angles, de sorte que la notion de retour de bits inchangé pour le Texel synthétisé ne s’applique pas et les dénormes peuvent être vidées.

Utilisez cette instruction pour étendre la plage de décalage de **gather4** à plus grande taille et programmable. Le suffixe « po » sur le nom signifie « décalage programmable ».

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

 

 






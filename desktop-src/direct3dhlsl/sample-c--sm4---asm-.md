---
title: sample_c (SM4-ASM)
description: Effectue un filtre de comparaison.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403635"
---
# <a name="sample_c-sm4---asm"></a>exemple \_ c (SM4-ASM)

Effectue un filtre de comparaison.



| exemple \_ c \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource. r,//doit être. r Swizzle srcSampler, srcReferenceValue//composant unique sélectionné |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                                                       | Description                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[dans \] l’adresse des résultats de l’opération.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[dans \] un ensemble de coordonnées de texture. Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[dans \] un registre de texture. Pour plus d’informations, consultez l' **exemple** d’instruction.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[dans \] un registre d’échantillonneur. Pour plus d’informations, consultez l' **exemple** d’instruction.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[dans \] un registre avec un seul composant sélectionné, qui est utilisé dans la comparaison.<br/>                            |



 

## <a name="remarks"></a>Notes

L’objectif principal de cette instruction est de fournir un bloc de construction pour Percentage-Closer le filtrage de profondeur. Le « c » dans l' **exemple \_ c** représente la comparaison.

Les opérandes de l' **exemple \_ c** sont identiques à ceux de l' [exemple](sample--sm4---asm-.md) d’instruction, à ceci près qu’il existe un opérande source float32 supplémentaire, *srcReferenceValue*, qui doit être un registre avec un composant unique sélectionné ou un littéral scalaire.

Le paramètre *srcResource* doit avoir un. r (rouge) Swizzle. l' **exemple \_ c** fonctionne exclusivement sur le composant rouge et retourne une valeur unique. Le. r Swizzle sur *srcResource* indique que le résultat scalaire est répliqué sur tous les composants.

Quand une mémoire tampon de profondeur est définie en tant que texture d’entrée, la valeur de profondeur s’affiche dans le composant rouge.

Si cette instruction est utilisée avec une ressource qui n’est pas un Texture1D/2D/2DArray/cube/CubeArray, elle produit des résultats non définis.

Lorsque cette instruction est exécutée, le matériel d’échantillonnage utilise le ComparisonFunction de l’échantillonneur actuel pour comparer *srcReferenceValue* par rapport à la valeur du composant rouge pour la ressource source à chaque « TAP » de filtre (Texel) que le filtre de texture actuellement configuré couvre, en fonction des coordonnées fournies dans *srcAddress*.

La comparaison se produit après que *srcReferenceValue* a été quantifiée à la précision du format de texture, exactement de la même façon que z est quantifiée à la précision de la mémoire tampon de profondeur avant la comparaison de profondeur au test de visibilité de la fusion de sortie. Cela comprend une bride à la plage de format (par exemple, \[ 0.. 1 \] pour un format UNORM).

Le composant rouge du Texel source est comparé au *srcReferenceValue* quantifié. Pour les texels qui sont en dehors de la ressource, la valeur du composant rouge est déterminée en appliquant les modes d’adresse (et BorderColorR en mode de bordure) à partir de l’échantillonneur. La comparaison honore toutes les règles de comparaison de virgule flottante D3D11, dans le cas où le format de texture est virgule flottante.

Chaque comparaison qui passe retourne 1,0 f comme valeur de composant rouge pour le Texel, et chaque comparaison qui échoue retourne 0,0 f comme valeur rouge pour la texture. Le filtrage se produit exactement comme spécifié par les États de l’échantillonneur, en opérant uniquement dans le composant rouge et en renvoyant un résultat de filtre scalaire unique au nuanceur, répliqué sur tous les composants de *dest* masqués.

L’utilisation de l' **exemple \_ c** est orthogonale à tous les autres contrôles de filtrage à usage général. l' **exemple \_ c** fonctionne de façon transparente avec les autres modes de filtre à usage général. l' **exemple \_ c** modifie le comportement des filtres à usage général de telle sorte que les valeurs qui sont filtrées deviennent 1,0 f ou 0.0 f en raison des résultats de la comparaison.

L’extraction à partir d’un emplacement d’entrée auquel rien n’est lié retourne 0 pour tous les composants.

Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.

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
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






---
title: tex1Dgrad
description: Échantillonne une texture 1D à l’aide d’un dégradé pour sélectionner le niveau MIP. | tex1Dgrad
ms.assetid: 30a28985-4808-4ce6-a3b1-40a9f93cbd8d
keywords:
- HLSL tex1Dgrad
topic_type:
- apiref
api_name:
- tex1Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 195607c8b3fc1844e7d417bb37de7dd270d5a448
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012744"
---
# <a name="tex1dgrad"></a>tex1Dgrad

Échantillonne une texture 1D à l’aide d’un dégradé pour sélectionner le niveau MIP.



| RET tex1Dgrad (s, t, DDX, ddy) |
|-------------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                         | Description                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*x*<br/>       | \[dans \] l’état de l’échantillonneur.<br/>                                         |
| <span id="t"></span><span id="T"></span>*t*<br/>       | \[dans \] la coordonnée de texture.<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*DDX*<br/> | \[en \] taux de changement de la géométrie de la surface dans l’axe x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[en \] taux de changement de la géométrie de la surface dans l’axe y.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Valeur des données de texture.

## <a name="type-description"></a>Description du type



| Nom | Entrée/Sortie | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler1D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| DDX  | in     | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| ddy  | in     | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| Av  | out    | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge                |
|-----------------------------------------------------------|--------------------------|
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui (nuanceur de pixels uniquement)  |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Oui (nuanceur de pixels uniquement) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Oui (nuanceur de pixels uniquement) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non                       |



 

1.  La réorganisation de code importante est effectuée pour déplacer des calculs de dégradé en dehors du contrôle de Flow.
2.  Si le \_ Cap D3DPSHADERCAPS2 0 est défini avec D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, le compilateur mappe cette fonction à texldd.

## <a name="remarks"></a>Notes

Lorsque le contrôle de Flow est présent dans un nuanceur, le résultat d’un calcul de dégradé demandé dans un chemin de branche donné est ambigu lorsque les pixels adjacents peuvent descendre dans des chemins de contrôle de Flow distincts. Par conséquent, il est jugé illégal d’utiliser toute opération de nuanceur de pixels qui demande un calcul de dégradé à un emplacement qui se trouve à l’intérieur d’une construction de contrôle de Flow qui peut varier d’un pixel à l’autre, pour une primitive donnée en cours de pixellisation. Si l’un des côtés d’une instruction **If** avec l’attribut Branch utilise une fonction de dégradé, une erreur de compilateur peut être générée. Consultez l' [instruction if (DirectX HLSL)](dx-graphics-hlsl-if.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


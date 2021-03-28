---
title: texCUBE (référence HLSL)-sélectionner le niveau MIP
description: Échantillonne une texture de cube à l’aide d’un dégradé pour sélectionner le niveau MIP. | texCUBE (référence HLSL)
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
keywords:
- HLSL texCUBE
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6286b4fedb94b9fd5c84c76171e9478f06e16ce4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982674"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a>texCUBE (référence HLSL)-sélectionner le niveau MIP

Échantillonne une texture de cube à l’aide d’un dégradé pour sélectionner le niveau MIP.



| RET texCUBE (s, t, DDX, ddy) |
|-----------------------------|



 

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
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [samplerCUBE](dx-graphics-hlsl-sampler.md)                    | 1    |
| t    | in     | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| DDX  | in     | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| ddy  | in     | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
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

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


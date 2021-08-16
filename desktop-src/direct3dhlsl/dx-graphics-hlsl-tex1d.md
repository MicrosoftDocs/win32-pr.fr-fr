---
title: tex1D (référence HLSL)
description: Échantillonne une texture 1D.
ms.assetid: 587be0fd-af12-4bf0-862b-84988435e90e
keywords:
- HLSL tex1D
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fd7c8b02d9bbd904ae9205201203bbfdb06ad48d749048be7bc81cbfa83caca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725687"
---
# <a name="tex1d-hlsl-reference"></a>tex1D (référence HLSL)

Échantillonne une texture 1D.



| RET tex1D (s, t) |
|-----------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*x*<br/> | \[dans \] l’état de l’échantillonneur.<br/>      |
| <span id="t"></span><span id="T"></span>*t*<br/> | \[dans \] la coordonnée de texture.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Valeur des données de texture.

## <a name="type-description"></a>Description du type



| Nom | Entrée/Sortie | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | commencer     | [**dessin**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler1D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | commencer     | [**Scala**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| Av  | out    | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Pris en charge                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui (nuanceur de pixels uniquement), mais vous devez utiliser l' [option de compilation héritée](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) lors de la compilation. |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Oui (nuanceur de pixels uniquement)                                                                                                           |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Oui (nuanceur de pixels uniquement)                                                                                                           |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Oui (nuanceur de pixels uniquement)                                                                                                           |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


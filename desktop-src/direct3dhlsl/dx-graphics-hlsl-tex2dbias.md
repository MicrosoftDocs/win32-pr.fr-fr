---
title: tex2Dbias
description: Échantillonne une texture 2D après avoir biaisé le niveau MIP par t.w.
ms.assetid: adf2891a-732a-4953-875b-df315c19748b
keywords:
- HLSL tex2Dbias
topic_type:
- apiref
api_name:
- tex2Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cfaec24e1d188460d36a24d68b0fde8ddcb45c29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316163"
---
# <a name="tex2dbias"></a>tex2Dbias

Échantillonne une texture 2D après avoir biaisé le niveau MIP par t.w.



| RET tex2Dbias (s, t) |
|---------------------|



 

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
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Av  | out    | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge               |
|-----------------------------------------------------------|-------------------------|
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui (nuanceur de pixels uniquement) |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Oui (nuanceur de pixels uniquement) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Oui (nuanceur de pixels uniquement) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non                      |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


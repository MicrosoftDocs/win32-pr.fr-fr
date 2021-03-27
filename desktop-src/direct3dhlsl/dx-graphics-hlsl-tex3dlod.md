---
title: tex3Dlod
description: Échantillonne une texture 3D avec des mipmaps. Le LOD mipmap est spécifié dans t.w.
ms.assetid: 9bdd8fa1-8c02-4765-8f4d-61ceb532354e
keywords:
- HLSL tex3Dlod
topic_type:
- apiref
api_name:
- tex3Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc25af449f7f32e94d4ca344bf5ef3a4d09b376c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971706"
---
# <a name="tex3dlod"></a>tex3Dlod

Échantillonne une texture 3D avec des mipmaps. Le LOD mipmap est spécifié dans t.w.



| RET tex3Dlod (s, t) |
|--------------------|



 

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
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Av  | out    | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge               |
|-----------------------------------------------------------|-------------------------|
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui (nuanceur de pixels uniquement) |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Oui (nuanceur de pixels uniquement) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non                      |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non                      |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


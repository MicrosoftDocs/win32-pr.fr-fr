---
title: bruit
description: Génère une valeur aléatoire à l’aide de l’algorithme perl-Noise.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- bruit HLSL
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228203"
---
# <a name="noise"></a>bruit

Génère une valeur aléatoire à l’aide de l’algorithme perl-Noise.




| bruit *RET* (*x*) |
|------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] un vecteur à virgule flottante à partir duquel générer le bruit perl.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Valeur de bruit perl dans une plage comprise entre-1 et 1.

## <a name="remarks"></a>Notes

Les valeurs de bruit perl évoluent correctement d’un point à un autre sur un espace, ce qui crée des valeurs générées de façon aléatoire et à l’aspect naturel. Vous pouvez utiliser le bruit Perl pour générer des textures procédurales pour des effets tels que la fumée et le feu.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle  |
| *Av* | [**Scala**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge           |
|------------------------------------------------------------------------------------|---------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | non                  |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Oui (TX \_ 1 \_ 0 uniquement) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


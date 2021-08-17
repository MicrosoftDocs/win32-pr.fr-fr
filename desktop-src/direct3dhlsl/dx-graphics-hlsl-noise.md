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
ms.openlocfilehash: 5eb93d32e7730b6840700bba9dc5a629bf3180f83673581f8589a254d467cff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120103"
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

## <a name="remarks"></a>Remarques

Les valeurs de bruit perl évoluent correctement d’un point à un autre sur un espace, ce qui crée des valeurs générées de façon aléatoire et à l’aspect naturel. Vous pouvez utiliser le bruit Perl pour générer des textures procédurales pour des effets tels que la fumée et le feu.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle  |
| *Av* | [**Scala**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Pris en charge           |
|------------------------------------------------------------------------------------|---------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | non                  |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Oui (TX \_ 1 \_ 0 uniquement) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


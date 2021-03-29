---
title: lerp
description: Effectue une interpolation linéaire.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- HLSL Lerp
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7a5251aaf410d7224b87b9ee9a8f0e8a0c947e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990940"
---
# <a name="lerp"></a>lerp

Effectue une interpolation linéaire.



| *RET* Lerp (*x*, *y*, *s*) |
|---------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la première valeur à virgule flottante.<br/>                                                     |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[dans \] la deuxième valeur à virgule flottante.<br/>                                                    |
| <span id="s"></span><span id="S"></span>*x*<br/> | \[dans \] une valeur qui interpole de manière linéaire entre le paramètre *x* et le paramètre *y* .<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Résultat de l’interpolation linéaire.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *y*   | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |
| *s*   | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |
| *Av* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="remarks"></a>Notes

L’interpolation linéaire est basée sur la formule suivante : x \* (1-s) + y \* s qui peut être écrit de façon équivalente sous la forme x + s (y-x).

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | Oui                         |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Oui (vs \_ 1 1 \_ et PS \_ 1 \_ 1) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


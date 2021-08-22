---
title: minute(s)
description: Sélectionne le plus petit de x et y.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- HLSL min
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ba9474383af448c36c6bb1130470aa6706fd8bd06c2d21bef66eb1c4bbcda0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513820"
---
# <a name="min"></a>minute(s)

Sélectionne le plus petit de x et y.



| RET min (x, y) |
|---------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur d’entrée x.<br/> |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[dans \] la valeur d’entrée y.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Paramètre *x* ou *y* , selon la valeur la plus petite.


## <a name="remarks"></a>Remarques

Les dénormals sont gérés comme suit :

| src0 src1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | -inf          | -inf | -inf |
| F           | -inf | src0 ou src1  | src0 | src0 |
| +inf        | -inf | src1          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F signifie nombre fini-réel.


## <a name="type-description"></a>Description du type

| Name | Entrée/Sortie      | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                 | Taille                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | commencer          | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                          |
| y    | commencer          | identique à l’entrée x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | la ou les mêmes dimensions comme entrée x |
| Av  | type de retour | identique à l’entrée x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | la ou les mêmes dimensions comme entrée x |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Pris en charge                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | oui                         |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Oui (vs \_ 1 \_ 1 et PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**Spécification fonctionnelle DirectX**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)
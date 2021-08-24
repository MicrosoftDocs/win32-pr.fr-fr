---
title: atan2 (Corecrt \_ Math. h)
description: Retourne l’arc tangente de deux valeurs (x, y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- langage HLSL atan2
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2932f82cf6d9e8b2071446b63f84e60727aff2da2213461d3c1194b2811fe1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854969"
---
# <a name="atan2"></a>atan2

Retourne l’arc tangente de deux valeurs (x, y).



| *RET* atan2 (*y*, *x*) |
|-----------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                    |
|--------------------------------------------------------|--------------------------------|
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[dans \] la valeur y.<br/> |
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur x.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Arctangente de (y, x).

## <a name="remarks"></a>Remarques

Les signes des paramètres *x* et *y* sont utilisés pour déterminer le quadrant des valeurs de retour dans la plage de-π à π. La fonction intrinsèque HLSL **atan2** est bien définie pour chaque point autre que l’origine, même si *y* est égal à 0 et que *x* n’est pas égal à 0.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *Av* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Pris en charge |
|------------------------------------------------------------------------------------|-----------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | oui       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


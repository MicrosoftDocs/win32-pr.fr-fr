---
title: fmod (Corecrt \_ Math. h)
description: Retourne le reste à virgule flottante de x/y.
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- HLSL fmod
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e35f4de2c935f88c92aa1ebde2b4fcf9e8987c7f0824b38e260b727d9d34150
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789719"
---
# <a name="fmod"></a>fmod

Retourne le reste à virgule flottante de x/y.



| *RET* fmod (*x*, *y*) |
|----------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] le dividende à virgule flottante.<br/> |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[dans \] le diviseur à virgule flottante.<br/>  |



 

## <a name="return-value"></a>Valeur renvoyée

Reste à virgule flottante du paramètre *x* divisé par le paramètre *y* .

## <a name="remarks"></a>Remarques

Le reste à virgule flottante est calculé de telle sorte que x = i \* y + f, où i est un entier, f a le même signe que x, et la valeur absolue de f est inférieure à la valeur absolue de y.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *y*   | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |
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

 


---
title: étape
description: Compare deux valeurs, en retournant 0 ou 1 en fonction de la valeur la plus élevée.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- étape HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c800e8d8c6f78386139f822f118163f3b431f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729525"
---
# <a name="step"></a>étape

Compare deux valeurs, en retournant 0 ou 1 en fonction de la valeur la plus élevée.



| *RET* , étape (*y*, *x*) |
|----------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[dans \] la première valeur à virgule flottante à comparer.<br/>  |
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la deuxième valeur à virgule flottante à comparer.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

1 si le paramètre *x* est supérieur ou égal au paramètre *y* ; Sinon, 0.

## <a name="remarks"></a>Notes

Cette fonction utilise la formule suivante : (*x*  >=  *y*) ? 1:0. La fonction retourne la valeur 0 ou 1, selon que le paramètre *x* est supérieur au paramètre *y* . Pour calculer une interpolation lisse entre 0 et 1, utilisez la fonction intrinsèque [**SmoothStep**](dx-graphics-hlsl-smoothstep.md) HLSL.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *x*   | identique à l’entrée *y*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *y* |
| *Av* | identique à l’entrée *y*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *y* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | Oui                         |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Oui (vs \_ 1 \_ 1 et PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


---
title: ldexp (Corecrt \_ Math. h)
description: Retourne le résultat de la multiplication de la valeur spécifiée par deux, élevé à la puissance de l’exposant spécifié.
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- HLSL ldexp
topic_type:
- apiref
api_name:
- ldexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fd5514e7fd942527931050d7f3efda33158d08329972900f836fe41e6822b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726267"
---
# <a name="ldexp"></a>ldexp

Retourne le résultat de la multiplication de la valeur spécifiée par deux, élevé à la puissance de l’exposant spécifié.



| *RET* ldexp (*x*, *exp*) |
|-------------------------|



 

Cette fonction utilise la formule suivante : *x* \* 2 <sup>exp</sup>

## <a name="parameters"></a>Paramètres



| Élément                                                         | Description                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/>       | \[dans \] la valeur spécifiée.<br/>    |
| <span id="exp"></span><span id="EXP"></span>*venir*<br/> | \[dans \] l’exposant spécifié.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Résultat de la multiplication du paramètre *x* par deux, élevé à la puissance du paramètre *exp* .

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *exp* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |
| *Av* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Pris en charge           |
|------------------------------------------------------------------------------------|---------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | oui                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Oui (vs \_ 1 \_ 1 uniquement) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


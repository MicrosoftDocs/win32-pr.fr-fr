---
title: frexp (Corecrt \_ Math. h)
description: Retourne la mantisse et l’exposant de la valeur à virgule flottante spécifiée.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- HLSL frexp
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953844"
---
# <a name="frexp"></a>frexp

Retourne la mantisse et l’exposant de la valeur à virgule flottante spécifiée.



| *RET* frexp (*x*, *exp*) |
|-------------------------|



 

La valeur de retour est la mantisse et la valeur retournée par le paramètre *exp* est l’exposant.

## <a name="parameters"></a>Paramètres



| Élément                                                         | Description                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/>       | \[dans \] la valeur à virgule flottante spécifiée. Si le paramètre *x* est égal à 0, cette fonction retourne 0 pour la mantisse et l’exposant.<br/> |
| <span id="exp"></span><span id="EXP"></span>*venir*<br/> | \[sortie \] de l’exposant retourné du paramètre *x* .<br/>                                                                                   |



 

## <a name="return-value"></a>Valeur renvoyée

Mantisse du paramètre *x* .

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *exp* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |
| *Av* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge           |
|------------------------------------------------------------------------------------|---------------------|
| [Nuancier modèle 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) et modèles de nuanceur plus élevés | Oui                 |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | Oui (PS \_ 2 \_ x uniquement) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | non                  |



 

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


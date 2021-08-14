---
title: isNaN (Corecrt \_ Math. h)
description: Détermine si la valeur spécifiée est NAN ou QNAN.
ms.assetid: 09085634-e610-4793-848e-abda8241f1cc
keywords:
- langage HLSL IsNaN
topic_type:
- apiref
api_name:
- isnan
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f60f04d577bcd2e2f8d13cf11e1c02237ae9ddfacd225dff3d0bfca4266c72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791938"
---
# <a name="isnan"></a>isNaN

Détermine si la valeur spécifiée est NAN ou QNAN.



| *RET* IsNaN (*x*) |
|------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur spécifiée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur de la même taille que l’entrée, avec une valeur égale à **true** si le paramètre *x* est NaN ou QNAN. Sinon, **false**.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle      |
| *Av* | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**bool**](/windows/desktop/WinProg/windows-data-types)                         | comme entrée |



 

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

 


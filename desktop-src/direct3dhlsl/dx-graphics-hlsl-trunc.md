---
title: trunc (Corecrt \_ Math. h)
description: Tronque une valeur à virgule flottante en composant entier.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- trunc HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411236"
---
# <a name="trunc"></a>trunc

Tronque une valeur à virgule flottante en composant entier.



| RET trunc (*x*) |
|----------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] l’entrée spécifiée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

La valeur d’entrée est tronquée à un composant entier.

## <a name="remarks"></a>Remarques

Cette fonction tronque une valeur à virgule flottante au composant entier. Étant donné une valeur à virgule flottante de 1,6, la fonction trunc retourne 1,0, où la fonction [**Round (DirectX HLSL)**](dx-graphics-hlsl-round.md) retourne 2,0.

## <a name="type-description"></a>Description du type



| Name | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *x*  | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                          |
| Av  | Même type que l’entrée x                                                                                           | [**float**](/windows/desktop/WinProg/windows-data-types)                        | La ou les mêmes dimensions comme entrée x |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge |
|------------------------------------------------------------------------------------|-----------|
| [Nuancier Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) et modèles de nuanceur plus élevés | Oui       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


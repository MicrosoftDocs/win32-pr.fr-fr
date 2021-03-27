---
title: all
description: Détermine si tous les composants de la valeur spécifiée sont non nuls.
ms.assetid: 9ee079ff-cd2c-41f5-98cd-ea1f4215e7d5
keywords:
- tous les langages HLSL
topic_type:
- apiref
api_name:
- all
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59d59e18655aab10d13af998f4e2aa94da3fa08b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971798"
---
# <a name="all"></a>all

Détermine si tous les composants de la valeur spécifiée sont non nuls.



| *RET* tout (*x*) |
|----------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur spécifiée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

**True** si tous les composants du paramètre *x* sont non null ; Sinon, **false**.

## <a name="remarks"></a>Notes

Cette fonction est similaire à [**toute**](dx-graphics-hlsl-any.md) fonction intrinsèque HLSL. La fonction **any** détermine si tous les composants de la valeur spécifiée sont non nuls, tandis que la fonction **All** détermine si tous les composants de la valeur spécifiée sont non nuls.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Taille |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle  |
| *Av* | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md)                            | [**Boolean**](/windows/desktop/WinProg/windows-data-types)                                                                                 | 1    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge             |
|------------------------------------------------------------------------------------|-----------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | Oui                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 et PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


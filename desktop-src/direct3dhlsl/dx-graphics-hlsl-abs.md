---
title: abs
description: Retourne la valeur absolue de la valeur spécifiée.
ms.assetid: 8c4cfd8f-8aac-4db3-8247-ce2bbf501e80
keywords:
- langage HLSL ABS
topic_type:
- apiref
api_name:
- abs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1acd1903e1a65a38f5af7549ab52577bc6cba51c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971770"
---
# <a name="abs"></a>abs

Retourne la valeur absolue de la valeur spécifiée.



| RET ABS (*x*) |
|--------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur spécifiée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Valeur absolue du paramètre *x* .

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                 | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                            |
| *Av* | identique à l’entrée *x*                                                                                              | identique à l’entrée *x*                                                              | la ou les mêmes dimensions comme entrée *x* |



 

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

 


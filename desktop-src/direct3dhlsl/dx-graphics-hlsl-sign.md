---
title: sign
description: Retourne le signe de x.
ms.assetid: 3e2e04e8-0ffc-4721-a5d8-1ccfa6ca2a1a
keywords:
- signer le langage HLSL
topic_type:
- apiref
api_name:
- sign
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80bd3395d2841a3a47e2218b7d8a5e06e8403f3e9d1d4c94ea5a85e6b39939b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120063"
---
# <a name="sign"></a>sign

Retourne le signe de *x*.



| signe *RET* (*x*) |
|-----------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur d’entrée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Retourne-1 si *x* est inférieur à zéro ; 0 si *x* est égal à zéro ; et 1 si *x* est supérieur à zéro.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                 | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                            |
| *Av* | identique à l’entrée *x*                                                                                              | [**int**](/windows/desktop/WinProg/windows-data-types)                                          | la ou les mêmes dimensions comme entrée *x* |



 

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

 


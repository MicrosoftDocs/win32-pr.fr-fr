---
title: asint
description: Interprète le modèle binaire de x comme un entier.
ms.assetid: e17e0a11-ef52-4b23-94b8-5db0b18aff4d
keywords:
- HLSL asint
topic_type:
- apiref
api_name:
- asint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 492e0b5e400adc4e5c847f12880a668fb5e3b98f683a0f64dbe32ec98f28a93c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789859"
---
# <a name="asint"></a>asint

Interprète le modèle binaire de *x* comme un entier.



| RET asint (*x*) |
|----------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur d’entrée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Entrée interprétée comme un entier.

## <a name="type-description"></a>Description du type



| Name  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                  | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **uint**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                            |
| *Av* | identique à l’entrée *x*                                                                                              | [**int**](/windows/desktop/WinProg/windows-data-types)                                           | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Pris en charge |
|---------------------------------------------------------------------|-----------|
| [Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs | oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | non        |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


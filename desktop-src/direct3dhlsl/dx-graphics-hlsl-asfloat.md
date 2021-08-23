---
title: asfloat
description: Interprète le modèle binaire de x comme un nombre à virgule flottante.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- HLSL asfloat
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d85f6010a8c82f8ae66d5fa56a979a9e946316a5e2737fe2c7257570499055d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043847"
---
# <a name="asfloat"></a>asfloat

Interprète le modèle binaire de *x* comme un nombre à virgule flottante.



| RET asfloat (*x*) |
|------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur d’entrée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Entrée interprétée comme un nombre à virgule flottante.

## <a name="type-description"></a>Description du type



| Name  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                            |
| *Av* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                                                                                | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="function-overloads"></a>Surcharges de fonction

<dl> 'float <x> asfloat (valeur flottante <x> ); `  
` float <x> asfloat ( <x> valeur int); `  
` float <x> asfloat ( <x> valeur uint); '
</dl>

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Pris en charge |
|---------------------------------------------------------------------|-----------|
| [Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs | oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | non        |



 

## <a name="remarks"></a>Remarques

Les compilateurs plus anciens ne `asfloat(bool)` sont pas correctement autorisés, mais notez que les entrées bool ne sont pas prises en charge.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


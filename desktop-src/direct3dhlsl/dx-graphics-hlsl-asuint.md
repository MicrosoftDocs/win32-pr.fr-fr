---
title: asuint
description: Interprète le modèle binaire de x comme un entier non signé.
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- HLSL asuint
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac8be8a81cca5c0ed7377475f2e3688a8c0c90c33fddcaab8c4de0f15f174eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514772"
---
# <a name="asuint"></a>asuint

Interprète le modèle binaire de *x* comme un entier non signé.



| RET asuint (*x*) |
|-----------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur d’entrée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Entrée interprétée comme un entier non signé.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                 | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                            |
| *Av* | identique à l’entrée *x*                                                                                              | [**uint**](/windows/desktop/WinProg/windows-data-types)                                         | la ou les mêmes dimensions comme entrée *x* |



 

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

 


---
title: modf, (Corecrt \_ Math. h)
description: Fractionne la valeur x en parties fractionnaires et entières, chacune ayant le même signe que x.
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- HLSL modf,
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c09af44cb95f35854d4366c05d238423fcecaff7c9a10c3c55fadf6b51dd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513810"
---
# <a name="modf"></a>modf

Fractionne la valeur x en parties fractionnaires et entières, chacune ayant le même signe que x.



| RET modf, (x, adresse IP out) |
|---------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                      | Description                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/>    | \[dans \] la valeur d’entrée x.<br/>           |
| <span id="ip"></span><span id="IP"></span>*adressesIP*<br/> | \[\]partie entière de *x*.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Partie décimale signée de x.

## <a name="type-description"></a>Description du type



| Name | Entrée/Sortie | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                 | Taille                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | commencer     | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                          |
| ip   | out    | identique à l’entrée x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | la ou les mêmes dimensions comme entrée x |
| Av  | out    | identique à l’entrée x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | la ou les mêmes dimensions comme entrée x |



 

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

 


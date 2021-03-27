---
title: dot
description: Retourne le produit scalaire de deux vecteurs.
ms.assetid: ad24c06c-0b40-4dc5-a2b9-1d5438635ed8
keywords:
- HLSL point
topic_type:
- apiref
api_name:
- dot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6d05abf0d67628d1d77b362b028107e07b83457
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941247"
---
# <a name="dot"></a>dot

Retourne le produit scalaire de deux vecteurs.



| *RET* point (*x*, *y*) |
|---------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] le premier vecteur.<br/>  |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[dans \] le second vecteur.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Produit scalaire du paramètre *x* et du paramètre *y* .

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                 | Taille                            |
|-------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| *x*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                             |
| *y*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mêmes dimensions (s) que l’entrée *x* |
| *Av* | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | 1                               |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge |
|------------------------------------------------------------------------------------|-----------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | Oui       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Oui       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


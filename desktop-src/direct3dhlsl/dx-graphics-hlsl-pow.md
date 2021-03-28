---
title: pow
description: Retourne la valeur spécifiée élevée à la puissance spécifiée.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- en HLSL pow
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463634"
---
# <a name="pow"></a>pow

Retourne la valeur spécifiée élevée à la puissance spécifiée.



| *RET* Pow (*x*, *y*) |
|---------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur spécifiée.<br/> |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[dans \] la puissance spécifiée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Le paramètre *x* élevé à la puissance du paramètre *y* .

## <a name="remarks"></a>Notes

La fonction intrinsèque Pow du langage **Pow** calcule *x*<sup>y</sup>.



| X      | Y      | Résultat                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| < 0 | n'importe laquelle    | NAN                                                                         |
| > 0 | = = 0   | 1                                                                           |
| = = 0   | > 0 | 0                                                                           |
| = = 0   | < 0 | fichier                                                                         |
| > 0 | < 0 | 1/X<sup>-Y</sup>                                                            |
| = = 0   | = = 0   | Dépend du processeur graphique<br/> 0, ou 1 ou NAN<br/> |



 

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *y*   | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |
| *Av* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge           |
|------------------------------------------------------------------------------------|---------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | Oui                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Oui (vs \_ 1 \_ 1 uniquement) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


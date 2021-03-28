---
title: DDX
description: Retourne la dérivée partielle de la valeur spécifiée par rapport à la coordonnée x de l’espace d’écran.
ms.assetid: a21c2d2a-7c62-4dc6-8521-273690be1104
keywords:
- DDX en HLSL
topic_type:
- apiref
api_name:
- ddx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc82f41e8968ccfadaf5d87a8058d332f04ce3a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382148"
---
# <a name="ddx"></a>DDX

Retourne la dérivée partielle de la valeur spécifiée par rapport à la coordonnée x de l’espace d’écran.



| *RET* DDX (*x*) |
|----------------|



 

Cette fonction calcule la dérivée partielle par rapport à la coordonnée x de l’espace d’écran. Pour calculer la dérivée partielle par rapport à la coordonnée y de l’espace d’écran, utilisez la fonction [**ddy**](dx-graphics-hlsl-ddy.md) .

Cette fonction est prise en charge uniquement dans les nuanceurs de pixels.

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur spécifiée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Dérivée partielle du paramètre *x* .

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *Av* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui                                       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                                  | Oui                                       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)                   | Oui                                       |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                   | Oui dans PS \_ 2 \_ x ; non pris en charge dans PS \_ 2 \_ 0. |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                   | non                                        |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


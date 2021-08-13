---
title: Round (Corecrt \_ Math. h)
description: Arrondit la valeur spécifiée à l’entier le plus proche.
ms.assetid: 258ce717-dca1-4ed2-ad98-1ecfdb58f939
keywords:
- rondes HLSL
topic_type:
- apiref
api_name:
- round
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3997e93dbbe7cfda210fea97a2759620f0afb47638d2ec519b9ad56abe3664c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513831"
---
# <a name="round"></a>round

Arrondit la valeur spécifiée à l’entier le plus proche. Les cas à mi-chemin sont arrondis au pair le plus proche.



| *RET* . aller-retour (*x*) |
|------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur spécifiée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Paramètre *x* , arrondi à l’entier le plus proche dans un type à virgule flottante.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *Av* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |



 

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

 


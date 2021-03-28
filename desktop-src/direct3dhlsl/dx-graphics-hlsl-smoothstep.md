---
title: smoothstep
description: Retourne une interpolation Smooth Hermite entre 0 et 1, si x est dans la plage \ min, Max \.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- HLSL SmoothStep
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971707"
---
# <a name="smoothstep"></a>smoothstep

Retourne une interpolation Smooth Hermite entre 0 et 1, si *x* est dans la plage \[ *min*, *Max* \] .



| *RET* SmoothStep (*min*, *Max*, *x*) |
|-------------------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                         | Description                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*min*<br/> | \[dans \] la plage minimale du paramètre *x* .<br/> |
| <span id="max"></span><span id="MAX"></span>*Max*<br/> | \[dans \] la plage maximale du paramètre *x* .<br/> |
| <span id="x"></span><span id="X"></span>*x*<br/>       | \[dans \] la valeur spécifiée à interpoler.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Retourne 0 si *x* est inférieur à *min*; 1 si *x* est supérieur à *Max*; Sinon, une valeur comprise entre 0 et 1 si *x* est comprise dans la plage \[ *min*, *Max* \] .

## <a name="remarks"></a>Notes

Utilisez la fonction intrinsèque **SmoothStep** HLSL pour créer une transition lisse entre deux valeurs. Par exemple, vous pouvez utiliser cette fonction pour fusionner deux couleurs en douceur.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *min* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |
| *max* | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |
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

 


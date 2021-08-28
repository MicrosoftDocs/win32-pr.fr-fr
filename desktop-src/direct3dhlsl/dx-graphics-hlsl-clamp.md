---
title: bride
description: Fixe la valeur spécifiée à la plage minimale et maximale spécifiée.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- verrouillage HLSL
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a0350127a26b0c65762e6c927ea38ca944101dcd646026713de231e33e987fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043837"
---
# <a name="clamp"></a>bride

Fixe la valeur spécifiée à la plage minimale et maximale spécifiée.



| *RET* clamp (*x*, *min*, *Max*) |
|--------------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                         | Description                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/>       | \[dans \] une valeur à brider.<br/>            |
| <span id="min"></span><span id="MIN"></span>*min*<br/> | \[dans \] la plage minimale spécifiée.<br/> |
| <span id="max"></span><span id="MAX"></span>*Max*<br/> | \[dans \] la plage maximale spécifiée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Valeur de fixation du paramètre *x* .

## <a name="remarks"></a>Remarques

Pour les valeurs de-INF ou INF, la bride se comportera comme prévu. Toutefois, pour les valeurs NaN, les résultats ne sont pas définis.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                 | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                            |
| *min* | identique à l’entrée *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | la ou les mêmes dimensions comme entrée *x* |
| *max* | identique à l’entrée *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | la ou les mêmes dimensions comme entrée *x* |
| *Av* | identique à l’entrée *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Pris en charge             |
|------------------------------------------------------------------------------------|-----------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | oui                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 et PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


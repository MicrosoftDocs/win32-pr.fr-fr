---
title: faceforward
description: Retourne la surface normale (si nécessaire) à la face dans une direction opposée à i ; retourne le résultat dans n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- HLSL faceforward
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101824"
---
# <a name="faceforward"></a>faceforward

Retourne la surface normale (si nécessaire) à la face dans une direction opposée à i ; retourne le résultat dans n.



| *RET* faceforward (*n*, *i*, *ng*) |
|-----------------------------------|



 

Cette fonction utilise la formule suivante :-*n*  signe (point (*i*, *ng*)).

## <a name="parameters"></a>Paramètres



| Élément                                                      | Description                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*n*<br/>    | \[dans \] le vecteur de surface à virgule flottante résultant-normal.<br/>                                           |
| <span id="i"></span><span id="I"></span>*cliqu*<br/>    | \[dans \] un vecteur à virgule flottante, vecteur d’incident qui pointe de la position de la vue à la position d’ombrage.<br/> |
| <span id="ng"></span><span id="NG"></span>*ng*<br/> | \[dans \] un vecteur de surface à virgule flottante-normal.<br/>                                                       |



 

## <a name="return-value"></a>Valeur renvoyée

Vecteur normal à virgule flottante qui est orienté vers le sens de la vue.

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *n*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *i*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *n* |
| *ng*  | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | mêmes dimensions que l’entrée *n*   |
| *Av* | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | mêmes dimensions que l’entrée *n*   |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge             |
|------------------------------------------------------------------------------------|-----------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | Oui                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 et PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


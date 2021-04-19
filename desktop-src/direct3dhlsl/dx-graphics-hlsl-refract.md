---
title: fraction
description: Retourne un vecteur de réfraction à l’aide d’une entrée Ray, d’une surface normale et d’un index de réfraction.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- réfractx HLSL
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991008"
---
# <a name="refract"></a>fraction

Retourne un vecteur de réfraction à l’aide d’une entrée Ray, d’une surface normale et d’un index de réfraction.



| *RET* réfract (*i*, *n*, ?) |
|----------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*cliqu*<br/> | \[dans \] un vecteur de direction de rayon à virgule flottante.<br/>    |
| <span id="n"></span><span id="N"></span>*n*<br/> | \[dans \] un vecteur de surface à virgule flottante, vecteur normal.<br/>   |
| *?*<br/>                                         | \[dans \] un index scalaire à virgule flottante, réfraction.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Vecteur à virgule flottante, réfraction. Si l’angle entre l’entrée de Ray i et la surface normale n est trop grand pour un index de réfraction donné ?, la valeur de retour est (0, 0, 0).

## <a name="type-description"></a>Description du type



| Nom              | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*               | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *n*               | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions que l’entrée *i* |
| ?                 | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |
| vecteur de réfraction | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions que l’entrée *i* |



 

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

 


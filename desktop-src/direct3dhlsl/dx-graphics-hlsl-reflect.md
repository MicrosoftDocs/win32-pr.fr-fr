---
title: correspond
description: Retourne un vecteur de réflexion à l’aide d’un rayon d’incident et d’une surface normale.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- réfléchir au HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524685"
---
# <a name="reflect"></a>correspond

Retourne un vecteur de réflexion à l’aide d’un rayon d’incident et d’une surface normale.



| *RET* réfléchi (*i*, *n*) |
|-------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*cliqu*<br/> | \[dans \] un vecteur d’incident à virgule flottante.<br/> |
| <span id="n"></span><span id="N"></span>*n*<br/> | \[dans \] un vecteur normal à virgule flottante.<br/>   |



 

## <a name="return-value"></a>Valeur renvoyée

Vecteur de réflexion à virgule flottante.

## <a name="remarks"></a>Remarques

Cette fonction calcule le vecteur de réflexion à l’aide de la formule suivante : v = i-2 \* n \* point (i n).

## <a name="type-description"></a>Description du type



| Name  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *n*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions que l’entrée *i* |
| *Av* | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions que l’entrée *i* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge |
|------------------------------------------------------------------------------------|-----------|
| [Nuancier Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) et modèles de nuanceur plus élevés | Oui       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


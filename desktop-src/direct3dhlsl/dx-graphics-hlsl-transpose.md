---
title: permuter
description: Transpose la matrice d’entrée spécifiée.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- transposer le langage HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382066"
---
# <a name="transpose"></a>permuter

Transpose la matrice d’entrée spécifiée.



| RET transposer (*x*) |
|--------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                             |
|--------------------------------------------------------|-----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la matrice spécifiée.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Valeur transposée du paramètre *x* .

## <a name="remarks"></a>Notes

Si les dimensions de la matrice source sont des *colonnes* de *lignes* , la matrice résultante est celle des *lignes* de *colonnes* .

## <a name="type-description"></a>Description du type



| Nom | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Taille                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| *x*  | [**matrice**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                                                                                    |
| Av  | [**matrice**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | Rows = même nombre de colonnes en entrée *x*, Columns = même nombre de lignes comme entrée *x* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge |
|------------------------------------------------------------------------------------|-----------|
| [Nuancier Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) et modèles de nuanceur plus élevés | Oui       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 


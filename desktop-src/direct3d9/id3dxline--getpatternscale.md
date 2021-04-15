---
description: Obtient la valeur de mise à l’échelle du modèle stipple.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'ID3DXLine :: GetPatternScale, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394263"
---
# <a name="id3dxlinegetpatternscale-method"></a>ID3DXLine :: GetPatternScale, méthode

Obtient la valeur de mise à l’échelle du modèle stipple.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)**

Retourne la valeur utilisée pour mettre à l’échelle le modèle stipple. 1.0 f est la valeur par défaut et ne représente aucune mise à l’échelle. Une valeur inférieure à 1,0 f réduit le modèle, et une valeur supérieure à 1,0 étire le modèle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::SetPatternScale**](id3dxline--setpatternscale.md)
</dt> </dl>

 

 

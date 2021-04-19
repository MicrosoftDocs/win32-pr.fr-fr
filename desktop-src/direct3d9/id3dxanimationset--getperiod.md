---
description: Obtient la période de l’animation définie.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'ID3DXAnimationSet :: GetPeriod, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545895"
---
# <a name="id3dxanimationsetgetperiod-method"></a>ID3DXAnimationSet :: GetPeriod, méthode

Obtient la période de l’animation définie.

## <a name="syntax"></a>Syntaxe


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **double**](../winprog/windows-data-types.md)**

Période de l’ensemble d’animations.

## <a name="remarks"></a>Notes

La période est la plage de temps pendant laquelle les images clés d’animation sont valides. Pour les animations de boucle, il s’agit de la période de la boucle. Les unités de temps dans lesquelles les images clés sont spécifiées (par exemple, secondes) sont déterminées par l’application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 

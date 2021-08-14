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
ms.openlocfilehash: d8e984d1593fbbd79561bbb15fb27b62a9961c1830c42465ed529f08c374e180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522328"
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

## <a name="remarks"></a>Remarques

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

 

 

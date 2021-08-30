---
description: Compte le nombre de frames d’une sous-arborescence qui ont des noms non null.
ms.assetid: bc1cb985-acd1-4ba0-bb3c-3e86fea559da
title: D3DXFrameNumNamedMatrices, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameNumNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db048c7c1cad932afb7841d70f9113fa685c63fc4592bad636f9011064f50cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986899"
---
# <a name="d3dxframenumnamedmatrices-function"></a>D3DXFrameNumNamedMatrices fonction)

Compte le nombre de frames d’une sous-arborescence qui ont des noms non null.

## <a name="syntax"></a>Syntaxe


```C++
UINT D3DXFrameNumNamedMatrices(
  _In_ const D3DXFRAME *pFrameRoot
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFrameRoot* \[ dans\]
</dt> <dd>

Type : **const [**D3DXFRAME**](d3dxframe.md) \***

Pointeur vers le nœud racine de la sous-arborescence.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **uint**](../winprog/windows-data-types.md)**

Retourne le nombre de frames.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’animation](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 

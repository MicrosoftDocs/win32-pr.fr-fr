---
description: Détruit la sous-arborescence des frames sous la racine, y compris la racine.
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: D3DXFrameDestroy, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4e20e878b402ad0b8c4d0a9b721cd9300154305b2a06426564d1639ceddd7a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988479"
---
# <a name="d3dxframedestroy-function"></a>D3DXFrameDestroy fonction)

Détruit la sous-arborescence des frames sous la racine, y compris la racine.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFrameRoot* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFRAME**](d3dxframe.md)**

Pointeur vers le nœud racine.

</dd> <dt>

*pAlloc* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Interface d’allocation utilisée pour libérer des nœuds de la hiérarchie d’images.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’animation](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 





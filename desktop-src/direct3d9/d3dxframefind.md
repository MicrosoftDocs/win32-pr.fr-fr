---
description: Recherche le frame enfant d’un frame racine.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: D3DXFrameFind, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f62cacabbf020d1fe9ff9e83c47acc6c58e52c4ab6be031586bda365745f595
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027659"
---
# <a name="d3dxframefind-function"></a>D3DXFrameFind fonction)

Recherche le frame enfant d’un frame racine.

## <a name="syntax"></a>Syntaxe


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFrameRoot* \[ dans\]
</dt> <dd>

Type : **const [**D3DXFRAME**](d3dxframe.md) \***

Pointeur vers le frame racine. Consultez [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*Nom* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom du Frame enfant à rechercher.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **LPD3DXFRAME**](d3dxframe.md)**

Retourne le frame enfant s’il est trouvé, ou **null** dans le cas contraire. Consultez [**D3DXFRAME**](d3dxframe.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’animation](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 

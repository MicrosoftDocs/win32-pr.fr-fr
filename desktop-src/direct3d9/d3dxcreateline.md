---
description: Utilise un système de coordonnées droitier pour créer une ligne.
ms.assetid: 0d2ef331-9edf-4b0a-ace4-ecb8bb2f7352
title: D3DXCreateLine, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f821f613babac6d4ee801b7321ff15d902b72e908401ce248604dd2617841c74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857129"
---
# <a name="d3dxcreateline-function"></a>D3DXCreateLine fonction)

Utilise un système de coordonnées droitier pour créer une ligne.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateLine(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXLINE        *ppLine
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la maille Box créée.

</dd> <dt>

*ppLine* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXLINE**](id3dxline.md)\***

Pointeur vers une interface [**ID3DXLine**](id3dxline.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 

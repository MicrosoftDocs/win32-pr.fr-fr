---
description: Récupère les paramètres de la surface de rendu.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'ID3DXRenderToSurface :: GetDesc, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211936"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a>ID3DXRenderToSurface :: GetDesc, méthode

Récupère les paramètres de la surface de rendu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pParameters* \[ à\]
</dt> <dd>

Type : **[ **D3DXRTS \_ desc**](d3dxrts-desc.md)\***

Pointeur vers une structure [**D3DXRTS \_ desc**](d3dxrts-desc.md) décrivant les paramètres de la surface de rendu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 





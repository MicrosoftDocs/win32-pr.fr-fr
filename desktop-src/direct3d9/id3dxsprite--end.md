---
description: 'Appelle ID3DXSprite :: Flush et restaure l’état de l’appareil pour qu’il se trouvait avant l’appel de ID3DXSprite :: Begin.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'ID3DXSprite :: end, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394184"
---
# <a name="id3dxspriteend-method"></a>ID3DXSprite :: end, méthode

Appelle [**ID3DXSprite :: Flush**](id3dxsprite--flush.md) et restaure l’état de l’appareil pour qu’il se trouvait avant l’appel de [**ID3DXSprite :: Begin**](id3dxsprite--begin.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Notes

**ID3DXSprite :: end** ne peut pas être utilisé comme substitut pour [**IDirect3DDevice9 :: EndScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface :: EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite :: Begin**](id3dxsprite--begin.md)
</dt> </dl>

 

 





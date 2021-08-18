---
description: Ajoute un Frame enfant à un frame.
ms.assetid: a04c9bbe-8e54-467a-8e02-27c6469f4dac
title: D3DXFrameAppendChild, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameAppendChild
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b6bc06eecb036f285e03b984e0fcd645d5c2416377684455dce491a3159d070
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988469"
---
# <a name="d3dxframeappendchild-function"></a>D3DXFrameAppendChild fonction)

Ajoute un Frame enfant à un frame.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXFrameAppendChild(
  _In_       LPD3DXFRAME pFrameParent,
  _In_ const D3DXFRAME   *pFrameChild
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFrameParent* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFRAME**](d3dxframe.md)**

Pointeur vers le nœud parent.

</dd> <dt>

*pFrameChild* \[ dans\]
</dt> <dd>

Type : **const [**D3DXFRAME**](d3dxframe.md) \***

Pointeur vers le nœud enfant.

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

 

 





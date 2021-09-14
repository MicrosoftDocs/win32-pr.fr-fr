---
description: 'Restaure l’état de l’appareil sur la manière dont il se trouvait lors de l’appel de ID3DXLine :: Begin.'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'ID3DXLine :: end, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998565"
---
# <a name="id3dxlineend-method"></a>ID3DXLine :: end, méthode

Restaure l’état de l’appareil sur la manière dont il se trouvait lors de l’appel de [**ID3DXLine :: Begin**](id3dxline--begin.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

**ID3DXLine :: end** ne peut pas être utilisé comme substitut pour [**IDirect3DDevice9 :: EndScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface :: EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine :: Begin**](id3dxline--begin.md)
</dt> </dl>

 

 





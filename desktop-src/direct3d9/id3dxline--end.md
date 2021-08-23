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
ms.openlocfilehash: 371463bfc24cbdba63ac51c9b729c267b9d020dd260d6d1b6c6a378bb38c3524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987229"
---
# <a name="id3dxlineend-method"></a>ID3DXLine :: end, méthode

Restaure l’état de l’appareil sur la manière dont il se trouvait lors de l’appel de [**ID3DXLine :: Begin**](id3dxline--begin.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Remarques

**ID3DXLine :: end** ne peut pas être utilisé comme substitut pour [**IDirect3DDevice9 :: EndScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface :: EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Configuration requise



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

 

 





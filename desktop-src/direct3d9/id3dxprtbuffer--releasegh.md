---
description: Dissocie un objet ID3DXTextureGutterHelper joint avec l’objet ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'ID3DXPRTBuffer :: ReleaseGH, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5691fc2601624733bb8d41b63140b694bd78027e0f6d548b02984bbc12406a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120533"
---
# <a name="id3dxprtbufferreleasegh-method"></a>ID3DXPRTBuffer :: ReleaseGH, méthode

Dissocie un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) joint avec l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode libère le pointeur vers l’interface [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .

Vous devez vous assurer que le nombre d’appels [**ID3DXPRTBuffer :: AttachGH**](id3dxprtbuffer--attachgh.md) correspond au nombre d’appels **ID3DXPRTBuffer :: ReleaseGH** . Après l’appel de **ID3DXPRTBuffer :: ReleaseGH**, le pointeur pGH retourné par **ID3DXPRTBuffer :: AttachGH** ne doit plus être utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 





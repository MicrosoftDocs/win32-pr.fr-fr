---
description: Associe un objet ID3DXTextureGutterHelper à l’objet ID3DXPRTBuffer.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'ID3DXPRTBuffer :: AttachGH, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: afb625c0f8db9d04737420ab386095bbe70b3e0f23e375f75c212da71e59b0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801947"
---
# <a name="id3dxprtbufferattachgh-method"></a>ID3DXPRTBuffer :: AttachGH, méthode

Associe un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) à l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGH* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Pointeur vers l’interface [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) d’un objet qui contient les données de la marge de texture.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK.

## <a name="remarks"></a>Remarques

Le décompte de références de l’objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) est automatiquement incrémenté d’une unité. Tous les pointeurs **ID3DXTextureGutterHelper** existants seront libérés.

Vous devez vous assurer que le nombre d’appels **ID3DXPRTBuffer :: AttachGH** correspond au nombre d’appels [**ID3DXPRTBuffer :: ReleaseGH**](id3dxprtbuffer--releasegh.md) . Après l’appel de **ID3DXPRTBuffer :: ReleaseGH**, le pointeur pGH retourné par **ID3DXPRTBuffer :: AttachGH** ne doit plus être utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 





---
description: Applique des gouttières à un objet de mémoire tampon ID3DXPRTBuffer.
ms.assetid: db09aa50-3175-4588-8433-dad6bd37cf0c
title: 'ID3DXTextureGutterHelper :: ApplyGuttersPRT, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersPRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a99d0cb5d54207d292398468e16b6c35deb4562
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762121"
---
# <a name="id3dxtexturegutterhelperapplyguttersprt-method"></a>ID3DXTextureGutterHelper :: ApplyGuttersPRT, méthode

Applique des gouttières à un objet de mémoire tampon [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ApplyGuttersPRT(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbuffer* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet de mémoire tampon [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Notes

Les [**texels de classe 2**](id3dxtexturegutterhelper.md) sont générés par le rééchantillonnage des texels de classe 1 et 4.

La largeur et la hauteur de la texture doivent être les mêmes que celles retournées par [**ID3DXTextureGutterHelper :: GetWidth**](id3dxtexturegutterhelper--getwidth.md) et [**ID3DXTextureGutterHelper :: GetHeight**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 





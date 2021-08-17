---
description: Modifie le nombre d’échantillons contenus dans la mémoire tampon.
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: 'ID3DXPRTBuffer :: Resize, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c6da4c5de4b38f5fe86b36622b7032e10ffe1be794ee8990ba19362cfd77d98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730072"
---
# <a name="id3dxprtbufferresize-method"></a>ID3DXPRTBuffer :: Resize, méthode

Modifie le nombre d’échantillons contenus dans la mémoire tampon.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Actualité* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’échantillons à contenir dans la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur suivante est retournée, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 

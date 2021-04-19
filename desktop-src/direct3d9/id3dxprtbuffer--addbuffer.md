---
description: Ajoute une autre mémoire tampon au ID3DXPRTBuffer et stocke les résultats dans ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'ID3DXPRTBuffer :: AddBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 90b86ad3d5d9fe5aa65db722757bdb34574a1006
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527962"
---
# <a name="id3dxprtbufferaddbuffer-method"></a>ID3DXPRTBuffer :: AddBuffer, méthode

Ajoute une autre mémoire tampon au [**ID3DXPRTBuffer**](id3dxprtbuffer.md) et stocke les résultats dans **ID3DXPRTBuffer**.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbuffer* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers une mémoire tampon qui contient les membres à ajouter aux membres respectifs de la mémoire tampon [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée.

## <a name="remarks"></a>Notes

pBuffer et [**ID3DXPRTBuffer**](id3dxprtbuffer.md) doivent avoir le même nombre d’échantillons, de coefficients et de canaux de couleur ; Sinon, la méthode échoue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 





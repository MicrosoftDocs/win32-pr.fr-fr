---
description: Rééchantillonne une mémoire tampon d’entrée ID3DXPRTBuffer et l’enregistre dans une mémoire tampon de sortie. Cette méthode peut être utilisée pour convertir une mémoire tampon de vertex en une mémoire tampon de texture et vice versa. Il peut également être utilisé pour convertir des mémoires tampons à canal unique en mémoires tampons de 3 canaux et vice versa.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'ID3DXPRTEngine :: ResampleBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa945be7b01c928a5dc8f5e44a6a31e8cb6d879be102145d25e03e7bef73f3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729613"
---
# <a name="id3dxprtengineresamplebuffer-method"></a>ID3DXPRTEngine :: ResampleBuffer, méthode

Rééchantillonne une mémoire tampon d’entrée [**ID3DXPRTBuffer**](id3dxprtbuffer.md) et l’enregistre dans une mémoire tampon de sortie. Cette méthode peut être utilisée pour convertir une mémoire tampon de vertex en une mémoire tampon de texture et vice versa. Il peut également être utilisé pour convertir des mémoires tampons à canal unique en mémoires tampons de 3 canaux et vice versa.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBufferIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers la mémoire tampon [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée.

</dd> <dt>

*pBufferOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers la mémoire tampon de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 





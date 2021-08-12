---
description: Crée un objet de nuanceur de texture à partir du nuanceur compilé.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: D3DXCreateTextureShader, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e989570c98b6b306782d8fb01e53b04d7157b1bb46db726a27fe2ade88a806c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298970"
---
# <a name="d3dxcreatetextureshader-function"></a>D3DXCreateTextureShader fonction)

Crée un objet de nuanceur de texture à partir du nuanceur compilé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFunction* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers le flux de fonction DWORD.

</dd> <dt>

*ppTextureShader* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***

Retourne un objet [**ID3DXTextureShader**](id3dxtextureshader.md) qui peut être utilisé pour remplir de façon procédurale le contenu d’une texture à l’aide des fonctions [**D3DXFillTextureTX**](d3dxfilltexturetx.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 

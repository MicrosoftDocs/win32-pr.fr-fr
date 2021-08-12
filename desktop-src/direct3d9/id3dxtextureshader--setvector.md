---
description: 'ID3DXTextureShader :: SetVector, méthode-définit un vecteur 4D.'
ms.assetid: befed2a8-7695-4f06-a6ee-aff466d1940a
title: 'ID3DXTextureShader :: SetVector, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53fef8dfaa3a8b05fa7a6565e980c677ece679dac2824a80423b0d7eeccb9d66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292418"
---
# <a name="id3dxtextureshadersetvector-method"></a>ID3DXTextureShader :: SetVector, méthode

Définit un vecteur 4D.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hConstant* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique de la constante Vector. Consultez [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pVector* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Pointeur vers un vecteur 4D. Consultez [**D3DXVECTOR4**](d3dxvector4.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 





---
description: Définit un vecteur normal pour chaque Texel dans un objet texture. Cette méthode est utilisée pour stocker des vecteurs normaux de vertex à partir d’une maille (ou des normales de vertex interpolées si le transfert de luminance précalculé basé sur les pixels (PRT) est calculé).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'ID3DXPRTEngine :: SetPerTexelNormal, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75877e8af86a22f80703742f148d5171e3a99e5c0c580bff588c27deba269b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293373"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a>ID3DXPRTEngine :: SetPerTexelNormal, méthode

Définit un vecteur normal pour chaque Texel dans un objet texture. Cette méthode est utilisée pour stocker des vecteurs normaux de vertex à partir d’une maille (ou des normales de vertex interpolées si le transfert de luminance précalculé basé sur les pixels (PRT) est calculé).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNormalTexture* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Pointeur vers un objet de texture [**IDirect3DTexture9**](/windows/desktop/api) qui sert de carte d’espace d’objet normale dans laquelle stocker les vecteurs normaux. La texture doit avoir les mêmes dimensions que [**ID3DXPRTBuffer**](id3dxprtbuffer.md) et doit être en mesure de stocker des formats de texture signés.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

 

 

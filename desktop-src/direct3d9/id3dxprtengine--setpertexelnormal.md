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
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918320"
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

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 

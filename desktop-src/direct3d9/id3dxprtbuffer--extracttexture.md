---
description: Extrait des données de coefficient à partir d’un canal de couleur de la mémoire tampon pour une plage de coefficients spécifiée, et ajoute les données à un objet IDirect3DTexture9.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'ID3DXPRTBuffer :: ExtractTexture, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ea6cfdc8fb6ec83f847ccf37d06972974ea4de8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953900"
---
# <a name="id3dxprtbufferextracttexture-method"></a>ID3DXPRTBuffer :: ExtractTexture, méthode

Extrait des données de coefficient à partir d’un canal de couleur de la mémoire tampon pour une plage de coefficients spécifiée, et ajoute les données à un objet [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chaîne* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Canal de couleur de la mémoire tampon à partir duquel extraire les données de texture.

</dd> <dt>

*StartCoefficient* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Valeur de départ du coefficient de mémoire tampon à partir duquel extraire les données de texture.

</dd> <dt>

*NumCoefficients* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de scalaires, en commençant par StartCoefficient, à partir duquel extraire les données de texture.

</dd> <dt>

*pTexture* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Pointeur vers un objet de texture [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui stocke les coefficients.

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

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 

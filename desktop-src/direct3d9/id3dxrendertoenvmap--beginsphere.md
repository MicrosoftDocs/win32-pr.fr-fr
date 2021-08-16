---
description: Lancer le rendu d’une carte d’environnement sphérique.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'ID3DXRenderToEnvMap :: BeginSphere, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f8bc555e3ea4f4fbb895c42f5c7a407cea88aedeacb9604ad1e78c7003bdf34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801289"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a>ID3DXRenderToEnvMap :: BeginSphere, méthode

Lancer le rendu d’une carte d’environnement sphérique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ptex* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui représente la texture vers laquelle effectuer le rendu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL. E \_ échec

## <a name="remarks"></a>Remarques

Consultez [**ID3DXRenderToEnvMap :: face**](id3dxrendertoenvmap--face.md) pour dessiner le visage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap :: fin**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 

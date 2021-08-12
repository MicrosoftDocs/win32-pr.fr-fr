---
description: Lancer le rendu d’une carte d’environnement cubique.
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: 'ID3DXRenderToEnvMap :: BeginCube, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 081e96425a7928cb1cd4a5a3ee48479d562c5c30a2f9017665acd32ffb539244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293273"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a>ID3DXRenderToEnvMap :: BeginCube, méthode

Lancer le rendu d’une carte d’environnement cubique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCubeTex* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Pointeur vers une interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) qui représente la texture de cube vers laquelle effectuer le rendu.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Consultez [**ID3DXRenderToEnvMap :: face**](id3dxrendertoenvmap--face.md) pour dessiner chacun des 6 visages.

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

 

 

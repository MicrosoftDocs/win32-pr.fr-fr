---
description: Commence une scène.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'ID3DXRenderToSurface :: BeginScene, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce6e120361972ac1ff4dbed5d37808dffa0f010af64feda365f65aad8dd393f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293105"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a>ID3DXRenderToSurface :: BeginScene, méthode

Commence une scène.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSurface* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Pointeur vers une interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , qui représente la surface de rendu.

</dd> <dt>

*pViewport* \[ dans\]
</dt> <dd>

Type : **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Pointeur vers une structure [**D3DVIEWPORT9**](d3dviewport9.md) , décrivant la fenêtre d’affichage de la scène.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL. D3DERR \_ OUTOFVIDEOMEMORY D3DXERR \_ sera déplacé E \_ OUTOFMEMORY

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> <dt>

[**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 

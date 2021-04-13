---
description: Récupère le périphérique Direct3D associé à la surface de rendu.
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: 'ID3DXRenderToSurface :: GetDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac01744887412349c71daa34194fc3a0b03b19a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323310"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a>ID3DXRenderToSurface :: GetDevice, méthode

Récupère le périphérique Direct3D associé à la surface de rendu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDevice* \[ out, retval\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Adresse d’un pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’objet appareil Direct3D associé à la surface de rendu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL. L’appel de cette méthode augmente le nombre de références internes sur l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Veillez à appeler [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) lorsque vous avez fini d’utiliser cette interface **IDirect3DDevice9** , sinon vous obtiendrez une fuite de mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 

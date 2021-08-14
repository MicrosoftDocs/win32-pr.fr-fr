---
description: Initiez le dessin de chaque face d’une carte d’environnement.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'ID3DXRenderToEnvMap :: face, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1190e033f9aa83b13f327fcb8a8b530be17132bfd330c9be6b9cc6d87d5e35a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801218"
---
# <a name="id3dxrendertoenvmapface-method"></a>ID3DXRenderToEnvMap :: face, méthode

Initiez le dessin de chaque face d’une carte d’environnement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Visage* \[ dans\]
</dt> <dd>

Type : **[ **D3DCUBEMAP \_ faces**](./d3dcubemap-faces.md)**

Première face du mappage de cube environnemental. Consultez [**D3DCUBEMAP \_ faces**](./d3dcubemap-faces.md).

</dd> <dt>

*MipFilter* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison valide d’un ou plusieurs indicateurs [de \_ filtre D3DX](d3dx-filter.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Cette méthode doit être appelée une fois pour chaque type de carte d’environnement. La seule exception est un mappage d’environnement cubique qui requiert que cette méthode soit appelée six fois, une fois pour chaque visage dans des \_ visages D3DCUBEMAP. Pour plus d’informations, consultez [mappage d’environnement (Direct3D 9)](environment-mapping.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 

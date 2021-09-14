---
description: Obtient l’appareil qui a créé le maillage.
ms.assetid: b03dadda-ca54-4a55-a0a5-cf5ccdb55a72
title: 'ID3DXPatchMesh :: GetDevice, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a026398b719bf3ba9a9c02082105cbc7dd299013
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998537"
---
# <a name="id3dxpatchmeshgetdevice-method"></a>ID3DXPatchMesh :: GetDevice, méthode

Obtient l’appareil qui a créé le maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDevice* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Pointeur vers l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

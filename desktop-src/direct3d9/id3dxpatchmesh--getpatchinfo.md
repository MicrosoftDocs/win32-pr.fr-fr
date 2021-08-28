---
description: Obtient les attributs du correctif.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'ID3DXPatchMesh :: GetPatchInfo, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10b6d327b665b30418478d06d21433614587824eeb481202a9bef202b8727001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847439"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a>ID3DXPatchMesh :: GetPatchInfo, méthode

Obtient les attributs du correctif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PatchInfo* \[ out, retval\]
</dt> <dd>

Type : **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**

Pointeur vers les structures contenant les attributs de correctif. Pour plus d’informations sur les attributs de correctif, consultez [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 





---
description: 'ID3DXPatchMesh :: GetDeclaration, méthode-obtient la déclaration de vertex.'
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'ID3DXPatchMesh :: GetDeclaration, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 120a9f4179819b550502c2c3764d334159b647fd4c8621d3a088516b9a669d56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747849"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a>ID3DXPatchMesh :: GetDeclaration, méthode

Obtient la déclaration de vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDeclaration* \[ à\]
</dt> <dd>

Type : **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) décrivant le format de vertex des vertex de maillage. La dimension de ce tableau déclarateur est [**la \_ \_ \_ taille max Commission**](./max-fvf-decl-size.md)de la déclaration de la valeur. Le tableau d’éléments de vertex se termine par la macro [**\_ end D3DDECL**](d3ddecl-end.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Le tableau d’éléments comprend la [**macro \_ end D3DDECL**](d3ddecl-end.md) , qui termine la déclaration.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

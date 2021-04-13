---
description: Obtient la déclaration de vertex.
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'ID3DXSkinInfo :: GetDeclaration, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de80694bbbb6eea29f391b3b39cff9caacd4791c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322602"
---
# <a name="id3dxskininfogetdeclaration-method"></a>ID3DXSkinInfo :: GetDeclaration, méthode

Obtient la déclaration de vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Déclaration* \[ de in, out\]
</dt> <dd>

Type : **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) décrivant le format de vertex des vertex de maillage. La limite supérieure de ce tableau déclarateur est [**la \_ \_ \_ taille maximale**](./max-fvf-decl-size.md)de la déclaration de la Commission de la Commission. Le tableau d’éléments de vertex se termine par la macro [**\_ end D3DDECL**](d3ddecl-end.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Le tableau d’éléments comprend la [**macro \_ end D3DDECL**](d3ddecl-end.md) , qui termine la déclaration.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetDeclaration**](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 

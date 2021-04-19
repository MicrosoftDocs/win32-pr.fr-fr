---
description: Obtient les paramètres de déplacement de la géométrie de maillage.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'ID3DXPatchMesh :: GetDisplaceParam, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ce6891af8a15aa8f4af5c85312f124db6c05321
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538554"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a>ID3DXPatchMesh :: GetDisplaceParam, méthode

Obtient les paramètres de déplacement de la géométrie de maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Texture* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***

Texture contenant les données de déplacement.

</dd> <dt>

*MinFilter* \[ dans\]
</dt> <dd>

Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Niveau de minimisation. Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MagFilter* \[ dans\]
</dt> <dd>

Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Niveau d’agrandissement. Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MipFilter* \[ dans\]
</dt> <dd>

Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Niveau de filtre MIP. Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Retour à la ligne* \[ dans\]
</dt> <dd>

Type : **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***

Mode de retour à la ligne de l’adresse de texture. Pour plus d’informations, consultez [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

*dwLODBias* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Niveau de la valeur de décalage des détails.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Les mappages de déplacement ne peuvent être que des textures 2D. Mappage MIP est ignoré pour le pavage non adaptatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

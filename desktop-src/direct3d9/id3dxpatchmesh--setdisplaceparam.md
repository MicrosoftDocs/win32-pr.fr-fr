---
description: Définit les paramètres de déplacement de la géométrie du maillage.
ms.assetid: 4c78e5b3-fb63-4341-a811-5531cf9564e7
title: 'ID3DXPatchMesh :: SetDisplaceParam, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.SetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1d59791859e0330415512db1551709729455d0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998515"
---
# <a name="id3dxpatchmeshsetdisplaceparam-method"></a>ID3DXPatchMesh :: SetDisplaceParam, méthode

Définit les paramètres de déplacement de la géométrie du maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 Texture,
  [in] D3DTEXTUREFILTERTYPE   MinFilter,
  [in] D3DTEXTUREFILTERTYPE   MagFilter,
  [in] D3DTEXTUREFILTERTYPE   MipFilter,
  [in] D3DTEXTUREADDRESS      Wrap,
  [in] DWORD                  dwLODBias
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Texture* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Texture contenant les données de déplacement.

</dd> <dt>

*MinFilter* \[ dans\]
</dt> <dd>

Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Niveau de minimisation. Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MagFilter* \[ dans\]
</dt> <dd>

Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Niveau d’agrandissement. Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MipFilter* \[ dans\]
</dt> <dd>

Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Niveau de filtre MIP. Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Retour à la ligne* \[ dans\]
</dt> <dd>

Type : **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**

Mode de retour à la ligne de l’adresse de texture. Pour plus d’informations, consultez [ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)

</dd> <dt>

*dwLODBias* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Niveau de la valeur de décalage des détails.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Les mappages de déplacement ne peuvent être que des textures 2D. Mappage MIP est ignoré pour le pavage non adaptatif.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

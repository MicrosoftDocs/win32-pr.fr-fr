---
description: Rééchantillonne une texture dans le paramétrage de ce gutterhelper.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'ID3DXTextureGutterHelper :: ResampleTex, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211880"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a>ID3DXTextureGutterHelper :: ResampleTex, méthode

Rééchantillonne une texture dans le paramétrage de ce gutterhelper.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTextureIn* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Texture qui correspond au paramétrage d’origine dans pMeshIn. Cette texture sera utilisée pour créer pTextureOut.

</dd> <dt>

*pMeshIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Maille contenant les paramétrages originaux et nouveaux. Il est nécessaire pour stocker le nouveau paramétrage dans l' \_ index 0 D3DDECLUSAGE texcoord.

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Utilisation des données de vertex (utilisée en association avec UsageIndex) qui identifie le composant de la déclaration de vertex qui contient le paramétrage d’origine dans pMeshIn. Consultez [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndex* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de base zéro (utilisé en association avec l’utilisation), qui identifie le composant de la déclaration de vertex qui contient le paramétrage d’origine dans pMeshIn. La combinaison de D3DDECLUSAGE \_ texcoord et de l’index 0 est requise pour le nouveau paramétrage ; toute autre combinaison d’utilisation/d’index peut être utilisée.

</dd> <dt>

*pTextureOut* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Texture rééchantillonnée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Un paramétrage dans le cas de cette fonction est un ensemble de coordonnées de texture qui mappe les triangles d’une maille aux triangles d’une texture. Le nouveau paramétrage est l’ensemble des coordonnées de texture contenues dans l’interface d’assistance de reliure, et le paramétrage d’origine est l’ensemble des coordonnées de texture contenues dans le maillage d’entrée.

Il est supposé que les coordonnées de texture sont comprises entre 0 et 1 (inclus), et le nouveau paramétrage doit être déclaré dans la déclaration de vertex comme index de coordonnée de texture 0. La texture d’origine et la texture rééchantillonnée doivent avoir la même largeur et la même hauteur.

Par exemple, pour préparer le rééchantillonnage d’une texture :

-   Créez l’interface de texture d’origine (pOriginalTex ci-dessous) à l’aide d’une fonction comme [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).
-   Créez la nouvelle interface de texture pour la texture rééchantillonnée (pResampledTex ci-dessous). La taille de cette texture doit correspondre à la taille (largeur et hauteur) de la texture d’assistance de la reliure.
-   Appelez [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) pour obtenir le nouveau paramétrage comme indiqué ici :


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



Un scénario courant consiste à utiliser UVAtlas pour créer un Atlas de textures, puis à utiliser ResampleTex pour rééchantillonner la texture dans le nouveau paramétrage. Pour plus d’informations sur les Atlas, consultez [utilisation de UVAtlas (Direct3D 9)](using-uvatlas.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> <dt>

[**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)
</dt> </dl>

 

 

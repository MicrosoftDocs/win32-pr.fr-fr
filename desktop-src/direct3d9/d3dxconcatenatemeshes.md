---
description: Concatène un groupe de maillages dans un maillage commun. Cette méthode peut éventuellement appliquer une transformation de matrice à chaque maillage d’entrée et ses coordonnées de texture.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: D3DXConcatenateMeshes, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21801c2f4b8ef8dd2a34c9788b402128da4ce4fed33c3c38a08e61c35a847e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857389"
---
# <a name="d3dxconcatenatemeshes-function"></a>D3DXConcatenateMeshes fonction)

Concatène un groupe de maillages dans un maillage commun. Cette méthode peut éventuellement appliquer une transformation de matrice à chaque maillage d’entrée et ses coordonnées de texture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppMeshes* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Tableau de pointeurs de maillage d’entrée (consultez [**ID3DXMesh**](id3dxmesh.md)). Le nombre d’éléments dans le tableau est NumMeshes.

</dd> <dt>

*NumMeshes* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de maillages d’entrée à concaténer.

</dd> <dt>

*Options* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Options de création de maillage ; Il s’agit d’une combinaison d’un ou plusieurs indicateurs [**D3DXMESH**](./d3dxmesh.md) . Les options de création de maillage sont équivalentes au paramètre d’options requis par [**D3DXCreateMesh**](d3dxcreatemesh.md).

</dd> <dt>

*pGeomXForms* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Tableau facultatif de transformations géométriques. Le nombre d’éléments dans le tableau est NumMeshes ; chaque élément est une matrice de transformation (consultez [**D3DXMATRIX**](d3dxmatrix.md)). Peut avoir la **valeur null**.

</dd> <dt>

*pTextureXForms* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Tableau facultatif de transformations de texture. Le nombre d’éléments dans le tableau est NumMeshes ; chaque élément est une matrice de transformation (consultez [**D3DXMATRIX**](d3dxmatrix.md)). Ce paramètre peut avoir la **valeur null**.

</dd> <dt>

*pDecl* \[ dans\]
</dt> <dd>

Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Pointeur facultatif vers une déclaration de vertex (consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)). Ce paramètre peut avoir la **valeur null**.

</dd> <dt>

*pD3DDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers un appareil [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) utilisé pour créer le nouveau maillage.

</dd> <dt>

*ppMeshOut* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse d’un pointeur vers la maille créée (voir [**ID3DXMesh**](id3dxmesh.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Si aucune [déclaration de vertex](vertex-declaration.md) n’est fournie dans le cadre du paramètre de création de maillage d’options, la méthode génère une Union de toutes les déclarations de vertex des sous-mailles, en promouvant les canaux et les types si nécessaire. La méthode crée une table d’attributs à partir des tables d’attributs des maillages d’entrée. Pour garantir la création d’une table d’attributs, appelez [**optimize**](id3dxmesh--optimize.md) avec les indicateurs définis sur D3DXMESHOPT \_ compact et D3DXMESHOPT \_ ATTRSORT (voir [**D3DXMESHOPT**](./d3dxmeshopt.md)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

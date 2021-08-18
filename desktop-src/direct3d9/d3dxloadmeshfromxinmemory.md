---
description: Charge une maille à partir de la mémoire.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: D3DXLoadMeshFromXInMemory, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19427da28b90fe4410a65f0321b5dcd486b4c917d209f1f20762d05899b4eb0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044947"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a>D3DXLoadMeshFromXInMemory fonction)

Charge une maille à partir de la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Mémoire* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers la mémoire tampon qui contient les données de maillage.

</dd> <dt>

*SizeOfMemory* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Taille du fichier en mémoire, en octets.

</dd> <dt>

*Options* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou de plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant les options de création du maillage.

</dd> <dt>

*pD3DDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil associé à la maille.

</dd> <dt>

*ppAdjacency* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) . Quand la méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORDs par visage qui spécifient les trois voisins pour chaque visage de la maille.

</dd> <dt>

*ppMaterials* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) . Lorsque cette méthode est retournée, ce paramètre est rempli avec un tableau de structures [**D3DXMATERIAL**](d3dxmaterial.md) , contenant les informations enregistrées dans le fichier DirectX.

</dd> <dt>

*ppEffectInstances* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Pointeur vers une mémoire tampon qui contient un tableau d’instances d’effet, une par groupe d’attributs dans le maillage retourné. Une instance Effect est une instance particulière d’informations d’état utilisée pour initialiser un effet. Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pNumMaterials* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers le nombre de structures [**D3DXMATERIAL**](d3dxmaterial.md) dans le tableau *ppMaterials* , lorsque la méthode retourne.

</dd> <dt>

*ppMesh* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage chargé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Tous les maillages du fichier seront réduits en un seul maillage de sortie. Si le fichier contient une hiérarchie de frames, toutes les transformations sont appliquées à la maille.

Pour les fichiers de maillage qui ne contiennent pas d’informations sur l’instance d’effet, les instances d’effet par défaut sont générées à partir des informations matérielles du fichier. x. Une instance d’effet par défaut aura des valeurs par défaut qui correspondent aux membres de la structure [**D3DMATERIAL9**](d3dmaterial9.md) .

Le nom de texture par défaut est également renseigné, mais est géré différemment. Le nom est Texture0@Name , ce qui correspond à une variable Effect par le nom de « Texture0 » avec une annotation appelée « Name ». Contient le nom de fichier de chaîne pour la texture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 

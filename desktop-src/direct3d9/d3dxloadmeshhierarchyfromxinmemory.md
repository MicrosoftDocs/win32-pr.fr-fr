---
description: D3DXLoadMeshHierarchyFromXInMemory fonction-charge la première hiérarchie d’images à partir d’un fichier. x.
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: D3DXLoadMeshHierarchyFromXInMemory, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 551810c839e619985d9a380197553f5fe4fc9be8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098207"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a>D3DXLoadMeshHierarchyFromXInMemory fonction)

Charge la première hiérarchie d’images à partir d’un fichier. x.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMemory* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers une mémoire tampon qui contient la hiérarchie de maillage.

</dd> <dt>

*SizeOfMemory* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Taille de la mémoire tampon pMemory, en octets.

</dd> <dt>

*MeshOptions* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) qui spécifient les options de création du maillage.

</dd> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil associé à la maille.

</dd> <dt>

*pAlloc* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Pointeur vers une interface [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .

</dd> <dt>

*pUserDataLoader* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Interface fournie par l’application qui permet le chargement des données utilisateur. Consultez [**ID3DXLoadUserData**](id3dxloaduserdata.md).

</dd> <dt>

*ppFrameHeirarchy* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXFRAME**](d3dxframe.md)\***

Retourne un pointeur vers la hiérarchie de frames chargée. Consultez [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ppAnimController* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Retourne un pointeur vers le contrôleur d’animation correspondant à l’animation dans le fichier. x. Il est créé avec des suivis et des événements par défaut. Consultez [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes 

Tous les maillages du fichier seront réduits en un seul maillage de sortie. Si le fichier contient une hiérarchie de frames, toutes les transformations sont appliquées à la maille.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’animation](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 

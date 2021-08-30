---
description: Retourne des informations matérielles enregistrées dans des fichiers Direct3D (. x).
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: D3DXMATERIAL, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: c90b03f5d6526fc3545ff1ffe1d48dfea20f96ea4ae34602f885ce7f062003b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027409"
---
# <a name="d3dxmaterial-structure"></a>D3DXMATERIAL, structure

Retourne des informations matérielles enregistrées dans des fichiers Direct3D (. x).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a>Membres

<dl> <dt>

**MatD3D**
</dt> <dd>

Type : **[ **D3DMATERIAL9**](d3dmaterial9.md)**

</dd> <dd>

Structure [**D3DMATERIAL9**](d3dmaterial9.md) qui décrit les propriétés du matériau.

</dd> <dt>

**pTextureFilename**
</dt> <dd>

Type : **LPSTR**

</dd> <dd>

Pointeur vers une chaîne qui spécifie le nom de fichier de la texture.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les fonctions [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) et [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) retournent un tableau de structures **D3DXMATERIAL** qui spécifient la couleur matérielle et le nom de la texture pour chaque matériau de la maille. L’application est ensuite requise pour charger la texture.

Le type LPD3DXMATERIAL est défini en tant que pointeur vers la structure **D3DXMATERIAL** .


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md)
</dt> <dt>

[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 





---
description: Décrit un volume.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: Structure D3DVOLUME_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1ddf80819818bf23985c5ca81e2d26e80b51662388ec5808579c74146c152ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300177"
---
# <a name="d3dvolume_desc-structure"></a>D3DVOLUME \_ desc, structure

Décrit un volume.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Format**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de surface du volume.

</dd> <dt>

**Type**
</dt> <dd>

Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membre du type énuméré [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identifiant cette ressource en tant que volume.

</dd> <dt>

**Utilisation**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Pas utilisé pour l’instant. Toujours retourné comme 0.

</dd> <dt>

**Pool**
</dt> <dd>

Type : **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , spécifiant la classe de mémoire allouée pour ce volume.

</dd> <dt>

**Width**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur du volume, en pixels.

</dd> <dt>

**Height**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur du volume, en pixels.

</dd> <dt>

**Profondeur**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Profondeur du volume, en pixels.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 

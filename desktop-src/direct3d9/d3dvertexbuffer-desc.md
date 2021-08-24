---
description: Décrit une mémoire tampon de vertex.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: Structure D3DVERTEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1f1809bbf9352b022d2acfb15b119db47b0feab6302020cdaf5b24746945aa05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750579"
---
# <a name="d3dvertexbuffer_desc-structure"></a>D3DVERTEXBUFFER \_ desc, structure

Décrit une mémoire tampon de vertex.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Format**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de surface des données de la mémoire tampon de vertex.

</dd> <dt>

**Type**
</dt> <dd>

Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membre du type énuméré [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identifiant cette ressource comme une mémoire tampon de vertex.

</dd> <dt>

**Utilisation**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinaison d’un ou plusieurs indicateurs [**D3DUSAGE**](d3dusage.md) .

</dd> <dt>

**Pool**
</dt> <dd>

Type : **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , spécifiant la classe de mémoire allouée pour cette mémoire tampon de vertex.

</dd> <dt>

**Taille**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille de la mémoire tampon de vertex, en octets.

</dd> <dt>

**CLOS**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinaison de [D3DFVF](d3dfvf.md) qui décrit le format de vertex des vertex dans cette mémoire tampon.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[Mémoires tampons de vertex (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 

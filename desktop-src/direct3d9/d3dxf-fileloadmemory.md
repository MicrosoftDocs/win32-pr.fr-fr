---
description: Identifie les données de mémoire.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: Structure D3DXF_FILELOADMEMORY (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012807"
---
# <a name="d3dxf_fileloadmemory-structure"></a>D3DXF \_ FILELOADMEMORY, structure

Identifie les données de mémoire.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a>Membres

<dl> <dt>

**lpMemory**
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Pointeur vers un bloc de mémoire à charger.

</dd> <dt>

**dSize**
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille du bloc de mémoire à charger, en octets.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure identifie les données à charger à partir de la mémoire lorsqu’une application utilise la méthode [**CreateEnumObject**](id3dxfile--createenumobject.md) et spécifie l' \_ \_ indicateur FROMMEMORY FILELOAD D3DXF.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de fichiers D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 

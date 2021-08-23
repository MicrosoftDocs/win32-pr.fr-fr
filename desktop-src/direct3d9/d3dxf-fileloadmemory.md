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
ms.openlocfilehash: b3709e6eeb99026b76d066edfccbae578b5c851d6e73936ffe06d10fbf69dcb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045057"
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

## <a name="remarks"></a>Remarques

Cette structure identifie les données à charger à partir de la mémoire lorsqu’une application utilise la méthode [**CreateEnumObject**](id3dxfile--createenumobject.md) et spécifie l' \_ \_ indicateur FROMMEMORY FILELOAD D3DXF.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de fichiers D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 

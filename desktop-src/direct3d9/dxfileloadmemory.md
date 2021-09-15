---
description: Identifie les données de mémoire. Action déconseillée.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: DXFILELOADMEMORY, structure (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403370"
---
# <a name="dxfileloadmemory-structure"></a>DXFILELOADMEMORY, structure

Identifie les données de mémoire. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a>Membres

<dl> <dt>

**lpMemory**
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Pointeur vers un bloc de mémoire à charger.

</dd> <dt>

**dSize**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille du bloc de mémoire à charger, en octets.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure identifie une ressource à charger lorsqu’une application utilise la méthode [**CreateEnumObject**](idirectxfile--createenumobject.md) et spécifie DXFILELOAD \_ FROMMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DXFile. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de fichiers X](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[Constantes DXFILE](dxfile.md)
</dt> </dl>

 

 

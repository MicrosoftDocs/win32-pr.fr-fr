---
description: Identifie les données d’animation d’image clé compressées.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: XFILECOMPRESSEDANIMATIONSET, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539161"
---
# <a name="xfilecompressedanimationset-structure"></a>XFILECOMPRESSEDANIMATIONSET, structure

Identifie les données d’animation d’image clé compressées.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a>Membres

<dl> <dt>

**CompressedBlockSize**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille totale, en octets, des données compressées dans le tampon de données d’animation d’image clé compressée.

</dd> <dt>

**TicksPerSec**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de battements d’image clé d’animation qui se produisent par seconde.

</dd> <dt>

**PlaybackType**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Type de la boucle de lecture du jeu d’animations. Consultez [**\_ type D3DXPLAYBACK**](./d3dxplayback-type.md).

</dd> <dt>

**BufferLength**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille minimale de la mémoire tampon, en octets, nécessaire pour contenir les données d’animation d’image clé compressées. La valeur est égale à ((CompressedBlockSize + 3)/4).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de fichiers D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)
</dt> </dl>

 

 

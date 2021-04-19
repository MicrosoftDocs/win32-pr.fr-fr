---
description: Spécifie le glyphe source et l’emplacement dans une surface monochrome dans laquelle copier les glyphes.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: D3DCOMPOSERECTDESTINATION, structure (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523174"
---
# <a name="d3dcomposerectdestination-structure"></a>D3DCOMPOSERECTDESTINATION, structure

Spécifie le glyphe source et l’emplacement dans une surface monochrome dans laquelle copier les glyphes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**SrcRectIndex**
</dt> <dd>

Type : **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Indexez un glyphe particulier à partir de la mémoire tampon de vertex contenant les structures [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) .

</dd> <dt>

**Reserved**
</dt> <dd>

Type : **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Réservé à des fins d’alignement.

</dd> <dt>

**X**
</dt> <dd>

Type : **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée gauche à laquelle commencer la copie.

</dd> <dt>

**O**
</dt> <dd>

Type : **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée supérieure à laquelle commencer la copie.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée dans les appels à [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) pour indiquer que les glyphes d’emplacement doivent être copiés vers et quel glyphe particulier doit être copié. Une mémoire tampon de vertex (voir [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) remplie avec ces structures est créée pour contenir les emplacements de glyphe. Les membres USHORT sont utilisés pour réduire autant que possible l’encombrement mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 

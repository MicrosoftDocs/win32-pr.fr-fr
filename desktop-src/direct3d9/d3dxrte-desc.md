---
description: Décrit une cible de rendu hors écran utilisée par une instance de ID3DXRenderToEnvMap.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: Structure D3DXRTE_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 91efe4dff2b392310ed2fd6bdc30db12c883c5d08e6b2cf110c2cb29d73c54ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027279"
---
# <a name="d3dxrte_desc-structure"></a>D3DXRTE \_ desc, structure

Décrit une cible de rendu hors écran utilisée par une instance de [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Taille**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur et hauteur en pixels.

</dd> <dt>

**Miplevels a**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre maximal de détails (LOD).

</dd> <dt>

**Format**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Format de la mémoire tampon des couleurs.

</dd> <dt>

**DepthStencil**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Indique si la mémoire tampon z est nécessaire.

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Format de la mémoire tampon de profondeur.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette méthode est utilisée pour retourner les paramètres de création utilisés lors de la création d’un objet [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

---
description: Caractéristiques du matériau de transfert de luminance (PRT) précalculées d’harmoniques sphériques (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: D3DXSHMATERIAL, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532437"
---
# <a name="d3dxshmaterial-structure"></a>D3DXSHMATERIAL, structure

Caractéristiques du matériau de transfert de luminance (PRT) précalculées d’harmoniques sphériques (SH).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a>Membres

<dl> <dt>

**Diffus**
</dt> <dd>

Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Albedo diffuse de l’aire. Cette valeur est ignorée si l’objet est un miroir.

</dd> <dt>

**bMirror**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Doit avoir la valeur **false**.

</dd> <dt>

**bSubSurf**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Affectez la valeur **true** pour activer la diffusion sous-surface ; tout objet qui effectue une diffusion sous-surface ne peut pas être un miroir.

</dd> <dt>

**RelativeIndexOfRefraction**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

L’index relatif de refraction correspond au rapport entre deux index absolus de réfraction. Un index de réfraction est le rapport entre le sinus de l’angle d’incidence et le sinus de l’angle de réfraction.

</dd> <dt>

**Absorption**
</dt> <dd>

Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Le coefficient d’absorption est un paramètre de l’équation de rendu de volume utilisée pour modéliser la propagation de la lumière dans un support participant.

</dd> <dt>

**ReducedScattering**
</dt> <dd>

Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Le coefficient de diffusion réduit est un paramètre de l’équation de rendu de volume utilisée pour modéliser la propagation de la lumière dans un support participant.

</dd> </dl>

## <a name="remarks"></a>Notes

Les scènes non spectrales utilisent le canal rouge à partir des matériaux au lieu de la valeur de luminance.

Pour plus d’informations sur PRT, consultez :

-   Jensen, Clément Wann, et al. SIGGRAPH, procédure : un modèle pratique pour le transport de lumière sous-surface, 2001.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

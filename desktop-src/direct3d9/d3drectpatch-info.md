---
description: Décrit un correctif rectangulaire de poids fort.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: Structure D3DRECTPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b73ebc548031fd931cce0d34edfadf81a73d71d60edf649718875c52cfc992f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850223"
---
# <a name="d3drectpatch_info-structure"></a>\_Structure d’informations D3DRECTPATCH

Décrit un correctif rectangulaire de poids fort.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**StartVertexOffsetWidth**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur du décalage du vertex de départ, en nombre de vertex.

</dd> <dt>

**StartVertexOffsetHeight**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur du décalage du vertex de départ, en nombre de vertex.

</dd> <dt>

**Width**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur de chaque vertex, en nombre de vertex.

</dd> <dt>

**Height**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur de chaque vertex, en nombre de vertex.

</dd> <dt>

**Progrès**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur du tableau de vertex imaginaire à deux dimensions, qui occupe le même espace que la mémoire tampon de vertex. Pour obtenir un exemple, consultez le diagramme ci-dessous.

</dd> <dt>

**basis**
</dt> <dd>

Type : **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Membre du type énuméré [**D3DBASISTYPE**](./d3dbasistype.md) , définissant le type de base pour le correctif rectangulaire de poids fort.



| Value                 | Commande prise en charge            | Largeur et hauteur                  |
|-----------------------|----------------------------|-----------------------------------|
| D3DBASIS \_ Bézier      | Linéaire, cubique et quintaux | Width = hauteur = (DWORD) ordre + 1 |
| D3DBASIS \_ BSPLINE     | Linéaire, cubique et quintaux | Width = hauteur > (DWORD) Order  |
| \_Interpolation D3DBASIS | Mètres                      | Width = hauteur > (DWORD) Order  |



 

</dd> <dt>

**Degré**
</dt> <dd>

Type : **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Membre du type énuméré [**D3DDEGREETYPE**](./d3ddegreetype.md) , définissant le degré pour le correctif rectangulaire.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le diagramme suivant identifie les paramètres qui spécifient un correctif de rectangle.

![diagramme d’un correctif de poids fort rectangulaire et des paramètres qui le spécifient](images/hop-rectpatch.png)

Chacun des vertex de la mémoire tampon de vertex est affiché sous la forme d’un point noir. Dans ce cas, la mémoire tampon de vertex contient 20 sommets, dont 16 dans le carreau de rectangle. Le Stride est le nombre de vertex dans la largeur de la mémoire tampon de vertex, dans ce cas cinq. Le décalage x du premier vertex est appelé StartIndexVertexWidth et est dans ce cas 1. Le décalage y du premier vertex patch est appelé StartIndexVertexHeight et est dans ce cas 0.

Pour afficher un flux de différents correctifs rectangulaires (non-mosaïques), vous devez interpréter votre géométrie comme un correctif rectangulaire long (1 x N). La structure d' **\_ informations D3DRECTPATCH** pour une telle bande (Bézier cubique) est configurée de la manière suivante.


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 

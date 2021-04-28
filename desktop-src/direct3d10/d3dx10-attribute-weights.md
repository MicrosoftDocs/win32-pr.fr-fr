---
description: 'Structure de D3DX10_ATTRIBUTE_WEIGHTS : spécifie les attributs de poids de maille.'
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: Structure D3DX10_ATTRIBUTE_WEIGHTS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ab163149493ad73f892a251a691ad82544d7f382
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094350"
---
# <a name="d3dx10_attribute_weights-structure"></a>\_Structure des \_ pondérations d’attribut d3dx10

Spécifie les attributs de poids de maille.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a>Membres

<dl> <dt>

**Position**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Endroit.

</dd> <dt>

**Limite**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Poids de fusion.

</dd> <dt>

**Normal**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal.

</dd> <dt>

**Diffus**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valeur d’éclairage diffus.

</dd> <dt>

**Spéculaire**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valeur d’éclairage spéculaire.

</dd> <dt>

**Texcoord**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Huit coordonnées de texture.

</dd> <dt>

**Tangente**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangence.

</dd> <dt>

**Binormal**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal.

</dd> </dl>

## <a name="remarks"></a>Notes 

Cette structure décrit comment une opération de simplification prend en compte les données de vertex lors du calcul des coûts relatifs entre les bords réduits. Par exemple, si le champ normal est 0,0, l’opération de simplification ignore le composant de vertex normal lors du calcul de l’erreur pour la réduction. Toutefois, si le champ normal est 1,0, l’opération de simplification utilise le composant de vertex normal. Si le champ normal est 2,0, doublez le nombre d’erreurs ; Si le champ normal est 4,0, Quadruplez le nombre d’erreurs, etc.

Le \_ type de \_ poids de l’attribut LPD3DX est défini en tant que pointeur vers la \_ structure des pondérations de l’attribut D3DX \_ .


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 

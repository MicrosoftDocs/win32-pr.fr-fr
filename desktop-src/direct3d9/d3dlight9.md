---
description: Définit un ensemble de propriétés d’éclairage.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: D3DLIGHT9, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211817"
---
# <a name="d3dlight9-structure"></a>D3DLIGHT9, structure

Définit un ensemble de propriétés d’éclairage.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Type : **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**

</dd> <dd>

Type de la source de lumière. Cette valeur est l’un des membres du type énuméré [**D3DLIGHTTYPE**](./d3dlighttype.md) .

</dd> <dt>

**Diffus**
</dt> <dd>

Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Couleur diffuse émise par la lumière. Ce membre est une structure [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Spéculaire**
</dt> <dd>

Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Couleur spéculaire émise par la lumière. Ce membre est une structure [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Ambiant**
</dt> <dd>

Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Couleur ambiante émise par la lumière. Ce membre est une structure [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Position**
</dt> <dd>

Type : **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Position de la lumière dans l’espace universel, spécifiée par une structure [**D3DVECTOR**](d3dvector.md) . Ce membre n’a aucune signification pour les lumières directionnelles et est ignoré dans ce cas.

</dd> <dt>

**Sens**
</dt> <dd>

Type : **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Direction de pointage de la lumière dans l’espace universel, spécifiée par une structure [**D3DVECTOR**](d3dvector.md) . Ce membre a une signification uniquement pour les directions et les lumières. Ce vecteur n’a pas besoin d’être normalisé, mais il doit avoir une longueur différente de zéro.

</dd> <dt>

**Plage**
</dt> <dd>

Type : **float**

</dd> <dd>

Distance au-delà de laquelle la lumière n’a aucun effet. La valeur maximale autorisée pour ce membre est la racine carrée de FLT \_ Max. Ce membre n’affecte pas les lumières directionnelles.

</dd> <dt>

**Atténuation**
</dt> <dd>

Type : **float**

</dd> <dd>

Diminution de l’éclairage entre le cône interne d’un projecteur (angle spécifié par thêta) et le bord extérieur du cône externe (angle spécifié par PHI).

L’effet de l’atténuation sur l’éclairage est subtil. En outre, une faible baisse des performances est provoquée par la mise en forme de la courbe décroissante. Pour ces raisons, la plupart des développeurs définissent cette valeur sur 1,0.

</dd> <dt>

**Attenuation0**
</dt> <dd>

Type : **float**

</dd> <dd>

Valeur spécifiant la façon dont l’intensité de la lumière change sur la distance. Les valeurs d’atténuation sont ignorées pour les lumières directionnelles. Ce membre représente une constante d’atténuation. Pour plus d’informations sur l’atténuation, consultez [Propriétés de la lumière (Direct3D 9)](light-properties.md). Les valeurs valides pour cette plage de membres sont comprises entre 0,0 et Infinity. Pour les lumières non directionnelles, les trois valeurs d’atténuation ne doivent pas être définies sur 0,0 en même temps.

</dd> <dt>

**Attenuation1**
</dt> <dd>

Type : **float**

</dd> <dd>

Valeur spécifiant la façon dont l’intensité de la lumière change sur la distance. Les valeurs d’atténuation sont ignorées pour les lumières directionnelles. Ce membre représente une constante d’atténuation. Pour plus d’informations sur l’atténuation, consultez [Propriétés de la lumière (Direct3D 9)](light-properties.md). Les valeurs valides pour cette plage de membres sont comprises entre 0,0 et Infinity. Pour les lumières non directionnelles, les trois valeurs d’atténuation ne doivent pas être définies sur 0,0 en même temps.

</dd> <dt>

**Attenuation2**
</dt> <dd>

Type : **float**

</dd> <dd>

Valeur spécifiant la façon dont l’intensité de la lumière change sur la distance. Les valeurs d’atténuation sont ignorées pour les lumières directionnelles. Ce membre représente une constante d’atténuation. Pour plus d’informations sur l’atténuation, consultez [Propriétés de la lumière (Direct3D 9)](light-properties.md). Les valeurs valides pour cette plage de membres sont comprises entre 0,0 et Infinity. Pour les lumières non directionnelles, les trois valeurs d’atténuation ne doivent pas être définies sur 0,0 en même temps.

</dd> <dt>

**Thêta**
</dt> <dd>

Type : **float**

</dd> <dd>

Angle, en radians, du cône interne d’une lumière, c’est-à-dire le cône entièrement éclairé. Cette valeur doit être comprise entre 0 et la valeur spécifiée par Phi.

</dd> <dt>

**Santé confidentielles**
</dt> <dd>

Type : **float**

</dd> <dd>

Angle, en radians, définissant le bord extérieur du cône externe de la lumière. Les points en dehors de ce cône ne sont pas allumés par la Spotlight. Cette valeur doit être comprise entre 0 et pi.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[**SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 

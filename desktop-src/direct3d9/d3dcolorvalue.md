---
description: D3DCOLORVALUE structure (D3D9Types. h)-décrit les valeurs de couleur.
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: D3DCOLORVALUE, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b8c188e1b50905abd61184c7e1fe67d4253e920aa26d5d1782c1633d843bd282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733351"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a>D3DCOLORVALUE, structure (D3D9Types. h)

Décrit les valeurs de couleur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a>Membres

<dl> <dt>

**r**
</dt> <dd>

Type : **float**

</dd> <dd>

Valeur à virgule flottante qui spécifie le composant rouge d’une couleur. Cette valeur est généralement comprise entre 0,0 et 1,0. La valeur 0,0 indique l’absence totale du composant rouge, tandis que la valeur 1,0 indique que le rouge est entièrement présent.

</dd> <dt>

**activée**
</dt> <dd>

Type : **float**

</dd> <dd>

Valeur à virgule flottante qui spécifie le composant vert d’une couleur. Cette valeur est généralement comprise entre 0,0 et 1,0. La valeur 0,0 indique l’absence totale du composant vert, tandis que la valeur 1,0 indique que le vert est entièrement présent.

</dd> <dt>

**b**
</dt> <dd>

Type : **float**

</dd> <dd>

Valeur à virgule flottante qui spécifie le composant bleu d’une couleur. Cette valeur est généralement comprise entre 0,0 et 1,0. La valeur 0,0 indique l’absence totale du composant bleu, tandis que la valeur 1,0 indique que le bleu est entièrement présent.

</dd> <dt>

**un**
</dt> <dd>

Type : **float**

</dd> <dd>

Valeur à virgule flottante qui spécifie le composant alpha d’une couleur. Cette valeur est généralement comprise entre 0,0 et 1,0. Une valeur de 0,0 indique une transparence complète, tandis que la valeur 1,0 indique une opacité totale.

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez définir les membres de cette structure sur des valeurs situées en dehors de la plage comprise entre 0 et 1 pour implémenter des effets inhabituels. Les valeurs supérieures à 1 produisent des lumières fortes qui ont tendance à nettoyer une scène. Les valeurs négatives produisent des lumières sombres qui suppriment en fait la lumière d’une scène.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 





---
description: Définit un volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: D3DBOX, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9b7e01641348594e962f546a431700db799600a08571bbb7cfaf13396e671036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805512"
---
# <a name="d3dbox-structure"></a>D3DBOX, structure

Définit un volume.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a>Membres

<dl> <dt>

**Left**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Position du côté gauche de la zone sur l’axe x.

</dd> <dt>

**Top**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Position du haut de la zone sur l’axe y.

</dd> <dt>

**Right**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Position du côté droit de la zone sur l’axe x.

</dd> <dt>

**Bas**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Position du bas de la zone sur l’axe y.

</dd> <dt>

**Front**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Position du premier plan de la zone sur l’axe z.

</dd> <dt>

**Précédent**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Position du arrière de la boîte sur l’axe z.

</dd> </dl>

## <a name="remarks"></a>Remarques

**D3DBOX** comprend les bords gauche, supérieur et avant ; Toutefois, les bords droit, inférieur et arrière ne sont pas inclus. Par exemple, une zone de 100 unités de largeur et commençant à 0 (y compris les points jusqu’à 99) sont exprimées avec la valeur 0 pour le membre de gauche et la valeur 100 pour le membre de droite. Notez qu’une valeur de 99 n’est pas utilisée pour le membre approprié.

Les restrictions sur l’ordre des côtés observées pour les **D3DBOX** sont de gauche à droite, de haut en bas et de premier plan à précédent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 

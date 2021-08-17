---
description: Décrit un événement d’animation.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: Structure D3DXEVENT_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d5569eccd5b99939cd50797ee73593ce5a2bfc8ddd60236e05218ddcca7f4383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731807"
---
# <a name="d3dxevent_desc-structure"></a>D3DXEVENT \_ desc, structure

Décrit un événement d’animation.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Type : **[ **D3DXEVENT \_**](./d3dxevent-type.md)**

</dd> <dd>

Type d’événement, tel que défini dans [**D3DXEVENT \_ type**](./d3dxevent-type.md).

</dd> <dt>

**Assurer**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificateur de suivi d’événement.

</dd> <dt>

**StartTime**
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

</dd> <dd>

Heure de début de l’événement dans l’heure globale.

</dd> <dt>

**Durée**
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

</dd> <dd>

Durée de l’événement dans l’heure globale.

</dd> <dt>

**Transition**
</dt> <dd>

Type : **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**

</dd> <dd>

Style de transition de l’événement, tel que défini dans [**D3DXTRANSITION \_ type**](./d3dxtransition-type.md).

</dd> <dt>

**Poids**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Suivre le poids de l’événement.

</dd> <dt>

**Vitesse**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Suivre la vitesse de l’événement.

</dd> <dt>

**Position**
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

</dd> <dd>

Position du suivi pour l’événement.

</dd> <dt>

**Activer**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Activer l’indicateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

---
description: Décrit une clé vectorielle à utiliser dans une animation d’image clé. Elle spécifie un vecteur à un moment donné. Il est utilisé pour les clés de mise à l’échelle et de traduction.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: Structure D3DXKEY_VECTOR3 (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0214582b3fb1267caeb30a6cca905cbf7243ecf5dd1af40365841b315359317f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119179"
---
# <a name="d3dxkey_vector3-structure"></a>D3DXKEY \_ VECTOR3, structure

Décrit une clé vectorielle à utiliser dans une animation d’image clé. Elle spécifie un vecteur à un moment donné. Il est utilisé pour les clés de mise à l’échelle et de traduction.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a>Membres

<dl> <dt>

**Time**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Horodatage de l’image clé.

</dd> <dt>

**Valeur**
</dt> <dd>

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)**

</dd> <dd>

Vecteur 3D [**D3DXVECTOR3**](d3dxvector3.md) qui fournit des valeurs d’échelle et/ou de translation.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

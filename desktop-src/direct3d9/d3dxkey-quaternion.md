---
description: Décrit une clé Quaternion à utiliser dans l’animation d’image clé. Une clé Quaternion est une valeur Quaternion à un moment donné.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: Structure D3DXKEY_QUATERNION (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322901"
---
# <a name="d3dxkey_quaternion-structure"></a>D3DXKEY, \_ structure de Quaternion

Décrit une clé Quaternion à utiliser dans l’animation d’image clé. Une clé Quaternion est une valeur Quaternion à un moment donné.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a>Membres

<dl> <dt>

**Time**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valeur de temps.

</dd> <dt>

**Valeur**
</dt> <dd>

Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)**

</dd> <dd>

[**D3DXQUATERNION**](d3dxquaternion.md) Quaternion qui fournit des valeurs de rotation.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

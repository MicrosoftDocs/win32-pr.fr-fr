---
description: Décrit une clé de rappel à utiliser dans l’animation d’image clé.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: Structure D3DXKEY_CALLBACK (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f488445bbb018b62445ff802abcf5a82c22b4e31c9d71618e61437efd5e36a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123067"
---
# <a name="d3dxkey_callback-structure"></a>\_Structure de rappel D3DXKEY

Décrit une clé de rappel à utiliser dans l’animation d’image clé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a>Membres

<dl> <dt>

**Time**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Horodatage de l’image clé.

</dd> <dt>

**pCallbackData**
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Pointeur vers les données de rappel de l’utilisateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 

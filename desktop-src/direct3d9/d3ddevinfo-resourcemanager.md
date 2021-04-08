---
description: Statistiques d’utilisation des ressources.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: Structure D3DDEVINFO_ResourceManager (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761966"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a>D3DDEVINFO \_ ResourceManager, structure

Statistiques d’utilisation des ressources.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a>Membres

<dl> <dt>

**stats**
</dt> <dd>

Type : **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**

</dd> <dd>

Tableau d’éléments de statistiques sur les ressources. Consultez [**D3DRESOURCESTATS**](d3dresourcestats.md).

</dd> </dl>

## <a name="remarks"></a>Notes

D3DRTYPECOUNT fait référence au nombre d’énumérations dans [**D3DRESOURCETYPE**](./d3dresourcetype.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 

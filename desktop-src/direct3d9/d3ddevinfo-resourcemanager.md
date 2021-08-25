---
description: Statistiques d’utilisation des ressources.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: Structure D3DDEVINFO_RESOURCEMANAGER (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_RESOURCEMANAGER
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d45d920383e9ed95a9fe50f2ce87bd6cf26d040d45aecc9e7891a5c08f4232cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850279"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a>D3DDEVINFO \_ RESOURCEMANAGER, structure

Statistiques d’utilisation des ressources.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DDEVINFO_RESOURCEMANAGER {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_RESOURCEMANAGER, *LPD3DDEVINFO_RESOURCEMANAGER;

```



## <a name="members"></a>Membres

<dl> <dt>

**stats**
</dt> <dd>

Type : **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**

</dd> <dd>

Tableau d’éléments de statistiques sur les ressources. Consultez [**D3DRESOURCESTATS**](d3dresourcestats.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

D3DRTYPECOUNT fait référence au nombre d’énumérations dans [**D3DRESOURCETYPE**](./d3dresourcetype.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 

---
description: Contient des données pour le signalement de la sollicitation de la mémoire.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: D3DMEMORYPRESSURE, structure (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527116"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a>D3DMEMORYPRESSURE, structure (D3d9types. h)

Contient des données pour le signalement de la sollicitation de la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>Membres

<dl> <dt>

**BytesEvictedFromProcess**
</dt> <dd>

Type : **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’octets qui ont été supprimés par le processus pendant la durée de la requête.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Type : **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre total d’octets placés dans des segments de mémoire non optimaux, en raison d’un espace insuffisant dans les segments de mémoire préférés.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Efficacité globale des allocations de mémoire qui ont été placées dans une mémoire non optimale. La valeur est exprimée sous la forme d’un pourcentage. Par exemple, la valeur 95 indique que les allocations placées dans des segments de mémoire qui ne sont pas préférés sont de 95% efficaces. Ce nombre ne doit pas être considéré comme une mesure exacte.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 

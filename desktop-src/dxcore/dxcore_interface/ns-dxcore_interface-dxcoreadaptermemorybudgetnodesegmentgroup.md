---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Décrit un groupe de segments de mémoire pour un adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916248"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a>DXCoreAdapterMemoryBudgetNodeSegmentGroup, structure

Décrit un groupe de segments de mémoire pour un adaptateur.

## <a name="syntax"></a>Syntaxe

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a>Membres

### <a name="nodeindex"></a>nodeIndex

Type : **uint32_t**

Spécifie la carte physique de l’appareil pour laquelle les informations de mémoire de l’adaptateur sont interrogées. Pour une opération à un seul adaptateur, définissez cette valeur sur zéro. S’il existe plusieurs nœuds d’adaptateur, définissez cette valeur sur l’index du nœud (la carte physique de l’appareil) pour lequel vous souhaitez interroger les informations sur la mémoire de l’adaptateur (voir [systèmes à plusieurs adaptateurs](../../direct3d12/multi-engine.md)).

### <a name="segmentgroup"></a>segmentGroup

Type : **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Spécifie le regroupement des segments de mémoire de l’adaptateur que vous souhaitez interroger.

## <a name="see-also"></a>Voir aussi

[Référence DXCore](../dxcore-reference.md)

[Utilisation de DXCore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)

[Systèmes à plusieurs adaptateurs](../../direct3d12/multi-engine.md)
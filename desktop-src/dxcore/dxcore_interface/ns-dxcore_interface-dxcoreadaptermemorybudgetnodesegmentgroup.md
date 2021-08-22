---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Décrit un groupe de segments de mémoire pour un adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b39557226034e9462e8d51c79aa9b8276659cfe296138df2a3a57f279106f5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118653"
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
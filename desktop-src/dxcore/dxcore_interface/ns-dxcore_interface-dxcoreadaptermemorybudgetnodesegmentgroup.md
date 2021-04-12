---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Décrit un groupe de segments de mémoire pour un adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382099"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a><span data-ttu-id="9fc3e-103">DXCoreAdapterMemoryBudgetNodeSegmentGroup, structure</span><span class="sxs-lookup"><span data-stu-id="9fc3e-103">DXCoreAdapterMemoryBudgetNodeSegmentGroup structure</span></span>

<span data-ttu-id="9fc3e-104">Décrit un groupe de segments de mémoire pour un adaptateur.</span><span class="sxs-lookup"><span data-stu-id="9fc3e-104">Describes a memory segment group for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc3e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fc3e-105">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a><span data-ttu-id="9fc3e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9fc3e-106">Members</span></span>

### <a name="nodeindex"></a><span data-ttu-id="9fc3e-107">nodeIndex</span><span class="sxs-lookup"><span data-stu-id="9fc3e-107">nodeIndex</span></span>

<span data-ttu-id="9fc3e-108">Type : **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="9fc3e-108">Type: **uint32_t**</span></span>

<span data-ttu-id="9fc3e-109">Spécifie la carte physique de l’appareil pour laquelle les informations de mémoire de l’adaptateur sont interrogées.</span><span class="sxs-lookup"><span data-stu-id="9fc3e-109">Specifies the device's physical adapter for which the adapter memory information is queried.</span></span> <span data-ttu-id="9fc3e-110">Pour une opération à un seul adaptateur, définissez cette valeur sur zéro.</span><span class="sxs-lookup"><span data-stu-id="9fc3e-110">For single-adapter operation, set this to zero.</span></span> <span data-ttu-id="9fc3e-111">S’il existe plusieurs nœuds d’adaptateur, définissez cette valeur sur l’index du nœud (la carte physique de l’appareil) pour lequel vous souhaitez interroger les informations sur la mémoire de l’adaptateur (voir [systèmes à plusieurs adaptateurs](../../direct3d12/multi-engine.md)).</span><span class="sxs-lookup"><span data-stu-id="9fc3e-111">If there are multiple adapter nodes, then set this to the index of the node (the device's physical adapter) for which you want to query for adapter memory information (see [Multi-adapter systems](../../direct3d12/multi-engine.md)).</span></span>

### <a name="segmentgroup"></a><span data-ttu-id="9fc3e-112">segmentGroup</span><span class="sxs-lookup"><span data-stu-id="9fc3e-112">segmentGroup</span></span>

<span data-ttu-id="9fc3e-113">Type : **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span><span class="sxs-lookup"><span data-stu-id="9fc3e-113">Type: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span></span>

<span data-ttu-id="9fc3e-114">Spécifie le regroupement des segments de mémoire de l’adaptateur que vous souhaitez interroger.</span><span class="sxs-lookup"><span data-stu-id="9fc3e-114">Specifies the adapter memory segment grouping that you want to query about.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fc3e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fc3e-115">See also</span></span>

[<span data-ttu-id="9fc3e-116">Référence DXCore</span><span class="sxs-lookup"><span data-stu-id="9fc3e-116">DXCore Reference</span></span>](../dxcore-reference.md)

[<span data-ttu-id="9fc3e-117">Utilisation de DXCore pour énumérer des adaptateurs</span><span class="sxs-lookup"><span data-stu-id="9fc3e-117">Using DXCore to enumerate adapters</span></span>](../dxcore-enum-adapters.md)

[<span data-ttu-id="9fc3e-118">Systèmes à plusieurs adaptateurs</span><span class="sxs-lookup"><span data-stu-id="9fc3e-118">Multi-adapter systems</span></span>](../../direct3d12/multi-engine.md)
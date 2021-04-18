---
title: DXCoreSegmentGroup
description: Définit des constantes qui spécifient le regroupement des segments de mémoire d’un adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106536278"
---
# <a name="dxcoresegmentgroup-enum"></a><span data-ttu-id="357d5-103">Énumération DXCoreSegmentGroup</span><span class="sxs-lookup"><span data-stu-id="357d5-103">DXCoreSegmentGroup enum</span></span>

<span data-ttu-id="357d5-104">Définit des constantes qui spécifient le regroupement des segments de mémoire d’un adaptateur.</span><span class="sxs-lookup"><span data-stu-id="357d5-104">Defines constants that specify an adapter's memory segment grouping.</span></span>

## <a name="syntax"></a><span data-ttu-id="357d5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="357d5-105">Syntax</span></span>

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a><span data-ttu-id="357d5-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="357d5-106">Constants</span></span>

### <a name="local"></a><span data-ttu-id="357d5-107">Local</span><span class="sxs-lookup"><span data-stu-id="357d5-107">Local</span></span>

<span data-ttu-id="357d5-108">Spécifie un regroupement de segments considérés comme locaux sur l’adaptateur et représente la mémoire la plus rapide disponible pour le GPU.</span><span class="sxs-lookup"><span data-stu-id="357d5-108">Specifies a grouping of segments that is considered local to the adapter, and represents the fastest memory available to the GPU.</span></span> <span data-ttu-id="357d5-109">Votre application doit cibler le groupe de segments local en tant que taille cible de sa plage de travail.</span><span class="sxs-lookup"><span data-stu-id="357d5-109">Your application should target the local segment group as the target size for its working set.</span></span>

### <a name="nonlocal"></a><span data-ttu-id="357d5-110">Non locale</span><span class="sxs-lookup"><span data-stu-id="357d5-110">NonLocal</span></span>

<span data-ttu-id="357d5-111">Spécifie un regroupement de segments considérés comme non locaux par l’adaptateur et peut avoir des performances plus lentes que le groupe de segments local.</span><span class="sxs-lookup"><span data-stu-id="357d5-111">Specifies a grouping of segments that is considered non-local to the adapter, and may have slower performance than the local segment group.</span></span>

## <a name="see-also"></a><span data-ttu-id="357d5-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="357d5-112">See also</span></span>

<span data-ttu-id="357d5-113">[Référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="357d5-113">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
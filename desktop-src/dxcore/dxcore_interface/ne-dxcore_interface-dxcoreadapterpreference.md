---
title: DXCoreAdapterPreference
description: Définit des constantes qui spécifient les préférences d’adaptateur DXCore à utiliser comme critères de tri de liste.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382384"
---
# <a name="dxcoreadapterpreference-enum"></a><span data-ttu-id="fa5bc-103">Énumération DXCoreAdapterPreference</span><span class="sxs-lookup"><span data-stu-id="fa5bc-103">DXCoreAdapterPreference enum</span></span>

## <a name="description"></a><span data-ttu-id="fa5bc-104">Description</span><span class="sxs-lookup"><span data-stu-id="fa5bc-104">Description</span></span>

<span data-ttu-id="fa5bc-105">Définit des constantes qui spécifient les préférences d’adaptateur DXCore à utiliser comme critères de tri de liste.</span><span class="sxs-lookup"><span data-stu-id="fa5bc-105">Defines constants that specify DXCore adapter preferences to be used as list-sorting criteria.</span></span> <span data-ttu-id="fa5bc-106">Vous pouvez trier une liste d’adaptateurs DXCore en passant un tableau de **DXCoreAdapterPreference** à [IDXCoreAdapterList :: sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span><span class="sxs-lookup"><span data-stu-id="fa5bc-106">You can sort a DXCore adapter list by passing an array of **DXCoreAdapterPreference** to [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa5bc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa5bc-107">Syntax</span></span>

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a><span data-ttu-id="fa5bc-108">Champs d’énumération</span><span class="sxs-lookup"><span data-stu-id="fa5bc-108">Enum fields</span></span>

### <a name="hardware"></a><span data-ttu-id="fa5bc-109">Matériel</span><span class="sxs-lookup"><span data-stu-id="fa5bc-109">Hardware</span></span>

<span data-ttu-id="fa5bc-110">Spécifie une préférence pour les cartes matérielles (par opposition aux adaptateurs logiciels).</span><span class="sxs-lookup"><span data-stu-id="fa5bc-110">Specifies a preference for hardware adapters (as opposed to software adapters).</span></span>

### <a name="minimumpower"></a><span data-ttu-id="fa5bc-111">MinimumPower</span><span class="sxs-lookup"><span data-stu-id="fa5bc-111">MinimumPower</span></span>

<span data-ttu-id="fa5bc-112">Spécifie une préférence pour le GPU avec une alimentation minimale (comme un processeur graphique intégré ou iGPU).</span><span class="sxs-lookup"><span data-stu-id="fa5bc-112">Specifies a preference for the minimum-powered GPU (such as an integrated graphics processor, or iGPU).</span></span>

### <a name="highperformance"></a><span data-ttu-id="fa5bc-113">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="fa5bc-113">HighPerformance</span></span>

<span data-ttu-id="fa5bc-114">Spécifie une préférence pour le GPU le plus performant, tel qu’un processeur graphique externe (xGPU), s’il est disponible, ou un processeur graphique discret (dGPU) s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="fa5bc-114">Specifies a preference for the highest-performance GPU, such as an external graphics processor (xGPU), if available, or discrete graphics processor (dGPU) if available.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa5bc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa5bc-115">See also</span></span>

<span data-ttu-id="fa5bc-116">[IDXCoreAdapterList :: sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="fa5bc-116">[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
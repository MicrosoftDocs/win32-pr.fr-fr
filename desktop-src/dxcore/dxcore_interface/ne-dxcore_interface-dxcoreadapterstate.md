---
title: DXCoreAdapterState
description: Définit des constantes qui spécifient les genres d’États de l’adaptateur DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315558"
---
# <a name="dxcoreadapterstate-enum"></a><span data-ttu-id="80671-103">Énumération DXCoreAdapterState</span><span class="sxs-lookup"><span data-stu-id="80671-103">DXCoreAdapterState enum</span></span>

<span data-ttu-id="80671-104">Définit des constantes qui spécifient les genres d’États de l’adaptateur DXCore.</span><span class="sxs-lookup"><span data-stu-id="80671-104">Defines constants that specify kinds of DXCore adapter states.</span></span> <span data-ttu-id="80671-105">Transmettez l’une de ces constantes à la méthode [IDXCoreAdapter :: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) pour récupérer l’élément d’état de l’adaptateur pour un genre d’État ; transmettez une constante à la méthode [IDXCoreAdapter :: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) pour définir les informations d’un adaptateur pour un élément d’État.</span><span class="sxs-lookup"><span data-stu-id="80671-105">Pass one of these constants to the [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) method to retrieve the adapter state item for a state kind; pass a constant to the [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) method to set an adapter's info for a state item.</span></span>

## <a name="syntax"></a><span data-ttu-id="80671-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80671-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a><span data-ttu-id="80671-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="80671-107">Constants</span></span>

### <a name="isdriverupdateinprogress"></a><span data-ttu-id="80671-108">IsDriverUpdateInProgress</span><span class="sxs-lookup"><span data-stu-id="80671-108">IsDriverUpdateInProgress</span></span>

<span data-ttu-id="80671-109">Spécifie l’état de l’adaptateur <em>IsDriverUpdateInProgress</em> , qui `true` indique qu’une mise à jour du pilote a été lancée sur l’adaptateur, mais qu’elle n’est pas encore terminée.</span><span class="sxs-lookup"><span data-stu-id="80671-109">Specifies the <em>IsDriverUpdateInProgress</em> adapter state, which when `true` indicates that a driver update has been initiated on the adapter but it has not yet completed.</span></span> <span data-ttu-id="80671-110">Si la mise à jour du pilote est déjà terminée, cela signifie que l’adaptateur a été invalidé et que votre appel [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) retourne un <b>HRESULT</b> de <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span><span class="sxs-lookup"><span data-stu-id="80671-110">If the driver update has already completed, then the adapter will have been invalidated, and your [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) call will return a <b>HRESULT</b> of <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span></span>

<span data-ttu-id="80671-111">Lors de l’appel de [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), l’élément d’état <em>IsDriverUpdateInProgress</em> a le type <b>Uint8_t</b>, représentant une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="80671-111">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>IsDriverUpdateInProgress</em> state item has type <b>uint8_t</b>, representing a Boolean value.</span></span>

<span data-ttu-id="80671-112"><b>Important</b>.</span><span class="sxs-lookup"><span data-stu-id="80671-112"><b>Important</b>.</span></span> <span data-ttu-id="80671-113">Cet élément d’État n’est pas pris en charge pour [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span><span class="sxs-lookup"><span data-stu-id="80671-113">This state item is not supported for [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span></span>

### <a name="adaptermemorybudget"></a><span data-ttu-id="80671-114">AdapterMemoryBudget</span><span class="sxs-lookup"><span data-stu-id="80671-114">AdapterMemoryBudget</span></span>

<span data-ttu-id="80671-115">Spécifie l’état de l’adaptateur <em>AdapterMemoryBudget</em> , qui récupère ou demande le budget de mémoire de l’adaptateur sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="80671-115">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span>

<span data-ttu-id="80671-116">Lors de l’appel de [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), l’état de l’adaptateur <em>AdapterMemoryBudget</em> a le type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> pour *inputStateDetails* et le type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> pour *OUTPUTBUFFER*.</span><span class="sxs-lookup"><span data-stu-id="80671-116">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> for *outputBuffer*.</span></span>

## <a name="see-also"></a><span data-ttu-id="80671-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80671-117">See also</span></span>

<span data-ttu-id="80671-118">[IDXCoreAdapter :: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter :: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="80671-118">[IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
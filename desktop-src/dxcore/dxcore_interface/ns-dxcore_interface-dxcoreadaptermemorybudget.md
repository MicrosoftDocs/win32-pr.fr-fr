---
title: DXCoreAdapterMemoryBudget
description: Décrit le budget de mémoire pour un adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463622"
---
# <a name="dxcoreadaptermemorybudget-structure"></a><span data-ttu-id="d02ec-103">DXCoreAdapterMemoryBudget, structure</span><span class="sxs-lookup"><span data-stu-id="d02ec-103">DXCoreAdapterMemoryBudget structure</span></span>

<span data-ttu-id="d02ec-104">Spécifie l’état de l’adaptateur <em>AdapterMemoryBudget</em> , qui récupère ou demande le budget de mémoire de l’adaptateur sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="d02ec-104">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span> <span data-ttu-id="d02ec-105">Le paramètre (demande) d’un budget représente la mémoire physique minimale requise à réserver, en octets, sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="d02ec-105">Setting (requesting) a budget represents the minimum required physical memory to reserve, in bytes, on the adapter.</span></span> <span data-ttu-id="d02ec-106">Nous vous recommandons de définir une réservation d’adaptateur pour indiquer la quantité de mémoire physique que votre application ne peut pas déconnecter sans.</span><span class="sxs-lookup"><span data-stu-id="d02ec-106">We recommend that you set an adapter reservation in order to denote the amount of physical memory that your application can't go without.</span></span> <span data-ttu-id="d02ec-107">Cette valeur permet au système d’exploitation de réduire rapidement l’impact des situations de sollicitation importante de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d02ec-107">This value helps the operating system (OS) to quickly minimize the impact of large memory-pressure situations.</span></span>

<span data-ttu-id="d02ec-108">Lors de l’appel de [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), l’état de l’adaptateur <em>AdapterMemoryBudget</em> a le type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> pour *inputStateDetails* et le type **DXCoreAdapterMemoryBudget** pour *OUTPUTBUFFER*.</span><span class="sxs-lookup"><span data-stu-id="d02ec-108">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **DXCoreAdapterMemoryBudget** for *outputBuffer*.</span></span>

<span data-ttu-id="d02ec-109">Lors de l’appel de [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), l’état de l’adaptateur <em>AdapterMemoryBudget</em> a le type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> pour *inputStateDetails* et le type **uint64_t** pour *inputData*.</span><span class="sxs-lookup"><span data-stu-id="d02ec-109">When calling [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **uint64_t** for *inputData*.</span></span>

## <a name="syntax"></a><span data-ttu-id="d02ec-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d02ec-110">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a><span data-ttu-id="d02ec-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d02ec-111">Members</span></span>

### <a name="budget"></a><span data-ttu-id="d02ec-112">budget</span><span class="sxs-lookup"><span data-stu-id="d02ec-112">budget</span></span>

<span data-ttu-id="d02ec-113">Type : **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="d02ec-113">Type: **uint64_t**</span></span>

<span data-ttu-id="d02ec-114">Spécifie le budget de mémoire de l’adaptateur fourni par le système d’exploitation, en octets, que votre application doit cibler.</span><span class="sxs-lookup"><span data-stu-id="d02ec-114">Specifies the OS-provided adapter memory budget, in bytes, that your application should target.</span></span> <span data-ttu-id="d02ec-115">Si la valeur de *currentUsage* est supérieure à celle du *budget*, votre application risque de subir des interruptions ou des altérations de performances dues à l’activité en arrière-plan par le système d’exploitation, qui est destinée à fournir à d’autres applications une utilisation équitable de la mémoire de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="d02ec-115">If *currentUsage* is greater than *budget*, then your application may incur stuttering or performance penalties due to background activity by the OS, which is intended to provide other applications with a fair usage of adapter memory.</span></span>

### <a name="currentusage"></a><span data-ttu-id="d02ec-116">currentUsage</span><span class="sxs-lookup"><span data-stu-id="d02ec-116">currentUsage</span></span>

<span data-ttu-id="d02ec-117">Type : **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="d02ec-117">Type: **uint64_t**</span></span>

<span data-ttu-id="d02ec-118">Spécifie l’utilisation actuelle de la mémoire de l’adaptateur application, en octets.</span><span class="sxs-lookup"><span data-stu-id="d02ec-118">Specifies your applicaton's current adapter memory usage, in bytes.</span></span>

### <a name="availableforreservation"></a><span data-ttu-id="d02ec-119">availableForReservation</span><span class="sxs-lookup"><span data-stu-id="d02ec-119">availableForReservation</span></span>

<span data-ttu-id="d02ec-120">Type : **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="d02ec-120">Type: **uint64_t**</span></span>

<span data-ttu-id="d02ec-121">Spécifie la quantité de mémoire de l’adaptateur, en octets, que votre application peut réserver.</span><span class="sxs-lookup"><span data-stu-id="d02ec-121">Specifies the amount of adapter memory, in bytes, that your application has available for reservation.</span></span> <span data-ttu-id="d02ec-122">Pour réserver cette mémoire d’adaptateur, votre application doit appeler [IDXCoreAdapter :: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) avec l' *État* défini sur [DXCoreAdapterState :: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span><span class="sxs-lookup"><span data-stu-id="d02ec-122">To reserve this adapter memory, your application should call [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) with *state* set to [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span></span>

### <a name="currentreservation"></a><span data-ttu-id="d02ec-123">currentReservation</span><span class="sxs-lookup"><span data-stu-id="d02ec-123">currentReservation</span></span>

<span data-ttu-id="d02ec-124">Type : **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="d02ec-124">Type: **uint64_t**</span></span>

<span data-ttu-id="d02ec-125">Spécifie la quantité de mémoire de l’adaptateur, en octets, qui est réservée par votre application.</span><span class="sxs-lookup"><span data-stu-id="d02ec-125">Specifies the amount of adapter memory, in bytes, that is reserved by your application.</span></span> <span data-ttu-id="d02ec-126">Le système d’exploitation utilise la réservation comme indicateur pour déterminer la plage de travail minimale de votre application.</span><span class="sxs-lookup"><span data-stu-id="d02ec-126">The OS uses the reservation as a hint to determine your application's minimum working set.</span></span> <span data-ttu-id="d02ec-127">Votre application doit tenter de s’assurer que l’utilisation de la mémoire de l’adaptateur peut être réduite pour répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="d02ec-127">Your application should attempt to ensure that its adapter memory usage can be trimmed to meet this requirement.</span></span>

## <a name="see-also"></a><span data-ttu-id="d02ec-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d02ec-128">See also</span></span>

<span data-ttu-id="d02ec-129">[Référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="d02ec-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
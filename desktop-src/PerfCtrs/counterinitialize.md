---
description: Inscrit le fournisseur et initialise les ensembles de compteurs.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: CounterInitialize fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18996fc4349a120069a9b38293a11faf70632033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952017"
---
# <a name="counterinitialize-function"></a><span data-ttu-id="0c28c-103">CounterInitialize fonction)</span><span class="sxs-lookup"><span data-stu-id="0c28c-103">CounterInitialize function</span></span>

<span data-ttu-id="0c28c-104">Inscrit le fournisseur et initialise les ensembles de compteurs.</span><span class="sxs-lookup"><span data-stu-id="0c28c-104">Registers the provider and initializes the counter sets.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c28c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c28c-105">Syntax</span></span>


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="0c28c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c28c-106">Parameters</span></span>

<span data-ttu-id="0c28c-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0c28c-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c28c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c28c-108">Return value</span></span>

<span data-ttu-id="0c28c-109">Retourne l’erreur \_ de réussite en cas de réussite ; sinon, code d’erreur Win32 standard.</span><span class="sxs-lookup"><span data-stu-id="0c28c-109">Returns ERROR\_SUCCESS on success; otherwise, a standard Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c28c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0c28c-110">Remarks</span></span>

<span data-ttu-id="0c28c-111">Votre fournisseur appelle cette fonction.</span><span class="sxs-lookup"><span data-stu-id="0c28c-111">Your provider calls this function.</span></span> <span data-ttu-id="0c28c-112">La fonction comprend des appels à la fonction [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) et à la fonction [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="0c28c-112">The function includes calls to the [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) function and the [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) function.</span></span>

<span data-ttu-id="0c28c-113">L’outil [**CTRPP**](ctrpp.md) génère cette fonction inline lorsque vous spécifiez l’argument **-o** .</span><span class="sxs-lookup"><span data-stu-id="0c28c-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="0c28c-114">Le nom de la fonction inclut une chaîne de *préfixe* si vous spécifiez l’argument **-prefix** .</span><span class="sxs-lookup"><span data-stu-id="0c28c-114">The function's name include a *prefix* string if you specify the **-prefix** argument.</span></span>

<span data-ttu-id="0c28c-115">Si vous spécifiez les arguments **-MemoryRoutines** ou **-NotificationCallback** (ou si vous spécifiez l’attribut **callback** pour l’élément [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) ), la signature **CounterInitialize** est remplacée par ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="0c28c-115">If you specify the **-MemoryRoutines** or **-NotificationCallback** arguments (or specify the **callback** attribute for the [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) element), the **CounterInitialize** signature changes to the following:</span></span>

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

<span data-ttu-id="0c28c-116">où :</span><span class="sxs-lookup"><span data-stu-id="0c28c-116">where,</span></span>

<dl> <dt>

<span data-ttu-id="0c28c-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span><span class="sxs-lookup"><span data-stu-id="0c28c-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span></span>
</dt> <dd>

<span data-ttu-id="0c28c-118">Nom de votre fonction de rappel [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) que vous implémentez pour recevoir la notification des demandes des consommateurs (par exemple, les demandes d’ajout ou de suppression de compteurs de la requête).</span><span class="sxs-lookup"><span data-stu-id="0c28c-118">The name of your [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) callback function that you implement to receive notification of consumer requests (for example, requests to add or remove counters from the query).</span></span> <span data-ttu-id="0c28c-119">Affectez la valeur **null** si vous n’implémentez pas la fonction de rappel *ControlCallback* .</span><span class="sxs-lookup"><span data-stu-id="0c28c-119">Set to **NULL** if you do not implement the *ControlCallback* callback function.</span></span>

</dd> <dt>

<span data-ttu-id="0c28c-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span><span class="sxs-lookup"><span data-stu-id="0c28c-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span></span>
</dt> <dd>

<span data-ttu-id="0c28c-121">Nom de votre fonction de rappel [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) que PERFLIB appelle pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0c28c-121">The name of your [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) callback function that PERFLIB calls to allocate memory.</span></span> <span data-ttu-id="0c28c-122">Affectez la valeur **null** si vous n’avez pas spécifié l’argument **-MemoryRoutines** .</span><span class="sxs-lookup"><span data-stu-id="0c28c-122">Set to **NULL** if you did not specify the **-MemoryRoutines** argument.</span></span>

</dd> <dt>

<span data-ttu-id="0c28c-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span><span class="sxs-lookup"><span data-stu-id="0c28c-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span></span>
</dt> <dd>

<span data-ttu-id="0c28c-124">Nom de votre fonction de rappel [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) que PERFLIB appelle pour libérer la mémoire allouée à l’aide de la fonction [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) .</span><span class="sxs-lookup"><span data-stu-id="0c28c-124">The name of your [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) callback function that PERFLIB calls to free the memory allocated using the [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) function.</span></span> <span data-ttu-id="0c28c-125">A la valeur **null** si *MemoryAllocationFunction* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0c28c-125">Set to **NULL** if *MemoryAllocationFunction* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0c28c-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span><span class="sxs-lookup"><span data-stu-id="0c28c-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span></span>
</dt> <dd>

<span data-ttu-id="0c28c-127">Informations de contexte à passer à votre allocation de mémoire et à vos routines gratuites.</span><span class="sxs-lookup"><span data-stu-id="0c28c-127">Context information to pass to your memory allocation and free routines.</span></span> <span data-ttu-id="0c28c-128">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0c28c-128">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c28c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c28c-129">Requirements</span></span>



| <span data-ttu-id="0c28c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c28c-130">Requirement</span></span> | <span data-ttu-id="0c28c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c28c-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0c28c-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c28c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0c28c-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c28c-133">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0c28c-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c28c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0c28c-135">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c28c-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 


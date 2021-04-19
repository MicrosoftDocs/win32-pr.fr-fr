---
description: Événement de suivi de la gestion de la mémoire pour une opération de réallocation du tas.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: Événement ETW_HEAP_EVENT_REALLOC (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524637"
---
# <a name="etw_heap_event_realloc-event"></a><span data-ttu-id="d3a69-103">\_Événement de \_ réallocation du tas ETW \_</span><span class="sxs-lookup"><span data-stu-id="d3a69-103">ETW\_HEAP\_EVENT\_REALLOC event</span></span>

<span data-ttu-id="d3a69-104">L' **événement \_ \_ \_ realloc du tas ETW** est un événement de suivi de gestion de la mémoire pour une opération de réallocation du tas.</span><span class="sxs-lookup"><span data-stu-id="d3a69-104">The **ETW\_HEAP\_EVENT\_REALLOC** event is a memory management tracing event for a heap reallocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a><span data-ttu-id="d3a69-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3a69-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3a69-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="d3a69-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a69-107">Handle du tas dans lequel la mémoire a été allouée.</span><span class="sxs-lookup"><span data-stu-id="d3a69-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="d3a69-108">Il s’agit du tas handle d’une application transmise à la fonction [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) lorsque la mémoire a été allouée.</span><span class="sxs-lookup"><span data-stu-id="d3a69-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="d3a69-109">*NewAddress*</span><span class="sxs-lookup"><span data-stu-id="d3a69-109">*NewAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a69-110">Nouvelle adresse de la mémoire qui a été allouée.</span><span class="sxs-lookup"><span data-stu-id="d3a69-110">The new address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="d3a69-111">*OldAddress*</span><span class="sxs-lookup"><span data-stu-id="d3a69-111">*OldAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a69-112">Ancienne adresse de la mémoire précédemment allouée.</span><span class="sxs-lookup"><span data-stu-id="d3a69-112">The old address of the memory that was previously allocated.</span></span>

</dd> <dt>

<span data-ttu-id="d3a69-113">*NewSize*</span><span class="sxs-lookup"><span data-stu-id="d3a69-113">*NewSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a69-114">Nouvelle taille en octets allouée à partir du tas.</span><span class="sxs-lookup"><span data-stu-id="d3a69-114">The new size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="d3a69-115">*OldSize*</span><span class="sxs-lookup"><span data-stu-id="d3a69-115">*OldSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a69-116">Ancienne taille en octets précédemment allouée à partir du tas.</span><span class="sxs-lookup"><span data-stu-id="d3a69-116">The old size in bytes previously allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="d3a69-117">*Source*</span><span class="sxs-lookup"><span data-stu-id="d3a69-117">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a69-118">Source de la mémoire que l’allocateur utilise pour l’allocation du tas.</span><span class="sxs-lookup"><span data-stu-id="d3a69-118">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="d3a69-119">Le tableau suivant répertorie les valeurs possibles pour le paramètre *source* , telles qu’elles sont définies dans le fichier d’en-tête *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="d3a69-119">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="d3a69-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3a69-120">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="d3a69-121">Signification</span><span class="sxs-lookup"><span data-stu-id="d3a69-121">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="d3a69-122"><dt>**Mémoire \_ À \_ partir de**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d3a69-122"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="d3a69-123">Mémoire de la liste des.</span><span class="sxs-lookup"><span data-stu-id="d3a69-123">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="d3a69-124"><dt>**Mémoire \_ À partir de \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d3a69-124"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="d3a69-125">Mémoire à partir du segment de fragmentation faible.</span><span class="sxs-lookup"><span data-stu-id="d3a69-125">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="d3a69-126"><dt>**Mémoire \_ À partir de \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d3a69-126"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="d3a69-127">Mémoire à partir du chemin de code principal.</span><span class="sxs-lookup"><span data-stu-id="d3a69-127">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="d3a69-128"><dt> **Mémoire \_ de \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d3a69-128"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="d3a69-129">Mémoire du c lent.</span><span class="sxs-lookup"><span data-stu-id="d3a69-129">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="d3a69-130"><dt>**Mémoire \_ DE \_ 5 non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d3a69-130"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="d3a69-131">Mémoire qui n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="d3a69-131">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="d3a69-132"><dt>**Mémoire \_ À partir du \_ \_ segment segment**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d3a69-132"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="d3a69-133">Cette valeur est réservée à une utilisation ultérieure et n’est jamais retournée.</span><span class="sxs-lookup"><span data-stu-id="d3a69-133">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

<span data-ttu-id="d3a69-134">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d3a69-134">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3a69-135">Notes</span><span class="sxs-lookup"><span data-stu-id="d3a69-135">Remarks</span></span>

<span data-ttu-id="d3a69-136">L’événement de réallocation d' **\_ événement du tas \_ \_ ETW** est consigné sur toutes les réallocations de tas.</span><span class="sxs-lookup"><span data-stu-id="d3a69-136">The **ETW\_HEAP\_EVENT\_REALLOC** event is logged on all heap reallocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a69-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3a69-137">Requirements</span></span>



| <span data-ttu-id="d3a69-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3a69-138">Requirement</span></span> | <span data-ttu-id="d3a69-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3a69-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a69-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3a69-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a69-141">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3a69-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d3a69-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3a69-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a69-143">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3a69-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d3a69-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3a69-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3a69-145"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3a69-145"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3a69-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3a69-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a69-147">Événements de suivi de gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="d3a69-147">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 

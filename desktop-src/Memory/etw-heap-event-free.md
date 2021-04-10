---
description: Événement de suivi de gestion de la mémoire pour une opération libre de segment de mémoire.
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: Événement ETW_HEAP_EVENT_FREE (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: fd30eccb5848917d752441df79881078dc14d36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862426"
---
# <a name="etw_heap_event_free-event"></a><span data-ttu-id="8ed50-103">Événement \_ libre du tas ETW \_ \_</span><span class="sxs-lookup"><span data-stu-id="8ed50-103">ETW\_HEAP\_EVENT\_FREE event</span></span>

<span data-ttu-id="8ed50-104">L' **événement \_ \_ \_ libre du tas ETW** est un événement de suivi de gestion de la mémoire pour une opération libre de segment de mémoire.</span><span class="sxs-lookup"><span data-stu-id="8ed50-104">The **ETW\_HEAP\_EVENT\_FREE** event is a memory management tracing event for a heap free operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a><span data-ttu-id="8ed50-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ed50-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ed50-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="8ed50-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="8ed50-107">Handle du tas dans lequel la mémoire a été allouée.</span><span class="sxs-lookup"><span data-stu-id="8ed50-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="8ed50-108">Il s’agit du tas handle d’une application transmise à la fonction [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) lorsque la mémoire a été allouée.</span><span class="sxs-lookup"><span data-stu-id="8ed50-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="8ed50-109">*Adresse*</span><span class="sxs-lookup"><span data-stu-id="8ed50-109">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="8ed50-110">Adresse de la mémoire libérée.</span><span class="sxs-lookup"><span data-stu-id="8ed50-110">The address of the memory that was freed.</span></span>

</dd> <dt>

<span data-ttu-id="8ed50-111">*Source*</span><span class="sxs-lookup"><span data-stu-id="8ed50-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="8ed50-112">Source de la mémoire que l’allocateur utilise pour l’allocation du tas.</span><span class="sxs-lookup"><span data-stu-id="8ed50-112">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="8ed50-113">Le tableau suivant répertorie les valeurs possibles pour le paramètre *source* , telles qu’elles sont définies dans le fichier d’en-tête *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="8ed50-113">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="8ed50-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ed50-114">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="8ed50-115">Signification</span><span class="sxs-lookup"><span data-stu-id="8ed50-115">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="8ed50-116"><dt>**Mémoire \_ À \_ partir de**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8ed50-116"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="8ed50-117">Mémoire de la liste des.</span><span class="sxs-lookup"><span data-stu-id="8ed50-117">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="8ed50-118"><dt>**Mémoire \_ À partir de \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8ed50-118"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="8ed50-119">Mémoire à partir du segment de fragmentation faible.</span><span class="sxs-lookup"><span data-stu-id="8ed50-119">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="8ed50-120"><dt>**Mémoire \_ À partir de \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8ed50-120"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="8ed50-121">Mémoire à partir du chemin de code principal.</span><span class="sxs-lookup"><span data-stu-id="8ed50-121">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="8ed50-122"><dt> **Mémoire \_ de \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8ed50-122"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="8ed50-123">Mémoire du c lent.</span><span class="sxs-lookup"><span data-stu-id="8ed50-123">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="8ed50-124"><dt>**Mémoire \_ DE \_ 5 non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8ed50-124"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="8ed50-125">Mémoire qui n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="8ed50-125">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="8ed50-126"><dt>**Mémoire \_ À partir du \_ \_ segment segment**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8ed50-126"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="8ed50-127">Cette valeur est réservée à une utilisation ultérieure et n’est jamais retournée.</span><span class="sxs-lookup"><span data-stu-id="8ed50-127">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ed50-128">Notes</span><span class="sxs-lookup"><span data-stu-id="8ed50-128">Remarks</span></span>

<span data-ttu-id="8ed50-129">L' **événement \_ \_ \_ libre du tas ETW** est enregistré dans toutes les opérations libres du tas.</span><span class="sxs-lookup"><span data-stu-id="8ed50-129">The **ETW\_HEAP\_EVENT\_FREE** event is logged on all heap free operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ed50-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ed50-130">Requirements</span></span>



| <span data-ttu-id="8ed50-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ed50-131">Requirement</span></span> | <span data-ttu-id="8ed50-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ed50-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed50-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ed50-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8ed50-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ed50-134">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8ed50-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ed50-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8ed50-136">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ed50-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8ed50-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ed50-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ed50-138"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ed50-138"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ed50-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ed50-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed50-140">Événements de suivi de gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="8ed50-140">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 

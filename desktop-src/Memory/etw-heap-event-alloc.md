---
description: Événement de suivi de gestion de la mémoire pour une opération d’allocation de tas.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: Événement ETW_HEAP_EVENT_ALLOC (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 57e09ed1785f31b6203c526f2b6d42cc4815a266
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318425"
---
# <a name="etw_heap_event_alloc-event"></a><span data-ttu-id="61706-103">\_ \_ Événement Alloc du tas ETW \_</span><span class="sxs-lookup"><span data-stu-id="61706-103">ETW\_HEAP\_EVENT\_ALLOC event</span></span>

<span data-ttu-id="61706-104">L' **événement \_ \_ \_ Alloc du tas ETW** est un événement de suivi de gestion de la mémoire pour une opération d’allocation de tas.</span><span class="sxs-lookup"><span data-stu-id="61706-104">The **ETW\_HEAP\_EVENT\_ALLOC** event is a memory management tracing event for a heap allocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a><span data-ttu-id="61706-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61706-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61706-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="61706-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="61706-107">Handle du tas dans lequel la mémoire a été allouée.</span><span class="sxs-lookup"><span data-stu-id="61706-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="61706-108">Il s’agit du tas handle d’une application transmise à la fonction [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) lorsque la mémoire a été allouée.</span><span class="sxs-lookup"><span data-stu-id="61706-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="61706-109">*Taille*</span><span class="sxs-lookup"><span data-stu-id="61706-109">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="61706-110">Taille, en octets, allouée à partir du tas.</span><span class="sxs-lookup"><span data-stu-id="61706-110">The size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="61706-111">*Adresse*</span><span class="sxs-lookup"><span data-stu-id="61706-111">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="61706-112">Adresse de la mémoire qui a été allouée.</span><span class="sxs-lookup"><span data-stu-id="61706-112">The address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="61706-113">*Source*</span><span class="sxs-lookup"><span data-stu-id="61706-113">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="61706-114">Source de la mémoire que l’allocateur utilise pour l’allocation du tas.</span><span class="sxs-lookup"><span data-stu-id="61706-114">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="61706-115">Le tableau suivant répertorie les valeurs possibles pour le paramètre *source* , telles qu’elles sont définies dans le fichier d’en-tête *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="61706-115">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="61706-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="61706-116">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="61706-117">Signification</span><span class="sxs-lookup"><span data-stu-id="61706-117">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="61706-118"><dt>**Mémoire \_ À \_ partir de**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="61706-118"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="61706-119">Mémoire de la liste des.</span><span class="sxs-lookup"><span data-stu-id="61706-119">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="61706-120"><dt>**Mémoire \_ À partir de \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="61706-120"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="61706-121">Mémoire à partir du segment de fragmentation faible.</span><span class="sxs-lookup"><span data-stu-id="61706-121">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="61706-122"><dt>**Mémoire \_ À partir de \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="61706-122"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="61706-123">Mémoire à partir du chemin de code principal.</span><span class="sxs-lookup"><span data-stu-id="61706-123">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="61706-124"><dt> **Mémoire \_ de \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="61706-124"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="61706-125">Mémoire à partir du chemin d’accès lent.</span><span class="sxs-lookup"><span data-stu-id="61706-125">Memory from slow path.</span></span><br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="61706-126"><dt>**Mémoire \_ DE \_ 5 non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="61706-126"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="61706-127">Mémoire qui n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="61706-127">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="61706-128"><dt>**Mémoire \_ À partir du \_ \_ segment segment**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="61706-128"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="61706-129">Cette valeur est réservée à une utilisation ultérieure et n’est jamais retournée.</span><span class="sxs-lookup"><span data-stu-id="61706-129">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61706-130">Notes</span><span class="sxs-lookup"><span data-stu-id="61706-130">Remarks</span></span>

<span data-ttu-id="61706-131">L' **événement \_ \_ \_ Alloc du tas ETW** est enregistré sur toutes les allocations de tas.</span><span class="sxs-lookup"><span data-stu-id="61706-131">The **ETW\_HEAP\_EVENT\_ALLOC** event is logged on all heap allocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="61706-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61706-132">Requirements</span></span>



| <span data-ttu-id="61706-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61706-133">Requirement</span></span> | <span data-ttu-id="61706-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="61706-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61706-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61706-135">Minimum supported client</span></span><br/> | <span data-ttu-id="61706-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61706-136">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="61706-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61706-137">Minimum supported server</span></span><br/> | <span data-ttu-id="61706-138">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61706-138">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="61706-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="61706-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="61706-140"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="61706-140"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61706-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61706-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61706-142">Événements de suivi de gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="61706-142">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 

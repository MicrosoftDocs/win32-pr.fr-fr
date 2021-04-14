---
description: Libère un bloc de mémoire qui a été alloué à partir d’un segment de mémoire par RtlAllocateHeap.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: RtlFreeHeap, fonction (Ntifs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523588"
---
# <a name="rtlfreeheap-function"></a><span data-ttu-id="96a5b-103">RtlFreeHeap fonction)</span><span class="sxs-lookup"><span data-stu-id="96a5b-103">RtlFreeHeap function</span></span>

<span data-ttu-id="96a5b-104">Libère un bloc de mémoire qui a été alloué à partir d’un segment de mémoire par [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span><span class="sxs-lookup"><span data-stu-id="96a5b-104">Frees a memory block that was allocated from a heap by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

## <a name="syntax"></a><span data-ttu-id="96a5b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96a5b-105">Syntax</span></span>


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a><span data-ttu-id="96a5b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96a5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96a5b-107">*HeapHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96a5b-107">*HeapHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96a5b-108">Handle pour le tas dont le bloc de mémoire doit être libéré.</span><span class="sxs-lookup"><span data-stu-id="96a5b-108">A handle for the heap whose memory block is to be freed.</span></span> <span data-ttu-id="96a5b-109">Ce paramètre est un handle retourné par [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span><span class="sxs-lookup"><span data-stu-id="96a5b-109">This parameter is a handle returned by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>

</dd> <dt>

<span data-ttu-id="96a5b-110">*Indicateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="96a5b-110">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="96a5b-111">Jeu d’indicateurs qui contrôle les aspects de la libération d’un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="96a5b-111">A set of flags that controls aspects of freeing a memory block.</span></span> <span data-ttu-id="96a5b-112">La spécification de la valeur suivante remplace la valeur correspondante qui a été spécifiée dans le paramètre *Flags* lorsque le segment de mémoire a été créé par [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span><span class="sxs-lookup"><span data-stu-id="96a5b-112">Specifying the following value overrides the corresponding value that was specified in the *Flags* parameter when the heap was created by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>



| <span data-ttu-id="96a5b-113">Indicateur</span><span class="sxs-lookup"><span data-stu-id="96a5b-113">Flag</span></span>                           | <span data-ttu-id="96a5b-114">Signification</span><span class="sxs-lookup"><span data-stu-id="96a5b-114">Meaning</span></span>                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a5b-115">segment de mémoire \_ non \_ sérialisé</span><span class="sxs-lookup"><span data-stu-id="96a5b-115">HEAP\_NO\_SERIALIZE</span></span><br/> | <span data-ttu-id="96a5b-116">L’exclusion mutuelle n’est pas utilisée quand **RtlFreeHeap** accède au segment de mémoire.</span><span class="sxs-lookup"><span data-stu-id="96a5b-116">Mutual exclusion will not be used when **RtlFreeHeap** is accessing the heap.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="96a5b-117">*HeapBase* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96a5b-117">*HeapBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96a5b-118">Pointeur vers le bloc de mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="96a5b-118">A pointer to the memory block to free.</span></span> <span data-ttu-id="96a5b-119">Ce pointeur est retourné par [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span><span class="sxs-lookup"><span data-stu-id="96a5b-119">This pointer is returned by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96a5b-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96a5b-120">Return value</span></span>

<span data-ttu-id="96a5b-121">Retourne la **valeur true** si le bloc a été correctement libéré ; **False** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96a5b-121">Returns **TRUE** if the block was freed successfully; **FALSE** otherwise.</span></span>

> [!Note]  
> <span data-ttu-id="96a5b-122">À compter de Windows 8, la valeur de retour est de type **logique**, avec une taille différente de celle de la valeur **booléenne**.</span><span class="sxs-lookup"><span data-stu-id="96a5b-122">Starting with Windows 8 the return value is typed as **LOGICAL**, which has a different size than **BOOLEAN**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96a5b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96a5b-123">Requirements</span></span>



| <span data-ttu-id="96a5b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96a5b-124">Requirement</span></span> | <span data-ttu-id="96a5b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="96a5b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a5b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96a5b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="96a5b-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96a5b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="96a5b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96a5b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="96a5b-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96a5b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="96a5b-130">Plateforme cible</span><span class="sxs-lookup"><span data-stu-id="96a5b-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="96a5b-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="96a5b-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="96a5b-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="96a5b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="96a5b-133"><dt>Ntifs. h (inclure Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96a5b-133"><dt>Ntifs.h (include Ntifs.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="96a5b-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="96a5b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="96a5b-135"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96a5b-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="96a5b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="96a5b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96a5b-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96a5b-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="96a5b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96a5b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a5b-139">**RtlAllocateHeap**</span><span class="sxs-lookup"><span data-stu-id="96a5b-139">**RtlAllocateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[<span data-ttu-id="96a5b-140">**RtlCreateHeap**</span><span class="sxs-lookup"><span data-stu-id="96a5b-140">**RtlCreateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[<span data-ttu-id="96a5b-141">**RtlDestroyHeap**</span><span class="sxs-lookup"><span data-stu-id="96a5b-141">**RtlDestroyHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 

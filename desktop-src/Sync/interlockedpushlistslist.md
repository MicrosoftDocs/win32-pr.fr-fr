---
UID: ''
title: InterlockedPushListSList, fonction
description: Insère une liste à liaison unique à l’avant d’une autre liste à liaison unique.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2020
ms.locfileid: "104381710"
---
# <a name="interlockedpushlistslist-function"></a><span data-ttu-id="fdad3-103">InterlockedPushListSList, fonction</span><span class="sxs-lookup"><span data-stu-id="fdad3-103">InterlockedPushListSList function</span></span>

## <a name="description"></a><span data-ttu-id="fdad3-104">Description</span><span class="sxs-lookup"><span data-stu-id="fdad3-104">Description</span></span>

<span data-ttu-id="fdad3-105">Insère une liste à liaison unique à l’avant d’une autre liste à liaison unique.</span><span class="sxs-lookup"><span data-stu-id="fdad3-105">Inserts a singly-linked list at the front of another singly linked list.</span></span>
<span data-ttu-id="fdad3-106">L’accès aux listes est synchronisé sur un système multiprocesseur.</span><span class="sxs-lookup"><span data-stu-id="fdad3-106">Access to the lists is synchronized on a multiprocessor system.</span></span>

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a><span data-ttu-id="fdad3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fdad3-107">Parameters</span></span>

### <a name="listhead-in-out"></a><span data-ttu-id="fdad3-108">ListHead [in, out]</span><span class="sxs-lookup"><span data-stu-id="fdad3-108">ListHead [in, out]</span></span>

<span data-ttu-id="fdad3-109">Pointeur vers une structure **SLIST_HEADER** qui représente l’en-tête d’une liste liée de façon unique.</span><span class="sxs-lookup"><span data-stu-id="fdad3-109">Pointer to an **SLIST_HEADER** structure that represents the head of a singly linked list.</span></span>
<span data-ttu-id="fdad3-110">La liste spécifiée par la *liste* et les paramètres d' *écoute* est insérée au début de cette liste.</span><span class="sxs-lookup"><span data-stu-id="fdad3-110">The list specified by the *List* and *ListEnd* parameters is inserted at the front of this list.</span></span>

### <a name="list-in-out"></a><span data-ttu-id="fdad3-111">List [in, out]</span><span class="sxs-lookup"><span data-stu-id="fdad3-111">List [in, out]</span></span>

<span data-ttu-id="fdad3-112">Pointeur vers une structure [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) qui représente le premier élément de la liste à insérer.</span><span class="sxs-lookup"><span data-stu-id="fdad3-112">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the first item in the list to be inserted.</span></span>

### <a name="listend-in-out"></a><span data-ttu-id="fdad3-113">ListEned [in, out]</span><span class="sxs-lookup"><span data-stu-id="fdad3-113">ListEnd [in, out]</span></span>

<span data-ttu-id="fdad3-114">Pointeur vers une structure [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) qui représente le dernier élément de la liste à insérer.</span><span class="sxs-lookup"><span data-stu-id="fdad3-114">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the last item in the list to be inserted.</span></span>

### <a name="count-in"></a><span data-ttu-id="fdad3-115">Nombre [in]</span><span class="sxs-lookup"><span data-stu-id="fdad3-115">Count [in]</span></span>

<span data-ttu-id="fdad3-116">Nombre d’éléments dans la liste à insérer.</span><span class="sxs-lookup"><span data-stu-id="fdad3-116">The number of items in the list to be inserted.</span></span>

## <a name="returns"></a><span data-ttu-id="fdad3-117">Retours</span><span class="sxs-lookup"><span data-stu-id="fdad3-117">Returns</span></span>

<span data-ttu-id="fdad3-118">La valeur de retour est le premier élément précédent dans la liste spécifiée par le paramètre *listhead* .</span><span class="sxs-lookup"><span data-stu-id="fdad3-118">The return value is the previous first item in the list specified by the *ListHead* parameter.</span></span>
<span data-ttu-id="fdad3-119">Si la liste était déjà vide, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="fdad3-119">If the list was previously empty, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdad3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="fdad3-120">Remarks</span></span>

<span data-ttu-id="fdad3-121">Tous les éléments de liste doivent être alignés sur une limite de **MEMORY_ALLOCATION_ALIGNMENT** ; dans le cas contraire, cette fonction se comportera de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="fdad3-121">All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary; otherwise, this function will behave unpredictably.</span></span>
<span data-ttu-id="fdad3-122">Consultez **_aligned_malloc**.</span><span class="sxs-lookup"><span data-stu-id="fdad3-122">See **_aligned_malloc**.</span></span>

<span data-ttu-id="fdad3-123">**Windows 8 et Windows Server 2012 :**  Cette fonction a été remplacée par [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span><span class="sxs-lookup"><span data-stu-id="fdad3-123">**Windows 8 and Windows Server 2012:**  This function has been superceded by [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span></span>
<span data-ttu-id="fdad3-124">Lors de la compilation avec **NTDDI_VERSION** défini sur **NTDDI_WIN8** ou une valeur supérieure, les appels à **InterlockedPushListSList** vont à **InterlockedPushListSListEx** à la place.</span><span class="sxs-lookup"><span data-stu-id="fdad3-124">When compiling with **NTDDI_VERSION** set to **NTDDI_WIN8** or greater, calls to **InterlockedPushListSList** will go to **InterlockedPushListSListEx** instead.</span></span>

## <a name="see-also"></a><span data-ttu-id="fdad3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdad3-125">See also</span></span>

[<span data-ttu-id="fdad3-126">Listes liées de façon isolée</span><span class="sxs-lookup"><span data-stu-id="fdad3-126">Interlocked Singly Linked Lists</span></span>](/windows/desktop/Sync/interlocked-singly-linked-lists)

[<span data-ttu-id="fdad3-127">InterlockedPopEntrySList</span><span class="sxs-lookup"><span data-stu-id="fdad3-127">InterlockedPopEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[<span data-ttu-id="fdad3-128">InterlockedPushEntrySList</span><span class="sxs-lookup"><span data-stu-id="fdad3-128">InterlockedPushEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[<span data-ttu-id="fdad3-129">InterlockedPushListSListEx</span><span class="sxs-lookup"><span data-stu-id="fdad3-129">InterlockedPushListSListEx</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[<span data-ttu-id="fdad3-130">InterlockedFlushSList</span><span class="sxs-lookup"><span data-stu-id="fdad3-130">InterlockedFlushSList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[<span data-ttu-id="fdad3-131">SLIST_ENTRY</span><span class="sxs-lookup"><span data-stu-id="fdad3-131">SLIST_ENTRY</span></span>](/windows/win32/api/winnt/ns-winnt-slist_entry)

[<span data-ttu-id="fdad3-132">Utilisation de listes liées de façon unique</span><span class="sxs-lookup"><span data-stu-id="fdad3-132">Using Singly Linked Lists</span></span>](/windows/desktop/Sync/using-singly-linked-lists)

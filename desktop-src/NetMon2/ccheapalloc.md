---
description: La fonction CCHeapAlloc alloue de la mémoire sur la base d’une capture par capture.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: CCHeapAlloc, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864798"
---
# <a name="ccheapalloc-function"></a><span data-ttu-id="41a8a-103">CCHeapAlloc fonction)</span><span class="sxs-lookup"><span data-stu-id="41a8a-103">CCHeapAlloc function</span></span>

<span data-ttu-id="41a8a-104">La fonction **CCHeapAlloc** alloue de la mémoire sur la base d’une capture par capture.</span><span class="sxs-lookup"><span data-stu-id="41a8a-104">The **CCHeapAlloc** function allocates memory on a capture-by-capture basis.</span></span>

## <a name="syntax"></a><span data-ttu-id="41a8a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41a8a-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="41a8a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41a8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a8a-107">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="41a8a-107">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="41a8a-108">Longueur demandée de la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="41a8a-108">Requested length of memory allocated.</span></span>

</dd> <dt>

<span data-ttu-id="41a8a-109">*bZeroInit*</span><span class="sxs-lookup"><span data-stu-id="41a8a-109">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="41a8a-110">Indique si la mémoire allouée a été initialisée.</span><span class="sxs-lookup"><span data-stu-id="41a8a-110">Indicator of whether allocated memory was initialized.</span></span> <span data-ttu-id="41a8a-111">Si la valeur du paramètre est **true**, la mémoire allouée est initialisée à zéro.</span><span class="sxs-lookup"><span data-stu-id="41a8a-111">If the parameter value is **TRUE**, the allocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a8a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41a8a-112">Return value</span></span>

<span data-ttu-id="41a8a-113">Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="41a8a-113">If the function is successful, the return value is a pointer to the allocated memory.</span></span> <span data-ttu-id="41a8a-114">Lorsque vous avez fini d’utiliser la mémoire allouée, libérez de la mémoire en appelant la fonction [**CCHeapFree**](ccheapfree.md) .</span><span class="sxs-lookup"><span data-stu-id="41a8a-114">When you have finished using the allocated memory, free the memory by calling the [**CCHeapFree**](ccheapfree.md) function.</span></span>

<span data-ttu-id="41a8a-115">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="41a8a-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="41a8a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41a8a-116">Requirements</span></span>



| <span data-ttu-id="41a8a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41a8a-117">Requirement</span></span> | <span data-ttu-id="41a8a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="41a8a-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="41a8a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41a8a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="41a8a-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41a8a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="41a8a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41a8a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="41a8a-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41a8a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="41a8a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="41a8a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="41a8a-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="41a8a-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="41a8a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41a8a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="41a8a-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41a8a-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="41a8a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="41a8a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41a8a-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41a8a-128"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41a8a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41a8a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a8a-130">**SetCCInstPtr**</span><span class="sxs-lookup"><span data-stu-id="41a8a-130">**SetCCInstPtr**</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="41a8a-131">**GetCCInstPtr**</span><span class="sxs-lookup"><span data-stu-id="41a8a-131">**GetCCInstPtr**</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="41a8a-132">**CCHeapFree**</span><span class="sxs-lookup"><span data-stu-id="41a8a-132">**CCHeapFree**</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="41a8a-133">**CCHeapReAlloc**</span><span class="sxs-lookup"><span data-stu-id="41a8a-133">**CCHeapReAlloc**</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="41a8a-134">**CCHeapSize**</span><span class="sxs-lookup"><span data-stu-id="41a8a-134">**CCHeapSize**</span></span>](ccheapsize.md)
</dt> </dl>

 

 





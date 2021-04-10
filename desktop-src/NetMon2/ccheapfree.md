---
description: La fonction CCHeapFree libère la mémoire allouée par la fonction CCHeapAlloc.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: CCHeapFree, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e89ca9a7d00559724edc6679a0ed99e4bdf9c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115743"
---
# <a name="ccheapfree-function"></a><span data-ttu-id="52bb8-103">CCHeapFree fonction)</span><span class="sxs-lookup"><span data-stu-id="52bb8-103">CCHeapFree function</span></span>

<span data-ttu-id="52bb8-104">La fonction **CCHeapFree** libère la mémoire allouée par la fonction **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="52bb8-104">The **CCHeapFree** function releases the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="52bb8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52bb8-105">Syntax</span></span>


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="52bb8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52bb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52bb8-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="52bb8-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="52bb8-108">Pointeur vers la mémoire libérée par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="52bb8-108">Pointer to the memory that this function releases.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52bb8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52bb8-109">Return value</span></span>

<span data-ttu-id="52bb8-110">Si la fonction **CCHeapFree** réussit, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="52bb8-110">If the **CCHeapFree** function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="52bb8-111">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="52bb8-111">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="52bb8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52bb8-112">Requirements</span></span>



| <span data-ttu-id="52bb8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52bb8-113">Requirement</span></span> | <span data-ttu-id="52bb8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="52bb8-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52bb8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52bb8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="52bb8-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52bb8-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="52bb8-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52bb8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="52bb8-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52bb8-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="52bb8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="52bb8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="52bb8-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="52bb8-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="52bb8-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="52bb8-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="52bb8-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52bb8-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="52bb8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="52bb8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52bb8-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52bb8-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52bb8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52bb8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52bb8-126">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="52bb8-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="52bb8-127">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="52bb8-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="52bb8-128">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="52bb8-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="52bb8-129">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="52bb8-129">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="52bb8-130">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="52bb8-130">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 





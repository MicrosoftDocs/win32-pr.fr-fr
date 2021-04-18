---
description: La fonction CCHeapSize retourne la taille de la mémoire allouée par la fonction CCHeapAlloc.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: CCHeapSize, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ae196253a66fc68f9066615b39c48f6921e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519383"
---
# <a name="ccheapsize-function"></a><span data-ttu-id="9b889-103">CCHeapSize fonction)</span><span class="sxs-lookup"><span data-stu-id="9b889-103">CCHeapSize function</span></span>

<span data-ttu-id="9b889-104">La fonction **CCHeapSize** retourne la taille de la mémoire allouée par la fonction **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="9b889-104">The **CCHeapSize** function returns the size of the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b889-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b889-105">Syntax</span></span>


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="9b889-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b889-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b889-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="9b889-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="9b889-108">Pointeur vers la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="9b889-108">Pointer to the allocated memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b889-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b889-109">Return value</span></span>

<span data-ttu-id="9b889-110">Si la fonction réussit, la valeur de retour est la taille du bloc de mémoire demandé, mesurée en octets.</span><span class="sxs-lookup"><span data-stu-id="9b889-110">If the function is successful, the return value is the size of the requested memory block   measured in bytes.</span></span>

<span data-ttu-id="9b889-111">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="9b889-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b889-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b889-112">Requirements</span></span>



| <span data-ttu-id="9b889-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b889-113">Requirement</span></span> | <span data-ttu-id="9b889-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b889-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9b889-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b889-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9b889-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b889-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9b889-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b889-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9b889-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b889-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9b889-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b889-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b889-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b889-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9b889-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9b889-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b889-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b889-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9b889-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9b889-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b889-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b889-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b889-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b889-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b889-126">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="9b889-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="9b889-127">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="9b889-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="9b889-128">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="9b889-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="9b889-129">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="9b889-129">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="9b889-130">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="9b889-130">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> </dl>

 

 





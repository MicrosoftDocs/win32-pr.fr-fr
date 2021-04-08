---
description: La fonction CCHeapReAlloc réalloue la mémoire allouée par la fonction CCHeapAlloc.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: CCHeapReAlloc, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756453"
---
# <a name="ccheaprealloc-function"></a><span data-ttu-id="0e47b-103">CCHeapReAlloc fonction)</span><span class="sxs-lookup"><span data-stu-id="0e47b-103">CCHeapReAlloc function</span></span>

<span data-ttu-id="0e47b-104">La fonction **CCHeapReAlloc** réalloue la mémoire allouée par la fonction **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="0e47b-104">The **CCHeapReAlloc** function reallocates memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e47b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e47b-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="0e47b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e47b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e47b-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="0e47b-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="0e47b-108">Pointeur vers la mémoire allouée d’origine.</span><span class="sxs-lookup"><span data-stu-id="0e47b-108">Pointer to the original allocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="0e47b-109">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="0e47b-109">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="0e47b-110">Taille de la mémoire réallouée, mesurée en octets.</span><span class="sxs-lookup"><span data-stu-id="0e47b-110">Size of the reallocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0e47b-111">*bZeroInit*</span><span class="sxs-lookup"><span data-stu-id="0e47b-111">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="0e47b-112">Indique si la mémoire réallouée a été initialisée.</span><span class="sxs-lookup"><span data-stu-id="0e47b-112">Indicator of whether reallocated memory was initialized.</span></span> <span data-ttu-id="0e47b-113">Si la valeur du paramètre est **true**, la mémoire nouvellement allouée est initialisée à zéro.</span><span class="sxs-lookup"><span data-stu-id="0e47b-113">If the parameter value is **TRUE**, the newly reallocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e47b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e47b-114">Return value</span></span>

<span data-ttu-id="0e47b-115">Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire réallouée.</span><span class="sxs-lookup"><span data-stu-id="0e47b-115">If the function is successful, the return value is a pointer to the reallocated memory.</span></span>

<span data-ttu-id="0e47b-116">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="0e47b-116">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e47b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e47b-117">Requirements</span></span>



| <span data-ttu-id="0e47b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e47b-118">Requirement</span></span> | <span data-ttu-id="0e47b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e47b-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0e47b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e47b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e47b-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e47b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0e47b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e47b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e47b-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e47b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0e47b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e47b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e47b-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e47b-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0e47b-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e47b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e47b-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e47b-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0e47b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0e47b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e47b-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e47b-129"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e47b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e47b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e47b-131">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="0e47b-131">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="0e47b-132">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="0e47b-132">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="0e47b-133">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="0e47b-133">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="0e47b-134">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="0e47b-134">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="0e47b-135">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="0e47b-135">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 





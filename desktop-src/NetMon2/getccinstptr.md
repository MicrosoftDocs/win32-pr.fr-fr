---
description: La fonction GetCCInstPtr retourne le pointeur vers les données d’instance ajoutées au contexte de capture.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: GetCCInstPtr, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750092"
---
# <a name="getccinstptr-function"></a><span data-ttu-id="5fd94-103">GetCCInstPtr fonction)</span><span class="sxs-lookup"><span data-stu-id="5fd94-103">GetCCInstPtr function</span></span>

<span data-ttu-id="5fd94-104">La fonction **GetCCInstPtr** retourne le pointeur vers les données d’instance ajoutées au contexte de capture.</span><span class="sxs-lookup"><span data-stu-id="5fd94-104">The **GetCCInstPtr** function returns the pointer to the instance data added to the capture context.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd94-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fd94-105">Syntax</span></span>


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a><span data-ttu-id="5fd94-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fd94-106">Parameters</span></span>

<span data-ttu-id="5fd94-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5fd94-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5fd94-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5fd94-108">Return value</span></span>

<span data-ttu-id="5fd94-109">Si la fonction réussit, la valeur de retour est un pointeur vers les données d’instance d’une capture spécifique.</span><span class="sxs-lookup"><span data-stu-id="5fd94-109">If the function is successful, the return value is a pointer to the instance data of a specific capture.</span></span>

<span data-ttu-id="5fd94-110">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="5fd94-110">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd94-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fd94-111">Requirements</span></span>



| <span data-ttu-id="5fd94-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fd94-112">Requirement</span></span> | <span data-ttu-id="5fd94-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fd94-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd94-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fd94-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd94-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fd94-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5fd94-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fd94-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd94-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fd94-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5fd94-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fd94-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fd94-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd94-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5fd94-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5fd94-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="5fd94-121"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fd94-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5fd94-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5fd94-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fd94-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fd94-123"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fd94-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fd94-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd94-125">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="5fd94-125">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="5fd94-126">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="5fd94-126">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="5fd94-127">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="5fd94-127">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="5fd94-128">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="5fd94-128">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="5fd94-129">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="5fd94-129">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 





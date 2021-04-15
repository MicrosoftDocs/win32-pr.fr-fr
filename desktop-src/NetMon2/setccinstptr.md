---
description: La fonction SetCCInstPtr capture un pointeur d’instance de contexte.
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: SetCCInstPtr, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526752"
---
# <a name="setccinstptr-function"></a><span data-ttu-id="088c9-103">SetCCInstPtr fonction)</span><span class="sxs-lookup"><span data-stu-id="088c9-103">SetCCInstPtr function</span></span>

<span data-ttu-id="088c9-104">La fonction **SetCCInstPtr** capture un pointeur d’instance de contexte.</span><span class="sxs-lookup"><span data-stu-id="088c9-104">The **SetCCInstPtr** function captures a context instance pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="088c9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="088c9-105">Syntax</span></span>


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a><span data-ttu-id="088c9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="088c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="088c9-107">*lpCurCaptureInst*</span><span class="sxs-lookup"><span data-stu-id="088c9-107">*lpCurCaptureInst*</span></span> 
</dt> <dd>

<span data-ttu-id="088c9-108">Pointeur vers les données d’instance ajoutées à la capture.</span><span class="sxs-lookup"><span data-stu-id="088c9-108">Pointer to the instance data added to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="088c9-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="088c9-109">Return value</span></span>

<span data-ttu-id="088c9-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="088c9-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="088c9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="088c9-111">Remarks</span></span>

<span data-ttu-id="088c9-112">Utilisez cette fonction pour stocker un pointeur vers un bloc qui a été alloué avec la fonction **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="088c9-112">Use this function to store a pointer to a block that was allocated with the **CCHeapAlloc** function.</span></span> <span data-ttu-id="088c9-113">Chaque analyseur peut définir une seule instance de données sur une capture.</span><span class="sxs-lookup"><span data-stu-id="088c9-113">Each parser can set a single instance of data on a capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="088c9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="088c9-114">Requirements</span></span>



| <span data-ttu-id="088c9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="088c9-115">Requirement</span></span> | <span data-ttu-id="088c9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="088c9-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="088c9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="088c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="088c9-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="088c9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="088c9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="088c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="088c9-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="088c9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="088c9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="088c9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="088c9-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="088c9-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="088c9-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="088c9-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="088c9-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="088c9-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="088c9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="088c9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="088c9-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="088c9-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="088c9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="088c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088c9-128">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="088c9-128">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="088c9-129">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="088c9-129">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="088c9-130">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="088c9-130">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="088c9-131">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="088c9-131">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="088c9-132">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="088c9-132">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 





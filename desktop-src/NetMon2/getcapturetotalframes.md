---
description: La fonction GetCaptureTotalFrames retourne le nombre total de frames dans la capture.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: GetCaptureTotalFrames, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: aa7c81e690e9f7eab258c832ae374f18f9b7afc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862014"
---
# <a name="getcapturetotalframes-function"></a><span data-ttu-id="eea93-103">GetCaptureTotalFrames fonction)</span><span class="sxs-lookup"><span data-stu-id="eea93-103">GetCaptureTotalFrames function</span></span>

<span data-ttu-id="eea93-104">La fonction **GetCaptureTotalFrames** retourne le nombre total de frames dans la capture.</span><span class="sxs-lookup"><span data-stu-id="eea93-104">The **GetCaptureTotalFrames** function returns the total number of frames in the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea93-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eea93-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="eea93-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eea93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea93-107">*hCapture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eea93-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea93-108">Handle de la capture.</span><span class="sxs-lookup"><span data-stu-id="eea93-108">Handle to the capture.</span></span> <span data-ttu-id="eea93-109">Pour plus d’informations sur l’obtention du descripteur de capture, consultez la section Notes de cette rubrique **GetCaptureTotalFrames** .</span><span class="sxs-lookup"><span data-stu-id="eea93-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTotalFrames** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eea93-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eea93-110">Return value</span></span>

<span data-ttu-id="eea93-111">Si la fonction réussit, la valeur de retour est le nombre total de frames dans la capture.</span><span class="sxs-lookup"><span data-stu-id="eea93-111">If the function is successful, the return value is the total number of frames in the capture.</span></span>

<span data-ttu-id="eea93-112">Si la fonction échoue, la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="eea93-112">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="eea93-113">Notes</span><span class="sxs-lookup"><span data-stu-id="eea93-113">Remarks</span></span>

<span data-ttu-id="eea93-114">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureTotalFrames** .</span><span class="sxs-lookup"><span data-stu-id="eea93-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTotalFrames** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea93-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eea93-115">Requirements</span></span>



| <span data-ttu-id="eea93-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eea93-116">Requirement</span></span> | <span data-ttu-id="eea93-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="eea93-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eea93-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eea93-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eea93-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eea93-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="eea93-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eea93-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eea93-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eea93-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="eea93-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="eea93-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea93-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="eea93-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="eea93-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eea93-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="eea93-125"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eea93-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="eea93-126">DLL</span><span class="sxs-lookup"><span data-stu-id="eea93-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eea93-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eea93-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





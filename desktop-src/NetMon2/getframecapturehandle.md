---
description: La fonction GetFrameCaptureHandle retourne un handle vers la capture en fonction d’un frame donné.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: GetFrameCaptureHandle, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3770ad0fd3db7d1c076b5d1f286c1fdbdc2707a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862010"
---
# <a name="getframecapturehandle-function"></a><span data-ttu-id="827b0-103">GetFrameCaptureHandle fonction)</span><span class="sxs-lookup"><span data-stu-id="827b0-103">GetFrameCaptureHandle function</span></span>

<span data-ttu-id="827b0-104">La fonction **GetFrameCaptureHandle** retourne un handle vers la capture en fonction d’un frame donné.</span><span class="sxs-lookup"><span data-stu-id="827b0-104">The **GetFrameCaptureHandle** function returns a handle to the capture based on a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="827b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="827b0-105">Syntax</span></span>


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="827b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="827b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="827b0-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="827b0-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="827b0-108">Handle vers un frame.</span><span class="sxs-lookup"><span data-stu-id="827b0-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="827b0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="827b0-109">Return value</span></span>

<span data-ttu-id="827b0-110">Si la fonction réussit, la valeur de retour est un handle vers la capture.</span><span class="sxs-lookup"><span data-stu-id="827b0-110">If the function is successful, the return value is a handle to the capture.</span></span>

<span data-ttu-id="827b0-111">Si la fonction échoue, la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="827b0-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="827b0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="827b0-112">Remarks</span></span>

<span data-ttu-id="827b0-113">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameCaptureHandle** .</span><span class="sxs-lookup"><span data-stu-id="827b0-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameCaptureHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="827b0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="827b0-114">Requirements</span></span>



| <span data-ttu-id="827b0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="827b0-115">Requirement</span></span> | <span data-ttu-id="827b0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="827b0-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="827b0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="827b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="827b0-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="827b0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="827b0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="827b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="827b0-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="827b0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="827b0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="827b0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="827b0-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="827b0-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="827b0-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="827b0-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="827b0-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="827b0-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="827b0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="827b0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="827b0-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="827b0-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





---
description: La fonction GetFrameFromFrameHandle retourne un pointeur vers un frame à partir d’un handle de frame.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: GetFrameFromFrameHandle, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517446"
---
# <a name="getframefromframehandle-function"></a><span data-ttu-id="59cca-103">GetFrameFromFrameHandle fonction)</span><span class="sxs-lookup"><span data-stu-id="59cca-103">GetFrameFromFrameHandle function</span></span>

<span data-ttu-id="59cca-104">La fonction **GetFrameFromFrameHandle** retourne un pointeur vers un frame à partir d’un handle de frame.</span><span class="sxs-lookup"><span data-stu-id="59cca-104">The **GetFrameFromFrameHandle** function returns a pointer to a frame from a frame handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="59cca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59cca-105">Syntax</span></span>


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="59cca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59cca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59cca-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59cca-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59cca-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="59cca-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59cca-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59cca-109">Return value</span></span>

<span data-ttu-id="59cca-110">Si la fonction réussit, la valeur de retour est un pointeur vers le frame.</span><span class="sxs-lookup"><span data-stu-id="59cca-110">If the function is successful, the return value is a pointer to the frame.</span></span>

<span data-ttu-id="59cca-111">Si la fonction échoue, la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="59cca-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="59cca-112">Notes</span><span class="sxs-lookup"><span data-stu-id="59cca-112">Remarks</span></span>

<span data-ttu-id="59cca-113">La fonction **GetFrameFromFrameHandle** récupère les données qui ne peuvent pas être récupérées par les autres fonctions d’assistance fournies par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="59cca-113">The **GetFrameFromFrameHandle** function retrieves data that cannot be retrieved by the other helper functions that Network Monitor provides.</span></span> <span data-ttu-id="59cca-114">Utilisez les fonctions suivantes dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="59cca-114">Use the following functions whenever possible.</span></span>

<dl>

[<span data-ttu-id="59cca-115">**GetFrameDstAddressOffset**</span><span class="sxs-lookup"><span data-stu-id="59cca-115">**GetFrameDstAddressOffset**</span></span>](getframedstaddressoffset.md)  
[<span data-ttu-id="59cca-116">**GetFrameSrcAddressOffset**</span><span class="sxs-lookup"><span data-stu-id="59cca-116">**GetFrameSrcAddressOffset**</span></span>](getframesrcaddressoffset.md)  
[<span data-ttu-id="59cca-117">**GetFrameCaptureHandle**</span><span class="sxs-lookup"><span data-stu-id="59cca-117">**GetFrameCaptureHandle**</span></span>](getframecapturehandle.md)  
[<span data-ttu-id="59cca-118">**GetFrameDestAddress**</span><span class="sxs-lookup"><span data-stu-id="59cca-118">**GetFrameDestAddress**</span></span>](getframedestaddress.md)  
[<span data-ttu-id="59cca-119">**GetFrameSourceAddress**</span><span class="sxs-lookup"><span data-stu-id="59cca-119">**GetFrameSourceAddress**</span></span>](getframesourceaddress.md)  
[<span data-ttu-id="59cca-120">**GetFrameMacHeaderLength**</span><span class="sxs-lookup"><span data-stu-id="59cca-120">**GetFrameMacHeaderLength**</span></span>](getframemacheaderlength.md)  
[<span data-ttu-id="59cca-121">**GetFrameLength**</span><span class="sxs-lookup"><span data-stu-id="59cca-121">**GetFrameLength**</span></span>](getframelength.md)  
[<span data-ttu-id="59cca-122">**GetFrameStoredLength**</span><span class="sxs-lookup"><span data-stu-id="59cca-122">**GetFrameStoredLength**</span></span>](getframestoredlength.md)  
[<span data-ttu-id="59cca-123">**GetFrameMacType**</span><span class="sxs-lookup"><span data-stu-id="59cca-123">**GetFrameMacType**</span></span>](getframemactype.md)  
[<span data-ttu-id="59cca-124">**GetFrameNumber**</span><span class="sxs-lookup"><span data-stu-id="59cca-124">**GetFrameNumber**</span></span>](getframenumber.md)  
[<span data-ttu-id="59cca-125">**GetFrameTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="59cca-125">**GetFrameTimeStamp**</span></span>](getframetimestamp.md)  
</dl>

<span data-ttu-id="59cca-126">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameFromFrameHandle** .</span><span class="sxs-lookup"><span data-stu-id="59cca-126">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameFromFrameHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="59cca-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59cca-127">Requirements</span></span>



| <span data-ttu-id="59cca-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59cca-128">Requirement</span></span> | <span data-ttu-id="59cca-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="59cca-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="59cca-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59cca-130">Minimum supported client</span></span><br/> | <span data-ttu-id="59cca-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59cca-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="59cca-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59cca-132">Minimum supported server</span></span><br/> | <span data-ttu-id="59cca-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59cca-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="59cca-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="59cca-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="59cca-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="59cca-135"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="59cca-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59cca-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="59cca-137"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59cca-137"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="59cca-138">DLL</span><span class="sxs-lookup"><span data-stu-id="59cca-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59cca-139"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59cca-139"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





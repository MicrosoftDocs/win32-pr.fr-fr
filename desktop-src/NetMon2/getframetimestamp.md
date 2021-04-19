---
description: La fonction GetFrameTimeStamp retourne l’horodatage d’un frame donné.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: GetFrameTimeStamp, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522019"
---
# <a name="getframetimestamp-function"></a><span data-ttu-id="17048-103">GetFrameTimeStamp fonction)</span><span class="sxs-lookup"><span data-stu-id="17048-103">GetFrameTimeStamp function</span></span>

<span data-ttu-id="17048-104">La fonction **GetFrameTimeStamp** retourne l’horodatage d’un frame donné.</span><span class="sxs-lookup"><span data-stu-id="17048-104">The **GetFrameTimeStamp** function returns the time stamp of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="17048-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17048-105">Syntax</span></span>


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="17048-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17048-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17048-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17048-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17048-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="17048-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17048-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17048-109">Return value</span></span>

<span data-ttu-id="17048-110">Si la fonction réussit, la valeur de retour est l’horodatage du frame en microsecondes.</span><span class="sxs-lookup"><span data-stu-id="17048-110">If the function is successful, the return value is the time stamp of the frame   in microseconds.</span></span>

<span data-ttu-id="17048-111">Si la fonction échoue, la valeur de retour est moins un (-1).</span><span class="sxs-lookup"><span data-stu-id="17048-111">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="17048-112">Notes</span><span class="sxs-lookup"><span data-stu-id="17048-112">Remarks</span></span>

<span data-ttu-id="17048-113">La fonction **GetFrameTimeStamp** retourne un horodatage qui indique le temps écoulé entre le début du processus de capture et l’enregistrement du frame.</span><span class="sxs-lookup"><span data-stu-id="17048-113">The **GetFrameTimeStamp** function returns a time stamp that shows the elapsed time between the start of the capture process, and the recording of the frame.</span></span>

<span data-ttu-id="17048-114">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="17048-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="17048-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17048-115">Requirements</span></span>



| <span data-ttu-id="17048-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17048-116">Requirement</span></span> | <span data-ttu-id="17048-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="17048-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17048-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17048-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17048-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17048-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="17048-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17048-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17048-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17048-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="17048-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="17048-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="17048-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="17048-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="17048-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17048-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="17048-125"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17048-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="17048-126">DLL</span><span class="sxs-lookup"><span data-stu-id="17048-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17048-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17048-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





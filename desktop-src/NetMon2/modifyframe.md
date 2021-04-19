---
description: La fonction ModifyFrame modifie un frame existant avec les nouvelles données.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: ModifyFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544689"
---
# <a name="modifyframe-function"></a><span data-ttu-id="7572c-103">ModifyFrame fonction)</span><span class="sxs-lookup"><span data-stu-id="7572c-103">ModifyFrame function</span></span>

<span data-ttu-id="7572c-104">La fonction **ModifyFrame** modifie un frame existant avec les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="7572c-104">The **ModifyFrame** function alters an existing frame with new data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7572c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7572c-105">Syntax</span></span>


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="7572c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7572c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7572c-107">*hCapture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7572c-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7572c-108">Handle de la capture.</span><span class="sxs-lookup"><span data-stu-id="7572c-108">Handle to the capture.</span></span> <span data-ttu-id="7572c-109">Pour plus d’informations sur l’obtention du descripteur de capture, consultez la section Notes de cette rubrique **ModifyFrame** .</span><span class="sxs-lookup"><span data-stu-id="7572c-109">For information about obtaining the capture handle, see the Remarks section of this **ModifyFrame** topic.</span></span>

</dd> <dt>

<span data-ttu-id="7572c-110">*FrameNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7572c-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7572c-111">Numéro d’index de la trame.</span><span class="sxs-lookup"><span data-stu-id="7572c-111">Frame index number.</span></span>

</dd> <dt>

<span data-ttu-id="7572c-112">*FrameData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7572c-112">*FrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7572c-113">Pointeur vers un tableau d’octets qui contient les nouvelles données de frame.</span><span class="sxs-lookup"><span data-stu-id="7572c-113">Pointer to an array of bytes that contain the new frame data.</span></span>

</dd> <dt>

<span data-ttu-id="7572c-114">*FrameLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7572c-114">*FrameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7572c-115">Longueur des nouvelles données, en octets.</span><span class="sxs-lookup"><span data-stu-id="7572c-115">Length of the new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7572c-116">*Horodateur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7572c-116">*TimeStamp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7572c-117">Horodatage indiquant la date de modification du frame.</span><span class="sxs-lookup"><span data-stu-id="7572c-117">Time stamp indicating when the frame was modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7572c-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7572c-118">Return value</span></span>

<span data-ttu-id="7572c-119">Si la fonction réussit, la valeur de retour est un handle vers un nouveau Frame.</span><span class="sxs-lookup"><span data-stu-id="7572c-119">If the function is successful, the return value is a handle to a new frame.</span></span>

<span data-ttu-id="7572c-120">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="7572c-120">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7572c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7572c-121">Remarks</span></span>

<span data-ttu-id="7572c-122">Si l’appel réussit, la fonction **ModifyFrame** détruit le frame d’origine.</span><span class="sxs-lookup"><span data-stu-id="7572c-122">If the call is successful, the **ModifyFrame** function destroys the original frame.</span></span>

<span data-ttu-id="7572c-123">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **ModifyFrame** .</span><span class="sxs-lookup"><span data-stu-id="7572c-123">[*Experts*](e.md) and [*parsers*](p.md) can call the **ModifyFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7572c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7572c-124">Requirements</span></span>



| <span data-ttu-id="7572c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7572c-125">Requirement</span></span> | <span data-ttu-id="7572c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7572c-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7572c-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7572c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7572c-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7572c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7572c-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7572c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7572c-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7572c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7572c-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="7572c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7572c-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7572c-132"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7572c-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7572c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="7572c-134"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7572c-134"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7572c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7572c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7572c-136"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7572c-136"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





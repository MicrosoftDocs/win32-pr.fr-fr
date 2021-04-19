---
description: La fonction GetEnabledProtocols retourne une table de tous les protocoles marqués comme activés.
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: GetEnabledProtocols, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 284d6c87bf5a3b26d6c3f379a710966be21006d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516834"
---
# <a name="getenabledprotocols-function"></a><span data-ttu-id="3cb36-103">GetEnabledProtocols fonction)</span><span class="sxs-lookup"><span data-stu-id="3cb36-103">GetEnabledProtocols function</span></span>

<span data-ttu-id="3cb36-104">La fonction **GetEnabledProtocols** retourne une table de tous les protocoles marqués comme activés.</span><span class="sxs-lookup"><span data-stu-id="3cb36-104">The **GetEnabledProtocols** function returns a table of all protocols that are marked Enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb36-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cb36-105">Syntax</span></span>


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="3cb36-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cb36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb36-107">*hCapture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3cb36-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb36-108">Handle de la capture.</span><span class="sxs-lookup"><span data-stu-id="3cb36-108">Handle to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb36-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3cb36-109">Return value</span></span>

<span data-ttu-id="3cb36-110">Si la fonction réussit, la valeur de retour est un pointeur vers une structure [PROTOCOLTABLE](protocoltable.md) qui répertorie tous les Protocoles activés dans la capture.</span><span class="sxs-lookup"><span data-stu-id="3cb36-110">If the function is successful, the return value is a pointer to a [PROTOCOLTABLE](protocoltable.md) structure that lists all the enabled protocols in the capture.</span></span>

<span data-ttu-id="3cb36-111">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="3cb36-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb36-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3cb36-112">Remarks</span></span>

<span data-ttu-id="3cb36-113">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetEnabledProtocols** .</span><span class="sxs-lookup"><span data-stu-id="3cb36-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetEnabledProtocols** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb36-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cb36-114">Requirements</span></span>



| <span data-ttu-id="3cb36-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cb36-115">Requirement</span></span> | <span data-ttu-id="3cb36-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cb36-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb36-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cb36-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb36-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cb36-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3cb36-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cb36-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb36-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cb36-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3cb36-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3cb36-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cb36-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cb36-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="3cb36-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3cb36-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3cb36-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cb36-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3cb36-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3cb36-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cb36-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cb36-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb36-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cb36-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb36-128">PROTOCOLTABLE</span><span class="sxs-lookup"><span data-stu-id="3cb36-128">PROTOCOLTABLE</span></span>](protocoltable.md)
</dt> </dl>

 

 





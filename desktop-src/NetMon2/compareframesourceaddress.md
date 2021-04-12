---
description: La fonction CompareFrameSourceAddress compare une adresse à l’adresse source d’un frame.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: CompareFrameSourceAddress, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204177"
---
# <a name="compareframesourceaddress-function"></a><span data-ttu-id="88557-103">CompareFrameSourceAddress fonction)</span><span class="sxs-lookup"><span data-stu-id="88557-103">CompareFrameSourceAddress function</span></span>

<span data-ttu-id="88557-104">La fonction **CompareFrameSourceAddress** compare une adresse à l’adresse source d’un frame.</span><span class="sxs-lookup"><span data-stu-id="88557-104">The **CompareFrameSourceAddress** function compares an address to the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="88557-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88557-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="88557-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88557-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88557-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="88557-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88557-108">Handle vers un frame.</span><span class="sxs-lookup"><span data-stu-id="88557-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="88557-109">*lpAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="88557-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88557-110">Pointeur vers une adresse.</span><span class="sxs-lookup"><span data-stu-id="88557-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88557-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88557-111">Return value</span></span>

<span data-ttu-id="88557-112">Si les adresses sont identiques, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="88557-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="88557-113">Si les adresses ne sont pas les mêmes, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="88557-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="88557-114">Notes</span><span class="sxs-lookup"><span data-stu-id="88557-114">Remarks</span></span>

<span data-ttu-id="88557-115">Pour que la fonction **CompareFrameSourceAddress** aboutisse, le type d’adresse source doit correspondre au type d’adresse spécifié dans le paramètre *lpAddress* .</span><span class="sxs-lookup"><span data-stu-id="88557-115">For the **CompareFrameSourceAddress** function to succeed, the source address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="88557-116">Moniteur réseau fournit deux autres fonctions pour comparer des adresses : [CompareFrameDestAddress](compareframedestaddress.md) et [CompareAddresses](compareaddresses.md).</span><span class="sxs-lookup"><span data-stu-id="88557-116">Network Monitor provides two other functions for comparing addresses: [CompareFrameDestAddress](compareframedestaddress.md) and [CompareAddresses](compareaddresses.md).</span></span> <span data-ttu-id="88557-117">La fonction **CompareFrameDestAddress** compare une adresse donnée à l’adresse de destination du frame, et la fonction **CompareAddress** compare deux adresses données.</span><span class="sxs-lookup"><span data-stu-id="88557-117">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="88557-118">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **CompareFrameSourceAddress** .</span><span class="sxs-lookup"><span data-stu-id="88557-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameSourceAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="88557-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88557-119">Requirements</span></span>



| <span data-ttu-id="88557-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88557-120">Requirement</span></span> | <span data-ttu-id="88557-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="88557-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="88557-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88557-122">Minimum supported client</span></span><br/> | <span data-ttu-id="88557-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88557-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="88557-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88557-124">Minimum supported server</span></span><br/> | <span data-ttu-id="88557-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88557-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="88557-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="88557-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="88557-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="88557-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="88557-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="88557-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="88557-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88557-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="88557-130">DLL</span><span class="sxs-lookup"><span data-stu-id="88557-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88557-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88557-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88557-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88557-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88557-133">CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="88557-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="88557-134">CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="88557-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> </dl>

 

 





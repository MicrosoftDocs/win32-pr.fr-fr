---
description: La fonction CompareFrameDestAddress compare une adresse à l’adresse de destination d’un frame.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: CompareFrameDestAddress, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864797"
---
# <a name="compareframedestaddress-function"></a><span data-ttu-id="7ad4d-103">CompareFrameDestAddress fonction)</span><span class="sxs-lookup"><span data-stu-id="7ad4d-103">CompareFrameDestAddress function</span></span>

<span data-ttu-id="7ad4d-104">La fonction **CompareFrameDestAddress** compare une adresse à l’adresse de destination d’un frame.</span><span class="sxs-lookup"><span data-stu-id="7ad4d-104">The **CompareFrameDestAddress** function compares an address to the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ad4d-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="7ad4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ad4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ad4d-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ad4d-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad4d-108">Handle vers un frame.</span><span class="sxs-lookup"><span data-stu-id="7ad4d-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="7ad4d-109">*lpAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ad4d-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad4d-110">Pointeur vers une adresse.</span><span class="sxs-lookup"><span data-stu-id="7ad4d-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ad4d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ad4d-111">Return value</span></span>

<span data-ttu-id="7ad4d-112">Si les adresses sont identiques, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="7ad4d-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="7ad4d-113">Si les adresses ne sont pas les mêmes, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="7ad4d-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ad4d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7ad4d-114">Remarks</span></span>

<span data-ttu-id="7ad4d-115">Pour que la fonction **CompareFrameDestAddress** retourne correctement, le type d’adresse de destination doit correspondre au type d’adresse spécifié dans le paramètre *lpAddress* .</span><span class="sxs-lookup"><span data-stu-id="7ad4d-115">For the **CompareFrameDestAddress** function to return successfully, the destination address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="7ad4d-116">Moniteur réseau fournit deux autres fonctions, [CompareFrameSourceAddress](compareframesourceaddress.md) et [CompareAddresses](compareaddresses.md), que vous pouvez utiliser pour comparer des adresses.</span><span class="sxs-lookup"><span data-stu-id="7ad4d-116">Network Monitor provides two other functions, [CompareFrameSourceAddress](compareframesourceaddress.md) and [CompareAddresses](compareaddresses.md), which you can use to compare addresses.</span></span> <span data-ttu-id="7ad4d-117">La fonction **CompareFrameSourceAddress** compare une adresse donnée à l’adresse source du frame, et la fonction **CompareAddress** compare deux adresses données.</span><span class="sxs-lookup"><span data-stu-id="7ad4d-117">The **CompareFrameSourceAddress** function compares a given address to the frame's source address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="7ad4d-118">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **CompareFrameDestAddress** .</span><span class="sxs-lookup"><span data-stu-id="7ad4d-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameDestAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ad4d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ad4d-119">Requirements</span></span>



| <span data-ttu-id="7ad4d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ad4d-120">Requirement</span></span> | <span data-ttu-id="7ad4d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ad4d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad4d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ad4d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ad4d-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ad4d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7ad4d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ad4d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ad4d-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ad4d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7ad4d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ad4d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ad4d-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad4d-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7ad4d-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ad4d-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ad4d-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ad4d-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ad4d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7ad4d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ad4d-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ad4d-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ad4d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ad4d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad4d-133">CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="7ad4d-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="7ad4d-134">CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="7ad4d-134">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 





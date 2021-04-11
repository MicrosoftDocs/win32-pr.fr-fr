---
title: WTSLISTENERNAME (WtsApi32. h)
description: Représente le nom d’un Services Bureau à distance écouteurs sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384952"
---
# <a name="wtslistenername"></a><span data-ttu-id="05101-109">WTSLISTENERNAME</span><span class="sxs-lookup"><span data-stu-id="05101-109">WTSLISTENERNAME</span></span>

<span data-ttu-id="05101-110">Représente le nom d’un Services Bureau à distance écouteurs sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="05101-110">Represents the name of a Remote Desktop Services listeners on a Remote Desktop Session Host (RD Session Host) server.</span></span>


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

<span data-ttu-id="05101-111">**WTSLISTENERNAMEW**</span><span class="sxs-lookup"><span data-stu-id="05101-111">**WTSLISTENERNAMEW**</span></span>
</dt> <dd>

<span data-ttu-id="05101-112">Nom Unicode de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="05101-112">The Unicode name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="05101-113">**WTSLISTENERNAMEA**</span><span class="sxs-lookup"><span data-stu-id="05101-113">**WTSLISTENERNAMEA**</span></span>
</dt> <dd>

<span data-ttu-id="05101-114">Pointeur vers le nom ANSI de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="05101-114">A pointer to the ANSI name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="05101-115">**WTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="05101-115">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="05101-116">Nom de l'écouteur.</span><span class="sxs-lookup"><span data-stu-id="05101-116">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="05101-117">**PWTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="05101-117">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="05101-118">Pointeur vers le nom de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="05101-118">A pointer to the name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="05101-119">**WTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="05101-119">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="05101-120">Nom de l'écouteur.</span><span class="sxs-lookup"><span data-stu-id="05101-120">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="05101-121">**PWTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="05101-121">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="05101-122">Pointeur vers le nom de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="05101-122">A pointer to the name of the listener.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05101-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05101-123">Requirements</span></span>



| <span data-ttu-id="05101-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05101-124">Requirement</span></span> | <span data-ttu-id="05101-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="05101-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05101-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05101-126">Minimum supported client</span></span><br/> | <span data-ttu-id="05101-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05101-127">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="05101-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05101-128">Minimum supported server</span></span><br/> | <span data-ttu-id="05101-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05101-129">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="05101-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="05101-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="05101-131"><dt>WtsApi32. h</dt></span><span class="sxs-lookup"><span data-stu-id="05101-131"><dt>WtsApi32.h</dt></span></span> </dl> |



 

 






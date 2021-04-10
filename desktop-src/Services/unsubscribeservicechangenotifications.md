---
description: Annule l’abonnement des notifications de modification de l’état du service.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: UnsubscribeServiceChangeNotifications, fonction (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866626"
---
# <a name="unsubscribeservicechangenotifications-function"></a><span data-ttu-id="4a2ea-103">UnsubscribeServiceChangeNotifications fonction)</span><span class="sxs-lookup"><span data-stu-id="4a2ea-103">UnsubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="4a2ea-104">Annule l’abonnement des notifications de modification de l’état du service.</span><span class="sxs-lookup"><span data-stu-id="4a2ea-104">Unsubscribes from service status change notifications.</span></span> <span data-ttu-id="4a2ea-105">Cette fonction utilise les abonnements retournés par [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span><span class="sxs-lookup"><span data-stu-id="4a2ea-105">This function uses subscriptions returned by [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2ea-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a2ea-106">Syntax</span></span>


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="4a2ea-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a2ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a2ea-108">*pSubscription* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a2ea-108">*pSubscription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2ea-109">Pointeur vers l’abonnement à désabonner.</span><span class="sxs-lookup"><span data-stu-id="4a2ea-109">A pointer to the subscription to be unsubscribed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a2ea-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4a2ea-110">Return value</span></span>

<span data-ttu-id="4a2ea-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4a2ea-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a2ea-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4a2ea-112">Remarks</span></span>

<span data-ttu-id="4a2ea-113">**UnsubscribeServiceChangeNotifications** n’est pas retourné tant que les rappels in-process en attente ne sont pas terminés.</span><span class="sxs-lookup"><span data-stu-id="4a2ea-113">**UnsubscribeServiceChangeNotifications** does not return until outstanding in-process callbacks are complete.</span></span> <span data-ttu-id="4a2ea-114">Par conséquent, vous ne pouvez pas appeler **UnsubscribeServiceChangeNotifications** dans le rappel sans provoquer de blocage.</span><span class="sxs-lookup"><span data-stu-id="4a2ea-114">So, you cannot call **UnsubscribeServiceChangeNotifications** within the callback without causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a2ea-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a2ea-115">Requirements</span></span>



| <span data-ttu-id="4a2ea-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a2ea-116">Requirement</span></span> | <span data-ttu-id="4a2ea-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a2ea-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2ea-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a2ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2ea-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a2ea-119">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4a2ea-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a2ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2ea-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a2ea-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4a2ea-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a2ea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a2ea-123"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2ea-123"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a2ea-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4a2ea-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a2ea-125"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a2ea-125"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2ea-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a2ea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2ea-127">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="4a2ea-127">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="4a2ea-128">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="4a2ea-128">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="4a2ea-129">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="4a2ea-129">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="4a2ea-130">**SubscribeServiceChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="4a2ea-130">**SubscribeServiceChangeNotifications**</span></span>](subscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="4a2ea-131">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="4a2ea-131">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 





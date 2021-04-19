---
description: Indique la durée pendant laquelle un composant prend le traitement de chaque échantillon.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d97514b4d2851f619f89f42e644766d50b7d25f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528601"
---
# <a name="ec_processing_latency"></a><span data-ttu-id="277cb-103">\_latence de traitement ce \_</span><span class="sxs-lookup"><span data-stu-id="277cb-103">EC\_PROCESSING\_LATENCY</span></span>

<span data-ttu-id="277cb-104">Indique la durée pendant laquelle un composant prend le traitement de chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="277cb-104">Indicates the amount of time that a component is taking to process each sample.</span></span>

## <a name="parameters"></a><span data-ttu-id="277cb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="277cb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="277cb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="277cb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="277cb-107">(**const Reference \_ Time**) durée de \* traitement de chaque échantillon, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="277cb-107">(**const REFERENCE\_TIME**\*) The amount of time to process each sample, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="277cb-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="277cb-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="277cb-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="277cb-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="277cb-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="277cb-110">Default Action</span></span>

<span data-ttu-id="277cb-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="277cb-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="277cb-112">Notes</span><span class="sxs-lookup"><span data-stu-id="277cb-112">Remarks</span></span>

<span data-ttu-id="277cb-113">Un présentateur pour le filtre EVR ( [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) ) peut envoyer ce message à EVR pour notifier le EVR de la latence de traitement du présentateur.</span><span class="sxs-lookup"><span data-stu-id="277cb-113">A presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR to notify the EVR about the presenter's processing latency.</span></span>

## <a name="requirements"></a><span data-ttu-id="277cb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="277cb-114">Requirements</span></span>



| <span data-ttu-id="277cb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="277cb-115">Requirement</span></span> | <span data-ttu-id="277cb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="277cb-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="277cb-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="277cb-117">Header</span></span><br/> | <dl> <span data-ttu-id="277cb-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="277cb-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="277cb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="277cb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277cb-120">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="277cb-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="277cb-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="277cb-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Le fournisseur d’horloge a été déconnecté.
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: EC_CLOCK_UNSET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ead35d89eee94bbffb38a96f658ccb2bb6e6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543802"
---
# <a name="ec_clock_unset"></a><span data-ttu-id="de4ec-103">horloge EC non \_ \_ définie</span><span class="sxs-lookup"><span data-stu-id="de4ec-103">EC\_CLOCK\_UNSET</span></span>

<span data-ttu-id="de4ec-104">Le fournisseur d’horloge a été déconnecté.</span><span class="sxs-lookup"><span data-stu-id="de4ec-104">The clock provider was disconnected.</span></span>

## <a name="parameters"></a><span data-ttu-id="de4ec-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de4ec-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de4ec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="de4ec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="de4ec-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="de4ec-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="de4ec-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="de4ec-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="de4ec-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="de4ec-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="de4ec-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="de4ec-110">Default Action</span></span>

<span data-ttu-id="de4ec-111">Le gestionnaire de graphe de filtre choisit une nouvelle horloge de référence lors de la prochaine pause ou de la commande Run.</span><span class="sxs-lookup"><span data-stu-id="de4ec-111">The Filter Graph Manager chooses a new reference clock on the next pause or run command.</span></span> <span data-ttu-id="de4ec-112">Il transfère également l’événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="de4ec-112">It also forwards the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="de4ec-113">Notes</span><span class="sxs-lookup"><span data-stu-id="de4ec-113">Remarks</span></span>

<span data-ttu-id="de4ec-114">KSProxy signale cet événement lorsque le pin d’un filtre fournissant des horloges est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="de4ec-114">KSProxy signals this event when the pin of a clock-providing filter is disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="de4ec-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de4ec-115">Requirements</span></span>



| <span data-ttu-id="de4ec-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de4ec-116">Requirement</span></span> | <span data-ttu-id="de4ec-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="de4ec-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de4ec-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="de4ec-118">Header</span></span><br/> | <dl> <span data-ttu-id="de4ec-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="de4ec-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de4ec-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de4ec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4ec-121">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="de4ec-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="de4ec-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="de4ec-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





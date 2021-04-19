---
description: Le convertisseur vidéo a été détruit ou supprimé du graphique.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532541"
---
# <a name="ec_window_destroyed"></a><span data-ttu-id="2e2a2-103">\_fenêtre EC \_ détruite</span><span class="sxs-lookup"><span data-stu-id="2e2a2-103">EC\_WINDOW\_DESTROYED</span></span>

<span data-ttu-id="2e2a2-104">Le convertisseur vidéo a été détruit ou supprimé du graphique.</span><span class="sxs-lookup"><span data-stu-id="2e2a2-104">The video renderer was destroyed or removed from the graph.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e2a2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e2a2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e2a2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2e2a2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2e2a2-107">(**IUnknown** \* ) Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="2e2a2-107">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2e2a2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2e2a2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2e2a2-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="2e2a2-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="2e2a2-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="2e2a2-110">Default Action</span></span>

<span data-ttu-id="2e2a2-111">Le gestionnaire de graphes de filtre libère cette fenêtre comme le focus, via l’interface [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="2e2a2-111">The filter graph manager releases this window as the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="2e2a2-112">Elle n’envoie pas la notification d’événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="2e2a2-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2a2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2e2a2-113">Remarks</span></span>

<span data-ttu-id="2e2a2-114">Le convertisseur vidéo envoie cet événement lorsqu’il quitte le graphique de filtre, dans sa méthode [**IBaseFilter :: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .</span><span class="sxs-lookup"><span data-stu-id="2e2a2-114">The video renderer sends this event when it leaves the filter graph, in its [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="2e2a2-115">(L’envoi de l’événement lorsque le filtre est détruit peut être trop tard, car, à ce stade, le gestionnaire de graphique de filtre peut également être détruit.)</span><span class="sxs-lookup"><span data-stu-id="2e2a2-115">(Sending the event when the filter is destroyed might be too late, because at that point the filter graph manager might also be destroyed.)</span></span>

<span data-ttu-id="2e2a2-116">Cet événement permet à d’autres filtres d’acquérir des ressources qui dépendent du focus de la fenêtre, tels que les périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="2e2a2-116">This event enables other filters to acquire resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2a2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e2a2-117">Requirements</span></span>



| <span data-ttu-id="2e2a2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e2a2-118">Requirement</span></span> | <span data-ttu-id="2e2a2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e2a2-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2a2-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e2a2-120">Header</span></span><br/> | <dl> <span data-ttu-id="2e2a2-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2a2-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e2a2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e2a2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2a2-123">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="2e2a2-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2e2a2-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="2e2a2-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Toutes les données d’un flux de données particulier ont été rendues.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536007"
---
# <a name="ec_complete"></a><span data-ttu-id="f23ec-103">EC \_ complet</span><span class="sxs-lookup"><span data-stu-id="f23ec-103">EC\_COMPLETE</span></span>

<span data-ttu-id="f23ec-104">Toutes les données d’un flux de données particulier ont été rendues.</span><span class="sxs-lookup"><span data-stu-id="f23ec-104">All data from a particular stream has been rendered.</span></span>

## <a name="parameters"></a><span data-ttu-id="f23ec-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f23ec-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f23ec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f23ec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f23ec-107">(**HRESULT**) État du flux à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f23ec-107">(**HRESULT**) Status of the stream on completion.</span></span> <span data-ttu-id="f23ec-108">Si aucune erreur ne s’est produite lors de la lecture, la valeur est \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f23ec-108">If no errors occurred during playback, the value is S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="f23ec-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f23ec-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f23ec-110">(**IUnknown** \* ) Zéro, ou un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du convertisseur.</span><span class="sxs-lookup"><span data-stu-id="f23ec-110">(**IUnknown**\*) Zero, or a pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="f23ec-111">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="f23ec-111">Default Action</span></span>

<span data-ttu-id="f23ec-112">Par défaut, le gestionnaire de graphes de filtre ne transfère pas cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="f23ec-112">By default, the filter graph manager does not forward this event to the application.</span></span> <span data-ttu-id="f23ec-113">Toutefois, une fois que tous les flux du graphique ont été rapportés par la **communauté \_**, le gestionnaire de graphes de filtre publie un événement **ce \_ complet** distinct dans l’application.</span><span class="sxs-lookup"><span data-stu-id="f23ec-113">However, after all the streams in the graph report **EC\_COMPLETE**, the filter graph manager posts a separate **EC\_COMPLETE** event to the application.</span></span>

<span data-ttu-id="f23ec-114">Si l’action par défaut est désactivée pour cet événement, l’application reçoit tous les événements d' **\_ achèvement ce** des convertisseurs.</span><span class="sxs-lookup"><span data-stu-id="f23ec-114">If the default action is disabled for this event, the application receives all of the **EC\_COMPLETE** events from the renderers.</span></span>

## <a name="remarks"></a><span data-ttu-id="f23ec-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f23ec-115">Remarks</span></span>

<span data-ttu-id="f23ec-116">Un filtre de convertisseur envoie cet événement lorsqu’il reçoit une notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="f23ec-116">A renderer filter sends this event when it receives an end-of-stream notice.</span></span> <span data-ttu-id="f23ec-117">(La fin de flux est signalée par le biais de la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .) Le filtre envoie exactement un événement **EC \_ Complete** pour chaque flux.</span><span class="sxs-lookup"><span data-stu-id="f23ec-117">(End-of-stream is signaled through the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.) The filter sends exactly one **EC\_COMPLETE** event for each stream.</span></span> <span data-ttu-id="f23ec-118">Le filtre doit traiter tous les échantillons en attente avant d’envoyer l’événement.</span><span class="sxs-lookup"><span data-stu-id="f23ec-118">The filter must process any pending samples before it sends the event.</span></span> <span data-ttu-id="f23ec-119">L’arrêt d’un convertisseur réinitialise tout état de fin de flux mis en cache.</span><span class="sxs-lookup"><span data-stu-id="f23ec-119">Stopping a renderer resets any end-of-stream state that was cached.</span></span>

<span data-ttu-id="f23ec-120">Si le convertisseur est suspendu, il n’envoie pas la méthode **EC \_ Complete** tant que la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="f23ec-120">If the renderer is paused, it does not send **EC\_COMPLETE** until the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method is called.</span></span> <span data-ttu-id="f23ec-121">En outre, il continue à envoyer des événements de type « **EC \_ complet** » pour chaque transition de pause à exécuter, jusqu’à ce que le filtre soit arrêté ou vidé.</span><span class="sxs-lookup"><span data-stu-id="f23ec-121">Furthermore, it continues to send **EC\_COMPLETE** events for each transition from pause to run, until the filter is either stopped or flushed.</span></span>

<span data-ttu-id="f23ec-122">Les filtres définissent le paramètre *lParam2* sur un pointeur [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="f23ec-122">Filters set the *lParam2* parameter to an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="f23ec-123">Si l’action par défaut est activée, le gestionnaire de graphique de filtre définit ce paramètre sur zéro.</span><span class="sxs-lookup"><span data-stu-id="f23ec-123">If the default action is enabled, the filter graph manager sets this parameter to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23ec-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f23ec-124">Requirements</span></span>



| <span data-ttu-id="f23ec-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f23ec-125">Requirement</span></span> | <span data-ttu-id="f23ec-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f23ec-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f23ec-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f23ec-127">Header</span></span><br/> | <dl> <span data-ttu-id="f23ec-128"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="f23ec-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23ec-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f23ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23ec-130">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="f23ec-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f23ec-131">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="f23ec-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="f23ec-132">Autres convertisseurs vidéo</span><span class="sxs-lookup"><span data-stu-id="f23ec-132">Alternative Video Renderers</span></span>](alternative-video-renderers.md)
</dt> </dl>

 

 





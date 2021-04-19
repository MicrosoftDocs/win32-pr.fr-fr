---
description: Un convertisseur vidéo requiert un redessin.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538750"
---
# <a name="ec_repaint"></a><span data-ttu-id="a0957-103">redessin ce \_</span><span class="sxs-lookup"><span data-stu-id="a0957-103">EC\_REPAINT</span></span>

<span data-ttu-id="a0957-104">Un convertisseur vidéo requiert un redessin.</span><span class="sxs-lookup"><span data-stu-id="a0957-104">A video renderer requires a repaint.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0957-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0957-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0957-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a0957-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a0957-107">(**IUnknown** \* ) Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche d’entrée du convertisseur vidéo, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="a0957-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the video renderer's input pin, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0957-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a0957-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a0957-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="a0957-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a0957-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="a0957-110">Default Action</span></span>

<span data-ttu-id="a0957-111">Le paramètre *lParam1* peut spécifier la broche d’entrée du convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="a0957-111">The *lParam1* parameter might specify the video renderer's input pin.</span></span> <span data-ttu-id="a0957-112">Si c’est le cas, le gestionnaire de graphique de filtre recherche la broche de sortie connectée à ce code confidentiel et l’interroge pour l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="a0957-112">If so, the filter graph manager finds the output pin connected to that pin and queries it for the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="a0957-113">Si la broche de sortie prend en charge **IMediaEventSink**, le gestionnaire de graphique de filtre appelle [**IMediaEventSink :: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) avec le \_ code d’événement de redessin ce.</span><span class="sxs-lookup"><span data-stu-id="a0957-113">If the output pin supports **IMediaEventSink**, the filter graph manager calls [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) with the EC\_REPAINT event code.</span></span> <span data-ttu-id="a0957-114">Cela donne au filtre en amont la possibilité de renvoyer le dernier échantillon.</span><span class="sxs-lookup"><span data-stu-id="a0957-114">This gives the upstream filter the opportunity to re-send the last sample.</span></span>

<span data-ttu-id="a0957-115">Si *lParam1* a la **valeur null**, ou si le code PIN ne prend pas en charge [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), ou si la méthode [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) échoue, le gestionnaire de graphique de filtre gère l' \_ événement de redessin ce par lui-même.</span><span class="sxs-lookup"><span data-stu-id="a0957-115">If *lParam1* is **NULL**, or if the pin does not support [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), or if the [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method fails, the filter graph manager handles the EC\_REPAINT event by itself.</span></span> <span data-ttu-id="a0957-116">Son comportement dépend de l’état du graphique :</span><span class="sxs-lookup"><span data-stu-id="a0957-116">Its behavior depends on the state of the graph:</span></span>

-   <span data-ttu-id="a0957-117">Running : ignore l’événement.</span><span class="sxs-lookup"><span data-stu-id="a0957-117">Running: Ignores the event.</span></span> <span data-ttu-id="a0957-118">(Le convertisseur recevra l’exemple suivant dans le flux.)</span><span class="sxs-lookup"><span data-stu-id="a0957-118">(The renderer will receive the next sample in the stream.)</span></span>
-   <span data-ttu-id="a0957-119">Paused : recherche le graphique à son emplacement actuel, ce qui a pour effet de vider le filtre et de remettre les données en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="a0957-119">Paused: Seeks the graph to its current location, thereby flushing the filter and re-queuing the data.</span></span>
-   <span data-ttu-id="a0957-120">Arrêté : suspend et arrête le graphique, ce qui a pour effet de replacer en file d’attente les données.</span><span class="sxs-lookup"><span data-stu-id="a0957-120">Stopped: Pauses and stops the graph, thereby re-queuing the data.</span></span>

<span data-ttu-id="a0957-121">Par défaut, le gestionnaire de graphes de filtre ne transmet pas cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="a0957-121">By default, the filter graph manager does not pass this event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0957-122">Notes</span><span class="sxs-lookup"><span data-stu-id="a0957-122">Remarks</span></span>

<span data-ttu-id="a0957-123">Les convertisseurs vidéo envoient ce message lorsqu’ils reçoivent un message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) et n’ont pas de données à afficher.</span><span class="sxs-lookup"><span data-stu-id="a0957-123">Video renderers send this message when they receive a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message and have no data to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0957-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0957-124">Requirements</span></span>



| <span data-ttu-id="a0957-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0957-125">Requirement</span></span> | <span data-ttu-id="a0957-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0957-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a0957-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0957-127">Header</span></span><br/> | <dl> <span data-ttu-id="a0957-128"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0957-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0957-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0957-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0957-130">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="a0957-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a0957-131">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0957-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 


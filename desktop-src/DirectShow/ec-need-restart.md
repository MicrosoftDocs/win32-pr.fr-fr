---
description: Un filtre demande que le graphique soit redémarré.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527978"
---
# <a name="ec_need_restart"></a><span data-ttu-id="e2ce6-103">redémarrage de l’EC \_ requis \_</span><span class="sxs-lookup"><span data-stu-id="e2ce6-103">EC\_NEED\_RESTART</span></span>

<span data-ttu-id="e2ce6-104">Un filtre demande que le graphique soit redémarré.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-104">A filter is requesting that the graph be restarted.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2ce6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2ce6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2ce6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e2ce6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e2ce6-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="e2ce6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e2ce6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e2ce6-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="e2ce6-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="e2ce6-110">Default Action</span></span>

<span data-ttu-id="e2ce6-111">Le gestionnaire de graphique de filtre met en pause et redémarre le graphique.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-111">The filter graph manager pauses and restarts the graph.</span></span> <span data-ttu-id="e2ce6-112">Elle ne passe pas l’événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-112">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2ce6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e2ce6-113">Remarks</span></span>

<span data-ttu-id="e2ce6-114">Si un filtre rejette un échantillon au milieu d’un flux, le pin amont arrête de fournir des exemples.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-114">If a filter rejects a sample in the middle of a stream, the upstream pin will stop delivering samples.</span></span> <span data-ttu-id="e2ce6-115">Le filtre peut redémarrer le flux en envoyant cet événement.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-115">The filter can restart the stream by sending this event.</span></span> <span data-ttu-id="e2ce6-116">Par exemple, le convertisseur audio peut perdre l’accès au périphérique audio, car une fenêtre vidéo a perdu le focus.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-116">For example, the audio renderer might lose access to the sound device, because a video window has lost focus.</span></span> <span data-ttu-id="e2ce6-117">À ce stade, le convertisseur audio commence à rejeter des exemples.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-117">At that point, the audio renderer starts rejecting samples.</span></span> <span data-ttu-id="e2ce6-118">Lorsqu’il regagne l’accès au périphérique audio, il envoie cet événement pour redémarrer le flux audio.</span><span class="sxs-lookup"><span data-stu-id="e2ce6-118">When it regains access to the sound device, it sends this event to restart the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ce6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2ce6-119">Requirements</span></span>



| <span data-ttu-id="e2ce6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2ce6-120">Requirement</span></span> | <span data-ttu-id="e2ce6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2ce6-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ce6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2ce6-122">Header</span></span><br/> | <dl> <span data-ttu-id="e2ce6-123"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ce6-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2ce6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2ce6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ce6-125">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="e2ce6-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e2ce6-126">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="e2ce6-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





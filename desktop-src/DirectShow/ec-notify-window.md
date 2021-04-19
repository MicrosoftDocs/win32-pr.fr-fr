---
description: Avertit un filtre de la fenêtre du convertisseur vidéo.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541715"
---
# <a name="ec_notify_window"></a><span data-ttu-id="16eb8-103">\_fenêtre EC Notify \_</span><span class="sxs-lookup"><span data-stu-id="16eb8-103">EC\_NOTIFY\_WINDOW</span></span>

<span data-ttu-id="16eb8-104">Avertit un filtre de la fenêtre du convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="16eb8-104">Notifies a filter of the video renderer's window.</span></span>

## <a name="parameters"></a><span data-ttu-id="16eb8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16eb8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16eb8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="16eb8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="16eb8-107">(**HWND**) Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="16eb8-107">(**HWND**) Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="16eb8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="16eb8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="16eb8-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="16eb8-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="16eb8-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="16eb8-110">Default Action</span></span>

<span data-ttu-id="16eb8-111">Cet événement est utilisé en interne par DirectShow.</span><span class="sxs-lookup"><span data-stu-id="16eb8-111">This event is used internally by DirectShow.</span></span> <span data-ttu-id="16eb8-112">Le gestionnaire de graphes de filtre ne transmet pas cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="16eb8-112">The filter graph manager does not pass this event to the application.</span></span> <span data-ttu-id="16eb8-113">Les applications ne peuvent pas remplacer l’action par défaut pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="16eb8-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="16eb8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="16eb8-114">Remarks</span></span>

<span data-ttu-id="16eb8-115">Lorsqu’un convertisseur vidéo est connecté, il vérifie si la broche de sortie en amont prend en charge l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="16eb8-115">When a video renderer is connected, it checks whether the upstream output pin supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="16eb8-116">Si c’est le cas, le convertisseur envoie cet événement au filtre amont.</span><span class="sxs-lookup"><span data-stu-id="16eb8-116">If so, the renderer sends this event to the upstream filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="16eb8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16eb8-117">Requirements</span></span>



| <span data-ttu-id="16eb8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16eb8-118">Requirement</span></span> | <span data-ttu-id="16eb8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="16eb8-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16eb8-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="16eb8-120">Header</span></span><br/> | <dl> <span data-ttu-id="16eb8-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="16eb8-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16eb8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16eb8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16eb8-123">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="16eb8-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="16eb8-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="16eb8-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





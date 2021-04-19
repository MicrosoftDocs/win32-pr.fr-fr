---
description: Un filtre ne reçoit pas suffisamment de données.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537328"
---
# <a name="ec_starvation"></a><span data-ttu-id="9c881-103">\_privation ce</span><span class="sxs-lookup"><span data-stu-id="9c881-103">EC\_STARVATION</span></span>

<span data-ttu-id="9c881-104">Un filtre ne reçoit pas suffisamment de données.</span><span class="sxs-lookup"><span data-stu-id="9c881-104">A filter is not receiving enough data.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c881-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c881-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c881-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9c881-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9c881-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="9c881-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="9c881-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9c881-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9c881-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="9c881-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="9c881-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="9c881-110">Default Action</span></span>

<span data-ttu-id="9c881-111">L’événement n’est pas envoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="9c881-111">The event is not sent to the application.</span></span> <span data-ttu-id="9c881-112">Si le graphique de filtre est en cours d’exécution, le gestionnaire de graphes de filtre interrompt le graphique et attend la fin de la pause.</span><span class="sxs-lookup"><span data-stu-id="9c881-112">If the filter graph is running, the filter graph manager pauses the graph and waits for the pause to complete.</span></span> <span data-ttu-id="9c881-113">Ensuite, il réexécute le graphique.</span><span class="sxs-lookup"><span data-stu-id="9c881-113">Then it runs the graph again.</span></span> <span data-ttu-id="9c881-114">Le filtre qui envoie l’événement ne doit pas terminer sa transition pour être suspendue jusqu’à ce qu’il dispose de suffisamment de données pour reprendre.</span><span class="sxs-lookup"><span data-stu-id="9c881-114">The filter sending the event should not complete its transition to paused until it has enough data to resume.</span></span> <span data-ttu-id="9c881-115">Si le graphique de filtre n’est pas en cours d’exécution, le gestionnaire de graphes de filtres ignore cet événement.</span><span class="sxs-lookup"><span data-stu-id="9c881-115">If the filter graph is not running, the filter graph manager ignores this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c881-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9c881-116">Remarks</span></span>

<span data-ttu-id="9c881-117">Un analyseur ou un filtre source peut envoyer cet événement si l’arrivée de données est trop faible.</span><span class="sxs-lookup"><span data-stu-id="9c881-117">A parser or source filter can send this event if too little data is arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c881-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c881-118">Requirements</span></span>



| <span data-ttu-id="9c881-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c881-119">Requirement</span></span> | <span data-ttu-id="9c881-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c881-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c881-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c881-121">Header</span></span><br/> | <dl> <span data-ttu-id="9c881-122"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c881-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c881-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c881-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c881-124">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="9c881-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9c881-125">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="9c881-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





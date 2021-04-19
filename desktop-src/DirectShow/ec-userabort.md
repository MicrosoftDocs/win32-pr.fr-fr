---
description: L’utilisateur a terminé la lecture.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524023"
---
# <a name="ec_userabort"></a><span data-ttu-id="ea847-103">\_USERABORT EC</span><span class="sxs-lookup"><span data-stu-id="ea847-103">EC\_USERABORT</span></span>

<span data-ttu-id="ea847-104">L’utilisateur a terminé la lecture.</span><span class="sxs-lookup"><span data-stu-id="ea847-104">The user has terminated playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea847-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea847-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea847-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ea847-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ea847-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="ea847-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="ea847-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ea847-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ea847-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="ea847-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ea847-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="ea847-110">Default Action</span></span>

<span data-ttu-id="ea847-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="ea847-111">None.</span></span> <span data-ttu-id="ea847-112">L’application doit décider d’arrêter ou non le graphique.</span><span class="sxs-lookup"><span data-stu-id="ea847-112">The application must decide whether to stop the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea847-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ea847-113">Remarks</span></span>

<span data-ttu-id="ea847-114">Ce code d’événement indique que l’utilisateur a terminé la lecture du graphique normal.</span><span class="sxs-lookup"><span data-stu-id="ea847-114">This event code signals that the user has terminated normal graph playback.</span></span> <span data-ttu-id="ea847-115">Par exemple, les convertisseurs vidéo envoient cet événement si l’utilisateur ferme la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="ea847-115">For example, video renderers send this event if the user closes the video window.</span></span>

<span data-ttu-id="ea847-116">Après l’envoi de cet événement, le filtre doit rejeter tous les exemples et ne pas envoyer d’événements de [**\_ redessin EC**](ec-repaint.md) , jusqu’à ce que le filtre s’arrête et soit réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="ea847-116">After sending this event, the filter should reject all samples and not send any [**EC\_REPAINT**](ec-repaint.md) events, until the filter stops and is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea847-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea847-117">Requirements</span></span>



| <span data-ttu-id="ea847-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea847-118">Requirement</span></span> | <span data-ttu-id="ea847-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea847-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea847-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea847-120">Header</span></span><br/> | <dl> <span data-ttu-id="ea847-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea847-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea847-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea847-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea847-123">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="ea847-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ea847-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="ea847-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





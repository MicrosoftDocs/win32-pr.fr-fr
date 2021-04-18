---
description: Le graphique supprime des exemples, pour le contrôle de la qualité.
ms.assetid: a21fe766-58a5-4851-a282-883374287e18
title: EC_QUALITY_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5752db30c8ad6ed85655948cf2adb9ef7ac8078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540136"
---
# <a name="ec_quality_change"></a><span data-ttu-id="c98ca-103">modification de la \_ qualité ce \_</span><span class="sxs-lookup"><span data-stu-id="c98ca-103">EC\_QUALITY\_CHANGE</span></span>

<span data-ttu-id="c98ca-104">Le graphique supprime des exemples, pour le contrôle de la qualité.</span><span class="sxs-lookup"><span data-stu-id="c98ca-104">The graph is dropping samples, for quality control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c98ca-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c98ca-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c98ca-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c98ca-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c98ca-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="c98ca-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="c98ca-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c98ca-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c98ca-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="c98ca-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c98ca-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="c98ca-110">Default Action</span></span>

<span data-ttu-id="c98ca-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c98ca-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c98ca-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c98ca-112">Remarks</span></span>

<span data-ttu-id="c98ca-113">Un filtre envoie cet événement s’il supprime des exemples en réponse à un message de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="c98ca-113">A filter sends this event if it drops samples in response to a quality control message.</span></span> <span data-ttu-id="c98ca-114">Il envoie l’événement uniquement lorsqu’il ajuste le niveau de qualité, et non pour chaque échantillon qu’il supprime.</span><span class="sxs-lookup"><span data-stu-id="c98ca-114">It sends the event only when it adjusts the quality level, not for each sample that it drops.</span></span> <span data-ttu-id="c98ca-115">Pour plus d’informations, consultez [gestion du contrôle qualité](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="c98ca-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c98ca-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c98ca-116">Requirements</span></span>



| <span data-ttu-id="c98ca-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c98ca-117">Requirement</span></span> | <span data-ttu-id="c98ca-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c98ca-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c98ca-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c98ca-119">Header</span></span><br/> | <dl> <span data-ttu-id="c98ca-120"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c98ca-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c98ca-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c98ca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c98ca-122">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="c98ca-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c98ca-123">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="c98ca-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





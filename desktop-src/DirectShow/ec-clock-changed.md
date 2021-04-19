---
description: L’horloge de référence a changé.
ms.assetid: f6de9e74-85fa-4f36-9d7d-3d95f2dbf873
title: EC_CLOCK_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f6a1346c4d445245e62c4823edb4f2cc5accfcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540483"
---
# <a name="ec_clock_changed"></a><span data-ttu-id="191cb-103">\_horloge EC \_ modifiée</span><span class="sxs-lookup"><span data-stu-id="191cb-103">EC\_CLOCK\_CHANGED</span></span>

<span data-ttu-id="191cb-104">L’horloge de référence a changé.</span><span class="sxs-lookup"><span data-stu-id="191cb-104">The reference clock has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="191cb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="191cb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="191cb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="191cb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="191cb-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="191cb-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="191cb-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="191cb-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="191cb-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="191cb-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="191cb-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="191cb-110">Default Action</span></span>

<span data-ttu-id="191cb-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="191cb-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="191cb-112">Notes</span><span class="sxs-lookup"><span data-stu-id="191cb-112">Remarks</span></span>

<span data-ttu-id="191cb-113">Le gestionnaire de graphique de filtre envoie cet événement lorsque sa méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) est appelée.</span><span class="sxs-lookup"><span data-stu-id="191cb-113">The filter graph manager sends this event when its [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="191cb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="191cb-114">Requirements</span></span>



| <span data-ttu-id="191cb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="191cb-115">Requirement</span></span> | <span data-ttu-id="191cb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="191cb-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="191cb-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="191cb-117">Header</span></span><br/> | <dl> <span data-ttu-id="191cb-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="191cb-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="191cb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="191cb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="191cb-120">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="191cb-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="191cb-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="191cb-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





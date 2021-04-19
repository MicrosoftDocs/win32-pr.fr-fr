---
description: Le graphique de filtre a changé d’État.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538103"
---
# <a name="ec_state_change"></a><span data-ttu-id="79a1f-103">\_changement d’État EC \_</span><span class="sxs-lookup"><span data-stu-id="79a1f-103">EC\_STATE\_CHANGE</span></span>

<span data-ttu-id="79a1f-104">Le graphique de filtre a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="79a1f-104">The filter graph has changed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="79a1f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79a1f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79a1f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="79a1f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="79a1f-107">(**DWORD**) Membre du type énuméré d' [**\_ État de filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) , indiquant le nouvel État du graphique.</span><span class="sxs-lookup"><span data-stu-id="79a1f-107">(**DWORD**) Member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the new graph state.</span></span>

</dd> <dt>

<span data-ttu-id="79a1f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="79a1f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="79a1f-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="79a1f-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="79a1f-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="79a1f-110">Default Action</span></span>

<span data-ttu-id="79a1f-111">Aucune action par défaut.</span><span class="sxs-lookup"><span data-stu-id="79a1f-111">No default action.</span></span> <span data-ttu-id="79a1f-112">L’événement n’est pas envoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="79a1f-112">The event is not sent to the application.</span></span>

> [!Note]  
> <span data-ttu-id="79a1f-113">Cet événement peut se produire lorsque le graphique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="79a1f-113">This event can occur when the graph shuts down.</span></span> <span data-ttu-id="79a1f-114">Si vous remplacez l’action par défaut et que vous écoutez cet événement, vous devez veiller à ne pas traiter les événements après avoir libéré le gestionnaire du graphique de filtres.</span><span class="sxs-lookup"><span data-stu-id="79a1f-114">If you override the default action and listen for this event, you must be especially careful not to process events after releasing the Filter Graph Manager.</span></span> <span data-ttu-id="79a1f-115">Dans le cas contraire, votre application peut référencer un pointeur [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) non valide et se bloquer.</span><span class="sxs-lookup"><span data-stu-id="79a1f-115">Otherwise, your application might reference an invalid [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) pointer and crash.</span></span> <span data-ttu-id="79a1f-116">Pour plus d’informations, consultez [réponse aux événements](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="79a1f-116">For more information, see [Responding to Events](responding-to-events.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79a1f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79a1f-117">Requirements</span></span>



| <span data-ttu-id="79a1f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79a1f-118">Requirement</span></span> | <span data-ttu-id="79a1f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="79a1f-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79a1f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="79a1f-120">Header</span></span><br/> | <dl> <span data-ttu-id="79a1f-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="79a1f-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79a1f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79a1f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79a1f-123">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="79a1f-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="79a1f-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="79a1f-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Une fenêtre vidéo est en cours d’activation ou de désactivation.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542375"
---
# <a name="ec_activate"></a><span data-ttu-id="4f0a3-103">\_activation EC</span><span class="sxs-lookup"><span data-stu-id="4f0a3-103">EC\_ACTIVATE</span></span>

<span data-ttu-id="4f0a3-104">Une fenêtre vidéo est en cours d’activation ou de désactivation.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-104">A video window is being activated or deactivated.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f0a3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f0a3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f0a3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4f0a3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4f0a3-107">(**Bool**) **True** si la fenêtre est activée ou **false** si la fenêtre est désactivée.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-107">(**BOOL**) **TRUE** if the window is activated, or **FALSE** if the window is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="4f0a3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4f0a3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4f0a3-109">(**IUnknown** \* ) Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du convertisseur.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-109">(**IUnknown**\*) Pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="4f0a3-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="4f0a3-110">Default Action</span></span>

<span data-ttu-id="4f0a3-111">Le gestionnaire de graphique de filtre définit le focus, via l’interface [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="4f0a3-111">The filter graph manager sets the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="4f0a3-112">Elle n’envoie pas la notification d’événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f0a3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4f0a3-113">Remarks</span></span>

<span data-ttu-id="4f0a3-114">Un convertisseur vidéo envoie cet événement chaque fois que sa fenêtre est activée ou désactivée (autrement dit, lorsqu’il reçoit un \_ message WM ACTIVATEAPP).</span><span class="sxs-lookup"><span data-stu-id="4f0a3-114">A video renderer sends this event whenever its window is activated or deactivated (that is, when it receives a WM\_ACTIVATEAPP message).</span></span> <span data-ttu-id="4f0a3-115">L’activation ou la désactivation de la fenêtre peut se produire parce que la fenêtre a obtenu ou perdu le focus, ou parce que le convertisseur a basculé entre le mode plein écran et le mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-115">Window activation or deactivation can occur because the window has gained or lost focus, or because the renderer has switched between full-screen mode and windowed mode.</span></span>

<span data-ttu-id="4f0a3-116">Cet événement permet au gestionnaire de graphes de filtre d’allouer des ressources qui dépendent du focus de la fenêtre, telles que les périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-116">This event enables the filter graph manager to allocate resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f0a3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f0a3-117">Requirements</span></span>



| <span data-ttu-id="4f0a3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f0a3-118">Requirement</span></span> | <span data-ttu-id="4f0a3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0a3-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0a3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f0a3-120">Header</span></span><br/> | <dl> <span data-ttu-id="4f0a3-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f0a3-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f0a3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f0a3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f0a3-123">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="4f0a3-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4f0a3-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="4f0a3-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





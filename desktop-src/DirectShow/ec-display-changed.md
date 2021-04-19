---
description: Le mode d’affichage a changé.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541667"
---
# <a name="ec_display_changed"></a><span data-ttu-id="e587a-103">\_affichage EC \_ modifié</span><span class="sxs-lookup"><span data-stu-id="e587a-103">EC\_DISPLAY\_CHANGED</span></span>

<span data-ttu-id="e587a-104">Le mode d’affichage a changé.</span><span class="sxs-lookup"><span data-stu-id="e587a-104">The display mode has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="e587a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e587a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e587a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e587a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e587a-107">(**IUnknown** \* ) Pointeur vers un tableau d’interfaces [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) pour les broches d’entrée du convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="e587a-107">(**IUnknown**\*) Pointer to an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces for the video renderer's input pins.</span></span> <span data-ttu-id="e587a-108">Si *lParam2* est égal à zéro, ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e587a-108">If *lParam2* is zero, this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e587a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e587a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e587a-110">Si *lParam2* est égal à zéro, *lParam1* contient un seul pointeur **IPIN** ou est égal à **null**.</span><span class="sxs-lookup"><span data-stu-id="e587a-110">If *lParam2* is zero, *lParam1* contains a single **IPin** pointer or equals **NULL**.</span></span> <span data-ttu-id="e587a-111">Si *lParam2* est supérieur à zéro, *lParam1* contient un tableau de pointeurs **IPIN** et le nombre d’éléments dans le tableau est donné par *lParam2*.</span><span class="sxs-lookup"><span data-stu-id="e587a-111">If *lParam2* is greater than zero, *lParam1* contains an array of **IPin** pointers, and the number of elements in the array is given by *lParam2*.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="e587a-112">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="e587a-112">Default Action</span></span>

<span data-ttu-id="e587a-113">Le gestionnaire de graphique de filtre arrête temporairement le graphique, puis se déconnecte et reconnecte le convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="e587a-113">The filter graph manager temporarily stops the graph, and then disconnects and reconnects the video renderer.</span></span> <span data-ttu-id="e587a-114">Elle ne passe pas l’événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="e587a-114">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="e587a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e587a-115">Remarks</span></span>

<span data-ttu-id="e587a-116">Les convertisseurs vidéo peuvent envoyer cet événement en réponse à un message [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .</span><span class="sxs-lookup"><span data-stu-id="e587a-116">Video renderers can send this event in response to a [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span> <span data-ttu-id="e587a-117">Le message **WM \_ DISPLAYCHANGE** indique que l’utilisateur a modifié la résolution d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e587a-117">The **WM\_DISPLAYCHANGE** message indicates that the user has changed the display resolution.</span></span>

<span data-ttu-id="e587a-118">Pendant la connexion de code confidentiel, la plupart des convertisseurs vidéo sélectionnent un format basé sur le mode d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="e587a-118">During pin connection, most video renderers pick a format based on the current display mode.</span></span> <span data-ttu-id="e587a-119">Si le mode d’affichage change, le convertisseur vidéo devra peut-être choisir un autre format.</span><span class="sxs-lookup"><span data-stu-id="e587a-119">If the display mode changes, the video renderer might need to choose another format.</span></span> <span data-ttu-id="e587a-120">En envoyant ce message, le convertisseur signale au gestionnaire de graphique de filtre qu’il doit être reconnecté.</span><span class="sxs-lookup"><span data-stu-id="e587a-120">By sending this message, the renderer signals to the filter graph manager that it needs to be reconnected.</span></span> <span data-ttu-id="e587a-121">Pendant la reconnexion, le convertisseur peut sélectionner un nouveau format.</span><span class="sxs-lookup"><span data-stu-id="e587a-121">During the reconnection, the renderer can select a new format.</span></span> <span data-ttu-id="e587a-122">Si la reconnexion échoue, le gestionnaire de graphique de filtre envoie un événement [**EC \_ ERRORABORT**](ec-errorabort.md) à l’application.</span><span class="sxs-lookup"><span data-stu-id="e587a-122">If the reconnection fails, the filter graph manager sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the application.</span></span>

### <a name="enhanced-video-renderer"></a><span data-ttu-id="e587a-123">Convertisseur vidéo amélioré</span><span class="sxs-lookup"><span data-stu-id="e587a-123">Enhanced Video Renderer</span></span>

<span data-ttu-id="e587a-124">Un présentateur personnalisé pour le [**convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR) doit envoyer cet événement à EVR si l’appareil Direct3D du présentateur change.</span><span class="sxs-lookup"><span data-stu-id="e587a-124">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) should send this event to the EVR if the presenter's Direct3D device changes.</span></span> <span data-ttu-id="e587a-125">Définissez *lParam1* et *lParam2* sur zéro ; EVR ignore les paramètres d’événement.</span><span class="sxs-lookup"><span data-stu-id="e587a-125">Set *lParam1* and *lParam2* to zero; the EVR ignores the event parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e587a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e587a-126">Requirements</span></span>



| <span data-ttu-id="e587a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e587a-127">Requirement</span></span> | <span data-ttu-id="e587a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e587a-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e587a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="e587a-129">Header</span></span><br/> | <dl> <span data-ttu-id="e587a-130"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e587a-130"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e587a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e587a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e587a-132">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="e587a-132">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e587a-133">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="e587a-133">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 


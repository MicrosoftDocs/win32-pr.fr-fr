---
description: Le convertisseur vidéo bascule en mode plein écran.
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: EC_FULLSCREEN_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf36b5652ea5f7cde26950a18de086af0862dac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525497"
---
# <a name="ec_fullscreen_lost"></a><span data-ttu-id="ab8d2-103">perte de la \_ fullscreen EC \_</span><span class="sxs-lookup"><span data-stu-id="ab8d2-103">EC\_FULLSCREEN\_LOST</span></span>

<span data-ttu-id="ab8d2-104">Le convertisseur vidéo bascule en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-104">The video renderer is switching out of full-screen mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab8d2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab8d2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab8d2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ab8d2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ab8d2-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="ab8d2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ab8d2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ab8d2-109">(**IUnknown** \* ) Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du convertisseur vidéo, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-109">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ab8d2-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="ab8d2-110">Default Action</span></span>

<span data-ttu-id="ab8d2-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab8d2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ab8d2-112">Remarks</span></span>

<span data-ttu-id="ab8d2-113">Lorsque le [convertisseur plein écran](full-screen-renderer-filter.md) perd l’activation, il envoie cet événement.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-113">When the [Full Screen Renderer](full-screen-renderer-filter.md) loses activation, it sends this event.</span></span> <span data-ttu-id="ab8d2-114">Lorsqu’un autre convertisseur vidéo bascule en mode plein écran, le gestionnaire de graphique de filtre envoie cet événement, en réponse à un événement [**EC \_ Activate**](ec-activate.md) du convertisseur.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-114">When another video renderer switches out of full-screen mode, the filter graph manager sends this event, in response to an [**EC\_ACTIVATE**](ec-activate.md) event from the renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab8d2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab8d2-115">Requirements</span></span>



| <span data-ttu-id="ab8d2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab8d2-116">Requirement</span></span> | <span data-ttu-id="ab8d2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab8d2-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab8d2-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab8d2-118">Header</span></span><br/> | <dl> <span data-ttu-id="ab8d2-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab8d2-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab8d2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab8d2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab8d2-121">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="ab8d2-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ab8d2-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="ab8d2-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: La taille de la vidéo native a changé.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520937"
---
# <a name="ec_video_size_changed"></a><span data-ttu-id="c554c-103">taille de la \_ vidéo ce \_ \_ modifiée</span><span class="sxs-lookup"><span data-stu-id="c554c-103">EC\_VIDEO\_SIZE\_CHANGED</span></span>

<span data-ttu-id="c554c-104">La taille de la vidéo native a changé.</span><span class="sxs-lookup"><span data-stu-id="c554c-104">The native video size has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="c554c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c554c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c554c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c554c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c554c-107">(**DWORD**) MOT de poids faible spécifie la nouvelle largeur, en pixels ; MOT de poids fort spécifie la nouvelle hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="c554c-107">(**DWORD**) Low-order WORD specifies the new width, in pixels; high-order WORD specifies the new height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c554c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c554c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c554c-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="c554c-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c554c-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="c554c-110">Default Action</span></span>

<span data-ttu-id="c554c-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c554c-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c554c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c554c-112">Remarks</span></span>

<span data-ttu-id="c554c-113">Les convertisseurs vidéo peuvent envoyer cet événement s’ils détectent une modification de la taille de la vidéo native.</span><span class="sxs-lookup"><span data-stu-id="c554c-113">Video renderers may send this event if they detect a change in the native video size.</span></span>

<span data-ttu-id="c554c-114">Le [convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7) et le [convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9) envoient cet événement en mode fenêtre, mais pas en mode sans fenêtre ni en mode de rendu.</span><span class="sxs-lookup"><span data-stu-id="c554c-114">The [Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) send this event in windowed mode, but not in windowless mode or renderless mode.</span></span> <span data-ttu-id="c554c-115">Pour plus d’informations sur le mode fenêtre dans VMR, consultez [rendu vidéo](video-rendering.md).</span><span class="sxs-lookup"><span data-stu-id="c554c-115">For more information about windowed mode in the VMR, see [Video Rendering](video-rendering.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c554c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c554c-116">Requirements</span></span>



| <span data-ttu-id="c554c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c554c-117">Requirement</span></span> | <span data-ttu-id="c554c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c554c-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c554c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c554c-119">Header</span></span><br/> | <dl> <span data-ttu-id="c554c-120"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c554c-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c554c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c554c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c554c-122">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="c554c-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c554c-123">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="c554c-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





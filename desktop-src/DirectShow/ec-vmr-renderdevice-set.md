---
description: Envoyé lorsque VMR a sélectionné son mécanisme de rendu.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536050"
---
# <a name="ec_vmr_renderdevice_set"></a><span data-ttu-id="6c8c2-103">\_ \_ jeu RENDERDEVICE EC \_ VMR</span><span class="sxs-lookup"><span data-stu-id="6c8c2-103">EC\_VMR\_RENDERDEVICE\_SET</span></span>

<span data-ttu-id="6c8c2-104">Envoyé lorsque VMR a sélectionné son mécanisme de rendu.</span><span class="sxs-lookup"><span data-stu-id="6c8c2-104">Sent when the VMR has selected its rendering mechanism.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c8c2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c8c2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8c2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6c8c2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6c8c2-107">Peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6c8c2-107">May be one of the following values:</span></span>



| <span data-ttu-id="6c8c2-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c8c2-108">Value</span></span>                        | <span data-ttu-id="6c8c2-109">Signification</span><span class="sxs-lookup"><span data-stu-id="6c8c2-109">Meaning</span></span>                                                  |
|------------------------------|----------------------------------------------------------|
| <span data-ttu-id="6c8c2-110">segmentation de l' \_ appareil de rendu VMR \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c8c2-110">VMR\_RENDER\_DEVICE\_OVERLAY</span></span> | <span data-ttu-id="6c8c2-111">VMR s’affiche sur la surface de recouvrement (VMR-7 uniquement).</span><span class="sxs-lookup"><span data-stu-id="6c8c2-111">The VMR will render to the overlay surface (VMR-7 only).</span></span> |
| <span data-ttu-id="6c8c2-112">VIDMEM de l' \_ appareil de rendu VMR \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c8c2-112">VMR\_RENDER\_DEVICE\_VIDMEM</span></span>  | <span data-ttu-id="6c8c2-113">VMR s’affichera dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="6c8c2-113">The VMR will render to video memory.</span></span>                     |
| <span data-ttu-id="6c8c2-114">SYSMEM de l' \_ appareil de rendu VMR \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c8c2-114">VMR\_RENDER\_DEVICE\_SYSMEM</span></span>  | <span data-ttu-id="6c8c2-115">VMR s’affichera dans la mémoire système (VMR-7 uniquement).</span><span class="sxs-lookup"><span data-stu-id="6c8c2-115">The VMR will render to system memory (VMR-7 only).</span></span>       |



 

</dd> <dt>

<span data-ttu-id="6c8c2-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6c8c2-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6c8c2-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="6c8c2-117">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c8c2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="6c8c2-118">Remarks</span></span>

<span data-ttu-id="6c8c2-119">Cet événement est envoyé par VMR-7 et VMR-9 et est transféré aux applications.</span><span class="sxs-lookup"><span data-stu-id="6c8c2-119">This event is sent by both the VMR-7 and the VMR-9 and it is forwarded to applications.</span></span> <span data-ttu-id="6c8c2-120">Notez que VMR-9 ne prend en charge que les cibles de rendu de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="6c8c2-120">Note that the VMR-9 only supports video memory render targets.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8c2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c8c2-121">Requirements</span></span>



| <span data-ttu-id="6c8c2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c8c2-122">Requirement</span></span> | <span data-ttu-id="6c8c2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c8c2-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8c2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c8c2-124">Header</span></span><br/> | <dl> <span data-ttu-id="6c8c2-125"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c8c2-125"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8c2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c8c2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8c2-127">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="6c8c2-127">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="6c8c2-128">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="6c8c2-128">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





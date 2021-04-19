---
description: Envoyé lorsque le titre de la vidéo active (STM) change.
ms.assetid: 7b8849c8-c71e-44d6-b33a-8e80247bdb22
title: EC_DVD_TITLE_SET_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_SET_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c5685cfb909a7fa24c39dff969076269845a663e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540397"
---
# <a name="ec_dvd_title_set_change"></a><span data-ttu-id="59605-103">\_modification du \_ jeu de titres du DVD EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="59605-103">EC\_DVD\_TITLE\_SET\_CHANGE</span></span>

<span data-ttu-id="59605-104">Envoyé lorsque le titre de la vidéo active (STM) change.</span><span class="sxs-lookup"><span data-stu-id="59605-104">Sent when current Video Title Set (VTS) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="59605-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59605-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59605-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="59605-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="59605-107">Le nouveau numéro de jeu de titres vidéo (VTSN).</span><span class="sxs-lookup"><span data-stu-id="59605-107">The new Video Title Set Number (VTSN).</span></span>

</dd> <dt>

<span data-ttu-id="59605-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="59605-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="59605-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="59605-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59605-110">Notes</span><span class="sxs-lookup"><span data-stu-id="59605-110">Remarks</span></span>

<span data-ttu-id="59605-111">Cet événement est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="59605-111">This event is disabled by default.</span></span> <span data-ttu-id="59605-112">Pour activer cet événement, appelez [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) et affectez à l’option **DVD \_ NotifyPositionChange** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="59605-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="59605-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59605-113">Requirements</span></span>



| <span data-ttu-id="59605-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59605-114">Requirement</span></span> | <span data-ttu-id="59605-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="59605-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59605-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="59605-116">Header</span></span><br/> | <dl> <span data-ttu-id="59605-117"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59605-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59605-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59605-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59605-119">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="59605-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="59605-120">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="59605-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="59605-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="59605-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





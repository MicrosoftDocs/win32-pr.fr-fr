---
description: Envoyé lors du démarrage d’un jeu de commandes de navigation sur DVD.
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: EC_DVD_BeginNavigationCommands (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BeginNavigationCommands
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: cda904c4fcc0b1acdd16c8fc4596eef332140ec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542701"
---
# <a name="ec_dvd_beginnavigationcommands"></a><span data-ttu-id="8cac7-103">\_BeginNavigationCommands de DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="8cac7-103">EC\_DVD\_BeginNavigationCommands</span></span>

<span data-ttu-id="8cac7-104">Envoyé lors du démarrage d’un jeu de commandes de navigation sur DVD.</span><span class="sxs-lookup"><span data-stu-id="8cac7-104">Sent when a set of DVD navigation commands are starting.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cac7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cac7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cac7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8cac7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8cac7-107">Valeur de l’énumération [**\_ NavCmdType DVD**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) .</span><span class="sxs-lookup"><span data-stu-id="8cac7-107">A value from the [**DVD\_NavCmdType**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="8cac7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8cac7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8cac7-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="8cac7-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cac7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8cac7-110">Remarks</span></span>

<span data-ttu-id="8cac7-111">Cet événement est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="8cac7-111">This event is disabled by default.</span></span> <span data-ttu-id="8cac7-112">Pour activer cet événement, appelez [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) et affectez à l’option **DVD \_ EnableLoggingEvents** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="8cac7-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cac7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cac7-113">Requirements</span></span>



| <span data-ttu-id="8cac7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cac7-114">Requirement</span></span> | <span data-ttu-id="8cac7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cac7-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cac7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="8cac7-116">Header</span></span><br/> | <dl> <span data-ttu-id="8cac7-117"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8cac7-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cac7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cac7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cac7-119">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="8cac7-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="8cac7-120">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="8cac7-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8cac7-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="8cac7-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





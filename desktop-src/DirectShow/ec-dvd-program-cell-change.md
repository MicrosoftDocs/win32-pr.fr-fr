---
description: Envoyé lorsque le numéro de programme DVD ou le numéro de cellule change.
ms.assetid: a500e86d-cd42-4716-9c57-828a72c4e1df
title: EC_DVD_PROGRAM_CELL_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CELL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: d41f691016c3e41cfc3e14ed1ce6fff276dcc70e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532546"
---
# <a name="ec_dvd_program_cell_change"></a><span data-ttu-id="745e7-103">\_modification des \_ cellules du programme de DVD EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="745e7-103">EC\_DVD\_PROGRAM\_CELL\_CHANGE</span></span>

<span data-ttu-id="745e7-104">Envoyé lorsque le numéro de programme DVD ou le numéro de cellule change.</span><span class="sxs-lookup"><span data-stu-id="745e7-104">Sent when the DVD program number or cell number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="745e7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="745e7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="745e7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="745e7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="745e7-107">Nouveau numéro de programme.</span><span class="sxs-lookup"><span data-stu-id="745e7-107">The new program number.</span></span>

</dd> <dt>

<span data-ttu-id="745e7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="745e7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="745e7-109">Nouveau numéro de cellule.</span><span class="sxs-lookup"><span data-stu-id="745e7-109">The new cell number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="745e7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="745e7-110">Remarks</span></span>

<span data-ttu-id="745e7-111">Cet événement est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="745e7-111">This event is disabled by default.</span></span> <span data-ttu-id="745e7-112">Pour activer cet événement, appelez [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) et affectez à l’option **DVD \_ NotifyPositionChange** la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="745e7-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="745e7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="745e7-113">Requirements</span></span>



| <span data-ttu-id="745e7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="745e7-114">Requirement</span></span> | <span data-ttu-id="745e7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="745e7-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="745e7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="745e7-116">Header</span></span><br/> | <dl> <span data-ttu-id="745e7-117"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="745e7-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="745e7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="745e7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="745e7-119">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="745e7-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="745e7-120">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="745e7-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="745e7-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="745e7-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Indique si un bloc angle est lu et si des modifications d’angle peuvent être effectuées.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4d2abb17b329323cf4a21128da5dba927b48d4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528939"
---
# <a name="ec_dvd_angles_available"></a><span data-ttu-id="b47fe-103">\_angles de DVD EC \_ \_ disponibles</span><span class="sxs-lookup"><span data-stu-id="b47fe-103">EC\_DVD\_ANGLES\_AVAILABLE</span></span>

<span data-ttu-id="b47fe-104">Indique si un bloc angle est lu et si des modifications d’angle peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="b47fe-104">Indicates whether an angle block is being played and angle changes can be performed.</span></span>

## <a name="parameters"></a><span data-ttu-id="b47fe-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b47fe-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b47fe-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b47fe-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b47fe-107">Valeur booléenne (**bool**) qui indique si un bloc angle est lu.</span><span class="sxs-lookup"><span data-stu-id="b47fe-107">Boolean (**BOOL**) value that indicates if an angle block is being played back.</span></span> <span data-ttu-id="b47fe-108">Zéro (0) indique que la lecture n’est pas dans un bloc angle et que les angles ne sont pas disponibles, un (1) indique qu’un bloc angle est lu et que des changements d’angle peuvent être effectués.</span><span class="sxs-lookup"><span data-stu-id="b47fe-108">Zero (0) indicates that playback is not in an angle block and angles are not available, One (1) indicates that an angle block is being played back and angle changes can be performed.</span></span>

</dd> <dt>

<span data-ttu-id="b47fe-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b47fe-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b47fe-110">Zéro.</span><span class="sxs-lookup"><span data-stu-id="b47fe-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b47fe-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b47fe-111">Remarks</span></span>

<span data-ttu-id="b47fe-112">Les changements d’angle ne sont pas limités aux blocs d’angle et la détection de la modification d’angle ne peut être vue que dans un bloc angle.</span><span class="sxs-lookup"><span data-stu-id="b47fe-112">Angle changes are not restricted to angle blocks and the manifestation of the angle change can be seen only in an angle block.</span></span>

## <a name="requirements"></a><span data-ttu-id="b47fe-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b47fe-113">Requirements</span></span>



| <span data-ttu-id="b47fe-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b47fe-114">Requirement</span></span> | <span data-ttu-id="b47fe-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b47fe-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47fe-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="b47fe-116">Header</span></span><br/> | <dl> <span data-ttu-id="b47fe-117"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b47fe-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b47fe-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b47fe-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b47fe-119">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="b47fe-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="b47fe-120">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="b47fe-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b47fe-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="b47fe-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





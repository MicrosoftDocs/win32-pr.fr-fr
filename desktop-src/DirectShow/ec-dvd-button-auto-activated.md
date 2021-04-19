---
description: Signale qu’un bouton de menu DVD a été automatiquement activé par des instructions sur le disque. Cela se produit lorsqu’un menu expire et que le disque a spécifié un bouton à activer automatiquement.
ms.assetid: ecd79c2a-1717-473d-b111-2b1db2ca4cc1
title: EC_DVD_BUTTON_AUTO_ACTIVATED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_AUTO_ACTIVATED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6a30ddcff32140165d5cb6cb648df84b3360a1b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540009"
---
# <a name="ec_dvd_button_auto_activated"></a><span data-ttu-id="cf052-103">\_bouton DVD \_ EC \_ \_ activé automatiquement</span><span class="sxs-lookup"><span data-stu-id="cf052-103">EC\_DVD\_BUTTON\_AUTO\_ACTIVATED</span></span>

<span data-ttu-id="cf052-104">Signale qu’un bouton de menu DVD a été automatiquement activé par des instructions sur le disque. Cela se produit lorsqu’un menu expire et que le disque a spécifié un bouton à activer automatiquement.</span><span class="sxs-lookup"><span data-stu-id="cf052-104">Signals that a DVD menu button has been automatically activated per instructions on the disc. This occurs when a menu times out and the disc has specified a button to be automatically activated.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf052-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf052-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf052-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cf052-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cf052-107">Valeur **DWORD** indiquant le bouton qui a été activé.</span><span class="sxs-lookup"><span data-stu-id="cf052-107">**DWORD** value indicating the button that was activated.</span></span>

</dd> <dt>

<span data-ttu-id="cf052-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cf052-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cf052-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="cf052-109">Zero.</span></span>

</dd> </dl>

<span data-ttu-id="cf052-110">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="cf052-110">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf052-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf052-111">Requirements</span></span>



| <span data-ttu-id="cf052-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf052-112">Requirement</span></span> | <span data-ttu-id="cf052-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf052-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf052-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf052-114">Header</span></span><br/> | <dl> <span data-ttu-id="cf052-115"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf052-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf052-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf052-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf052-117">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="cf052-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="cf052-118">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="cf052-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="cf052-119">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="cf052-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





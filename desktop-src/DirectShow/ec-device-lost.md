---
description: Un appareil Plug-and-Play a été supprimé ou est à nouveau disponible.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fa3f6368e85f8dc54ca6fd8cc2e0eee21262a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545946"
---
# <a name="ec_device_lost"></a><span data-ttu-id="b6458-103">\_appareil EC \_ perdu</span><span class="sxs-lookup"><span data-stu-id="b6458-103">EC\_DEVICE\_LOST</span></span>

<span data-ttu-id="b6458-104">Un appareil Plug-and-Play a été supprimé ou est à nouveau disponible.</span><span class="sxs-lookup"><span data-stu-id="b6458-104">A Plug and Play device was removed or became available again.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6458-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6458-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6458-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b6458-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b6458-107">(**IUnknown** \* ) Pointeur vers l’interface **IUnknown** du filtre qui représente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b6458-107">(**IUnknown**\*) Pointer to the **IUnknown** interface of the filter that represents the device.</span></span>

</dd> <dt>

<span data-ttu-id="b6458-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b6458-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b6458-109">Zéro si l’appareil a été supprimé, ou 1 si l’appareil est à nouveau disponible.</span><span class="sxs-lookup"><span data-stu-id="b6458-109">Zero if the device was removed, or 1 if the device is available again.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b6458-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="b6458-110">Default Action</span></span>

<span data-ttu-id="b6458-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b6458-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6458-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b6458-112">Remarks</span></span>

<span data-ttu-id="b6458-113">Lorsque l’appareil redevient disponible, l’état précédent du filtre de périphérique n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="b6458-113">When the device becomes available again, the previous state of the device filter is no longer valid.</span></span> <span data-ttu-id="b6458-114">L’application doit reconstruire le graphique pour pouvoir utiliser l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b6458-114">The application must rebuild the graph in order to use the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6458-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6458-115">Requirements</span></span>



| <span data-ttu-id="b6458-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6458-116">Requirement</span></span> | <span data-ttu-id="b6458-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6458-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6458-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6458-118">Header</span></span><br/> | <dl> <span data-ttu-id="b6458-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6458-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6458-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6458-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6458-121">Notification de suppression de l’appareil</span><span class="sxs-lookup"><span data-stu-id="b6458-121">Device Removal Notification</span></span>](device-removal-notification.md)
</dt> <dt>

[<span data-ttu-id="b6458-122">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="b6458-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b6458-123">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="b6458-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





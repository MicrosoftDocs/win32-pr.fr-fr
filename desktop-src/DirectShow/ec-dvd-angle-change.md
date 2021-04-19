---
description: Signale que le nombre d’angles disponibles a changé ou que le numéro d’angle actuel a changé.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 08914e3fcb93d38ccad25053f7c33480e900ad93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531036"
---
# <a name="ec_dvd_angle_change"></a><span data-ttu-id="cce51-103">\_changement d' \_ angle de DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="cce51-103">EC\_DVD\_ANGLE\_CHANGE</span></span>

<span data-ttu-id="cce51-104">Signale que le nombre d’angles disponibles a changé ou que le numéro d’angle actuel a changé.</span><span class="sxs-lookup"><span data-stu-id="cce51-104">Signals that either the number of available angles changed or that the current angle number changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="cce51-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cce51-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce51-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cce51-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cce51-107">Valeur **DWORD** indiquant le nombre d’angles disponibles.</span><span class="sxs-lookup"><span data-stu-id="cce51-107">**DWORD** value indicating the number of available angles.</span></span> <span data-ttu-id="cce51-108">Lorsque le nombre d’angles disponibles est 1, la vidéo actuelle n’est pas multiangle.</span><span class="sxs-lookup"><span data-stu-id="cce51-108">When the number of available angles is 1, the current video is not multiangle.</span></span>

</dd> <dt>

<span data-ttu-id="cce51-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cce51-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cce51-110">Valeur **DWORD** indiquant le nombre d’angles en cours.</span><span class="sxs-lookup"><span data-stu-id="cce51-110">**DWORD** value indicating the current angle number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cce51-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cce51-111">Remarks</span></span>

<span data-ttu-id="cce51-112">Les nombres en angle sont compris entre 1 et 9.</span><span class="sxs-lookup"><span data-stu-id="cce51-112">Angle numbers range from 1 to 9.</span></span>

<span data-ttu-id="cce51-113">Le numéro d’angle actuel peut changer automatiquement à l’aide d’une commande de navigation créée sur le disque, ainsi que via le contrôle d’application à l’aide de l’interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="cce51-113">The current angle number can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="cce51-114">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="cce51-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="cce51-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cce51-115">Requirements</span></span>



| <span data-ttu-id="cce51-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cce51-116">Requirement</span></span> | <span data-ttu-id="cce51-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="cce51-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cce51-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="cce51-118">Header</span></span><br/> | <dl> <span data-ttu-id="cce51-119"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cce51-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cce51-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cce51-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce51-121">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="cce51-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="cce51-122">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="cce51-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="cce51-123">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="cce51-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





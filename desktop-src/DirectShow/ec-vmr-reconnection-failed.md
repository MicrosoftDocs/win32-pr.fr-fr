---
description: Envoyé par VMR-7 et VMR-9 lorsqu’il n’a pas pu accepter une demande de modification de format dynamique du décodeur en amont.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d29703d5ede068710966119f16c44a9e3637249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520936"
---
# <a name="ec_vmr_reconnection_failed"></a><span data-ttu-id="54df0-103">échec de la \_ \_ reconnexion EC VMR \_</span><span class="sxs-lookup"><span data-stu-id="54df0-103">EC\_VMR\_RECONNECTION\_FAILED</span></span>

<span data-ttu-id="54df0-104">Envoyé par VMR-7 et VMR-9 lorsqu’il n’a pas pu accepter une demande de modification de format dynamique du décodeur en amont.</span><span class="sxs-lookup"><span data-stu-id="54df0-104">Sent by the VMR-7 and the VMR-9 when it was unable to accept a dynamic format change request from the upstream decoder.</span></span>

## <a name="parameters"></a><span data-ttu-id="54df0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54df0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54df0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="54df0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="54df0-107">(**HRESULT**) Code d’état retourné par [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sur la broche d’entrée VMR qui n’a pas réussi la reconnexion.</span><span class="sxs-lookup"><span data-stu-id="54df0-107">(**HRESULT**) Status code returned from [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the VMR's input pin that failed the reconnection.</span></span>

</dd> <dt>

<span data-ttu-id="54df0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="54df0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="54df0-109">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="54df0-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54df0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="54df0-110">Remarks</span></span>

<span data-ttu-id="54df0-111">Cet événement est transféré aux applications.</span><span class="sxs-lookup"><span data-stu-id="54df0-111">This event is forwarded to applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="54df0-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54df0-112">Requirements</span></span>



| <span data-ttu-id="54df0-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54df0-113">Requirement</span></span> | <span data-ttu-id="54df0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="54df0-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54df0-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="54df0-115">Header</span></span><br/> | <dl> <span data-ttu-id="54df0-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="54df0-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54df0-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54df0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54df0-118">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="54df0-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="54df0-119">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="54df0-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Signale que le numéro de flux audio actuel a changé pour le titre principal du DVD.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 947e19310a77869dbff97851e1ffa0684a3e43a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529952"
---
# <a name="ec_dvd_audio_stream_change"></a><span data-ttu-id="7ea37-103">\_modification du \_ \_ flux audio du DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="7ea37-103">EC\_DVD\_AUDIO\_STREAM\_CHANGE</span></span>

<span data-ttu-id="7ea37-104">Signale que le numéro de flux audio actuel a changé pour le titre principal du DVD.</span><span class="sxs-lookup"><span data-stu-id="7ea37-104">Signals that the current audio stream number changed for the DVD main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ea37-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ea37-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ea37-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7ea37-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7ea37-107">Valeur **DWORD** indiquant le nouveau numéro de flux audio de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ea37-107">**DWORD** value indicating the new user audio stream number.</span></span> <span data-ttu-id="7ea37-108">Les numéros de flux audio sont compris entre 0 et 7.</span><span class="sxs-lookup"><span data-stu-id="7ea37-108">Audio stream numbers range from 0 to 7.</span></span> <span data-ttu-id="7ea37-109">Stream 0xFFFFFFFF indique qu’aucun flux n’est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7ea37-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="7ea37-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7ea37-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7ea37-111">Zéro.</span><span class="sxs-lookup"><span data-stu-id="7ea37-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ea37-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7ea37-112">Remarks</span></span>

<span data-ttu-id="7ea37-113">Le flux audio actuel peut changer automatiquement à l’aide d’une commande de navigation créée sur le disque, ainsi que via le contrôle d’application à l’aide de l’interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="7ea37-113">The current audio stream can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="7ea37-114">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="7ea37-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ea37-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ea37-115">Requirements</span></span>



| <span data-ttu-id="7ea37-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ea37-116">Requirement</span></span> | <span data-ttu-id="7ea37-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ea37-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea37-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ea37-118">Header</span></span><br/> | <dl> <span data-ttu-id="7ea37-119"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ea37-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ea37-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ea37-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea37-121">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="7ea37-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7ea37-122">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="7ea37-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7ea37-123">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="7ea37-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





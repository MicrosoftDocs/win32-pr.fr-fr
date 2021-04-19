---
description: Spécifie l’horodatage de l’étape de Frame la plus récente.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542415"
---
# <a name="ec_scrub_time"></a><span data-ttu-id="6d8a7-103">\_temps de nettoyage ce \_</span><span class="sxs-lookup"><span data-stu-id="6d8a7-103">EC\_SCRUB\_TIME</span></span>

<span data-ttu-id="6d8a7-104">Spécifie l’horodatage de l’étape de Frame la plus récente.</span><span class="sxs-lookup"><span data-stu-id="6d8a7-104">Specifies the time stamp for the most recent frame step.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d8a7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d8a7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d8a7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6d8a7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6d8a7-107">(**DWORD**) 32 bits inférieurs de l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="6d8a7-107">(**DWORD**) Lower 32 bits of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="6d8a7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6d8a7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6d8a7-109">(**DWORD**) 32 bits supérieurs de l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="6d8a7-109">(**DWORD**) Upper 32 bits of the time stamp.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="6d8a7-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="6d8a7-110">Default Action</span></span>

<span data-ttu-id="6d8a7-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6d8a7-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d8a7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6d8a7-112">Remarks</span></span>

<span data-ttu-id="6d8a7-113">Le présentateur pour le filtre EVR ( [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) ) envoie ce message à EVR lorsqu’il termine une étape de trame.</span><span class="sxs-lookup"><span data-stu-id="6d8a7-113">The presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter sends this message to the EVR when it completes a frame step.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d8a7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d8a7-114">Requirements</span></span>



| <span data-ttu-id="6d8a7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d8a7-115">Requirement</span></span> | <span data-ttu-id="6d8a7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d8a7-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d8a7-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d8a7-117">Header</span></span><br/> | <dl> <span data-ttu-id="6d8a7-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d8a7-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d8a7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d8a7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d8a7-120">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="6d8a7-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 





---
description: Déclenché par une sortie approuvée pour envoyer des informations d’État sur l’application de la stratégie de sortie.
ms.assetid: 4906f6c3-1570-421f-aef1-914bd338bb1f
title: Événement MEPolicyReport (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0053fb551a69b820beeb4237211cb9af446f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529747"
---
# <a name="mepolicyreport-event"></a><span data-ttu-id="fde2a-103">Événement MEPolicyReport</span><span class="sxs-lookup"><span data-stu-id="fde2a-103">MEPolicyReport event</span></span>

<span data-ttu-id="fde2a-104">Déclenché par une sortie approuvée pour envoyer des informations d’État sur l’application de la stratégie de sortie.</span><span class="sxs-lookup"><span data-stu-id="fde2a-104">Raised by a trusted output to send status information about the enforcement of the output policy.</span></span>

## <a name="event-values"></a><span data-ttu-id="fde2a-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="fde2a-105">Event values</span></span>

<span data-ttu-id="fde2a-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="fde2a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="fde2a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="fde2a-107">VARTYPE</span></span>              | <span data-ttu-id="fde2a-108">Description</span><span class="sxs-lookup"><span data-stu-id="fde2a-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="fde2a-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="fde2a-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="fde2a-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="fde2a-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fde2a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fde2a-111">Remarks</span></span>

<span data-ttu-id="fde2a-112">Les attributs et les codes d’État pour cet événement dépendent du système de protection de contenu spécifique appliqué par la sortie approuvée.</span><span class="sxs-lookup"><span data-stu-id="fde2a-112">Attributes and status codes for this event depend on the specific content protection system enforced by the trusted output.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde2a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fde2a-113">Requirements</span></span>



| <span data-ttu-id="fde2a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fde2a-114">Requirement</span></span> | <span data-ttu-id="fde2a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fde2a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fde2a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fde2a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fde2a-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fde2a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fde2a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fde2a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fde2a-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fde2a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fde2a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="fde2a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde2a-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fde2a-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fde2a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fde2a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde2a-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fde2a-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





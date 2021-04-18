---
description: Déclenché par le moteur de stratégie lorsque l’individualisation est terminée. Pour plus d’informations, consultez événement MEIndividualizationStart.
ms.assetid: 44a4956f-19ba-410d-b96c-e7774cbe2d7e
title: Événement MEIndividualizationCompleted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7143274d12a9ad113f714062ff8f88c1fb8277cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533802"
---
# <a name="meindividualizationcompleted-event"></a><span data-ttu-id="7e7f5-104">Événement MEIndividualizationCompleted</span><span class="sxs-lookup"><span data-stu-id="7e7f5-104">MEIndividualizationCompleted event</span></span>

<span data-ttu-id="7e7f5-105">Déclenché par le moteur de stratégie lorsque l’individualisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="7e7f5-105">Raised by the policy engine when individualization is complete.</span></span> <span data-ttu-id="7e7f5-106">Pour plus d’informations, consultez événement [MEIndividualizationStart](meindividualizationstart.md) .</span><span class="sxs-lookup"><span data-stu-id="7e7f5-106">For more information, see [MEIndividualizationStart](meindividualizationstart.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="7e7f5-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="7e7f5-107">Event values</span></span>

<span data-ttu-id="7e7f5-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e7f5-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7e7f5-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7e7f5-109">VARTYPE</span></span>              | <span data-ttu-id="7e7f5-110">Description</span><span class="sxs-lookup"><span data-stu-id="7e7f5-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="7e7f5-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="7e7f5-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="7e7f5-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="7e7f5-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="7e7f5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e7f5-113">Requirements</span></span>



| <span data-ttu-id="7e7f5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e7f5-114">Requirement</span></span> | <span data-ttu-id="7e7f5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e7f5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7f5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e7f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7e7f5-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e7f5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7e7f5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e7f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7e7f5-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e7f5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7e7f5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e7f5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e7f5-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e7f5-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e7f5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e7f5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7f5-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e7f5-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





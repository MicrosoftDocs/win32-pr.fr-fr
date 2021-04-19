---
description: Levée lorsque l’acquisition de licence est terminée. Pour plus d’informations, consultez MELicenseAcquisitionStart.
ms.assetid: f577131b-887a-4912-8278-1165a801c2b3
title: Événement MELicenseAcquisitionCompleted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 545fa012f974637f5d268a7d8257daaf9b393f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518384"
---
# <a name="melicenseacquisitioncompleted-event"></a><span data-ttu-id="daa19-104">Événement MELicenseAcquisitionCompleted</span><span class="sxs-lookup"><span data-stu-id="daa19-104">MELicenseAcquisitionCompleted event</span></span>

<span data-ttu-id="daa19-105">Levée lorsque l’acquisition de licence est terminée.</span><span class="sxs-lookup"><span data-stu-id="daa19-105">Raised when license acquisition is complete.</span></span> <span data-ttu-id="daa19-106">Pour plus d’informations, consultez [MELicenseAcquisitionStart](melicenseacquisitionstart.md).</span><span class="sxs-lookup"><span data-stu-id="daa19-106">For more information, see [MELicenseAcquisitionStart](melicenseacquisitionstart.md).</span></span>

## <a name="event-values"></a><span data-ttu-id="daa19-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="daa19-107">Event values</span></span>

<span data-ttu-id="daa19-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="daa19-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="daa19-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="daa19-109">VARTYPE</span></span>              | <span data-ttu-id="daa19-110">Description</span><span class="sxs-lookup"><span data-stu-id="daa19-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="daa19-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="daa19-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="daa19-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="daa19-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="daa19-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daa19-113">Requirements</span></span>



| <span data-ttu-id="daa19-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="daa19-114">Requirement</span></span> | <span data-ttu-id="daa19-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="daa19-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daa19-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="daa19-116">Minimum supported client</span></span><br/> | <span data-ttu-id="daa19-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="daa19-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="daa19-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="daa19-118">Minimum supported server</span></span><br/> | <span data-ttu-id="daa19-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="daa19-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="daa19-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="daa19-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="daa19-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="daa19-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daa19-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daa19-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daa19-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="daa19-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





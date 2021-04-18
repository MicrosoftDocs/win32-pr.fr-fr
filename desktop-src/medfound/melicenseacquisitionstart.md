---
description: Déclenché par le moteur de stratégie lorsque l’acquisition de licence est sur le le début. L’acquisition de licence est effectuée à l’aide de l’implémentation d’applications de l’interface IMFContentProtectionManager.
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: Événement MELicenseAcquisitionStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914d2580c95cf40986a844a994c1e284c5ad9e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519008"
---
# <a name="melicenseacquisitionstart-event"></a><span data-ttu-id="d4411-104">Événement MELicenseAcquisitionStart</span><span class="sxs-lookup"><span data-stu-id="d4411-104">MELicenseAcquisitionStart event</span></span>

<span data-ttu-id="d4411-105">Déclenché par le moteur de stratégie lorsque l’acquisition de licence est sur le le début.</span><span class="sxs-lookup"><span data-stu-id="d4411-105">Raised by the policy engine when license acquisition is about to begin.</span></span> <span data-ttu-id="d4411-106">L’acquisition de licence est effectuée à l’aide de l’implémentation de l’interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) de l’application.</span><span class="sxs-lookup"><span data-stu-id="d4411-106">License acquisition is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="d4411-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="d4411-107">Event values</span></span>

<span data-ttu-id="d4411-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4411-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d4411-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d4411-109">VARTYPE</span></span>              | <span data-ttu-id="d4411-110">Description</span><span class="sxs-lookup"><span data-stu-id="d4411-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d4411-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="d4411-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d4411-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="d4411-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d4411-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d4411-113">Remarks</span></span>

<span data-ttu-id="d4411-114">Lorsque l’acquisition de licence est terminée, le moteur de stratégie déclenche l’événement [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d4411-114">When license acquisition is completed, the policy engine raises the [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4411-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4411-115">Requirements</span></span>



| <span data-ttu-id="d4411-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4411-116">Requirement</span></span> | <span data-ttu-id="d4411-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4411-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4411-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4411-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d4411-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4411-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d4411-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4411-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d4411-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4411-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d4411-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4411-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4411-123"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4411-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4411-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4411-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4411-125">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4411-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





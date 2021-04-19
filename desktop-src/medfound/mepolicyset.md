---
description: 'Déclenché par une autorité de confiance de sortie (OTA) lorsque la méthode IMFOutputTrustAuthority :: SetPolicy se termine de façon asynchrone.'
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: Événement MEPolicySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238af6cbd740e62825ae0b661769c1cf1bf880ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524555"
---
# <a name="mepolicyset-event"></a><span data-ttu-id="cac1f-103">Événement MEPolicySet</span><span class="sxs-lookup"><span data-stu-id="cac1f-103">MEPolicySet event</span></span>

<span data-ttu-id="cac1f-104">Déclenché par une autorité de confiance de sortie (OTA) lorsque la méthode [**IMFOutputTrustAuthority :: SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="cac1f-104">Raised by an output trust authority (OTA) when the [**IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="cac1f-105">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="cac1f-105">Event values</span></span>

<span data-ttu-id="cac1f-106">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="cac1f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cac1f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cac1f-107">VARTYPE</span></span>              | <span data-ttu-id="cac1f-108">Description</span><span class="sxs-lookup"><span data-stu-id="cac1f-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="cac1f-109">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="cac1f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="cac1f-110">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="cac1f-110">No event data.</span></span><br/> <br/> |
| <span data-ttu-id="cac1f-111">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="cac1f-111">VT\_UI4</span></span><br/> | <span data-ttu-id="cac1f-112">Identificateur qui peut être défini sur un [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) via l’attribut [MF_POLICY_ID](mf-policy-id.md) .</span><span class="sxs-lookup"><span data-stu-id="cac1f-112">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) through the [MF_POLICY_ID](mf-policy-id.md) attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="cac1f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cac1f-113">Requirements</span></span>



| <span data-ttu-id="cac1f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cac1f-114">Requirement</span></span> | <span data-ttu-id="cac1f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cac1f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac1f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cac1f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cac1f-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cac1f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cac1f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cac1f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cac1f-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cac1f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cac1f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="cac1f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac1f-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cac1f-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac1f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cac1f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac1f-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cac1f-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





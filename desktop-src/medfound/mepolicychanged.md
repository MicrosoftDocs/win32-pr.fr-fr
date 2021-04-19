---
description: Déclenché par un composant de pipeline lorsque la stratégie de sortie du flux change. Cet événement s’applique uniquement au contenu protégé.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Événement MEPolicyChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544251"
---
# <a name="mepolicychanged-event"></a><span data-ttu-id="424d3-104">Événement MEPolicyChanged</span><span class="sxs-lookup"><span data-stu-id="424d3-104">MEPolicyChanged event</span></span>

<span data-ttu-id="424d3-105">Déclenché par un composant de pipeline lorsque la stratégie de sortie du flux change.</span><span class="sxs-lookup"><span data-stu-id="424d3-105">Raised by a pipeline component when the output policy for the stream changes.</span></span> <span data-ttu-id="424d3-106">Cet événement s’applique uniquement au contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="424d3-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="424d3-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="424d3-107">Event values</span></span>

<span data-ttu-id="424d3-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="424d3-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="424d3-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="424d3-109">VARTYPE</span></span>                | <span data-ttu-id="424d3-110">Description</span><span class="sxs-lookup"><span data-stu-id="424d3-110">Description</span></span>                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="424d3-111">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="424d3-111">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="424d3-112">Pointeur vers l’interface [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) de la nouvelle stratégie pour le flux.</span><span class="sxs-lookup"><span data-stu-id="424d3-112">Pointer to the [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) interface of the new policy for the stream.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="424d3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="424d3-113">Remarks</span></span>

<span data-ttu-id="424d3-114">Toutes les sorties approuvées doivent gérer cet événement.</span><span class="sxs-lookup"><span data-stu-id="424d3-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="424d3-115">Les transformations de Media Foundation (MFTs) reçoivent cet événement via la méthode [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) .</span><span class="sxs-lookup"><span data-stu-id="424d3-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="424d3-116">Les récepteurs multimédias reçoivent cet événement par le biais de la méthode [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="424d3-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="424d3-117">La sortie approuvée doit appliquer la nouvelle stratégie ou retourner le code d’erreur MF \_ E \_ stratégie \_ non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="424d3-117">The trusted output must apply the new policy or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="424d3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="424d3-118">Requirements</span></span>



| <span data-ttu-id="424d3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="424d3-119">Requirement</span></span> | <span data-ttu-id="424d3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="424d3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="424d3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="424d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="424d3-122">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="424d3-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="424d3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="424d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="424d3-124">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="424d3-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="424d3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="424d3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="424d3-126"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="424d3-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="424d3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="424d3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="424d3-128">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="424d3-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





---
description: Déclenché par un composant de pipeline lorsque la configuration change pour l’un des schémas de protection de sortie. Cet événement s’applique uniquement au contenu protégé.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Événement MEContentProtectionMessage (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f96ac75711559881232ced4cec6bfca2bc030c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753181"
---
# <a name="mecontentprotectionmessage-event"></a><span data-ttu-id="3a1c1-104">Événement MEContentProtectionMessage</span><span class="sxs-lookup"><span data-stu-id="3a1c1-104">MEContentProtectionMessage event</span></span>

<span data-ttu-id="3a1c1-105">Déclenché par un composant de pipeline lorsque la configuration change pour l’un des schémas de protection de sortie.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-105">Raised by a pipeline component when the configuration changes for one of the output protection schemes.</span></span> <span data-ttu-id="3a1c1-106">Cet événement s’applique uniquement au contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="3a1c1-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="3a1c1-107">Event values</span></span>

<span data-ttu-id="3a1c1-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3a1c1-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3a1c1-109">VARTYPE</span></span>              | <span data-ttu-id="3a1c1-110">Description</span><span class="sxs-lookup"><span data-stu-id="3a1c1-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="3a1c1-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="3a1c1-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3a1c1-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3a1c1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3a1c1-113">Remarks</span></span>

<span data-ttu-id="3a1c1-114">Toutes les sorties approuvées doivent gérer cet événement.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="3a1c1-115">Les transformations de Media Foundation (MFTs) reçoivent cet événement via la méthode [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) .</span><span class="sxs-lookup"><span data-stu-id="3a1c1-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="3a1c1-116">Les récepteurs multimédias reçoivent cet événement par le biais de la méthode [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="3a1c1-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="3a1c1-117">La sortie approuvée doit appliquer les modifications de stratégie ou retourner le code d’erreur MF \_ E \_ stratégie \_ non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-117">The trusted output must apply the policy changes or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

<span data-ttu-id="3a1c1-118">Les données d’événement et les attributs dépendent du système de protection du contenu en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-118">The event data and attributes depend on the content protection system in use.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1c1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a1c1-119">Requirements</span></span>



| <span data-ttu-id="3a1c1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a1c1-120">Requirement</span></span> | <span data-ttu-id="3a1c1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a1c1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1c1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a1c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3a1c1-123">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="3a1c1-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="3a1c1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a1c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3a1c1-125">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="3a1c1-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="3a1c1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a1c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a1c1-127"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a1c1-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a1c1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a1c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1c1-129">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a1c1-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





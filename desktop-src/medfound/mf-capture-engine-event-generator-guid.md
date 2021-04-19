---
description: Identifie le composant qui a généré un événement de capture.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: Attribut MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9a5068db357523a626404910fb7d752ea0b621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519345"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a><span data-ttu-id="514c9-103">\_ \_ \_ \_ Attribut Guid du générateur d’événements du moteur de capture MF \_</span><span class="sxs-lookup"><span data-stu-id="514c9-103">MF\_CAPTURE\_ENGINE\_EVENT\_GENERATOR\_GUID attribute</span></span>

<span data-ttu-id="514c9-104">Identifie le composant qui a généré un événement de capture.</span><span class="sxs-lookup"><span data-stu-id="514c9-104">Identifies the component that generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="514c9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="514c9-105">Data type</span></span>

<span data-ttu-id="514c9-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="514c9-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="514c9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="514c9-107">Remarks</span></span>

<span data-ttu-id="514c9-108">Cet attribut apparaît sur certains événements du moteur de capture.</span><span class="sxs-lookup"><span data-stu-id="514c9-108">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="514c9-109">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) sur l’objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="514c9-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) on the event object.</span></span> <span data-ttu-id="514c9-110">L’objet d’événement est passé à l’application par le biais de la méthode [**IMFCaptureEngineOnEventCallback :: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .</span><span class="sxs-lookup"><span data-stu-id="514c9-110">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

<span data-ttu-id="514c9-111">La valeur est un identificateur d’interface pour le composant qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="514c9-111">The value is an interface identifier for the component that generated the event.</span></span> <span data-ttu-id="514c9-112">Par exemple, la valeur **IID \_ IMFCapturePreviewSink** indique le récepteur d’aperçu ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span><span class="sxs-lookup"><span data-stu-id="514c9-112">For example, the value **IID\_IMFCapturePreviewSink** indicates the preview sink ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span></span> <span data-ttu-id="514c9-113">Tous les événements de capture ne contiennent pas cet attribut.</span><span class="sxs-lookup"><span data-stu-id="514c9-113">Not every capture event contains this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="514c9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="514c9-114">Requirements</span></span>



| <span data-ttu-id="514c9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="514c9-115">Requirement</span></span> | <span data-ttu-id="514c9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="514c9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="514c9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="514c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="514c9-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="514c9-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="514c9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="514c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="514c9-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="514c9-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="514c9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="514c9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="514c9-122"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="514c9-122"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514c9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="514c9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514c9-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="514c9-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="514c9-125">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="514c9-125">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="514c9-126">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="514c9-126">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





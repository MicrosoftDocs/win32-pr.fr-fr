---
description: Identifie le flux qui a généré un événement de capture.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: Attribut MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863597"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a><span data-ttu-id="f9d90-103">\_Attribut d' \_ \_ index du flux d’événements du moteur de \_ capture MF \_</span><span class="sxs-lookup"><span data-stu-id="f9d90-103">MF\_CAPTURE\_ENGINE\_EVENT\_STREAM\_INDEX attribute</span></span>

<span data-ttu-id="f9d90-104">Identifie le flux qui a généré un événement de capture.</span><span class="sxs-lookup"><span data-stu-id="f9d90-104">Identifies which stream generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="f9d90-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f9d90-105">Data type</span></span>

<span data-ttu-id="f9d90-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f9d90-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f9d90-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="f9d90-107">Get/set</span></span>

<span data-ttu-id="f9d90-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f9d90-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9d90-109">Notes</span><span class="sxs-lookup"><span data-stu-id="f9d90-109">Remarks</span></span>

<span data-ttu-id="f9d90-110">Cet attribut apparaît sur certains événements du moteur de capture.</span><span class="sxs-lookup"><span data-stu-id="f9d90-110">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="f9d90-111">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) sur l’objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="f9d90-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) on the event object.</span></span> <span data-ttu-id="f9d90-112">L’objet d’événement est passé à l’application par le biais de la méthode [**IMFCaptureEngineOnEventCallback :: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .</span><span class="sxs-lookup"><span data-stu-id="f9d90-112">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d90-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9d90-113">Requirements</span></span>



| <span data-ttu-id="f9d90-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9d90-114">Requirement</span></span> | <span data-ttu-id="f9d90-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9d90-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d90-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9d90-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f9d90-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9d90-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f9d90-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9d90-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f9d90-119">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9d90-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f9d90-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9d90-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9d90-121"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9d90-121"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9d90-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9d90-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9d90-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f9d90-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f9d90-124">**IMFCaptureEngineOnEventCallback :: OnEvent**</span><span class="sxs-lookup"><span data-stu-id="f9d90-124">**IMFCaptureEngineOnEventCallback::OnEvent**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 





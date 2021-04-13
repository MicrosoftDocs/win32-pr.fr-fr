---
description: Déclenché par le convertisseur audio lorsque les paramètres de regroupement changent pour la session audio.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Événement MEAudioSessionGroupingParamChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac115bb30a4c01247da537f3255e9bc40099e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201678"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a><span data-ttu-id="f02b2-103">Événement MEAudioSessionGroupingParamChanged</span><span class="sxs-lookup"><span data-stu-id="f02b2-103">MEAudioSessionGroupingParamChanged event</span></span>

<span data-ttu-id="f02b2-104">Déclenché par le convertisseur audio lorsque les paramètres de regroupement changent pour la session audio.</span><span class="sxs-lookup"><span data-stu-id="f02b2-104">Raised by the audio renderer when the grouping parameters change for the audio session.</span></span>

<span data-ttu-id="f02b2-105">La session multimédia transmet cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="f02b2-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="f02b2-106">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="f02b2-106">Event values</span></span>

<span data-ttu-id="f02b2-107">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="f02b2-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f02b2-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f02b2-108">VARTYPE</span></span>                | <span data-ttu-id="f02b2-109">Description</span><span class="sxs-lookup"><span data-stu-id="f02b2-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f02b2-110">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="f02b2-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="f02b2-111">Pointeur vers l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="f02b2-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f02b2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f02b2-112">Remarks</span></span>

<span data-ttu-id="f02b2-113">Cet événement est envoyé par le récepteur de flux du convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="f02b2-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="f02b2-114">L’événement est déclenché lorsque le convertisseur audio reçoit un événement [**IAudioSessionEvents :: OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) à partir de la session audio.</span><span class="sxs-lookup"><span data-stu-id="f02b2-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) event from the audio session.</span></span>

<span data-ttu-id="f02b2-115">Pour récupérer les nouveaux paramètres de regroupement, appelez [**IMFAudioPolicy :: GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span><span class="sxs-lookup"><span data-stu-id="f02b2-115">To get the new grouping parameters, call [**IMFAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span></span>

## <a name="requirements"></a><span data-ttu-id="f02b2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f02b2-116">Requirements</span></span>



| <span data-ttu-id="f02b2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f02b2-117">Requirement</span></span> | <span data-ttu-id="f02b2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f02b2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f02b2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f02b2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f02b2-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f02b2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f02b2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f02b2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f02b2-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f02b2-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f02b2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f02b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f02b2-124"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f02b2-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f02b2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f02b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f02b2-126">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f02b2-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f02b2-127">**IMFAudioPolicy::GetGroupingParam**</span><span class="sxs-lookup"><span data-stu-id="f02b2-127">**IMFAudioPolicy::GetGroupingParam**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[<span data-ttu-id="f02b2-128">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="f02b2-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 

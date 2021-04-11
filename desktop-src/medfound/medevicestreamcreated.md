---
description: MEDeviceStreamCreated est un type d’événement multimédia étendu généré avec un événement de média MEUnknown par la MFT de l’appareil.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Événement MEDeviceStreamCreated (mftransform. h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 632ebc305473cd596656a21f562be25d53c2bace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201726"
---
# <a name="medevicestreamcreated-event"></a><span data-ttu-id="da043-103">Événement MEDeviceStreamCreated</span><span class="sxs-lookup"><span data-stu-id="da043-103">MEDeviceStreamCreated event</span></span>

<span data-ttu-id="da043-104">MEDeviceStreamCreated est un type d’événement multimédia étendu généré avec un événement de média MEUnknown par la MFT de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="da043-104">MEDeviceStreamCreated is an extended media event type generated with an MEUnknown media event by the Device MFT.</span></span>

<span data-ttu-id="da043-105">Ce type d’événement multimédia étendu n’a pas de charge utile.</span><span class="sxs-lookup"><span data-stu-id="da043-105">This extended media event type has no payload.</span></span>  <span data-ttu-id="da043-106">Le HRESULT approprié doit être fourni par le biais de la méthode [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="da043-106">Appropriate HRESULT should be provided via the [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) method.</span></span>




## <a name="remarks"></a><span data-ttu-id="da043-107">Notes</span><span class="sxs-lookup"><span data-stu-id="da043-107">Remarks</span></span>

<span data-ttu-id="da043-108">Cet événement de média étendu doit être envoyé par la MFT de l’appareil dans le cadre de la sélection du type de média sur le flux de sortie de l’DMFT.</span><span class="sxs-lookup"><span data-stu-id="da043-108">This extended media event must be sent by the Device MFT as a part of the media type selection on the output stream of the DMFT.</span></span>  <span data-ttu-id="da043-109">Lorsque le SetOutputStreamState est appelé sur l’interface IMFDeviceTransform, le DMFT est chargé de signaler la modification dans les États de flux d’entrée requis avec l’événement de média [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) .</span><span class="sxs-lookup"><span data-stu-id="da043-109">When the SetOutputStreamState is invoked on the IMFDeviceTransform interface, the DMFT is responsible for signaling the change in the required input stream states with the [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) media event.</span></span> <span data-ttu-id="da043-110">Lorsque la modification de l’état du flux d’entrée a été reconnue par le pipeline avec l’appel de SetInputStreamState du DMFT, le DMFT est chargé d’effectuer sa configuration d’état interne et de déclencher le type d’événement multimédia étendu **MEDeviceStreamCreated** .</span><span class="sxs-lookup"><span data-stu-id="da043-110">When the input stream state change has been acknowledged by the pipeline with the call into SetInputStreamState of the DMFT, the DMFT is responsible for completing its internal state configuration and raising the **MEDeviceStreamCreated** extended media event type.</span></span>

<span data-ttu-id="da043-111">Si ce type d’événement multimédia étendu n’est pas déclenché, Device Transform Manager ne remet pas d’images d’entrée au DMFT.</span><span class="sxs-lookup"><span data-stu-id="da043-111">If this extended media event type is not raised, the Device Transform Manager will not deliver any input frames to the DMFT.</span></span>
<span data-ttu-id="da043-112">Le type d’événement de média étendu doit également être défini en tant qu’attribut de IMFMediaEvent, l’ID de flux de sortie à l’aide de l’attribut **MF_EVENT_MFT_INPUT_STREAM_ID** .</span><span class="sxs-lookup"><span data-stu-id="da043-112">The extended media event type must also set as an attribute of the IMFMediaEvent, the output stream ID using the **MF_EVENT_MFT_INPUT_STREAM_ID** attribute.</span></span>

```cpp
IMFMediaEvent* pMediaEvent = nullptr;

hr = MFCreateMediaEvent (MEUnknown,
                         MEDeviceStreamCreated,
                         S_OK,
                         nullptr,
                         &pMediaEvent);
if (SUCCEEDED(hr))
{
    hr = pMediaEvent->SetUINT32(MF_EVENT_MFT_INPUT_STREAM_ID, GetOutputStreamId());
}

if (SUCCEEDED(hr))
{
    hr = m_pEventQueue->QueueEvent(pMediaEvent);
}

if (nullptr != pMediaEvent)
{
    pMediaEvent->Release();
    pMediaEvent = nullptr;
}

return hr;
```

## <a name="requirements"></a><span data-ttu-id="da043-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da043-113">Requirements</span></span>



| <span data-ttu-id="da043-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da043-114">Requirement</span></span> | <span data-ttu-id="da043-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="da043-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da043-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da043-116">Minimum supported client</span></span><br/> | <span data-ttu-id="da043-117">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da043-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da043-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da043-118">Minimum supported server</span></span><br/> | <span data-ttu-id="da043-119">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da043-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da043-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="da043-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="da043-121"><dt>mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="da043-121"><dt>mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da043-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da043-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da043-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da043-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="da043-124">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="da043-124">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
